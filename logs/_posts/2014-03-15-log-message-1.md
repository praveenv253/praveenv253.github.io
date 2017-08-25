---
layout: blog
title: Order of linking static libraries with ld and g++
date: 2014-03-15 22:55:56 +0530
day: Saturday
tags:
  - log message
  - g++
  - gcc
  - ld
  - C++
  - C
  - make
---

When linking object files (static libraries) into an executable, the order in which you give the libraries matters. For simple scenarios where there are no cyclic references, the *dependent* library should come on the left, and the library which *provides said dependency* should come on the right. Take a look at [this SO question](http://stackoverflow.com/questions/45135/linker-order-gcc) to see a diagrammatic view of this, and also to see how cyclic dependencies can be resolved.
