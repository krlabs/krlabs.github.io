---
layout: post
title: How make responsive Contact Form 7 in WordPress
description: Hook for style css to make responsive on mobile devices contact form 7 in CMS WordPress
---

# How make responsive Contact Form 7 on mobile devices in WordPress

```
@media screen and (max-width: 768px){
.wpcf7 #Personal-Details, .wpcf7 #Education, .wpcf7 #Profession, .wpcf7 #To-Teach, .wpcf7 #Timings, .wpcf7 #Colscol, .wpcf7 #Upload {
height:auto;
padding: 20px;
}
#Teacher-column #left {
width: 100%;
float: none;
margin-bottom: 20px;
}
 
.input-text, input[type=email], input[type=password], input[type=search], input[type=tel], input[type=text], input[type=url], textarea {
width: 100%;
}
 
span.wpcf7-list-item {
display: block;
margin: 20px 0 0 1em;
}
 
.wpcf7 #Upload p{
line-height:21px;
}
}
```
[back]({{ site.url }})