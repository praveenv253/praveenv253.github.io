---
layout: blog
title: NVidia kernel module reinstall
date: 2013-07-11 20:32:24 +0530
day: Thursday
tags:
  - log message
  - nvidia
  - kernel module
  - cuda
---

You need to reinstall the driver every time you update your linux kernel. This is so that the nvidia kernel module is correctly created inside the appropriate kernel folder. Uninstallation is achieved with "installer.run --uninstall". Reinstallation can be done as usual with "installer.run --optimus" and then selecting the driver for installtion.
