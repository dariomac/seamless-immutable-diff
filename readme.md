# seamless-immutable-diff [![Build Status](https://travis-ci.org/micnews/seamless-immutable-diff.png?branch=master)](https://travis-ci.org/micnews/seamless-immutable-diff)

Given two objects, get the seamless-immutable-diff between them

## Installation

Download node at [nodejs.org](http://nodejs.org) and install it, if you haven't already.

```sh
npm install seamless-immutable-diff --save
```

## Usage

```js
import diff from 'seamless-immutable-diff';
import Immutable from 'seamless-immutable';

const from = Immutable({ beep: { boop: true }, foo: { bar: false } });
const to = { beep: { hello: 'world' }, foo: { bar: false } };
const result = diff(from, to);

// will be true since from.foo is deep equal to to.foo
console.log(from.foo === result.foo);
// will be a seamless-immutable object { hello: 'world' }
console.log(result.beep);

```

## Tests

```sh
npm install
npm test
```

## Dependencies

- [dift](https://github.com/ashaffer/dift): Super fast list diff algorithm
- [immutable-array-methods](https://github.com/micnews/immutable-array-methods): Immutable versions of normally mutable array methods, such as pop(), push(), splice()

## Dev Dependencies

- [ava](https://github.com/sindresorhus/ava): Futuristic test runner 🚀
- [babel-cli](https://github.com/babel/babel/tree/master/packages): Babel command line.
- [babel-core](https://github.com/babel/babel/tree/master/packages): Babel compiler core.
- [babel-preset-es2015](https://github.com/babel/babel/tree/master/packages): Babel preset for all es2015 plugins.
- [nyc](https://github.com/bcoe/nyc): a code coverage tool that works well with subprocesses.
- [package-json-to-readme](https://github.com/zeke/package-json-to-readme): Generate a README.md from package.json contents
- [seamless-immutable](https://github.com/rtfeldman/seamless-immutable): Immutable data structures for JavaScript which are backwards-compatible with normal JS Arrays and Objects.
- [semistandard](https://github.com/Flet/semistandard): All the goodness of `feross/standard` with semicolons sprinkled on top.
- [snazzy](https://github.com/feross/snazzy): Format JavaScript Standard Style as Stylish (i.e. snazzy) output


## License

MIT

_Generated by [package-json-to-readme](https://github.com/zeke/package-json-to-readme)_
