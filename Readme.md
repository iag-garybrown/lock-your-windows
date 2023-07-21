lock-your-windows
============

Activate the Windows lock screen (Win+L), or check if Windows is currently locked.

## Requirements

- [Node.js and NPM](https://nodejs.org/en/) (version 18.x)
- [node-gyp](https://www.npmjs.com/package/node-gyp) (version 9.3.1)
- [Visual Studio](https://www.visualstudio.com/downloads/) (tested on 2015 Community Edition)
- [Visual Studio Code](https://code.visualstudio.com/download) (tested on 1.80)
- [Unified Windows Platform SDK](https://developer.microsoft.com/en-us/windows/downloads/windows-sdk/) (tested on Windows 10 22H2)

## Installation
```bash
npm install --save lock-your-windows
```

## Usage

```javascript
var lockYourWindows = require('lock-your-windows');

var isLocked = lockYourWindows.isLocked();
console.log("Windows is currently "+(isLocked ? "locked" : "unlocked"));

console.log("Locking Windows...");
lockYourWindows.lock();
```

## Developing

### Recompile the native C++ addon

```bash
node-gyp rebuild
```

### Run tests

```bash
npm test
```