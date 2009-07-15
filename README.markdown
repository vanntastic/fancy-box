Fancy Box Jquery Plugin
=======================

FancyBox is a tool for displaying images, html content and multi-media in a Mac-style "lightbox" that floats overtop of web page. Note that this is simply a mirror of the plugin, the origin and page of the author is located at : http://fancy.klade.lv/


How to implement
================

First, make sure you are using valid DOCTYPE, this is required for FancyBox to look and function correctly.
  
1. Include nessesary JS files 
      
      <script type="text/javascript" src="path-to-file/jquery.js"></script>
      <script type="text/javascript" src="path-to-file/jquery.fancybox.js"></script>

Optional, add if you wish to use fancy transitions as jQuery by default supports only "swing" and "linear"

      <script type="text/javascript" src="path-to-file/jquery.easing.js"></script>
      
2. Add FancyBox CSS file 

Don`t forget to change image paths if CSS file is not in the same directory as images used by FancyBox

      <link rel="stylesheet" href="path-to-file/fancybox.css" type="text/css" media="screen">
      
3. Create a link element (<a href>) 

For images:
    
      <a id="single_image" href="image_big.jpg"><img src="image_small.jpg" alt=""/></a>
      
Inline content:

      <a id="inline" href="#data">This shows content of element who has id="data"</a>
      
Iframe:
      
      <a href="http://www.example?iframe">This goes to iframe</a>
      
or

      <a class="iframe" href="http://www.example">This goes to iframe</a>
Ajax

      <a href="http://www.example/data.php">This takes content using ajax</a>

Optional: Use the title attribute if you want to show a caption 
Note: You may want to set hideOnContentClick to false if you display iframed or inline content and it containts clickable elements (for example - play buttons for movies, links to other pages) 

4. Fire plugin using jQuery selector 

If you are not familiar with jQuery, please, read at least this tutorial for beginners 

Sample examples:

      $(document).ready(function() {

      	/* This is basic - uses default settings */
	
      	$("a#single_image").fancybox();
	
      	/* Using custom settings */
	
      	$("a#inline").fancybox({
      		'hideOnContentClick': true
      	});

      	$("a.group").fancybox({
      		'zoomSpeedIn':		300, 
      		'zoomSpeedOut':	300, 
      		'overlayShow':		false
      	});
      });

Galleries are created from found anchors who have the same "rel" tags

Available options
=================

You can pass them as shown above or modify them at the bottom of FancyBox JS file
padding	Padding around content

- imageScale : If true, images are scaled to fit in viewport
- zoomOpacity :	If true, changes content transparency when animating
- zoomSpeedIn :	Speed in miliseconds of the zooming-in animation 
(no animation if 0)
- zoomSpeedOut : Speed in miliseconds of the zooming-out animation 
(no animation if 0)
- zoomSpeedChange :	Speed in miliseconds of the animation when changing gallery items
(no animation if 0)
- easingIn, easingOut, easingChange	: Easing used for animations
- frameWidth : Default width for iframed and inline content
- frameHeight	: Default height for iframed and inline content
- overlayShow	: If true, shows the overlay (false by default) Overlay color is defined in CSS file
- overlayOpacity : Opacity of overlay (from 0 to 1)
- hideOnContentClick : Hides FancyBox when cliked on opened item
- centerOnScroll : If true, content is centered when user scrolls page
- itemArray	: Optional, can set custom item array
- callbackOnStart :	Optional, called on start
- callbackOnShow : Optional, called on displaying content
- callbackOnClose : Optional, called on close


Find this documentation at : http://fancy.klade.lv/howto