---
layout: blog
title: "Visualizing the output of python's cprofile"
date: 2017-06-13 04:21:16 -0400
day: Tuesday
tags:
  - log message
  - python
  - profiling
  - visualization
  - kcachegrind
---

To better visualize the call tree after profiling a python script, first save your output from cProfile using `python -m cProfile -o <myscript.profile> <myscript.py>`. You will need to install [`pyprof2calltree`](https://pypi.python.org/pypi/pyprof2calltree/) via pip and `kcachegrind` via apt. Then, visualize the profile data with `pyprof2calltree -i <myscript.profile> -k`. Reference: [this](https://stackoverflow.com/a/3561512/525169) SO answer.
