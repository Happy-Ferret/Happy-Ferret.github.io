---
layout: post
type: post
comments: true
title: Renewed Anima OS development efforts
summary: "A short announcement on the state of Anima OS" 
# All dates must be YYYY-MM-DD format!
date: 2020-03-03 09:30:00 +0200
labels:
  - Anima OS
  - OS Development
---

With recent personal developments I have decided to reboot Anima OS and refocus my efforts
on turning the browser into a usable desktop environment.

The first two videos outlining my current development focus/approach can be found below.


#### My hopes/plans

{:.ui .list}
* Base Quokka (the OS' browser) on a more recent release of Firefox (ideally, the **release** branch).
* Ditch XUL and the custom SDK (known as STK or "Savannah Toolkit") for an extended **Webextension** API.
* Securely integrate things like time/date, battery status and gamma control/nightlight into the browser UI.
* Create a secure and stable desktop bus privileged parts of the browser can use to communicate with the rest of the OS.
* Implement PWAs, allowing the user to launch them from a built-in app launcher.
* Create a simple desktop environment consisting of a window manager, a basic desktop (wallpaper), compositor and the browser.
  * Alternatively, consider a dock outside the browser.

<iframe width="560" height="315" src="https://www.youtube.com/embed/g6bfIQzwwQg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="560" height="315" src="https://www.youtube.com/embed/tlLwd2tZMak" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
