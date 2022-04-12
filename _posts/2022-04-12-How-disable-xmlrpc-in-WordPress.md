---
layout: post
title: How disable xmlrpc in WordPress
description: Hook how easy disable vulnerability xmlrpc.php in CMS WordPress
---

# How easy disable xmlrpc in WordPress

```
# add in .htaccess
<Files xmlrpc.php>
order deny,allow
 deny from all
</Files>
 
# add in functions.php
add_filter('xmlrpc_enabled', '__return_false');
```
[back]({{ site.url }})