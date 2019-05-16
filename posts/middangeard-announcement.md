---
layout: post
type: post
comments: true
title: Introducing Middangeard
# All dates must be YYYY-MM-DD format!
date: 2019-05-16
labels:
  - Interactive Fiction
  - Adventure Games
  - 8-Bit
  - Game Development
  - Game Engine
images:
  - image_path: /images/blog/cloak-carbon.svg
    title: Cloak of Darkness Middangeard Source
---

<a href="https://github.com/middangeard-fiction/middangeard"><i class="large github icon"></i>Source</a>

It is with great excitement that I'm announcing my newest venture into game design.

**Middangeard** is a modern Interactive Fiction (AKA Text Adventure) engine written in Go.
Reborn out of an idea I had back in 2014 (to write a similar framework in 
[Inform 7](http://inform7.com/). An idea that eventually crumbled under 
the sheer load of plugins and the inherent complexity of writing code in a natural language),
I have already made great strives since first starting work on it earlier this month.

While the initial parser implementation will be somewhat limited, I already have a long list of
plans for future feature releases.
Including but not limited to 
full audio support (through a subsystem dubbed **Operatmos**), graphics (potentially reference implementations in HTML5 and SDL/OpenGL)
and [Lua](www.lua.org) scripting.

Eventually, the plan is to move past "simple" Interactive Fiction and enable the creation
of games belonging to other genres, such as point & click adventures. Similarly
to how [AGOS](https://wiki.scummvm.org/index.php/AGOS), the adventure engine driving graphical point & click adventures such as Simon the Sorcerer,
originally came about (as a textual MUD engine with a set of graphical extensions).

Middangeard 1 is on track of being released by the end of May, under the BSD3 license.

**Below: Code from a WIP Middangeard implementation of the [Cloak of Darkness](http://www.firthworks.com/roger/cloak/) reference adventure demo game.**