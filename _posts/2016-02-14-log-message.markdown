---
layout: blog
title: Installing scikit-learn via pip, without sudo and with a static ATLAS
date: 2016-02-14 04:41:56 -0500
day: Sunday
tags:
  - log message
  - atlas
  - blas
  - lapack
  - scikit-learn
  - pip
  - install
---

Installing scikit-learn via pip on a machine with no sudo privileges, and a static ATLAS lib can be a nightmare if you do not know what you are doing: the idea is to use the --global-option flag of pip install to pass extra commands to build_ext. See [this](http://stackoverflow.com/a/22942120/525169) SO answer. In this particular instance, you probably want to use something like --global-option=build_ext --global-option=-I/path/to/include --global-option=-L/path/to/lib --global-option=-latlas --global-option=-lcblas ... scikit-learn (where ... is for the other blas libs). Also see [this](http://scikit-learn-general.narkive.com/FSKFd98i/on-building-scikit-learn-0-14-1-with-static-atlas-on-non-standard-location) thread, which helped me out with these options 
