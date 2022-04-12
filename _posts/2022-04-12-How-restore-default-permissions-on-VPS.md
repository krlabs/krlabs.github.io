---
layout: post
title: How restore default permissions on VPS
description: Basic hook how restore default permissions on Linux virtual server.
---

# How restore default permissions on VPS

```
find /var/www/ -type d -exec chmod 755 {} \;
find /var/www/ -type f -exec chmod 644 {} \;
```
[back]({{ site.url }})