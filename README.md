# <span style="color:#ff8333">Logstack</span> [![NPM Version](https://badge.fury.io/js/logstack.svg)](https://www.npmjs.com/package/logstack) [![Total Download](https://img.shields.io/npm/dt/logstack.svg)](https://www.npmjs.com/package/logstack) ![CI status](https://img.shields.io/badge/build-passing-brightgreen.svg)

<!-- [![npm](https://nodei.co/npm/logstack.png)](https://www.npmjs.com/package/logstack) -->

Logstack is simple logger alternative to console.log() which is written in specified file instead of terminal window.

## Installation

This is a [Node.js](https://nodejs.org/en/) module available through the
[npm registry](https://www.npmjs.com/).<br />
Installation is done using the
[`npm install` command](https://docs.npmjs.com/getting-started/installing-npm-packages-locally):

```bash
$ npm install logstack
```

## Example & Usage
### To Log the message
```js
const logstack = require('logstack');
const path = require('path');

// Please make sure the directory is available and use it only for logstack
const directory = path.join(__dirname, './directory');
const logFileCount = 3;
let log = function (logMessage) {
    // To create log
    logstack.createLog(directory, logFileCount, logMessage);
}
// Just call the function with specified log message
log("Hello from logstack");
```

### To disable logstack
```js
const logstack = require('logstack');
const path = require('path');

// Please make sure the directory is available and use it only for logstack
const directory = path.join(__dirname, './directory');
const logFileCount = 3;
let log = function (logMessage) {
    // Passing false argument will not log the message
    logstack.createLog(directory, logFileCount, logMessage, false);
}
log("Hello from logstack");
```

### To delete log
```js
const logstack = require('logstack');
const path = require('path');

// Please make sure the directory is available and use it only for logstack
const directory = path.join(__dirname, './directory');
const logFileCount = 3;
let deleteLog = function (fileName) {
    logstack.deleteLog(directory, fileName);
}
```

## Features
* Prints log messages with time in specific date file
* Provides option to create daily log file
* Useful in applications where you may want to log error, info while in development and production for different parts of the code
* Option to enable and disable logging anytime
* Option to delete log

## Author
Rohan Shukla [GitHub](https://github.com/rohanshukla) [LinkedIn](https://www.linkedin.com/in/shuklarohan)

## License
© Licensed under the [MIT License](LICENSE).
