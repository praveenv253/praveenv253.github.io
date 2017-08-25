---
layout: blog
title: Debugging python deadlocks
date: 2017-06-15 02:38:01 -0400
day: Thursday
tags:
  - log message
  - python
  - deadlock
  - hanging
  - stuck
  - trace
---

Sometimes, a python script just gives up and hangs. Even Ctrl-C does not exit the program. You do not have to have a loop with a catch-all `except` command or anything. Apparently, this can happen because of what is known as a "deadlock", which refers to some kind of race condition when running a threaded program. I was not running a threaded program, except I *was*, because I was using BLAS. In this case, OpenBLAS, which appears to have had a history with deadlocks, and maybe still does, or maybe it was due to my having accidentally installed numpy with MKL and scipy with OpenBLAS. In any event, the only reason I found out that the issue was with blas.py is thanks to [this excellent little piece of software](https://pypi.python.org/pypi/hanging_threads/2.0.3), which shows you a stack trace if your program is inactive for more than 10 seconds. It is a python package called [`hanging_threads`](https://github.com/niccokunzmann/hanging_threads) and works like a charm. This invaluable tool was found after I finally figured out what to google for, and landed on [this SO page](https://stackoverflow.com/q/3443607/525169), and then scrolled down a lot after the top answer (`trace`) did not work for me. [`trace`](https://docs.python.org/3.4/library/trace.html) is a python module and is also really useful. It prints out the commands currently being executed. This is really neat because if your program suddenly (and hopefully deterministically) gives up, you get a full history of all the commands executed. The `--ignore-dir` flag is extremely useful, since you can avoid printing out various internal modules. I was lucky, since my packages of interest (`sht`, `cross_validation`, etc.) were under `$HOME/.local`, so I could just supply `--ignore-dir=/usr` and prevent tracing through imports like `sys` and `numpy`.
