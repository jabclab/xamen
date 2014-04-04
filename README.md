# xamen

Xamen is a minimal CI tool for node.js apps written in JavaScript.

### Objectives

Xamen aims to be a minimal CI tool which will initially solely notify
you of if your tests passed or failed. It is written in JavaScript
(using V8 supported [ES6](http://kangax.github.io/es5-compat-table/es6/)
functions) and is designed for testing [node.js](http://nodejs.org/)
apps.

The initial objectives of the project are:

* Full install is possible via `npm install -g xamen`
* App can be started via `xamen start`
* Tests run in a sandboxed environment
* Tests can be run against multiple versions of node.js
* Configuration at both global and test job level is defined via JSON
  files
* Notifications are sent when job passes *or* fails

### Installation

```
$ npm install xamen -g
```

In order to run Xamen you must run node(1) with the `--harmony` flag (see `man node | grep harmony`). If you want to avoid doing this on every run you could create a function in your `~/.bashrc` as follows:

```bash
function xamen() { command xamen "$@" --harmony; } 
```
