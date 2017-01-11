---
layout: post
category :  blog
title: "setting up blog using github"
tags : [jekyll]
---
{% include JB/setup %}
# 使用github pages搭建blog。譬如[本站](https://github.com/PetersonLian/PetersonLian.github.io);
# jekyll使用注意
## jekyll使用markdown和liquid语法，来生成需要的静态页面。同时伴有YAML语法
### liquid
语法参见 [链接一](http://www.cnblogs.com/lslvxy/p/3651936.html)
[liquid官网](https://help.shopify.com/themes/liquid/basics)
### YAML语法参见
### include JB/setup
JB下面有setup文件
其中如下代码:

    !% else %!
      !% capture ASSET_PATH %!!! BASE_PATH !!/assets/themes/!! page.theme.name !!!% endcapture %!
    !% endif %!  

说明，需要设置`theme.name`，否则会资源文件404
当前，存在两个情况。

*   情况一，很早之前（一开始），我在`_layouts/default.html`里头定义了`theme.name`

        ---
        theme : 
          name : solar
        ---
        !% include JB/setup %!
        !% include themes/solar/default.html %!
又由于`_layouts/`下面的所有html文件，都有一个`layout: default`,从而能保证`theme.name`在所有地方都被定义了，并且为`solar`，从而不会报错

*   情况二，之后。情况一失效了。所以，目前的解决方案可以是在每一个页面(譬如index.md, 2016-xxxx-xx.md)一开始，就用`YAML`语法定义`theme.name`

    但我此处采用了另一种方案。在_includes/下新建custom/setup。然后再_config.yml里头的JB选项下配置setup选项。便于custom/setup里头使用。从而最终将asset路径配置正确
    参考。[Jekyll Global Variables](http://jekyllrb.com/docs/variables/); custom/setup的编写，则使用 liquid 语法
    