---
layout: blog
title: C++ template functions and header files
date: 2014-03-15 22:52:34 +0530
day: Saturday
tags:
  - log message
  - C++
  - templates
  - template functions
---

"The implementation of a non-specialized template must be visible to a translation unit that uses it. The compiler must be able to see the implementation in order to generate code for all specializations in your code." What this essentially means is that you cannot define an external templated function in the typical way: have the template function declaration in the header, followed by an implementation of the template function in a C++ file, which then gets compiled into an object file, and later gets linked with the main program. This method does not work. Why? Because the compiler needs to "know" what the "full" definition of the function is (with actual classes of the templated types) in order to actually compile the program. A template function is simply a sort of shorthand for writing many functions of that do the same thing with different data types; but the compiler still needs to actually create "specializations" of this template for each type that actually gets used. That is the only way it can generate object code. Check out [this link](http://stackoverflow.com/questions/10632251/undefined-reference-to-template-function) on ways to resolve this issue. One method involves putting the implementation in the header. The other method involves pre-defining the specializations.