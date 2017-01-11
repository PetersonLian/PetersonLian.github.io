---    
layout : post
category : html&css
tagline : "notes"
tags : [html, css]
---
{% include JB/setup %}

通过[这个网站](http://learn.shayhowe.com/html-css/)学习HTML&CSS的各种笔记

# Lesson2 
  *Gettting to Know HTML*  
    1. Block VS. Inline Elements. Can your refer?  
    2. Deciding Between `<article>`, `<section>`, or`<div>` Elements  
# Lesson3
  *Getting to Know CSS*  
    1. Specificity Points?  
    2. Layering Styles with Multiple Classes?  
    3. Color:rgb(a),hsl(a),key  

# Lesson4
  *Opening the Box Model*  
    1. Display:inline, block, inline-block?  
    2. The Space Between Inline-Block Elements?  
    3. Box Model?  
    4. margin’s top and bottom are not accepted by inline-level elements?  
    5. Margin &amp; Padding on Inline-Level Elements?
    6. Margin &amp; Padding Colors?  
    7. border-radius property?  
    8. Box sizing:   
     1. Content Box  
     2. Padding Box  
     3. Border Box  

# Lesson5
  *Positioning Content*  
    1. Float:why set width, margin?  
    2. Float May Change an Elements’s Display value:the element is removed from flow?  

# Lesson6 
  *Working with Typography*  
  1.Typeface vs. Font?  
> A typeface is what we see. It is the artistic impression of how text looks, feels, and reads.  
>
> A font is a file that __contains a typeface__. Using a font on a computer allows the computer to access the typeface.  

  2.Typeface Weights?
>Before using a numeric value, we need to check and see whether the typeface we are using comes in the weight we’d like to use. Attempting touse a weight that’s not available for a given typeface will cause those styles to default to the closest value.
>
>For example, the Times New Roman typeface comes in two weights: normal, or 400, and bold, or 700. Attempting to use a weight of 900 will default the typeface to the closest related weight, 700 in this case.

  3.Line Height?  
the distance between two line of text.  

# Lesson7
  *Setting Background & Gradients*  
  1.Background repeat?  
>By default, a background image will repeat indefinitely, both vertically and horizontally, unless otherwise specified. The background-repeat property may be used to change the direction in which a background image is repeated, if repeated at all.

  2.Background Position?  
  3.Background shorthand:
                 background-color, background-image, background-position, and background-repeat ?  
  4.Designing Gradient Backgrounds?
>Within CSS, gradient backgrounds are treated as background images. 
>
>The property value for a gradient background varies depending on what type of gradient we’d like, linear or radial.  
>example
>
>     div {
>      background: #466368;
>      background: -webkit-linear-gradient(#648880, #293f50);
>      background:    -moz-linear-gradient(#648880, #293f50);
>      background:         linear-gradient(#648880, #293f50);
>      }

# Lesson9 
  *Adding Media*  
  1.Sizing Images  
>It is important to identify the size of an image in order to tell the browser how large the image should be before the page even loads; thus the browser can reserve space for the image and render the page __faster__.

>CSS over HTML
>Additionally, images may be sized using the width and height properties in CSS. When both the HTML attributes and CSS properties are used, the CSS attributes will take precedence over the HTML attributes.

  2.Adding Audio
>Several other attributes may accompany the src attribute on the <audio> element; the most popular include autoplay, controls, loop, and preload.

  3.Audio Fallbacks & Multiple Sources
> 
>     <audio controls>
>     <source src="jazz.ogg" type="audio/ogg">
>     <source src="jazz.mp3" type="audio/mpeg">
>     <source src="jazz.wav" type="audio/wav">
>     Please <a href="jazz.mp3" download>download</a> the audio file.
>     </audio>

  4.Adding Video | Poster Attribute
>One additional attribute available for the `<video>` element is the poster attribute. The poster attribute allows us to specify an image, inthe form of a URL, to be shown before a video is played. The example below uses a screen capture from the video as the poster for the Earth video.
>
>     <video src="earth.ogv" controls poster="earth-video-screenshot.jpg"></video>

  5.Adding Inline Frames
you can use this mechanism to include google maps inside your page  
>     <iframe src="https://www.google.com/maps/embed?..."></iframe>

  Besides, you need to know what is "Seamless Inline Frames"