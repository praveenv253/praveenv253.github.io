---
layout: blog
title: Autoloading inputrc on ssh login
date: 2014-09-28 18:36:16 -0400
day: Sunday
tags:
  - log message
  - bash
  - inputrc
  - reload
---

When I ssh-ed into the ece server, `inputrc` was not loaded by default. So command-line history was not iPython-like. To make this happen, just press `Ctrl-X Ctrl-R` in bash. It re-reads the init file, i.e. reloads commands from `.inputrc`. [Source](http://superuser.com/questions/241187/how-do-i-reload-inputrc). [Reference](http://www.gnu.org/software/bash/manual/bashref.html#Miscellaneous-Commands).
