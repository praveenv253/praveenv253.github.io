---
layout: blog
title: Debugging a C program with a python frontend
date: 2013-07-19 12:33:41 +0530
day: Friday
tags:
  - log message
  - gdb
  - debugging
  - python
---

If you want to debug a C or C++ program that has a python frontend, then run python using gdb. Then, inside gdb, use the `set args` command to set the python script to execute. Run the script until it encounters an issue, at which point you can use backtrace to show you the stack. `help stack` tells you how to examine the stack. 
