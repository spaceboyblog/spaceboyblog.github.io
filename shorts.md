---
layout: single
title: shorts
---

{% for short in site.shorts %}  
#### [{{ short.title }}]({{ short.url }})  
[{{ short.excerpt | remove: '<p>' | remove: '</p>' }}]({{ short.url }})  
{% endfor %}