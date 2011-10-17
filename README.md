Infinite Rounded Tabs JQuery Plugin
===================================

There are quite a few Tab plugins for JQuery, including [JQuery UI's own tab widget](http://jqueryui.com/demos/tabs/), however none of them support the concept of infinite scrolling tabs.  Google Docs has a great implementation of infinite scrolling tabs to manage worksheets, so this plugin is inspired by the Google Docs Spreadsheet tab system, along with the [rounded tabs solution by Chris Coyier](http://css-tricks.com/14001-tabs-with-round-out-borders/).

Features
---
 - Allows you to lock / pin tabs to the left hand side
 - Once there are too many tabs to fit in the container, then a left and right arrow will appear allowing a user to scroll through the tabs
 - All tabs are nicely rounded at the top and at the bottom
 - Full support for Firefox, Chrome, Safari, and Internet Explorer 9+
 - Visually degraded but fully functional support for Internet Explorer 7-8
 - All style sheets are constructed with SASS/SCSS so you can either change the variables in the SCSS and regenerate your own CSS files, or you can simply override or modify the CSS files directly.
 - All CSS & JQuery files are minified and Gzipped down to just over 2k.

Example
-------
[http://mattheworiordan.com/projects/jquery.infinite.tabs.js/example.min.html](http://mattheworiordan.com/projects/jquery.infinite.tabs.js/example.min.html)

Screen shot
-----------
![image](https://github.com/mattheworiordan/jquery.infinite.tabs/raw/master/screen-shot.png)

Usage
-----

Include jquery.infinite.tabs.min.js file after JQuery has been included.  If you want IE7-8 support, please conditionally include selectivizr-min.js which resides in the vendor/js folder.  Please refer to example.html for usage.

Include CSS link to css/infinite.tabs.min.css in your HTML within the head.  Please refer to example.html for usage.  If you want IE7-8 support, please conditionally include CSS link to css/infinite.tabs.lteqi8.min.css.

All tab lists must be ul (unordered lists) with the class "infinite-tabs".  Example to follow:

    // set up the tab system
    $("ul.infinite-tabs#target").infiniteTabs()
      .find('li').click(function(e) {
        e.preventDefault();
        e.stopPropagation();
        $(this).parents('ul.infinite-tabs').find('li').removeClass("active");
        $(this).addClass("active");
		// code goes here to react to tab change
      });

	<ul class="infinite-tabs">
      <li class="active locked"><a href="#pinned">Pinned</a></li>
      <li class="locked"><a href="#pinned-two">Also pinned</a></li>
   	  <li><a href="#one">1</a></li>
      <li><a href="#two">2</a></li>
      <li><a href="#three">3</a></li>
    </ul>


Repository and forking
-----

I welcome feedback and commits to this library.  Please fork me on Github at  [https://github.com/mattheworiordan/jquery.infinite.tabs.js](https://github.com/mattheworiordan/jquery.infinite.tabs.js)

About
-----

This script was written by **Matthew O'Riordan**

 - [http://mattheworiordan.com](http://mattheworiordan.com)
 - [@mattheworiordan](http://twitter.com/#!/mattheworiordan)
 - [Linked In](http://www.linkedin.com/in/lemon)

License
-------

jquery.infinite.tabs.js is Copyright © 2011 Matthew O'Riordan, inc. It is free software, and may be redistributed under the terms specified in the LICENSE file.