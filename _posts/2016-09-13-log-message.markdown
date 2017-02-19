---
layout: blog
title: Log Message
date: 2016-09-13 14:07:40 -0400
day: Tuesday
tags:
  - log message
  - vim
  - print
  - hardcopy
  - syntax-highlighting
  - colorscheme
---

If you want to export from vim to a pdf file with syntax highlighting, hardcopy does not seem to use the correct syntax highlighting file. Or rather, it uses GUI settings, which means that unless your syntax highlighting file takes care of looking good on gvim, it will not give you a good result. For you to get syntax highlighting _at all_, you must first `:set term=xterm-256color-italic` even if it is already set. Do it even if `:set term` returns `xterm-256color-italic`. Then, to actually get _terminal colours_, use `:TOhtml`, which converts the file into an html page, which you can then print from your browser. For a good print colorscheme, run `:colorscheme print`, which is is a custom light-background colorscheme I made for printing. Do this before running `:TOhtml`, obviously. 