---
layout: blog
title: Installing DejaVu Sans Mono for LyX typewriter
date: 2013-11-03 23:40:55 +0530
day: Sunday
tags:
  - log message
  - lyx
  - fonts
  - dejavu
  - bera mono
---

To install DejaVu Sans Mono for lyx typewriter, install Bera Mono instead. It is almost the same. This is available via the package texlive-fonts-extra. You can then select article (noweb) as your document class for scrap, and still get the DejaVu font for code. Note that you cannot use ttf fonts via xetex or luatex when using the article (noweb) document class. I do not yet know why this is the case. 
