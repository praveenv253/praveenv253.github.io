---
layout: blog
title: Linear regression in numpy and scipy
date: 2015-03-22 03:14:02 -0400
day: Sunday
tags:
  - log message
  - numpy
  - scipy
  - linear regression
---

Note that there are multiple numpy/scipy functions that do regression, fitting, etc. Of these, `scipy.stats.linregress` fits a line and forces an intercept. You do not have to explicitly add 1s or anything. `numpy.linalg.lstsq` does plain old linear regression - your inputs can even be matrices. It simply returns `argmin |ax - b|^2` for given `a` and `b`, and therefore does not force an intercept. The last one I want to mention is `scipy.optimize.leastsq`. This one is a non-linear least squares solver, and I know nothing more about it.
