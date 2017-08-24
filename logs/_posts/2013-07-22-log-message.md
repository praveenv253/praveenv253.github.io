---
layout: blog
title: cudaMemcpyToSymbol issues
date: 2013-07-22 17:59:08 +0530
day: Monday
tags:
  - log message
  - cuda
  - constant memory
  - cudamemcpytosymbol
---

When using `cudaMemcpyToSymbol`, you can directly use the name of the variable you are transferring data to. In fact, this is the only way it seems to work. `var`, `&var`, etc. all do not have the desired effect, despite the function seeming to request a const char or a pointer. Also note that if you are including the `cudaMemcpyKind`, then it is the fifth parameter, not the fourth. The fourth parameter is an offset.
