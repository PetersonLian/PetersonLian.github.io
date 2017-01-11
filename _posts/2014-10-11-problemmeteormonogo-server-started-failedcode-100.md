---
layout: post
title: "Problem|meteor|monogo server started failed|code 100"
description: "this is the diary recording me resovling a problem"
category: meteor
tags: [meteor]
---
{% include JB/setup %}
Must *first* watch this [comment](http://stackoverflow.com/questions/10103830/problems-to-run-examples-in-meteor#answer-15752736) from this [question](http://stackoverflow.com/questions/10103830/problems-to-run-examples-in-meteor) in stackoverflow.com.    

# In my case , I resovled it by 'meteor reset'  
Even though I resolved it.But I still think should read the comment aforementioned.  

# While follow the comment. I occured problem locating the directory where my 'meteor isntalled.
>    
>    dpkg -L package  

But unfortunate, my meteor wasn't installed by `apt-get install`  
By all means, I found out my 'meteor was installed in my /home/$ME  