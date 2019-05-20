---
layout: post
type: post
comments: true
title: Adventures in SCUMM, Part 1
# All dates must be YYYY-MM-DD format!
date: 2019-05-20 9:01:30 +0200
labels:
  - Point & Click
  - Adventure Games
  - 8-Bit
  - Game Development
  - Game Engine
  - iMuse
  - Lucas Arts
---

Complementary to my work on Middangeard, I'm also taking the time
to dig into other adventure engines. Both contemporary and "retro", text based and graphical.

Amongst these engines (others are [Inform 6/7](http://inform7.com/), [SCI](http://scicompanion.com), as well as 
the sources for adventure games by 
[Magnetic Scrolls](https://gitlab.com/strandgames/brahman/blob/master/mscrolls/src/alice/alice.f23) 
and [Infocom](https://github.com/historicalsource/sherlock)) 
is Lucas Arts' [SCUMM (Script Creation Utility for Maniac Mansion)](https://en.wikipedia.org/wiki/SCUMM).

I spent the past weekend deconstructing the way audio files (both **MIDI** music and **VOC** SFX) can be created and loaded inside
SCUMMC.

These findings will soon be added to my [personal fork of the ScummC wiki](https://github.com/Happy-Ferret/scummc/wiki).
In the meantime, here's a brief summary:

### MIDI

MIDI music is stored as MIDI type 0. In essence, that means there is a single track and a maximum of 16 channels.
All information from the other tracks is merged into the first channel. The downside to this is that headers outside
of the first track are not retained. It's advised composers keep a backup of their original composition pre-merge around.

MIDI files can be created with common software tools, both online and offline.
My personal favorite in that regard is [Soundtrap](https://www.soundtrap.com).

Merging the tracks can either be achieved from inside the MIDI composition software, or through
a tool (aptly named **midi**) included with ScummC.

The latter's syntax is a bit on the obscure end, but here is how I managed merging tracks 1-2 into track 0 (i e the very
first track) 

```cmd
midi music/test.mid sounds/test.mid -merge-track 0 -merge-track 1 -merge-track 2 -set-type 0
```

This translates into the following deconstructed syntax:

```cmd
midi <path to source file> <path to output> -merge-track <first track> -merge-track <number of track to be merged into first track> -set-type <MIDI file type>
```

### VOC

VOC (Creative Voice) is a specialty audio format widely used in 90s' video games and originally created to accompany
Creative's line of 8-bit Soundblaster cards. In SCUMM games (v5 and up) it was commonly used for voices and sound effects.

While VOC supports both 8-bit and 16-bit audio, SCUMM only supports the former.

Files should be saved/converted to **8-bit Mono/11000 Hz**.

The only seemingly modern tool I have found that handles the format gracefully, 
runs on modern hardware, is easy to use and within the realm of the affordable
is [GoldWave](https://www.goldwave.com/).

It is important to note that any attempt to diverge from the above specifications will crash ScummVM in the process.
