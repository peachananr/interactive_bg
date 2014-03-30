#Interactive BG (Background) by Pete R.
A jQuery plugin that will let you create an interactive moving background/object that reacts to viewer's cursor
Created by [Pete R.](http://www.thepetedesign.com), Founder of [Travelistly](http://www.travelistly.com) and [BucketListly](http://www.bucketlistly.com)

License: [Attribution-ShareAlike 4.0 International](http://creativecommons.org/licenses/by-sa/4.0/deed.en_US)

[![Interactive BG (Background)](http://www.thepetedesign.com/images/interactive_bg_image.png "Interactive BG (Background")](http://www.thepetedesign.com/demos/interactive_bg_demo.html)


## Demo
[View demo](http://www.thepetedesign.com/demos/interactive_bg_demo.html)

## Compatibility
Modern browsers such as Chrome, Firefox, and Safari on both desktop and smartphones have been tested. Not tested on IE.

## Basic Usage

To add a cool parallax like effect to your background, you will have to include the latest jQuery library (preferably version 2.0.0 or higher) together with `jquery.interactive_bg.js` into your document's `<head>`. Make sure you have a background image ready to be used. 
  
Prepare your HTML as follows:

````html
<body>
  ..
  <div class="bg" data-ibg-bg="bg.jpg"></div>
  ..
</body>

````

The `data-ibg-bg` attribute must reflect the location of the image you want to use as your background. For example, if your image is on the root folder and is called "background.png", change the attribute to "/background.png".

Now call the function as follows and your background will magically reacts to viewers cursor.

````javascript
 $(".bg").interactive_bg({
   strength: 25,              // Movement Strength when the cursor is moved. The higher, the faster it will reacts to your cursor. The default value is 25.
   scale: 1.05,               // The scale in which the background will be zoomed when hovering. Change this to 1 to stop scaling. The default value is 1.05.
   animationSpeed: "100ms",   // The time it takes for the scale to animate. This accepts CSS3 time function such as "100ms", "2.5s", etc. The default value is "100ms".
   contain: true,             // This option will prevent the scaled object/background from spilling out of its container. Keep this true for interactive background. Set it to false if you want to make an interactive object instead of a background. The default value is true.
   wrapContent: false         // This option let you choose whether you want everything inside to reacts to your cursor, or just the background. Toggle it to true to have every elements inside reacts the same way. The default value is false
 });
````

## Advanced Features
The problem with using options above is all your planets will look the same. To specify each of your planet's style, you can utilize the HTML markup I've provided:

### Responsive Background
To make the background responsive to the windows width and height, make sure you add this snippet below the function call as follows:

````javascript

  $(document).ready(function(){
    
    $(".bg").interactive_bg(); // function call
	});
  
  // change background size on window resize
  $(window).resize(function() {
	  $(".bg > .ibg-bg").css({
	    width: $(window).outerWidth(),
	    height: $(window).outerHeight()
	  })
	})
````

### Accelerometer on Mobile
Since mouse event is not available on mobile, the plugin will automatically switch to react to the mobile's accelerometer instead without you having to do anything. Just call the function normally, and the plugin will  detects and switch to the fallback automatically.

Now your background will have this interactive parallax effect like no other sites have for a minimal effort.

If you want to see more of my plugins, visit [The Pete Design](http://www.thepetedesign.com/#design), or follow me on [Twitter](http://www.twitter.com/peachananr) and [Github](http://www.github.com/peachananr).

## Other Resources
- Tutorial (Coming Soon)