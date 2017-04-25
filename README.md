# npmdoc-http2

#### basic api documentation for  [http2 (v3.3.6)](https://github.com/molnarg/node-http2)  [![npm package](https://img.shields.io/npm/v/npmdoc-http2.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-http2) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-http2.svg)](https://travis-ci.org/npmdoc/node-npmdoc-http2)

#### An HTTP/2 client and server implementation

[![NPM](https://nodei.co/npm/http2.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/http2)

- [https://npmdoc.github.io/node-npmdoc-http2/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-http2/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-http2/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-http2/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-http2/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-http2/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Gábor Molnár",
        "url": "http://gabor.molnar.es"
    },
    "bugs": {
        "url": "https://github.com/molnarg/node-http2/issues"
    },
    "contributors": [
        {
            "name": "Nick Hurley"
        },
        {
            "name": "Mike Belshe"
        },
        {
            "name": "Yoshihiro Iwanaga"
        },
        {
            "name": "Igor Novikov"
        },
        {
            "name": "James Willcox"
        },
        {
            "name": "David Björklund"
        },
        {
            "name": "Patrick McManus"
        }
    ],
    "dependencies": {},
    "description": "An HTTP/2 client and server implementation",
    "devDependencies": {
        "bunyan": "*",
        "chai": "*",
        "docco": "*",
        "istanbul": "*",
        "mocha": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "7df06227e02b5b5a5841deea08239b3198d04bec",
        "tarball": "https://registry.npmjs.org/http2/-/http2-3.3.6.tgz"
    },
    "engines": {
        "node": ">=0.12.0"
    },
    "gitHead": "2c4c310f414d3249421340c0e2618873b07c17cb",
    "homepage": "https://github.com/molnarg/node-http2",
    "keywords": [
        "http",
        "http2",
        "client",
        "server"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "molnarg"
        },
        {
            "name": "todesschaf"
        }
    ],
    "name": "http2",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/molnarg/node-http2.git"
    },
    "scripts": {
        "doc": "docco lib/* --output doc --layout parallel --template root.jst --css doc/docco.css && docco lib/protocol/* --output doc/protocol --layout parallel --template protocol.jst --css doc/docco.css",
        "test": "istanbul test _mocha -- --reporter spec --slow 500 --timeout 15000"
    },
    "version": "3.3.6",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
