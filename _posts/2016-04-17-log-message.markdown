---
layout: blog
title: Log Message
date: 2016-04-17 19:35:35 -0400
day: Sunday
tags:
  - log message
  - python
  - cvxopt
  - pip
  - mkl
---

To install cvxopt linked to Intel MKL using pip, set environment variables in the installation commands as follows: `sudo CVXOPT_BLAS_LIB_DIR=/opt/intel/mkl/lib/intel64 CVXOPT_BLAS_LIB=mkl_rt CVXOPT_LAPACK_LIB=mkl_rt HOME=$HOME pip3 install cvxopt`. It is as easy as that! To see more configuration options, download the cvxopt source files and look at the `setup.py` script. It lists which environment variables you can set. 