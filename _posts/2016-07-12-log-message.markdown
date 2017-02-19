---
layout: blog
title: Log Message
date: 2016-07-12 13:20:11 -0400
day: Tuesday
tags:
  - log message
  - python
  - user defined
  - module
  - package
---

To make a user-defined python module that you can import in many scripts, you must place your module in one of the site-packages directories in `sys.path`. If you are not using a virtual environment to run your programs in, then the correct place for this is `~/.local/lib/python3.4/site-packages/`. It was meant for exactly this purpose; see [PEP 370](https://www.python.org/dev/peps/pep-0370/). If you are using a virtualenv, then you could simply create a symbolic link in the virtualenv site-packages directory to your module. Or you could install your module in `/usr/lib/python3.4` with sudo privileges (probably not a good idea though). There should be a way to get virtualenv to look in `~/.local` as well, but I have not yet figured this out. 