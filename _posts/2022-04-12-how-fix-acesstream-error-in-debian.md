---
layout: post
title: How fix Acestreamplayer error in Debian Linux
description: Hook for fix some acestreamplayer error in Debian Linux
---

# How fix some Acestreamplayer error in Debian 

```
sudo apparmor_parser -r /etc/apparmor.d/*snap-confine* 
sudo apparmor_parser -r /var/lib/snapd/apparmor/profiles/*
snap run acestreamplayer
```
[back]({{ site.url }})