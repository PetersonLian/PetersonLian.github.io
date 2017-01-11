---
layout: post
title: "Read Sourcecode Elisp 'simple.el.gz' 'next line'"
description: ""
category: "emacs"
tags: [elisp]
---
{% include JB/setup %}
#How to find file 'simple.el.gz'?
Reading Elisp inside emacs, evoking `M-h k`, then inputing "Ctrl-n" in minibuffer.  
Go to ```simple.el'`` and click RET. There you go.  
#Notes
##hard-newlines vs. soft-newlines?
check this [site](http://ergoemacs.org/emacs_manual/emacs/Hard-and-Soft-Newlines.html) out for detals.  
##car?cdr?
these are opretion working on CONs cells.  
>car (short for "Contents of the Address part of Register number")  
>cdr ("Contents of the Decrement part of Register number")

For your better understanding:  
`(car (cons x y))` evaluates to x, and `(cdr (cons x y))` evaluates to y.  

#Still dont know...
##abbrev-mode
    (let ((abbrev-mode nil))
	    (end-of-line)
	    (insert (if use-hard-newlines hard-newline "\n")))
is `abbrev-mode` a global variable?  
If `abbrev-mode` is a local variable, why didn't it be used in `let` expression?  
##condition-case
    (condition-case err
	    (line-move arg nil nil try-vscroll)
	  ((beginning-of-buffer end-of-buffer)
	   (signal (car err) (cdr err))))
After reading the documentation(evoke by `M-h f`),I still feel confused.
##what if arg is set greater than 1.
Scenario:`C-u 3 RET C-n`  
what is the "execute path" in the code?I just can't work it out.  

    