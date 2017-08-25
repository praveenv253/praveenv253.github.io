---
layout: blog
title: C++ chrono lib resolution
date: 2013-09-13 18:01:01 +0530
day: Friday
tags:
  - log message
  - chrono
  - timing
---

Dug a little deeper into outputting time durations. It turns out that `time_point` has a default accuracy that is system-implementation-dependent or something. My system seems to be only microsecond accurate. Read [this](http://stackoverflow.com/questions/15777073/how-do-you-print-a-c11-time-point) for more info.
