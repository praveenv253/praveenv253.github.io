---
layout: blog
title: Expanding the number of dimensions of a numpy array
date: 2014-10-30 02:14:03 -0400
day: Thursday
tags:
  - log message
  - numpy
  - ndarray
  - expanding dimensions
---

In order to expand the number of dimensions of a numpy array, there are several options: `np.expand_dims(x, axis=1)` or `x[:, np.newaxis]` or `x[:, None]`. Refer [this](http://docs.scipy.org/doc/numpy/reference/generated/numpy.expand_dims.html) doc page.
