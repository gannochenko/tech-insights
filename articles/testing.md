# Testing

* Unit tests
    * Test one piece of code, whatever this is
* Integration tests
    * Tests how two parts of code work together
* Automation tests
    * The UI tests, testing scenarios
 
## Parts
   
* Test runners
    * Mocha
    * [Jest](https://jestjs.io/)
    * Jasmine
    * Karma
* Assertion library
    * Chai
    * Jest
    * Jasmine
* Mocks and spies
    * Jest
    * Jasmine
    * [Sinon.js](https://sinonjs.org/)
* Code coverage reporters
    * Jest
    * Istanbul

## Browser emulators

* Puppeter
* jsdom

## Mocking API

* Local
    * [json-server](https://github.com/typicode/json-server)
* SAAS
    * [swapi](https://swapi.co)
    * [dogapi](https://dog.ceo/dog-api/)
    * [json placeholder](https://jsonplaceholder.typicode.com/)
* A list of free APIs
    * [GraphQL](https://github.com/APIs-guru/graphql-apis)

## React testing

* [enzyme](https://github.com/airbnb/enzyme)
    * `shallow` renders a component without it's children
    * `mount` does component mounting with a lifecycle, it is required to have `jsdom` in order to work
    * `render` renders a component into a string
* [redux-mock-store](https://www.npmjs.com/package/redux-mock-store)
* Do snapshot testing

## API testing
   
* Mocking API with [nock](https://www.npmjs.com/package/nock)
* Testing API with [supertest](https://www.npmjs.com/package/supertest)

## Commands
   `npm test -- --coverage`

## Useful links

* [Jest cheat sheet](https://github.com/sapegin/jest-cheat-sheet)
