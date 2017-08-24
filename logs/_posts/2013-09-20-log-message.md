---
layout: blog
title: Change the default GUI editor
date: 2013-09-20 22:09:00 +0530
day: Friday
tags:
  - log message
  - gvim
  - gedit
  - default gui editor
---

To change the default GUI editor, you simply need to change the corresponding records in the file `/usr/share/applications/defaults.list`. I just went there and did a `:%s/gedit/gvim/g` in order to get text files to open in gvim instead of in gedit.
