# How to optimize a website

DO NOT use premature optimization, but how we can optimize the website:

* Decrease network lag,
    * Minimize and concat source files
    * Minimize images by utilizing
        * Photoshop
        * [jpeg optimizer](http://jpeg-optimizer.com/)
        * [tinypng.com](https://tinypng.com/),
        * for `jpeg` set 30-60% qualify
        * Read about [image formats](https://www.sitepoint.com/gif-png-jpg-which-one-to-use/)
    * For different screen sizes provide background-image of different sizes, by using media queries
        * Use [srcset](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images) to define different `<img>` tag src attribute values
    * Use resource CDN
        * [imgix &#10084;](https://www.imgix.com/)
        * [filestack](https://www.filestack.com/)
    * Remove metadata (Exif) from image files with [verexif.com](http://www.verexif.com/)
* Optimize backend work,
* Optimize frontend work
    * Analyze the critical render path (DOM -> CSSOM (DOMContentLoaded) -> RenderTree -> Layout -> Paint (Load))
    * Get CSS to the browser as soon as possible
    * Get JS to the browser as late as possible (JS parsing and execution slows down the load process)
    * Postpone loading anything that is below the page fold (like, i.e. images)
    * Use tools to analyze the website
        * [webpagetest.org](https://www.webpagetest.org/)
        * [page speed insights](https://developers.google.com/speed/pagespeed/insights/)
        * Use [pageweight](https://pageweight.imgix.com/) to analyze your image assets impact
    * Script
        * async - add this attribute to all scripts which don't affect DOM or CSS (analytic or tracking scripts)
        * defer - not important, third-party scripts should go with this attribute
    * Try to get rid of jQuery: [youmightnotneedjquery.com](http://youmightnotneedjquery.com/)
    * Try to use [resource prefetching](https://css-tricks.com/prefetching-preloading-prebrowsing/)
    * [Max parallel connects per a browser](https://stackoverflow.com/questions/985431/max-parallel-http-connections-in-a-browser)
    * Use [HTTP/2](https://developers.google.com/web/fundamentals/performance/http2/)
        `const http2 = require('http2);`
