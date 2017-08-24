---
layout: blog
title: Creating desktop applications you can launch from X
date: 2014-05-13 22:52:00 +0530
day: Tuesday
tags:
  - log message
  - ubuntu
  - launcher
  - desktop
  - tvim
---

In order to make applications that you can "summon" from X, say by double-clicking on a file in nautilus, you need to create a `.desktop` file corresponding to your application. To figure out how to do this, look at [this link](https://help.ubuntu.com/community/UnityLaunchersAndDesktopFiles). [`tvim.desktop`](https://github.com/praveenv253/misc/blob/master/tvim.desktop) makes for a good template. I have also made a couple of notes in [`misc/tvim.sh`](https://github.com/praveenv253/misc/blob/master/tvim.sh).
