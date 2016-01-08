---
layout: post
title: "CSS animations"
description: "css3 animation; css3 properties"
category: "html&css" 
tags: [CSS3, animation, property]
---
{% include JB/setup %}
CSS3 Animations
#Why?
With CSS3, we can create animations which can replace Flash animations, animated images, and JavaScripts in existing web pages.
#How?
##create animation with @keyframes Rule
Specify a CSS style inside the @keyframes rule and the animation will gradually change from the current style to the new style.  
Example:
   
    @-webkit-keyframes myfirst {
    from {background: red;}
    to {background: yellow;}
    }

    @keyframes myfirst {
    from {background: red;}
    to {background: yellow;}
    }
##Bind to selector
At least specifying two properties:
 1.the name of the animation
 2.the duration of the animation
Example:  

    div {
    -webkit-animation: myfirst 5s; /* Chrome, Safari, Opera */
    animation: myfirst 5s;
    }

##What exactly are CSS3 Animations?
An animation lets an element gradually change from **one style to another.**
##Usage
You can change as many properties you want, as many times you want.  
You can specify when the change will happen in percent, or you can use the keywords "from" and "to" (which represents 0% and 100%).  
0% represents the start of the animation, 100% is when the animation is complete.  
#CSS3 Properties
##CSS3 `animation-timing-function` Property
###Example  
Play an animation with the same speed from beginning to end:  

    div {
        -webkit-animation-timing-function: linear; /* Safari and Chrome */ 
        animation-timing-function: linear;
        }
###Property Values
linear:  
     The animation has the same speed from start to end   
ease:  
     Default value. The animation has a slow start, then fast, before it ends slowlyease-in   
ease-in:
     The animation has a slow start  
###More info about `animation-timing-function`
[Check it](http://www.w3schools.com/cssref/css3_pr_animation-timing-function.asp).  
##CSS3 `transform` Property
###Definition and Usage
The transform property applies a 2D or 3D transformation to an element. This property allows you to rotate, scale, move, skew, etc., elements.
###Example
Rotate a div element:

    div
    {
    transform:rotate(7deg);
    -ms-transform:rotate(7deg); /* IE 9 */
    -webkit-transform:rotate(7deg); /* Opera, Chrome, and Safari */
    }
###[More Details](http://www.w3schools.com/cssref/css3_pr_transform.asp)
