# source-fragment

[![NPM version](https://img.shields.io/npm/v/source-fragment.svg)](https://www.npmjs.com/package/source-fragment)
[![Build Status](https://travis-ci.org/lahmatiy/source-fragment.svg?branch=master)](https://travis-ci.org/lahmatiy/source-fragment)

Fetch source file fragment with highlighting

## Install

```
npm install source-fragment
```

## Example

Suppose we have the code (`example.js`):

```js
function hello() {
    return (
      'world' +
      '!!!'
    );
}
```

To get colored fragment of this code:

```js
var sf = require('source-fragment');

console.log(fs.getColoredSourceFragment('example.js:2:12:5:6', { format: 'tty' }));
```

You'll see in console:

![Example output (tty)](https://user-images.githubusercontent.com/270491/31044865-9150bf3a-a5e0-11e7-8d28-192d5475e0da.png)

The same but in `HTML` format:

```js
fs.getColoredSourceFragment('example.js:2:12:5:6', { format: 'html' });
// <div class="j5as83pdmd85mv2c-source">
// <style>...</style>
// <div class="j5as83pdmd85mv2c-line"><span class="j5as83pdmd85mv2c-num">  2</span>...</div>
// ...
// </div>
```

When pasted on HTML page looks like:

![Example output (html)](https://user-images.githubusercontent.com/270491/31044911-40e99b38-a5e1-11e7-9fb2-22dfd5c7b212.png)

## License

MIT
