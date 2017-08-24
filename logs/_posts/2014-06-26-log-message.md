---
layout: blog
title: Find headers required by a cpp file
date: 2014-06-26 00:45:40 +0530
day: Thursday
tags:
  - log message
  - g++
  - make
  - dependencies
---

In order to find out which headers each .cpp file requires, perform a `g++ -MM file.cpp`. This lists out the dependencies for converting `file.cpp` into an object file. `man g++` and do a `/-M` for the whole list of sub-options. `-MM` does not list system libraries.
