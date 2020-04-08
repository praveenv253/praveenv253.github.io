---
layout: blog
title: Encrypting files with gpg
date: 2014-07-14 00:47:50 +0530
day: Monday
tags:
  - log message
  - encryption
  - gpg
---

Encrypt a file with `gpg -c <file>`. Decrypt with `gpg <file>`. Be sure to delete the un-encrypted file after encryption. `shred` it, perhaps.