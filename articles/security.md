# Security

* Vectors to concern
    * Authentication
    * Injection
        * `' or 1=1--`
        * `'; drop table users; --`
        * attack with (in example) `el.html(somevar)` and `<script>alert('hack')</script>`
        * attack with `el.innerHTML = somevar` and `<img src="/" onerror="alert('hak')" />`
            * use `el.innerText = somevar` or `document.createTextNode(somevar)`
        * how to cope with that
            * sanitize / escape input
            * use prepared statement for both `sql` and `dom`
            * use a template engine with built-in `escaping` turned on by default
            * use ORM
            * don't use `el.innerHTML` unless the content is sanitized / escaped
            * don't use `eval()`
            * don't use `document.write()`
    * 3rd party libraries
    * Logging   
        * [winston](https://www.npmjs.com/package/winston)
        * [morgan](https://www.npmjs.com/package/morgan)
    * HTTPS
    * XSS - cross site scripting (typically combined with session hijacking)
    * [CSRF](https://en.wikipedia.org/wiki/Cross-site_request_forgery#Prevention) - cross site request forgery
    * Use [Content security policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP)
    * Code secrets
    * Secure headers
    * Access control
    * Data management
    * Don't trust anyone
    * Cookies<br />
        If we send some sensitive info by using cookies, we set [the following flags](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies) on it:
            * `httpOnly` - the cookie could not be read with javascript code
            * `secure` - the cookie will be send only over `https` requests
* Use [jwt](https://www.npmjs.com/package/jwt-express) for `API`, but don't forget about [CSRF](https://en.wikipedia.org/wiki/Cross-site_request_forgery#Prevention)
