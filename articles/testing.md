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

* [json-server](https://github.com/typicode/json-server)
* [swapi](https://swapi.co)

## React testing

* [enzyme](https://github.com/airbnb/enzyme)
    * `shallow` renders a component without it's children
    * `mount` does component mounting with a lifecycle, it is required to have `jsdom` in order to work
    * `render` renders a component into a string
* Do snapshot testing

## Commands
   `npm test -- --coverage`

## Useful links

* [Jest cheat sheet](https://github.com/sapegin/jest-cheat-sheet)