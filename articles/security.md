# Security

* Vectors to concern
    * Authentication
    * Injection
        * `' or 1=1--`
        * `'; drop table users; --`
    * 3rd party libraries
    * Logging
    * HTTPS
    * XSS & CSRF
    * Code secrets
    * Secure headers
    * Access control
    * Data management
    * Don't trust anyone
* Use [jwt](https://www.npmjs.com/package/jwt-express) for `API`, but dont forget about [CSRF](https://en.wikipedia.org/wiki/Cross-site_request_forgery#Prevention)
