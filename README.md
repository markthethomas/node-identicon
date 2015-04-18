# node-identicon

[![Npm version][npm-image]][npm-url]
[![Build Status][travis-image]][travis-url]
[![Dependency Status][gemnasium-image]][gemnasium-url]
  
[Identicon](https://github.com/donpark/identicon) generator for Node.js

## Installation

```bash
$ npm install identicon
```

## Example

```javascript
var identicon = require('identicon');
var fs = require('fs');

// Asynchronous API
identicon.generate({ id: 'ajido', size: 150 }, function(err, buffer) {
    if (err) throw err;

    // buffer is identicon in PNG format.
    fs.writeFileSync(__dirname + '/identicon.png', buffer);
});

// Synchronous API
var buffer = identicon.generateSync({ id: 'ajido', size: 40 });
```

<img src="https://cloud.githubusercontent.com/assets/206827/7214948/529f8966-e5fc-11e4-8aa0-c84ada23acc2.png" width="150" height="150">

## License

(The MIT License)

Copyright (c) 2010-2012 Daiki Kuriyama &lt;dkuriyam@gmail.com&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[travis-image]: https://img.shields.io/travis/Ajido/node-identicon.svg?style=flat-square
[travis-url]: https://travis-ci.org/Ajido/node-identicon
[npm-image]: https://img.shields.io/npm/v/identicon.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/identicon
[gemnasium-image]: http://img.shields.io/gemnasium/Ajido/node-identicon.svg?style=flat-square
[gemnasium-url]: https://gemnasium.com/Ajido/node-identicon
