---
layout: post
title: Different SEO redirects for .htaccess Apache server
description: Different SEO-hook redirects for .htaccess Apache web-server
---

# Different SEO-redirects for .htaccess

```
# HTTP to HTTPS
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule (.*) https://%{HTTP_HOST}%{REQUEST_URI}
 
# Non-Slash to Slash URLs
<IfModule mod_rewrite.c>
RewriteEngine on
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^(.*[^/])$ /$1/ [L,R=301]
</IfModule>
 
# www to non-www 301
<IfModule mod_rewrite.c>
RewriteEngine On
RewriteCond %{HTTP_HOST} ^www.domain.com$
RewriteRule (.*) https://domain.com/$1 [R=301,L]
</IfModule>
 
# WORDPRESS brilliant 301 redirect www to non-www
RewriteEngine On
RewriteBase /
RewriteCond %{HTTP_HOST} ^www.(.*)$ [NC]
RewriteRule ^(.*)$ http://%1/$1 [R=301,L]
 
# Redirect from index to homepage
 
<IfModule mod_rewrite.c>
RewriteEngine On
RewriteRule ^index\.html / [R=301,L]
RewriteBase /
RewriteRule ^index\.php$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . /index.php [L]
</IfModule>
```
[back]({{ site.url }})