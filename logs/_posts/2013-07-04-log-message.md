---
layout: blog
title: Reload NVidia kernel module after suspend
date: 2013-07-04 14:04:30 +0530
day: Thursday
tags:
  - log message
  - nvidia
  - cuda
  - suspend
  - kernel module
---

So I was facing this problem wherein the nvidia kernel module seemed to be getting unloaded after the computer was put to sleep. This can be resolved by explicitly adding the nvidia kernel module to the list of modules unloaded and reloaded before/after suspend. You do this by editing/creating the file `/etc/pm/config.d/unload_modules`. In it, add the following line: `SUSPEND_MODULES="$SUSPEND_MODULES nvidia"`. And that's it! Putting the computer to sleep now will not interfere with cuda executability! See [this link](http://www.techytalk.info/ubuntu-fix-network-stopped-working-after-resume-from-sleep/).
