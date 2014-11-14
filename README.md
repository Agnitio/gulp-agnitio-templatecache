# gulp-agnitio-templatecache

[![License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](https://npmjs.org/package/gulp-angular-templatecache)
[![NPM version](http://img.shields.io/npm/v/gulp-angular-templatecache.svg?style=flat)](https://npmjs.org/package/gulp-angular-templatecache)
[![NPM version](http://img.shields.io/npm/dm/gulp-angular-templatecache.svg?style=flat)](https://npmjs.org/package/gulp-angular-templatecache)
[![Build Status](http://img.shields.io/travis/miickel/gulp-angular-templatecache.svg?style=flat)](http://travis-ci.org/miickel/gulp-angular-templatecache)
[![Dependency Status](http://img.shields.io/gemnasium/miickel/gulp-angular-templatecache.svg?style=flat)](https://gemnasium.com/miickel/gulp-angular-templatecache)

> Concatenates and registers HTML templates in the `app.cache`.

<a href="#install">Install</a> |
<a href="#example">Example</a> |
<a href="#api">API</a> |
[Releases](https://github.com/miickel/gulp-agnitio-templatecache/releases) |
<a href="#license">License</a>

----


## Install

Install with [npm](https://npmjs.org/package/gulp-angular-templatecache)

```
npm install gulp-angular-templatecache --save-dev
```


## Example

**gulpfile.js**

> Concatinate the contents of all .html-files in the templates directory and save to _public/templates.js_ (default filename).

```js
var templateCache = require('gulp-agnitio-templatecache');

gulp.task('default', function () {
	gulp.src('slides/**/*.html')
		.pipe(templateCache())
		.pipe(gulp.dest('templates'));
});
```

**Result (_templates/templates.js_)**

Include this file in your app and Agnitio Accelerator will use the app.cache to load HTML when available.

## API

gulp-agnitio-templatecache([filename](https://github.com/miickel/gulp-angular-templatecache#filename---string-filenametemplatesjs), [options](https://github.com/miickel/gulp-angular-templatecache#options))

---- 

### filename - {string} [filename='templates.js']

> Name to use when concatinating.

### options

#### root - {string} [root='']

> Prefix for template URLs.

#### base {string | function} [base=file.base]

> Override file base path.

#### moduleSystem {string} [moduleSystem]

> Wrap the templateCache in a module system. Currently supported systems: `RequireJS`, `Browserify`.


## Changes

> This plugin uses Semantic Versioning 2.0.0

### 1.0.0

- Forked from [gulp-angular-templatecache](https://github.com/miickel/gulp-angular-templatecache)
- Updated output from Angular to app.cache


## License

The MIT License (MIT)

Copyright (c) 2014 [Mickel](http://mickel.me)

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[![Analytics](https://ga-beacon.appspot.com/UA-46880034-1/gulp-angular-templatecache/readme?pixel)](https://github.com/igrigorik/ga-beacon)
