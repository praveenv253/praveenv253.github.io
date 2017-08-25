---
layout: blog
title: Getting time stamps for bash history
date: 2014-07-23 18:07:20 +0530
day: Wednesday
tags:
  - log message
  - bash
  - history
  - timestamp
---

In order to get a time-stamped command line history for bash, look up the `HISTTIMEFORMAT` setting in the man pages for bash. My `HISTTIMEFORMAT` is currently set to `%F %T`, to understand which you have to look at the arguments to `strftime(3)`. `%F` means `YYYY-MM-DD` and `%T` means `hh:mm:ss`. These time stamps are stored in a weird fashion, possibly seconds from epoch or something, so you cannot understand them by just looking at the `.bash_history` file. Instead, use the `history` command. Here, the timestamps are formatted as requested. To find out more, do a `help history` (not `man`! - this is a bash thing).
