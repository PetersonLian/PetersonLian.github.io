---
layout: post
title: "jekyll configuration none?"
category: jekyll
tags: [jekyll, configuration, localhost]
---
{% include JB/setup %}
#When I run `jekyll serve` locally, the output has "Configuration:none" outcome and cannot be accessed through my browser.Why?
one possible reason is that you you run command `jekyll serve` in one subdirectory instead of root directory.  
To correct this, just switch to the root directory of your project and run `jekyll serve` there.