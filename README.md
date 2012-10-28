# check-types.js

A small JavaScript library for checking types and throwing exceptions.

[![Build status][ci-image]][ci-status]

## Installation

### Node.js

```
npm install check-types
```

### Browser

git clone git@github.com:philbooth/check-types.js.git

## Usage

### Loading the library

#### Node.js

```
var check = require('check-types');
```

#### Browser

```
<script type="text/javascript" src=".../check-types.js/src/check-types.min.js"></script>
```

### Calling the exported functions

A number of different functions are exported:

#### quacksLike (thing, duck)

Tests whether an object 'quacks like a duck'. Returns `true`
if the first argument has all of the properties of the second,
archetypal argument (the 'duck'). Returns `false` otherwise.
If either argument is not an object, an exception is thrown.

#### isInstance (thing, prototype)

Returns `true` if an object is an instance of a prototype,
`false` otherwise.

#### verifyInstance (thing, prototype, message)

Throws an exception if an object is not an instance of a
prototype.

#### isObject (thing)

Returns `true` if something is a non-null, non-array object,
`false` otherwise.

#### verifyObject (thing, message)

Throws an exception unless something is a non-null, non-array
object.

#### isArray (thing)

Returns `true` something is an array, `false` otherwise.

#### verifyArray (thing, message)

Throws an exception unless something is an array.

#### isFunction (thing)

Returns `true` if something is function, `false` otherwise.

#### verifyFunction (thing, message)

Throws an exception unless something is function.

#### isUnemptyString (thing)

Returns `true` if something is a non-empty string, `false`
otherwise.

#### verifyUnemptyString (thing, message)

Throws an exception unless something is a non-empty string.

#### isString (thing)

Returns `true` if something is a string, `false` otherwise.

#### verifyString (thing, message)

Throws an exception unless something is a string.

#### isNumber (thing)

Returns `true` if something is a number, `false` otherwise. In
this instance, `NaN` is not considered a number.

#### verifyNumber (thing, message)

Throws an exception unless something is a number. In this
instance, `NaN` is not considered a number.

## Development

### Dependencies

The build environment relies on [Node.js][node], [NPM], [Jake],
[JSHint], [Mocha] and [Chai].  Assuming that
you already have Node.js and NPM set up, you just need to run
`npm install` to install all of the dependencies as listed in
`package.json`.

### Unit tests

The unit tests are in `test/check-types.coffee`. You can run them
with the command `npm test` or `jake jstest`.

[ci-image]: https://secure.travis-ci.org/philbooth/check-types.coffee.png?branch=master
[ci-status]: http://travis-ci.org/#!/philbooth/check-types.coffee
[onejs]: https://github.com/azer/onejs
[browserify]: https://github.com/substack/node-browserify
[node]: http://nodejs.org/
[npm]: https://npmjs.org/
[jake]: https://github.com/mde/jake
[jshint]: https://github.com/jshint/node-jshint
[mocha]: http://visionmedia.github.com/mocha
[chai]: http://chaijs.com/
[uglifyjs]: https://github.com/mishoo/UglifyJS

