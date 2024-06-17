# cfr

A JavaScript port of the [CFR decompiler](https://github.com/leibnitz27/cfr).

## Example

```js
const fs = require("fs");
const { decompile } = require("./cfr.js"); // get it from the dist/ directory or jsDelivr

const data = fs.readFileSync("./your/package/HelloWorld.class"); // read a class file
console.log(decompile(data, {
    classes: [] /* no additional classes for analysis */,
    options: {
        /* see https://github.com/leibnitz27/cfr/blob/master/src/org/benf/cfr/reader/util/getopt/OptionsImpl.java#L274 */
        "hidelangimports": "false", /* testing option - don't hide java.lang imports */
    },
}));
```

Or see the browser-based proof-of-concept in the [docs](./docs) directory.

## Licensing

The supporting code for this project and the CFR decompiler are licensed under the MIT License
([supporting code](./LICENSE), [CFR](https://github.com/leibnitz27/cfr/blob/master/LICENSE)).
