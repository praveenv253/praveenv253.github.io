---
layout: blog
title: Undoing a git commit --amend
date: 2013-07-19 21:50:03 +0530
day: Friday
tags:
  - log message
  - git
  - commit
  - undo amend
---

In order to undo a `git commit --amend`, take a look at the `git reflog`. `HEAD@{1}` will contain the commit just before the amend (assuming that the amend was made _just_ now). So, reset to `HEAD@{1}` softly. This will make the erroneous amendment show up in the staging area. Then, you can commit it separately, with `git commit -C HEAD@{1}`, for example. Note that after resetting, the reflog has changed so that `HEAD@{1}` is now pointing to the amended commit. Take a look at [this link](http://stackoverflow.com/questions/1459150/how-to-undo-git-commit-amend-done-instead-of-git-commit).
