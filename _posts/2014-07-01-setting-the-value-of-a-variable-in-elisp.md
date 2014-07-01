---
layout: post
title: "Setting the Value of a Variable in elisp"
description: ""
category: "elisp"
tags: []
---
{% include JB/setup %}

Quoted from [here](https://www.gnu.org/software/emacs/manual/html_node/eintr/set-_0026-setq.html)  
>  There are several ways by which a variable can be given a value. One of the ways is to use either the function set or the function setq. Another way is to use let(see let). (The jargon for this process is to bind a variable to a value.)
Now, you need to ask your self following questions.  
#Q1:what does `set` and `setq` differ?  
A1:`setq` is like `set` except that the first argument is quoted automatically.  
It means `(set 'carnivores '(lion tiger leopard))` has the same effect with `(setq carnivores '(lion tiger leopard))`.The first argument `carnivores` must be quoted in `set` statement or else it will be evaluated first without doing anything else.For your better understanding.Supposing you have a argument `carnivores` with value of "lion",if you don't quote it in a `set` statement, the "lion" will be used to store the list "(lion tiger leopard)" witch will be wrong because " Symbol's value as variable is void ".  
*Also* setq can be used to assign different values to different variables.e.q.`(setq trees '(pine fir oak maple)
           herbivores '(gazelle antelope zebra))`  
#Q2:what's the differences between `let` and `set*`?  
A2:`let` expression is more like a setq that is temporary and local.Let creates a name for a local variable that overshadows any use of the same name outside the let expression. The local variables have no effect outside the let expression.  
Also, let gives each variable it creates an initial value, either a value specified by you, or nil.  