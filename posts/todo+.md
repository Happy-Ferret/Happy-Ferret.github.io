---
layout: post
type: post
comments: true
title: "Todo+ as a modern .plan file replacement"
# All dates must be YYYY-MM-DD format!
date: 2019-06-20 19:12:00 +0200
labels:
  - Staying organized
  - Game Development
images:
  - image_path: /images/blog/todo.png
    title: TODO+ file with embedded todo
---

<a href="https://marketplace.visualstudio.com/items?itemName=fabiospampinato.vscode-todo-plus"><i class="large home icon"></i>Extension Page</a>

I've recently become interested in taking a more organized approach to my work.
Being a lifelong John Carmack fanboy, I still remember his infamous [.plan](https://github.com/ESWAT/john-carmack-plan-archive.git) files.

Earlier this week I was thus looking for a modern replacement (something a bit more refined and interactive than using regular markdown).
Initially, my research led me to [Taskwarrior](https://taskwarrior.org). While this one is, undoubtedly, a very appealing tool, it's
also quite limited in its portability. At my day job I'm still constrained to Windows 8.1 (because reasons), so no WSL and,
consequently, no Taskwarrior. Furthermore, Taskwarrior uses a database and requires additional tooling to put it under
version control.

Looking further then, I stumbled upon TODO+. TODO+ is a portable Visual Studio Code (my editor of choice) extension
that adds a **TODO** file to your project of choice, as well as a right-click context menu and a new sidebar option.
It also comes with its own language mode/syntax highlighting.

While I've yet to take full advantage of a .plan-esque/daily blog-like organizational pattern 
(most of my work &mdash; especially that which is open-source &mdash; isn't something I've been able to organize into daily routines),
the basic feature set makes for some visually pleasing to-do lists already.

Lastly, TODO+ also supports **embedded todos**. Embedded todos are **TODO** and **DEBUG** comments stored in code. Those can be
(optionally and individually) added to the main TODO file, adding a link back to the original file/comment.
While unarguably a useful feature it does, unfortunately, look a wee bit encumbered.