---
layout: post
category :  html&css
tags : [css]
title: Cascading Order|css规则权重
---
{% include JB/setup %}

这篇文章是一个总结，总结css规则是如何应用的。
来源自[w3文档](https://www.w3.org/TR/2011/REC-CSS2-20110607/cascade.html#cascading-order)

# 先集合可应用于element的所有规则，在满足media type(media query)的前提下

# 根据重要度和来源，如下规则的权重有低至高
1.  浏览器(user agent)声明的规则
2.  用户(不是网站的程序员)普通声明的规则
3.  网站作者(程序员)普通声明的规则
4.  网站作者(程序员)重要声明(!important)的规则
5.  用户(不是网站的程序员)重要声明(!important)的规则

# 当两条规则重要度和来源都一样时,计算规则的权重,计算出来的值较高的获胜
1.  首先最后计算出来的权重分为4位（千、百、十、个），分别对应（a,b,c,d）
2.  如果是element的style属性（例如html代码中style="xxx"）,那么a=1(赋值为1)，否则就是a=0;
3.  规则里头的选择器(selector).如果出现一次id，那么b+1;最后b=id选择器出现次数;
4.  规则里头的选择器(selector).计算出现attributes(譬如类名)和假类的数量(我认为，应该是不重复。一个类算一次);数量赋予c;
5.  规则里头的选择器(selector).计算出现的标签名和假标签(譬如 :first-line)的次数；数量赋予d;
