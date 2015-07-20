---
layout: blog
title: Setting AFS permissions recursively
date: 2015-06-22 02:21:04 -0400
day: Monday
tags:
  - log message
  - afs
  - acl
  - file permissions
---

In order to recursively set AFS ACL permissions for a directory, you need to manually use `find -exec` as follows: `find <dir> -type d -exec fs sa {} <user> <permissions> \;`. [Here](http://kb.mit.edu/confluence/pages/viewpage.action?pageId=3907138) is the reference for this. 
