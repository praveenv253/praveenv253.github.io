---
layout: blog
title: glibc version
date: 2014-05-04 22:46:39 +0530
day: Sunday
tags:
  - log message
  - glibc version
  - ldd
---

You can find out your glibc version by running `ldd --version`. You can also do a `locate libc.so.6` and then execute the shared library like a program. This actually displays the version and some additional compile information.