---
layout: blog
title: Changing user and group IDs in Linux
date: 2014-01-03 17:21:26 +0530
day: Friday
tags:
  - log message
  - linux
  - usermod
  - users
  - uid
---

Changing a user id will only change ownership of files that are in that user's home directory. Look at [this SO question](http://stackoverflow.com/questions/18248056/change-user-id-in-linux). Also, you might have to change the group id of the user's group before changing the user and group ids of a user, because the new group must exist before you can change the group id. Doing a `man usermod` also helps.
