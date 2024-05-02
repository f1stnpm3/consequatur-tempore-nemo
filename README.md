# @f1stnpm3/consequatur-tempore-nemo <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS WeakMap? This module works cross-realm/iframe, and despite ES6 @@toStringTag.

## Example

```js
var isWeakMap = require('@f1stnpm3/consequatur-tempore-nemo');
assert(!isWeakMap(function () {}));
assert(!isWeakMap(null));
assert(!isWeakMap(function* () { yield 42; return Infinity; });
assert(!isWeakMap(Symbol('foo')));
assert(!isWeakMap(1n));
assert(!isWeakMap(Object(1n)));

assert(!isWeakMap(new Set()));
assert(!isWeakMap(new WeakSet()));
assert(!isWeakMap(new Map()));

assert(isWeakMap(new WeakMap()));

class MyWeakMap extends WeakMap {}
assert(isWeakMap(new MyWeakMap()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@f1stnpm3/consequatur-tempore-nemo
[npm-version-svg]: https://versionbadg.es/inspect-js/@f1stnpm3/consequatur-tempore-nemo.svg
[deps-svg]: https://david-dm.org/inspect-js/@f1stnpm3/consequatur-tempore-nemo.svg
[deps-url]: https://david-dm.org/inspect-js/@f1stnpm3/consequatur-tempore-nemo
[dev-deps-svg]: https://david-dm.org/inspect-js/@f1stnpm3/consequatur-tempore-nemo/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@f1stnpm3/consequatur-tempore-nemo#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@f1stnpm3/consequatur-tempore-nemo.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@f1stnpm3/consequatur-tempore-nemo.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@f1stnpm3/consequatur-tempore-nemo.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@f1stnpm3/consequatur-tempore-nemo
[codecov-image]: https://codecov.io/gh/inspect-js/@f1stnpm3/consequatur-tempore-nemo/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@f1stnpm3/consequatur-tempore-nemo/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@f1stnpm3/consequatur-tempore-nemo
[actions-url]: https://github.com/f1stnpm3/consequatur-tempore-nemo/actions
