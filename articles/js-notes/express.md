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
