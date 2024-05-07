# @diotoborg/amet-cum-culpa <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Get the `byteOffset` out of a DataView, robustly.

This will work in node <= 0.10 and < 0.11.4, where there's no prototype accessor, only a nonconfigurable own property.
It will also work in modern engines where `DataView.prototype.byteOffset` has been deleted after this module has loaded.

## Example

```js
const dataViewByteOffset = require('@diotoborg/amet-cum-culpa');
const assert = require('assert');

const ab = new ArrayBuffer(42);
const dv = new DataView(ab, 2);
assert.equal(dataViewByteOffset(dv), 2);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@diotoborg/amet-cum-culpa
[npm-version-svg]: https://versionbadg.es/inspect-js/@diotoborg/amet-cum-culpa.svg
[deps-svg]: https://david-dm.org/inspect-js/@diotoborg/amet-cum-culpa.svg
[deps-url]: https://david-dm.org/inspect-js/@diotoborg/amet-cum-culpa
[dev-deps-svg]: https://david-dm.org/inspect-js/@diotoborg/amet-cum-culpa/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@diotoborg/amet-cum-culpa#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@diotoborg/amet-cum-culpa.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@diotoborg/amet-cum-culpa.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@diotoborg/amet-cum-culpa.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@diotoborg/amet-cum-culpa
[codecov-image]: https://codecov.io/gh/inspect-js/@diotoborg/amet-cum-culpa/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@diotoborg/amet-cum-culpa/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@diotoborg/amet-cum-culpa
[actions-url]: https://github.com/inspect-js/@diotoborg/amet-cum-culpa/actions
