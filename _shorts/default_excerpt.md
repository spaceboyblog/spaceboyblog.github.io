---
layout: single
title: 디폴트 excerpt 발췌, 인용
---
_config.yml의 디폴트는 excerpt_separator: "\n\n"


excerpt 는 자동으로 <p> 태그로 묶습니다.  
이러한 태그를 제거하려면 remove 필터를 적용하세요.
{% raw %}
    {% for short in site.shorts %}  
        [{{ short.excerpt | remove: '<p>' | remove: '</p>' }}]({{ short.url }})  
    {% endfor %}
{% endraw %}  

Key information users need to know to achieve their goal. 
{: .notice--success} 

<div>
<strong>&#123;% raw %&#125;</strong>  <br>
&emsp;&emsp;&#123;% for short in site.shorts %&#125;  <br>
&emsp;&emsp;&emsp;&emsp;[&#123;&#123; short.excerpt | remove: '&lt;p&gt;' | remove: '&lt;/p&gt;' &#125;&#125;]  (&#123;&#123; short.url &#125;&#125;)   <br>
&emsp;&emsp;&#123;% endfor %&#125;   <br>
<strong>&#123;% endraw %&#125;</strong>   <br>
</div>
{: .notice--danger} 

<div>
{% raw %}
&#123;% raw %&#125;   <br>
&emsp;&emsp;{% for short in site.shorts %}  <br>
&emsp;&emsp;&emsp;&emsp;[{{ short.excerpt | remove: '&lt;p&gt;' | remove: '&lt;/p&gt;' }}]({{ short.url }})  <br>
&emsp;&emsp;{% endfor %}  <br>
&#123;% endraw %&#125;
{% endraw %}
</div>

> [!TIP]
> Optional information to help a user be more successful.
> {{ post.excerpt | remove: '<p>' | remove: '</p>' }}

참조 링크  
[텍스트 강조 1](https://mmistakes.github.io/minimal-mistakes/docs/utility-classes/#notices)    
[텍스트 강조 2](https://sehoon1207.github.io/jekyll/jekyll-_1_notice/)  


