# Sha256HmacKey2019 Crypto Suite Context _(sha256-hmac-key-2019-context)_

[![Build status](https://img.shields.io/github/workflow/status/digitalbazaar/sha256-hmac-key-2019-context/Node.js%20CI)](https://github.com/digitalbazaar/sha256-hmac-key-2019-context/actions?query=workflow%3A%22Node.js+CI%22)
[![Coverage status](https://img.shields.io/codecov/c/github/digitalbazaar/sha256-hmac-key-2019-context)](https://codecov.io/gh/digitalbazaar/sha256-hmac-key-2019-context)
[![NPM Version](https://img.shields.io/npm/v/sha256-hmac-key-2019-context.svg)](https://npm.im/sha256-hmac-key-2019-context)

> A JSON-LD context for the Sha256HmacKey2019 crypto suite for JavaScript.

## Table of Contents

- [Background](#background)
- [Install](#install)
- [Usage](#usage)
- [Commercial Support](#commercial-support)
- [License](#license)

## Background

See also (related specs):

* [WebKMS v0.1](https://w3c-ccg.github.io/webkms/)

## Install

Requires Node.js 12+

To install via NPM:

```
npm install sha256-hmac-key-2019-context
```

## Usage

```js
import hmacCtx from 'sha256-hmac-key-2019-context';
// or
const hmacCtx = require('sha256-hmac-key-2019-context');
const {contexts, constants, appContextMap} = hmacCtx;

hmacCtx.CONTEXT_URL
// 'https://w3id.org/security/sha256-hmac-2019/v1'

// Codec term map value for CBOR-LD
hmacCtx.constants.CBORLD_CODEC_VALUE
// 0x1B

// get context data for a specific context
hmacCtx.CONTEXT
// full context object
```

This package can be used with bundlers, such as [webpack][], in browser
applications.

## API

The library exports the following properties:
- `CONTEXT_URL`
- `CONTEXT`
- `constants`: A Object that maps constants to well-known context URLs. The
  main constant `CONTEXT_URL` may be updated from time to time to the
  latest context location.
- `contexts`: A `Map` that maps URLs to full context data.
- `appContextMap`: For use with `cborld` library.

## Developing

WARNING: The `.jsonld` in `contexts/` is auto-generated by the `npm run build` script,
each time you run the test suite.

DO NOT edit it directly (or your changes will be quickly overwritten).
Instead, make all context changes to `js/context.js`.

## Commercial Support

Commercial support for this library is available upon request from
Digital Bazaar: support@digitalbazaar.com

## License

- BSD 3-Clause © Digital Bazaar
- See the [LICENSE](./LICENSE) file for details.

[webpack]: https://webpack.js.org/
