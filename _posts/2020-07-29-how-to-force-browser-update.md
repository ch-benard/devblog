# How to force your browser to reload cached CSS/JS files during development phase ?

During developement phase, if you're a heavy user of the try/error method, you can get bored cleaning your cache browser to get the last version of the js script attached to your html page. To force a new version into the browser, you can add a query string to the request, and automatically change the version number each time the page is reloaded. Here is a simple trick you can use to automatically generate a query string parameter:

```javascript
<script>document.write('<script src="/myJavascript.js?dev=' + Math.floor(Math.random() * 100) + '"\><\/script>');</script>
```
[Source](https://stackoverflow.com/questions/118884/how-to-force-the-browser-to-reload-cached-css-js-files)
