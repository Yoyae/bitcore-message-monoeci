# Monoeci Message Verification and Signing for Bitcore-monoeci


[![NPM Package](https://img.shields.io/npm/v/bitcore-message-monoeci.svg?style=flat-square)](https://www.npmjs.org/package/bitcore-message-monoeci)
[![Build Status](https://img.shields.io/travis/yoyae/bitcore-message-monoeci.svg?branch=master&style=flat-square)](https://travis-ci.org/yoyae/bitcore-message-monoeci)
[![Coverage Status](https://img.shields.io/coveralls/yoyae/bitcore-message-monoeci.svg?style=flat-square)](https://coveralls.io/r/yoyae/bitcore-message-monoeci?branch=master)

bitcore-message-monoeci adds support for verifying and signing monoeci messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main bitcore-monoeci repo](https://github.com/yoyae/bitcore-monoeci) for more information.

## Getting Started

```sh
npm install bitcore-message-monoeci
```

```sh
bower install bitcore-message-monoeci
```

To sign a message:

```javascript
var bitcore = require('bitcore-lib-monoeci');
var Message = require('bitcore-message-monoeci');

var privateKey = bitcore.PrivateKey.fromWIF('cPBn5A4ikZvBTQ8D7NnvHZYCAxzDZ5Z2TSGW2LkyPiLxqYaJPBW4');
var signature = Message('hello, world').sign(privateKey);
```

To verify a message:

```javascript
var address = 'n1ZCYg9YXtB5XCZazLxSmPDa8iwJRZHhGx';
var signature = 'H/DIn8uA1scAuKLlCx+/9LnAcJtwQQ0PmcPrJUq90aboLv3fH5fFvY+vmbfOSFEtGarznYli6ShPr9RXwY9UrIY=';
var verified = Message('hello, world').verify(address, signature);
```

## Contributing

See [CONTRIBUTING.md](https://github.com/yoyae/bitcore-monoeci/blob/master/CONTRIBUTING.md) on the main bitcore-monoeci repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.

