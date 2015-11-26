# jstransformer-templayed

[templayed.js](https://github.com/heldr/node-templayed) support for [JSTransformers](http://github.com/jstransformers).

[![Build Status](https://img.shields.io/travis/jstransformers/jstransformer-templayed/master.svg)](https://travis-ci.org/jstransformers/jstransformer-templayed)
[![Coverage Status](https://img.shields.io/coveralls/jstransformers/jstransformer-templayed/master.svg)](https://coveralls.io/r/jstransformers/jstransformer-templayed?branch=master)
[![Dependency Status](https://img.shields.io/david/jstransformers/jstransformer-templayed/master.svg)](http://david-dm.org/jstransformers/jstransformer-templayed)
[![NPM version](https://img.shields.io/npm/v/jstransformer-templayed.svg)](https://www.npmjs.org/package/jstransformer-templayed)

## Installation

    npm install jstransformer-templayed

## API

```js
var hamlc = require('jstransformer')(require('jstransformer-templayed'))
var template = '<ul>{{#names}}<li>{{../fullName}}</li>{{/names}}</ul>';
var data = {
  names: [{firstName: "Paul", lastName: "Engel"}, {firstName: "Chunk", lastName: "Norris"}],
  fullName: function() {
    return this.lastName + ", " + this.firstName;
  }
};
templayed.render(template, data).body
//=> '<ul><li>Engel, Paul</li><li>Norris, Chunk</li></ul>'
```

## License

MIT
