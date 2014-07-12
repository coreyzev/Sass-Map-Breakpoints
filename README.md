Sass-Map-Breakpoints
====================

Simpler media queries using maps in SASS.

Maps are REALLY REALLY cool, and they can save you a lot of time.

Using a map like this, you can build out all our media query mixins:

```` scss
// Breakpoints, from smallest to biggest 
$breakpointMap: (
//size-name //min-breakpoint    //columns //gutter
xSmall:     (280px,             4,        30px),
small:      (480px,             4,        30px),
medium:     (750px,             8,        30px),
large:      (960px,             12,       30px),
xLarge:     (1024px,            12,       30px)
);
````

Name them whatever you want, but make them go from smallest to largest. (I will try to fix that later).

# Usage

````
@include media($size: xSmall, $modifier: up) {
	color: #fff;
}
`````

````
$size - would be the name of the sizes
$modifier:
   up - mobile first
   only - for only that breakpoint
   down - desktop first
````

[Check out the results](https://github.com/coreyzev/Sass-Map-Breakpoints/blob/master/stylesheets/master.css)

# Requirements

Sass `"~>3.3.0"`"

If you plan on using Compass, you must use the most recent version: Compass `"~>1.0.0.alpha.20"`

To install the alpha, use: `sudo gem install compass --pre`