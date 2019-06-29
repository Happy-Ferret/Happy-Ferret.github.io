---
layout: post
type: post
comments: true
title: "Blog codebase updates"
# All dates must be YYYY-MM-DD format!
date: 2019-06-29 13:25:00 +0200
labels:
  - Blogging
---

In the coming months, I plan on actively updating parts
of my blog to better serve my readers through usability/readability
improvements.

One such feature is now online. **Tooltips**.

Tooltips provide additional explanations
that the reader would otherwise have to research for themselves,
or that I would have to painstakingly embed between
a set of parentheses or otherwise separate from the main
body text.

In the future, look for bold text with a question mark next to it.
I plan on making extensive use of this feature.


_Example:_
<div class="tooltip" style="display: inline-block;">Jekyll</div>
<div class="ui popup inverted">
 Jekyll is a static site generator and the centerpiece of this blog. Rather than hosting dynamic content on a private host or in the cloud, all the content you see on here is generated ahead of time, using a mix of CSS, Markdown <div class="tooltip" data-title='Hypertext Markup Language' data-content="The graphical and contextual backbone of the internet." data-variation="inverted">HTML</div> and JavaScript.
 <br/>
 <br/>
 This allows me to host the content free of charge, on
 <a href="https://github.com/">Github.<i class="big github icon icon-color" style="color: rgba(255,255,255,0.8);"></i></a>
</div>

On another note, I have now enabled image captions. Since these re-use the **`<alt>`** value, most images on my blog should
already be properly captioned.