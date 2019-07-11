---
layout: post
type: post
comments: true
title: "Idea for a (toy) programming language"
# All dates must be YYYY-MM-DD format!
date: 2019-07-11 13:03:00 +0200
labels:
  - Creative Coding
  - Design Patterns
  - Language Design
---

<a href="https://tabby-lang.github.io/"><i class="large home icon"></i>Project Page (WIP)</a>

With the advent of [V](https://vlang.io/) (which I only took a cursory look at. Alas, what I saw I liked very much. It looks and feels like [Go](https://golang.org/) on steroids)
I've recently become interested in writing my own (toy) language. Partly to serve as a learning/teaching aid in language theory
(My niece. My mother. The trainees at my day job. I'll be damned if I don't turn everybody I meet into a programming nerd 😹). Partly to have a modern,
easy to use language for writing small applications and games.

The initial implementation is unlikely to be "high fidelity". Just straightforward <strong class="tooltip" data-title="Backus–Naur form" data-content="A context-free notation technique. Used to describe the overall syntax of programming languages and document formats." data-variation="inverted">BNF</strong> for the grammar,
**Go** for the compiler/generator, and a few bits and bobs in **C++**.
<br/><small><small>**PSA that I'm not even remotely a language theorist, nor a compiler designer**</small></small>.

#### Initial Ideas

{:.ui .list}
* File extension: <span style="color: SandyBrown;">**.tby**</span>
* No unsightly semicolons.
  * Just like Go and V.
* **int** as a shortcut for **int32**
  * **int** should ALWAYS be 32 bits wide. Even on 64 bit systems. 
    <br/> Contrary to Go but similar to C#.
  * Arithmetic overflow checks.
    * Subtracting a larger numerical from a smaller one <br/> should, for starters, either
      *return* 0 or throw a runtime/compiler error.
* Immutable by default.
  * Prepend a variable/structure with **~** to signify its mutability.
* <strong class="tooltip" data-content="Pure functions are functions that ALWAYS return a (typed) value of some sort. The return value itself is solely determined by the function's input values (ergo 'pure'). Such functions lack side-effects associated with regular functions. I e the output is guaranteed to be always the same, not dependend on any external/global state." data-variation="inverted">Pure functions</strong> by default.
* Support for conditional imports (<span style="color: LightCoral;">**?**</span>).
* Go, Rust, C++ or V as "IR" (intermediate representation).
  * [go-compiler](github.com/Lebonesco/go-compiler) uses C++, but that could
    be altered quite easily.
  * For Go I would have to test the code extensively, with <strong class="tooltip" data-title="Garbage Collection" data-content="A form of automatic memory management that liberates the programmer from the burden of manually freeing memory. Usually at the expense of performance." data-variation="inverted">GC</strong> disabled.
* Standard library that includes some form of graphics support. Potentially, Cairo/SDL2/OpenGL.
* Support for 32Blit and other embedded gaming devices.
* Microsoft UWP support (requires OpenGL ES or DirectX bindings).