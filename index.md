---
layout: page
title: 连培培 AKA Peterson Lian
---
{% include JB/setup %}
## Who is PetersonLian(连培培)?  
   Peterson is a 22 year old guy living in mainland China, earning very low payroll and hoping to see the world better with [Github](http://www.github.com).
   I am currently very screwed by fate and very happy to meet your.  
## Posts  
<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a><br/>
    {{ post.content | strip_html | truncatewords: 50 }}
    </li>
  {% endfor %}
</ul>  
## Contact Me?  
   Just email me:lianpeipei202@gmail.com.
