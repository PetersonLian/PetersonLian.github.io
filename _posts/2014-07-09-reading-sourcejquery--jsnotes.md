---
layout: post
title: "reading source:jquery & js;notes"
description: ""
category: jquery
tags: [jquery, js, notes]
---
* * *
Code:  
{% include JB/setup %}
    (function($){
        $.fn.disableSelection = function() {
            return this
                 .attr('unselectable', 'on')
                 .css('user-select', 'none')
                 .on('selectstart', false);
                 };
    })(jQuery);
#What does (function($) {})(jQuery); mean?
##`(function(){...})()` means...
At the most basic level, something of the form (function(){...})() is a function literal that is executed immediately. What this means is that you have defined a function and you are calling it immediately.
##jQuery plugin
A variation of this basic form is what you see in **jQuery plugins** (or in this module pattern in general).   
##More
for more details ,check this [site](http://stackoverflow.com/questions/6984323/what-does-function-jquery-mean?lq=1).  
Check a easy [jQuery tutorial](http://www.queness.com/post/112/a-really-simple-jquery-plugin-tutorial).
* * *
jQuery.cssHooks
#What is it?
The `$.cssHooks` object provides a way to define functions for getting and setting particular CSS values. It can also be used to create new cssHooks for normalizing CSS3 features such as box shadows and gradients.
#How it is written?
##First, you wrote something.Which is basically the same as follows.
    if ( !$.cssHooks ) {
    // If not, output an error message
    throw( new Error( "jQuery 1.4.3 or above is required for this plugin to work" ) );
    }
##Then,you wrote 'styleSupport' function.Which is basically the same as follows.
    function styleSupport( prop ) {
    var vendorProp, supportedProp,
        capProp = prop.charAt(0).toUpperCase() + prop.slice(1),
        prefixes = [ "Moz", "Webkit", "O", "ms" ],
        div = document.createElement( "div" );
 
    if ( prop in div.style ) {
      supportedProp = prop;
    } else {
      for ( var i = 0; i < prefixes.length; i++ ) {
        vendorProp = prefixes[i] + capProp;
        if ( vendorProp in div.style ) {
          supportedProp = vendorProp;
          break;
        }
      }
    }
 
    div = null;
    $.support[ prop ] = supportedProp
    return supportedProp;
  }
##Now, you set your own customized 'cssHooks' functionality code.
For Example:  

    if ( animationDuration && animationDuration !== "animationDuration" ) {
       $.cssHooks.animationDuration = {
       get: function( elem, computed, extra ) {
        return $.css( elem, animationDuration );
        },
      set: function( elem, value) {
        elem.style[ animationDuration ] = value;
      }
    };
    }
#See an whole example?
Check this [site](http://jenniferdewalt.com/js/bouncing_ball.js).