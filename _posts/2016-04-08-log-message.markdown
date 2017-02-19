---
layout: blog
title: Log Message
date: 2016-04-08 00:22:21 -0400
day: Friday
tags:
  - log message
  - sudo
  - environment
---

Test whether or not sudo is using the environment you expect by creating a small test script with `echo $HOME` for instance, and then running it as `sudo bash test.sh`. Note that testing the environment with `sudo echo $HOME` will *not* work, as bash expands `$HOME` before the command gets hit with sudo. The best way to get sudo to use the environment *you* want for a one-time job is to simply supply the environment variable while executing: `sudo HOME=/home/praveen pip3 install numpy`. For a more permanent solution, edit the /etc/sudoers file using `sudo visudo`. 