---
layout: post
title: "emacs flyspell mode conflict with auto complete "
description: "auto-complete isn't working"
category: emacs
tags: [emacs, auto-complete, fly-spell]
---
{% include JB/setup %}
#Why doesn't auto-complete mode work in some modes?
A: please make sure these modes don't have a fly-spell minor mode opening.
#What if my fly-spell minor mode is automaticaly opened?
A:well.I don't know what to do yet.Currently I manually close fly-spell mode in the specified buffer and
then invoke Auto-Complete-mode