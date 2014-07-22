---
layout: post
title: learn JQuery
tagline: "JQuery"
category: JQuery
tags: [JQuery]
---
{% include JB/setup %}

Read Documents in [this site](http://learn.jquery.com).
This is what I refine from the site above.  

#JavaScript 101       

##1.`$( document ).ready` 

>  run *ONCE* when *DOM* is ready for javascript code to execute.

##2.`$(window).load(function(){...})`

>  run *ONCE* when entire *PAGE*(images or iframes) is ready, not just DOM!

##3.named function   
>  e.g.   
>function readFn( jQuery ){     
>}

##4.put jQuery into *NO-CONFLICT* mode    
>  key code: `jQuery.noConflict()`   
>  e.g.      
    var $j = jQuery.noConflict();
>  now,you can use `$j` instead of `$`     
>  you can also name it as `jq` or `$JQ` etc. instead of `$j`

##5.another way for putting jQuery into *NO-CONFLICT* mode  
          
          <!-- Another way to put jQuery into no-conflict mode. -->
          <script src="prototype.js"></script>
          <script src="jquery.js"></script>
          <script>
          
          jQuery.noConflict();
          
          jQuery( document ).ready(function( $ ) {
          // You can use the locally-scoped $ in here as an alias to jQuery.
          $( "div" ).hide();
          });
          
          // The $ variable in the global scope has the prototype.js meaning.
          window.onload = function(){
          var mainDiv = $( "main" );
          }
          
          </script>

  pay attention to the code `jQuery( document ).ready(function( $ )`."function" gets a parameter which is `$`   

##6.don't conflict `$` in JQuery library with `$` in other library(e.g. prototype.js library) compare with *topic 4* and *topic 5* above  

  In this scenario, you don't need to call `jQuery.noConflict()`.
  *just load jQuery BEFORE* other libraries which will conflict `$` of JQeury.  
following is an example code snippet:

          <!-- Loading jQuery before other libraries. -->
          <script src="jquery.js"></script>
          <script src="prototype.js"></script>
          <script>
          
          // Use full jQuery function name to reference jQuery.
          jQuery( document ).ready(function() {
          jQuery( "div" ).hide();
          });
          
          // Use the $ variable as defined in prototype.js
          window.onload = function() {
          var mainDiv = $( "main" );
          };
          
          </script>

  you use `jQuery` instead of `$` and you are then in no need for calling `jQuery.noConflict()`.You use `$` normally for library *prototype.js* 

##7.**get** and **set** an elment's attributes     
  key code :_`.attr()`          
  it can be used as both setter and getter  

##8.Selectors    
  1.to use any of the meta-characters, must be escaped with __**two backslashes**__`\\`         
  2.Attribute Selector

    $("a[attributes]")  //<a> with attributes
    $("div[attributes]")    //<div> with attributes

  3.:animated Selector

    $("div:animated")   //<div> witch is in animation

  check out this [site](http://api.jquery.com/category/selectors/) for more.
##9.Data Method        
  store data with elements and JQuery manages the **Memory** issue for you！  

    $( "#myDiv" ).data( "keyName", { foo: "bar" } );
 
    $( "#myDiv" ).data( "keyName" );   // Returns { foo: "bar" }  

##10.Iterate over JQuery and Non-JQuery Objects.  
  key code:  
  `$.each()` for *non-jquery* objects.  
  `.each()` for *jquery* collections.   

  see this [site](http://learn.jquery.com/using-jquery-core/iterating/) for more!  

##11.[`.index()`](http://learn.jquery.com/using-jquery-core/understanding-index/) function  

##12.Draggable Widget
In **jQuery UI** library.  
Allow elements to be moved using the mouse.  
[An Example](http://jenniferdewalt.com/building_blocks.html) is here.  
