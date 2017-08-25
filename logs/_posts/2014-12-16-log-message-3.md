---
layout: blog
title: "Remapping Caps Lock to Control in Ubuntu 14.04"
date: 2014-12-16 11:32:00 +0530
day: Tuesday
tags:
  - log message
  - remap
  - caps lock
  - ctrl
  - 14.04
---

Remapping Caps Lock to Control in 14.04 was one of the biggest headaches in a long long time. But here is what you have to do: [this link](http://www.linux.com/learn/tutorials/769644-hacking-your-linux-keyboard-with-xkb) shows you how you can use xkb to make modifications to key functions. But it does not list all possible modifications that exist. To see what modifications xkb already provides, take a look at `/usr/share/X11/xkb/symbols`. There are files called `ctrl` and `capslock` and such. The file `ctrl`, for example, has a modification called `nocaps`. You can now use this modification from command line by saying: `setxkbmap -option "ctrl:nocaps"`. Another modification I liked was `"shift:both_capslock"`, which toggles caps lock when you press both shift keys together. To be continued...
