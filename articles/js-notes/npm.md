# NPM

* How to view dependences<br />
    `npm list <dependency>`<br />
    [See more here](https://stackoverflow.com/questions/25997519/how-to-view-the-dependency-tree-of-a-given-npm-module)

* How to update all the top level packages
    `npm update --save-dev`

* How to read `semver`<br />
    Version consists of the following parts: `MAJOR`.`MINOR`.`PATCH`
    * `MAJOR` - version for when there are incompatible API changes
    * `MINOR` - version for when functionality is added in a backwards compatible manner
    * `PATCH` - version for when backwards compatible bug fixes are done

    Examples of constraints:
    * To Allow Patch Releases: 1.0 or 1.0.x or ~1.0.4
    * To Allow Minor Releases: 1 or 1.x or ^1.0.4
    * To Allow Major Releases: * or x

    [See more](https://www.hostingadvice.com/how-to/update-npm-packages/)

## Libraries

* React
    * [immutable js](http://facebook.github.io/immutable-js/)
* Redux
    * [redux-thunk](https://www.npmjs.com/package/redux-thunk)
    * [redux-promise](https://www.npmjs.com/package/redux-promise)
    * [redux-logger](https://www.npmjs.com/package/redux-logger)
    * [redux-saga](https://github.com/redux-saga/redux-saga)
    * [redux reselect](https://github.com/reduxjs/reselect)
* Helpers
    * [Ramda](https://ramdajs.com)
    * [Lodash](https://www.npmjs.com/search?q=lodash)
        * You can import `lodash` methods as separated `npm` modules
    * Underscore
    * [Latinize](https://www.npmjs.com/package/latinize) - turn any text into a latin equivalent
* Styling
    * [Glamorous](https://glamorous.rocks)
    * [MaterialUI](https://material-ui.com/)
    * [SemanticUI](http://react.semantic-ui.com/)
    * [Reactstrap](https://reactstrap.github.io) - the react binding for bootstrap
    * [Foundation](https://foundation.zurb.com/)
    * [Bootstrap](https://getbootstrap.com/)
    * [Bootflat](http://bootflat.github.io/) - a flat version of Bootstrap 3, seems to be not maintained any longer
    * [Spinkit](http://tobiasahlin.com/spinkit/) - a kit of spinners for react
    * [CSS-loaders](https://github.com/lukehaas/css-loaders) - another kit of spinners
* Development
    * [Why-did-you-update](https://www.npmjs.com/package/why-did-you-update)
* Deployment
    * [gh-pages](https://www.npmjs.com/package/gh-pages)
* Testing
    * [jest](https://www.npmjs.com/package/jest)
    * [enzyme](https://github.com/airbnb/enzyme)
* Mockers
    * API
        * [json-server](https://github.com/typicode/json-server)
* Server emulators
    * [nodemon](https://www.npmjs.com/package/nodemon)
    * [webpack dev server](https://www.npmjs.com/package/webpack-dev-server)
* Data visualization
    * [bizcharts](https://www.npmjs.com/package/bizcharts)
* REST callers
    * [isomorphic unfetch](https://www.npmjs.com/package/isomorphic-unfetch)
    * [axios](https://www.npmjs.com/package/axios)
    * [superagent](https://www.npmjs.com/package/superagent)
* ORM / ODM
    * [knex](https://knexjs.org/)
    * [mongoose](https://mongoosejs.com/)
* Security
    * [csurf]()
    * [cask]()
    * [helmet](https://www.npmjs.com/package/helmet)
    * [cors](https://www.npmjs.com/package/cors)
* Security audit
    * [snyk](https://www.npmjs.com/package/snyk)
* Logging
    * [winston](https://www.npmjs.com/package/winston)
    * [morgan](https://www.npmjs.com/package/morgan)
* Environment
    * [dotenv](https://www.npmjs.com/package/dotenv)
* Hashing
    * [bcrypt](https://www.npmjs.com/package/bcrypt)
    * [bcrypt-nodejs](https://www.npmjs.com/package/bcrypt-nodejs)
    * [scrypt](https://www.npmjs.com/package/scrypt)
* Anti-DDOS
    * [ratelimiter](https://www.npmjs.com/package/ratelimiter)
* Maps and geodata
    * [Cesium.js](https://cesiumjs.org)
* Express middleware
    * [GZIP](https://www.npmjs.com/package/compression)
* UI
    * [Swipe detection](https://www.npmjs.com/package/react-swipeable)
* Website stress test
    * [loadtest](https://www.npmjs.com/package/loadtest)
