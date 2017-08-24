---
layout: blog
title: Friendship is not inherited
date: 2013-07-16 17:33:31 +0530
day: Tuesday
tags:
  - log message
  - C++
  - friend
  - inheritance
---

Friendship is **not** inherited. `class A { friend class B; }; class B { }; class C : public B { };` => `C` cannot access private and protected members of `A`! 
