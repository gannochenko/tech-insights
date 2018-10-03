# Progressive web applications

* Check how good your app is with [Google Lighthouse](https://developers.google.com/web/tools/lighthouse/)
* [One story](http://debuggerdotbreak.judahgabriel.com/2018/04/13/i-built-a-pwa-and-published-it-in-3-app-stores-heres-what-i-learned/)
* Add [meta viewport](https://developers.google.com/web/tools/lighthouse/audits/has-viewport-meta-tag): `<meta name="viewport" content="width=device-width, initial-scale=1 shrink-to-fit=no">`
* Add [favicon](https://realfavicongenerator.net/) and other icons
* Add manifest
* Add https
    * [Letsencrypt](https://letsencrypt.org/)
* Add service worker
    Basically this feature is a proxy which allows to detect whether we are offline or not, and if we do, serve static assets from [CacheStorage](https://developer.mozilla.org/ru/docs/Web/API/CacheStorage)
* Think of [accessibility](https://www.w3.org/standards/webdesign/accessibility)
