---
layout: blog
title: Numpy float sizes
date: 2013-12-23 10:37:15 +0530
day: Monday
tags:
  - log message
  - numpy
  - float
  - sizeof
---

Numpy uses 64-bit floats by default, although supposedly this is implementation dependent. If you are reading this several years from now, then you will have to re-check the validity of this number. In any case, in order to use, say, 32-bit floats instead, use `np.float32`. You also have a float16 and a float128, as of now.
