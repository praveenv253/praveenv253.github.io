---
layout: blog
title: Using apt-get behind a proxy
date: 2014-02-11 12:29:20 +0530
day: Tuesday
tags:
  - log message
  - apt
  - proxy
  - sudoers
---

Often what happens is that the proxy settings that are set via the command line are not reflected when executing `sudo apt-get update`/`upgrade`. The reason this happens is because root has a different set of environment variables than the ones that the user calling sudo does. In order to pass on environment variables to root when executing sudo, you need to edit the `/etc/sudoers` file. WARNING: Editing this file is dangerous. A corrupted sudoers file may prevent you from using sudo mode. Always use `visudo` to edit the sudoers file. The sudoers file, by default, has a setting that goes `Defaults env_reset`. This resets all but a few key environment variables. In order to retain variables of your choice, you need to add them to the `env_keep` list. This goes: `Defaults env_keep += "http_proxy https_proxy ftp_proxy"`, for example. `man sudoers`. Also `man visudo`. Take a look at [this link](https://help.ubuntu.com/community/AptGet/Howto) for more apt options. Take a look at [this SO question](http://stackoverflow.com/questions/8633461/how-to-keep-environment-variables-when-using-sudo) regarding retaining environment variables while using sudo. Also, [here's my answer on AskUbuntu](https://askubuntu.com/a/424542/251032) regarding this issue.
