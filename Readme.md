### Precinct [![npm](http://img.shields.io/npm/v/module-definition.svg)](https://npmjs.org/package/precinct) [![npm](http://img.shields.io/npm/dm/precinct.svg)](https://npmjs.org/package/precinct)

> Unleash the detectives

`npm install precinct`

Uses the appropriate detective to find the dependencies of a file.

Supports: AMD, CommonJS, and ES6 modules.

Also supports SASS dependencies via [detective-sass](https://github.com/mrjoelkemp/node-detective-sass).

### Usage

```js
var precinct = require('precinct');

var content = fs.readFileSync('myFile.js', 'utf8');

var deps = precinct(content);
```

Finding SASS dependencies:

```js
var content = fs.readFileSync('styles.scss', 'utf8');

var deps = precinct(content, 'sass');

```

If you just want to pass in a filepath and get the dependencies:

```js
var paperwork = require('precinct').paperwork;

var deps = paperwork('myFile.js');
```

#### Options

###### `precinct.paperwork(filename, options)`

* `includeCore`: (default: true) set to `false` to exclude core Node dependencies from the list of dependencies.

### License

MIT
