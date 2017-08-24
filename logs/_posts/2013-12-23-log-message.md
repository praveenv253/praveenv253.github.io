---
layout: blog
title: C++ stdlib manpages
date: 2013-12-23 10:23:35 +0530
day: Monday
tags:
  - log message
  - cpp
  - man
  - c++
---

In order to look at the C++ man pages, do a `man std_<blah>`. For example, `man std_list` or `man std_complex`. To see what man pages are available, do an `apropos -r "^std_" | grep <blah>`. Note that these man pages are available only after you have installed `libstdc++6-x.x-doc`.
