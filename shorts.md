---
layout: single
title: shorts
---
<style>
body h4 > a,
body h4 > a:link,
body h4 > a:visited,
body h4 > a:hover,
body h4 > a:focus,
body h4 > a:active {
    text-decoration: none;
    color: black;
    outline: none;
}
</style>
{% for short in site.shorts %}
#### [{{ short.title }}]({{ short.url }})  
[{{ short.excerpt | remove: '<p>' | remove: '</p>' }}]({{ short.url }})
{% endfor %}