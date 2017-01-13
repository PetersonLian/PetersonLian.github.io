---
layout: post
category :  WebApp
tags : [WebApp, viewport]
---
{% include JB/setup %}

这篇[文章](http://www.cnblogs.com/2050/p/3877280.html)解释地很好。此blog是这篇文章的要点提炼。

# css的1px并不等于物理上的一个像素?
# 三种viewport?
1.  layout viewport
2.  visual viewport
3.  ideal viewport
;iphone系列都是360.android有320、360、384、400等几种

# layout viewport js访问?
document.clientWidth

clientWidth, [mdn](https://developer.mozilla.org/en-US/docs/Web/API/Element/clientWidth)

without scrollbar、border、margin
# visual viewport js访问?
window.innerWidth

innerWidth, [mdn](https://developer.mozilla.org/en-US/docs/Web/API/Window/innerWidth)

包括scrollbar
# 如何调整到ideal viewport?
**使用viewport的meta标签**
## width=device-width
iphone和ipad,不管水平模式还是垂直模式，都是跟垂直模式的width一致
## initial-scale
相对于ideal-viewport的宽度

譬如值为2，那么原始的ideal-viewport为640,设为2后，实际为320
## target-densitydpi(已弃用)