Media.match
===========

Testing css media queries in Javascript. Not a polyfill and perhaps faster than native window.matchMedia.

Why?
---
* **Browser support**: Tested in IE 6-9, Chrome, Firefox, Opera and Safari
* **Feature support**: Has all the basics + most of the spec http://www.w3.org/TR/css3-mediaqueries/
* **Speed**: In many browsers, ops/sec rival or exceed native matchMedia. See 'test' to run your own speed tests using JSLitmus
* **Size**: 3kb minified

Media type support
---
* **all**
* **screen**
* **print**
* **speech**
* **projection**
* **handheld**
* **tv**
* **braille**
* **embossed**
* **tty**

Media feature support
---
* **width**:                `width`, `min-width`, `max-width`
* **height**:                `height`, `min-height`, `max-height`
* **device-width**:         `device-width`, `min-device-width`, `max-device-width`
* **device-height**:        `device-height`, `min-device-height`, `max-device-height`
* **aspect-ratio**:         `aspect-ratio`, `min-aspect-ratio`, `max-aspect-ratio`
* **device-aspect-ratio**:  `device-aspect-ratio`, `min-device-aspect-ratio`, `max-device-aspect-ratio`

###Unverified support
* **orientation**:          `orientation`
* **color**:                `color`, `min-color`, `max-color`
* **color-index**:          `color-index`, `min-color-index`, `max-color-index`
* **monochrome**:           `monochrome`, `min-monochrome`, `max-monochrome`
* **resolution**:           `resolution`, `min-resolution`, `max-resolution`

###Lacks support
* **scan**: `scan`
* **grid**: `grid`

Example
---
```
<script type="text/javascript">
    Media
        .match('screen and (min-width: 600px) and (min-height: 400px), screen and (min-height: 400px)')
        .addListener(function(mql) {
            // Your code here..
        });
</script>
```