# Single Page Nav

Apply the 'singlePageNav' function to a container element.
Clicking on any links within the container will cause an animated scroll down to
the element whose ID is identified by that link's "hash" (if it exists). The 
currently highlighted link in the nav bar will also cycle as the user scrolls 
down the page (useful with a fixed-position nav bar. Intended for use on single 
page websites, such as a portfolio.

Bug reports and pull requests more than welcome. This was my first plugin release.

Live demo:
http://chriswojcik.net/demos/single-page-nav/

## Features

* The coordinates of each target element are determined dynamically, resizing the 
browser or appending content to a section will not break the plugin.
* Configurable options.

## Sample Use
```js
$('#navigation-bar').singlePageNav();
```

## Options

* 'offset' - An offset in pixels above the target element when scrolling (useful 
for accounting for the height of a "sticky navigation bar", see the demo)
* 'threshold' - The distance above each section in pixels when the "current" link
in the nav bar will change.
* 'speed' - The animated scroll speed in milliseconds.
* 'easing' - The easing function to use with the animation (Default is 'swing').
* 'currentClass' - The class to apply to the link in the nav bar corresponding to
the active section on the page.
* 'updateHash' - In browsers that support the history object, update the url's hash when clicking on the links (Default is false)
* 'filter' - By default, the plugin will be applied to all links within the container,
use this to filter out certain links using jquery's built in filter method (e.g. ':not(.external)')
* 'beforeStart' - This function will fire when a user clicks on a link but before the scrolling
animation starts
* 'onComplete' - This function will fire when the scrolling animation completes

## Limitations

* The order of the links in the navigation bar MUST match the order of the sections 
as laid out on the page or unexpected behavior will occur.

## TODO (future updates)

* Add support for horizontal scrolling sites.

## References

The functionality of this plugin is admittedly similar to some others. But it was
my first plugin, so be kind. Here are a few links to such plugins if you find them 
more helpful.

* [onePageNav plugin] (https://github.com/davist11/jQuery-One-Page-Nav)
* [scrollTo plugin] (https://github.com/flesler/jquery.scrollTo)
* [jQuery Waypoints] (https://github.com/imakewebthings/jquery-waypoints)
