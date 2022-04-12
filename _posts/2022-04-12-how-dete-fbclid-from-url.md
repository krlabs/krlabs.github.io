---
layout: post
title: How delete fbclid param from URLs
description: Hook how delete fbclid param from URLs of your website.
---

# How delete fbclid param from URLs

```
# need add in .htaccess
 
RewriteCond %{QUERY_STRING} "fbclid=" [NC]
RewriteRule (.*) /$1? [R=301,L]
```
[back]({{ site.url }})