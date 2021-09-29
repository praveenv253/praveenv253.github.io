---
layout: blog
title: Temporarily redifining macros with gcc
date: 2014-02-03 19:00:46 +0530
day: Monday
tags:
  - log message
  - gcc
  - preprocessor
  - macros
---

You can save and restore macros by using `#pragma push_macro("<macro_name>")` and `#pragma pop_macro("<macro_name>")` respectively! This means that you can temporarily redefine macros! For example, I used this to temporarily redefine `GSL_REAL` to `std::real`, and then define it back once the need had passed.