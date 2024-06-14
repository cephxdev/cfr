# cfr

A JavaScript port of the [CFR decompiler](https://github.com/leibnitz27/cfr).

## Example

```js
const fs = require("fs");
const cfr = require("./cfr.min.js"); // get it from the dist/ directory or jsDelivr

cfr.main(); // initialize the API object

const data = fs.readFileSync("./your/package/HelloWorld.class"); // read a class file
console.log(cfr.api.decompile("your.package.HelloWorld", {
    classes: {
        "your.package.HelloWorld": data,
    }
}));
```

Or see the browser-based proof-of-concept in the [docs](./docs) directory.

## Licensing

The supporting code for this project and the CFR decompiler are licensed under the MIT License
([supporting code](./LICENSE), [CFR](https://github.com/leibnitz27/cfr/blob/master/LICENSE)).
