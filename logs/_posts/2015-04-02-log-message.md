---
layout: blog
title: Exporting multi-page pdfs with GIMP
date: 2015-04-02 11:46:10 -0400
day: Thursday
tags:
  - log message
  - gimp
  - export
  - pdf
---

Gimp imports multi-page pdfs as one layer-per-page. But it does not re-export multi-layer figures as a multi-page pdf, with one page-per-layer. It just exports the topmost visible layer. I found a solution for this [here](http://registry.gimp.org/node/25400). You need to reverse the order of layers, export the project as a .mng animation. Then, from command line, call `convert file.mng file.pdf`. Apparently, for convert to work, you need to have ImageMagick installed, but I think I had it by default.