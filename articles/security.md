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
            * sanitize input
            * escape input
            * use prepared statement for both `sql` and `dom`
            * use a template engine with built-in `escaping` turned on by default
            * use ORM
            * don't use `el.innerHTML` unless the content is sanitized / escaped
    * 3rd party libraries
    * Logging
    * HTTPS
    * XSS & CSRF
    * Code secrets
    * Secure headers
    * Access control
    * Data management
    * Don't trust anyone
* Use [jwt](https://www.npmjs.com/package/jwt-express) for `API`, but don't forget about [CSRF](https://en.wikipedia.org/wiki/Cross-site_request_forgery#Prevention)
