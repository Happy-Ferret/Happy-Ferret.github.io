---
layout: post
type: post
comments: true
title: Introducing Yggdrasil (and Rosetta-Go/Rosetta-TS)
# All dates must be YYYY-MM-DD format!
date: 2019-08-25 17:10:00 +0200
labels:
  - Interactive Fiction
  - Adventure Games
  - 8-Bit
  - Game Development
  - Point & Click
  - Game Engine
  - i18n
images:
  - image_path: /images/blog/yggdrasil.svg
    title: Yggdrasil logo
  - image_path: /images/blog/yggdrasil-UI.png
    title: Yggdrasil v0.3.0 UI
  - image_path: /images/blog/yggdrasil-UI2.png
    title: Yggdrasil v0.3.0 UI
---

<a href="https://github.com/middangeard-fiction/yggdrasil"><i class="large github icon"></i>Yggdrasil</a>
<a href="https://github.com/middangeard-fiction/rosetta-go"><i class="large github icon"></i>Rosetta-Go</a>
<a href="https://github.com/middangeard-fiction/yggdrasil/tree/master/src/rosetta"><i class="large github icon"></i>Rosetta-TS</a>

In this short triple feature I'd like to talk a bit about my latest work in regards to [Middangeard](/posts/middangeard-announcement).

After some tinkering with [Trizbort](https://www.trizbort.com/) &mdash; which I discovered upon playing with [adventuron](https://adventuron.io/) &mdash;
I decided a map editor of that kind would make an excellent addition to **Middangeard**. An IDE of some kind (later on, I intend
adding a "Run" option to interactively playtest games straight from the UI) that would make creating interactive fiction
a breeze.

I spent a few hours hacking away on the Trizbort source code before I stumbled upon [Trizbort.io](http://trizbort.io),
a web UI based rewrite of **Trizbort**. Browsing the source code, I soon realized this would make a better basis
for my plans than the regular, C# based **Trizbort**.

**Yggdrasil** is the result of this short R&D venture. A web based editor but also a more complete desktop application,
with support for Windows, Mac OS and GNU/Linux.

After a few weeks of intensive work, Yggdrasil is now heading towards v0.3.0. The main focus of this release is
translation/internationalization. Which brings us to two subprojects spawned as a result of my work.

### Rosetta-Go and Rosetta-TS.

Rosetta-Go/Rosetta-TS are two localization libraries, for Go and TypeScript respectively.
The goal of either one is to provide a [Chrome i18n](https://developer.chrome.com/extensions/i18n) compatible API.

Re-using Chrome i81n will make ports to <strong class="tooltip" data-content="A lightweight, Google-centric operating system usually run on dedicated hardware. So called Chromebooks." data-variation="inverted">Chrome OS</strong> straightforward. Furthermore, it's well supported by the likes of [transifex](https://www.transifex.com/) 
and [Crowdin](https://crowdin.com/).

The basic setup process is already similar for both implementations.

1. Import the library.
2. Initialize the library with a path to the locales and additional options.
3. Create a locale-specific translation in the i18n format [messages.json](https://raw.githubusercontent.com/middangeard-fiction/yggdrasil/master/locales/en/messages.json).
4. Call the library's **getMessage(key: string)** function with a translation specific key from the previous step.

In the following weeks I hope to refine both libraries and officially launch them (as well as Yggdrasil) on their respective
platforms.

**Web Demo:** [English](https://pedantic-heyrovsky-f84015.netlify.com) &mdash; [German](https://pedantic-heyrovsky-f84015.netlify.com/?lang=de#)

All three projects are available under the MIT license. **Rosetta-TS** is currently a part of Yggdrasil, but will be split
into its own distinct repository soon. **Rosetta-Go** is a fork of [gotrans](https://github.com/bykovme/gotrans).

<br/>

<br/>