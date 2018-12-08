# Express

Express on its own can parse parameters from routes:
```js
app.get('/api/courses/:year/:month', (req, res) => {
    res.send({
        query: req.query,
        params: req.params,
    });
});
```

You can use `req.body` in `post` query only when you attach json bodyparser middleware:
~~~
app.use(express.json());
~~~

## Security
* [express helmet](https://helmetjs.github.io/)

Middleware function always has 3 parameters: req, res, next. Parameter `next` is a reference to the next middleware in the line, without calling it the request will stale.
~~~
module.exports = (req, res, next) => {
    console.dir('hey this is middleware speaking');
    next();
};
~~~

Generic middlewares:
* `express.json()` - if content type is `application/json` and the body looks like `JSON`, the middleware will parse it and put the result to `req.body`
* `express.urlencoded({ extended: true })` - if the verb is `post` and the content type is `x-www-form-urlencoded` (which typically happens when you submit a `<form>`), it converts the body from `field1=value1&field2=value2` into `JSON` and put it to `req.body`. When `extended` is set to true, we can additionally send fields as arrays in the PHP-format, like `field1[]=one&field1[]=two`
* `express.static('public')` - allows to serve static assets from the specified folder

[Browse all popular middleware](https://expressjs.com/en/resources/middleware.html)

How to get envs:
* `process.env.NODE_ENV`
* `app.env()`

We can use `express.Router()` in order to attach middlewares, instead of putting them just to `app`

Promises:
    * `Promise.all()` to wait for all
    * `Promise.race()` to wait for the first one

## Mongo

* Update
    * `save`
    * `update`
    * `updateMany`
    * Two ways of updating
        * `.update()` by filter
        * get, check data consistency and then `.save()`
* Delete
    * `findByIdAndRemove`
    * `deleteMany`
