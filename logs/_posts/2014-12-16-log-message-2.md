---
layout: blog
title: Making xkb modifications permanent
date: 2014-12-16 11:38:45 +0530
day: Tuesday
tags:
  - log message
  - remap
  - caps lock
  - ctrl
  - 14.04
---

How do you make the settings described in the previous log message permanent? The first thing you need to do is to install dconf-editor. Open it up and go to org > gnome > desktop > input-sources. Here, there is an xkb-options setting. This is where you need to place your modifications. So change xkb-options to `['shift:both_capslock','ctrl:nocaps']`. This should take effect immediately and work fine on login. However, it will only work as long as you stay with the same keyboard configuration. If you change keyboard configurations, the xkb-options setting gets reset, and will not continue to work.
