---
layout: blog
title: Changing or adding fonts to Matplotlib
date: 2014-06-14 22:33:13 +0530
day: Saturday
tags:
  - log message
  - matplotlib
  - fonts
---

When trying to change fonts in matplotlib, you might run into an error that says that the font or the font family was not found. To fix this, you need to actually add the font to matplotlib's font database. For me, this is in `/usr/share/matplotlib/mpl-data/fonts/ttf`. Create a symbolic link to the font of your choice over here. Then use the _name_ of the font package - open the font file with the default Font Viewer for this - in matplotlibrc to set your font preference.
