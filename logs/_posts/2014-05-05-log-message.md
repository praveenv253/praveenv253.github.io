---
layout: blog
title: Generating RSA keys
date: 2014-05-05 16:43:58 +0530
day: Monday
tags:
  - log message
  - ssh
  - keygen
  - id_rsa
---

In order to create a pair of RSA keys, use `ssh-keygen -t rsa -C "user@host"`. The `-C` option is optional, but can be used to put your email address into the key.
