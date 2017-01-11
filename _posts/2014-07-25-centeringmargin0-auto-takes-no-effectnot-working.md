---
layout: post
title: "centering(margin:0 auto) takes no effect(not working)"
description: ""
category: html&css
tags: [css]
---
{% include JB/setup %}
#why does action centering(margin:0 auto) takes no effect(not working)?
A:there can be mulitple reasons.  
1. It may because of browsers' fault.Make sure you are not using old IE or any unsupported browsers.  
2. It may because of block-level element or inline-level element related .  
3. It may because of you didn't add 'width' property .  
#Ok, I have addressed the reason. Now how to fix it?
check out [this post](http://stackoverflow.com/questions/5734199/margin0-auto-not-working) for details.