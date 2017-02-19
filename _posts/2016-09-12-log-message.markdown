---
layout: blog
title: Making vim display italicised text
date: 2016-09-12 18:23:07 -0400
day: Monday
tags:
  - log message
  - vim
  - italics
  - comments
---

To make vim display italicised text, see [this](http://www.nerdyweekly.com/posts/enable-italic-text-vim-tmux-gnome-terminal/) wonderful blog entry. Essentially, we need to manually map the escape sequences to the keywords `sitm` and `ritm`, which are used by vim to set and remove italic mode respectively. The file in question, `xterm-256color-italic.terminfo`, has been added to the `misc` repository as well. It contains all relevant install info. Note that `TERM` must be set to `xterm-256color-italic` by `gnome-terminal` for this to take effect. [This](http://askubuntu.com/questions/233280/gnome-terminal-reports-term-to-be-xterm) askubuntu question tells you how to do it. Set the command executed by `gnome-terminal` to be `env TERM=xterm-256color-italic /bin/bash`. 
