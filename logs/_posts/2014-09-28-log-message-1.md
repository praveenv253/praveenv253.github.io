---
layout: blog
title: Autoloading .bashrc on ssh login
date: 2014-09-28 18:41:52 -0400
day: Sunday
tags:
  - log message
  - profile
  - bashrc
---

My `~/.bashrc` file was not getting automatically loaded when I ssh-ed into the ece server. Turns out that you need a `~/.profile` file, which tells bash to load `~/.bashrc`. So I copied the default `~/.profile` file from my computer.
