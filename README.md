[![devDependency Status](https://david-dm.org/maroslaw/rainyday.js/dev-status.png)](https://david-dm.org/maroslaw/rainyday.js#info=devDependencies)
[![Build Status](https://travis-ci.org/maroslaw/rainyday.js.png)](https://travis-ci.org/maroslaw/rainyday.js)

# rainyday.js

A simple script for simulating raindrops falling on a glass surface.

For demos and more information see the [project page](http://maroslaw.github.io/rainyday.js/).

### How to use:

```js
var engine = new RainyDay({
    element: 'background',  // ID of image element or an element itself
                            // If the element is not an Image the background-image property will be used
                            // If not provided document.body will be used
    parentElement: someDiv, // Element to be used as a parent for the canvas
                            // If not provided assuming the 'body' element
    crop: [ 0, 0, 50, 60],  // Coordinates if only a part of the image should be used
                            // If not provided entire image will be used
    blur: 10,               // Defines blur due to rain effect
                            // Assuming 10 if not provided
                            // Use 0 value to disable the blur
    opacity: 1,             // Opacity of rain drops
                            // Assuming 1 if not provided
    fps: 30                 // Frame rate per second
                            // This value is required
});
engine.rain([ [3, 3, 0.88], [5, 5, 0.9], [6, 2, 1] ], 100);
```
