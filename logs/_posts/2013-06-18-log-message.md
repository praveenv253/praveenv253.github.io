---
layout: blog
title: Retain colors after piping through less
date: 2013-06-18 22:17:01 +0530
day: Tuesday
tags:
  - log message
  - less
  - colour
  - grep
---

In order to retain colours when passing output through less, use the -R option. Also ensure that the program sending output is configured to send out colour even if it detects that the output is going to a pipe and not to stdout. For eg. grep will give you colour through a pipe only if you use the --color=always command line argument. --color=auto does not do so.
