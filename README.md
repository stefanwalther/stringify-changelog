# stringify-changelog [![NPM version](https://img.shields.io/npm/v/stringify-changelog.svg?style=flat)](https://www.npmjs.com/package/stringify-changelog) [![NPM downloads](https://img.shields.io/npm/dm/stringify-changelog.svg?style=flat)](https://npmjs.org/package/stringify-changelog) [![Build Status](https://img.shields.io/travis/jonschlinkert/stringify-changelog.svg?style=flat)](https://travis-ci.org/jonschlinkert/stringify-changelog)

Generate a markdown-formatted changelog from an object, array or yaml file.

Converts valid YAML, like this:

```yaml
v0.1.0:
  date: "2016-12-26"
  changes:
    - Got stuck in another chimney.
```

Into this:

```markdown
**DATE**       **VERSION**   **CHANGES**                  
* 2016-12-26   v0.1.0        Got stuck in another chimney.
```

## Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install --save stringify-changelog
```

## Usage

```js
var changelog = require('stringify-changelog');
changelog(value, options);
```

**Params**

* `value` **{String|Object|Array}**: File path of YAML file to read, object or array of changes (see below)
* `options` **{Object}**: the following options may be passed to modify output
  - `dateFn` **{Function}** modify the date format
  - `headingFn` **{Function}** modify the headings

See [columnify](https://github.com/timoxley/columnify) for additional options.

## Data format

Data can either be formatted as an array or an object.

**Array**

```js
[ { date: '2016-12-26',
    version: 'v0.1.0',
    changes: [ 'Got stuck in another chimney.' ] } ]
```

**Object**

```js
{ 'v0.1.0':
   { date: '2016-12-26',
     changes: [ 'Got stuck in another chimney.' ] } }
```

## About

### Related projects

[helper-changelog](https://www.npmjs.com/package/helper-changelog): Template helper for generating a markdown-formatted changelog from an object, array or yaml file. | [homepage](https://github.com/jonschlinkert/helper-changelog "Template helper for generating a markdown-formatted changelog from an object, array or yaml file.")

### Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](../../issues/new).

### Running tests

Install dev dependencies:

```sh
$ npm install -d && npm test
```

### Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

### License

Copyright © 2016, [Jon Schlinkert](https://github.com/jonschlinkert).
Released under the [MIT license](https://github.com/jonschlinkert/stringify-changelog/blob/master/LICENSE).

***

_This file was generated by [verb](https://github.com/verbose/verb), v0.9.0, on July 21, 2016._