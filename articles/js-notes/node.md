# NodeJs notes

* In both browser (besides `window`) and node we have `global` object.
* When node loads a file (module), it wraps file contents with `(function(exports, require, module, __filename, __dirname){ ...file-contents... })();`<br />
    That is why `var hz = 1;` does not go to `global.hz`
* Use `EventEmitter` in order to make communication between modules
