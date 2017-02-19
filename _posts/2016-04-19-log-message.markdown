---
layout: blog
title: Log Message
date: 2016-04-19 23:38:17 -0400
day: Tuesday
tags:
  - log message
  - pdf
  - builtins
  - two pages per side
---

To convert a pdf document into one containing two pages per side, simply `man pdfnup`. This is a convenient frontend to the more complex `pdfjam`. For most purposes, this should suffice: `pdfnup --paper letter document.pdf`, which will produce a `document-nup.pdf` in the current directory, with two pages per side in landscape orientation. 