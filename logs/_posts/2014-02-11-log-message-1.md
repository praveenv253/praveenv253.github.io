---
layout: blog
title: Fixing a corrupted sudoers file
date: 2014-02-11 12:46:08 +0530
day: Tuesday
tags:
  - log message
  - sudoers
  - file corruption
---

If you accidentally corrupt your `/etc/sudoers` file (usually by reading it without sudo, incorrectly interpreting that it is empty, and then writing into it _with_ sudo, and finally being unable to correct it because you can no longer use sudo mode), there is a way out. You can use `pkexec visudo`, which will allow you to edit the sudoers file, provided you are authorized to run programs as root with PolicyKit. Find the default `/etc/sudoers` file online: [https://wiki.debian.org/sudo](https://wiki.debian.org/sudo). In case you are not authorized via PolicyKit, you can still edit the sudoers file using a live CD. Mount the computer hard drive at `/mnt`, say, and then `sudo visudo -f /mnt/etc/sudoers`. Courtesy of [this AU question](http://askubuntu.com/questions/73864). Of course, `man sudoers` and `man visudo` will tell you more as well.
