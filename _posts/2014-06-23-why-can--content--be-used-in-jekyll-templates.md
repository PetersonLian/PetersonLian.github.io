---
layout: post
title: "why can '{{ content }}' be used in Jekyll templates"
category: liquid
tags: [liquid, {{content}}, jekyll, template]
---
{% include JB/setup %}
#Question: why can '{{ content }}' be used in Jekyll templates？         
that is because `content` is a special variable in **all templates**.  
The content variable holds the **page/post content** including any sub-template content previously defined.  
Render the `content` variable **wherever** you want into your template  
Example Usage:

        <body>
        <div id="sidebar"> ... </div>
        <div id="main">	{% raw %}
	    {{ content }}{% endraw %}
        </div>
        </body>

See more?Go to this [site](http://jekyllbootstrap.com/lessons/jekyll-introduction.html) where I figured out the answer to the question.