### gulp-dos2unix
> :tropical_drink: Gulp plug-in to convert DOS (\r\n) to Unix (\n) line endings using pure JS module.

[![Build Status](https://travis-ci.org/stpettersens/gulp-dos2unix-js.png?branch=master)](https://travis-ci.org/stpettersens/gulp-dos2unix-js)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](https://github.com/feross/standard)
[![npm version](https://badge.fury.io/js/gulp-dos2unix-js.svg)](http://npmjs.com/package/gulp-dos2unix-js)
[![Dependency Status](https://david-dm.org/stpettersens/gulp-dos2unix-js.png?theme=shields.io)](https://david-dm.org/stpettersens/gulp-dos2unix-js) [![Development Dependency Status](https://david-dm.org/stpettersens/gulp-dos2unix-js/dev-status.png?theme=shields.io)](https://david-dm.org/stpettersens/gulp-dos2unix-js#info=devDependencies)

##### Install:

    $ npm install --save-dev gulp-dos2unix-js

##### Usage:
```js
'use strict'
const gulp = require('gulp')
const dos2unix = require('gulp-dos2unix-js')

gulp.task('default', function () {
  return gulp.src(['README.md', 'LICENSE'])
  .pipe(dos2unix()) // This defaults to {feedback: false, write: false}
  .pipe(gulp.dest('out'))
})
```

##### Options:

Omittable options object with following allowable parameters
(same as [ssp-dos2unix-js](http://github.com/stpettersens/ssp-dos2unix-js)):

* `feedback` (Boolean) - Display feedback (*"File already has UNIX line endings..."*).
* `writable` (Boolean) - Write change to file rather than pipe through to copy.

All options are false if omitted.
