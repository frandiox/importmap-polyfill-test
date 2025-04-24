# Double loading es-module-shim test

1. Run `npx serve`.
2. Open `http://localhost:3000` in Firefox or older versions of Safari/Chrome.
3. Dynamic module is not loaded properly, but it works when removing the second polyfill script from `index.html`.

Error in Firefox:

```sh
Uncaught (in promise) Error: Unable to resolve specifier 'dynamically-imported-module' imported from http://localhost:3000/1
    throwUnresolved es-module-shims.js:493
    _resolve es-module-shims.js:411
    importHandler es-module-shims.js:445
    importShim es-module-shims.js:456
    <anonymous> 1:3
```
