# api documentation for  [nodegit (v0.18.0)](http://nodegit.org)  [![npm package](https://img.shields.io/npm/v/npmdoc-nodegit.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-nodegit) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-nodegit.svg)](https://travis-ci.org/npmdoc/node-npmdoc-nodegit)
#### Node.js libgit2 asynchronous native bindings

[![NPM](https://nodei.co/npm/nodegit.png?downloads=true)](https://www.npmjs.com/package/nodegit)

[![apidoc](https://npmdoc.github.io/node-npmdoc-nodegit/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-nodegit_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-nodegit/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-nodegit/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-nodegit/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tim Branyen",
        "url": "@tbranyen"
    },
    "binary": {
        "module_name": "nodegit",
        "module_path": "./build/Release/",
        "host": "https://nodegit.s3.amazonaws.com/nodegit/nodegit/"
    },
    "bugs": {
        "url": "https://github.com/nodegit/nodegit/issues"
    },
    "contributors": [
        {
            "name": "John Haley",
            "email": "john@haley.io"
        },
        {
            "name": "Max Korp",
            "email": "maxkorp@8bytealchemy.com"
        }
    ],
    "dependencies": {
        "fs-extra": "~0.26.2",
        "lodash": "^4.13.1",
        "nan": "^2.2.0",
        "node-gyp": "^3.5.0",
        "node-pre-gyp": "~0.6.32",
        "promisify-node": "~0.3.0"
    },
    "description": "Node.js libgit2 asynchronous native bindings",
    "devDependencies": {
        "aws-sdk": "^2.3.19",
        "babel-cli": "^6.7.7",
        "babel-preset-es2015": "^6.6.0",
        "clean-for-publish": "~1.0.2",
        "combyne": "~0.8.1",
        "coveralls": "~2.11.4",
        "istanbul": "~0.3.20",
        "js-beautify": "~1.5.10",
        "jshint": "~2.8.0",
        "lcov-result-merger": "~1.0.2",
        "mocha": "~2.3.4",
        "walk": "^2.3.9"
    },
    "directories": {
        "build": "./build",
        "lib": "./lib"
    },
    "dist": {
        "shasum": "d4df65e4539003f1ed27853d101350f39c4746b3",
        "tarball": "https://registry.npmjs.org/nodegit/-/nodegit-0.18.0.tgz"
    },
    "engines": {
        "node": ">= 4"
    },
    "gitHead": "6ff12edfefbc03f29db33763ee634296ec3a955c",
    "homepage": "http://nodegit.org",
    "keywords": [
        "libgit2",
        "git2",
        "git",
        "native"
    ],
    "license": "MIT",
    "main": "dist/nodegit.js",
    "maintainers": [
        {
            "name": "tbranyen",
            "email": "tim@tabdeveloper.com"
        },
        {
            "name": "faceleg",
            "email": "mike@pagesofinterest.net"
        },
        {
            "name": "johnhaley81",
            "email": "johnhaley81@gmail.com"
        },
        {
            "name": "maxkorp",
            "email": "maxkorp@8bytealchemy.com"
        }
    ],
    "name": "nodegit",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/nodegit/nodegit.git"
    },
    "scripts": {
        "babel": "babel --presets es2015 -d ./dist ./lib",
        "cov": "npm run cppcov && npm run filtercov && npm run mergecov",
        "coveralls": "cat ./test/coverage/merged.lcov | coveralls",
        "cppcov": "mkdir -p test/coverage/cpp && ./lcov-1.10/bin/lcov --gcov-tool /usr/bin/gcov-4.9 --capture --directory build/Release/obj.target/nodegit/src --output-file test/coverage/cpp/lcov_full.info",
        "filtercov": "./lcov-1.10/bin/lcov --extract test/coverage/cpp/lcov_full.info $(pwd)/src/* $(pwd)/src/**/* $(pwd)/include/* $(pwd)/include/**/* --output-file test/coverage/cpp/lcov.info && rm test/coverage/cpp/lcov_full.info",
        "generateJson": "node generate/scripts/generateJson",
        "generateMissingTests": "node generate/scripts/generateMissingTests",
        "generateNativeCode": "node generate/scripts/generateNativeCode",
        "install": "node lifecycleScripts/preinstall && node lifecycleScripts/install",
        "installDebug": "BUILD_DEBUG=true npm install",
        "lint": "jshint lib test/tests test/utils examples lifecycleScripts",
        "mergecov": "lcov-result-merger 'test/**/*.info' 'test/coverage/merged.lcov' && ./lcov-1.10/bin/genhtml test/coverage/merged.lcov --output-directory test/coverage/report",
        "mocha": "mocha test/runner test/tests --timeout 15000",
        "mochaDebug": "mocha --debug-brk test/runner test/tests --timeout 15000",
        "postinstall": "node lifecycleScripts/postinstall",
        "prepublish": "npm run babel",
        "rebuild": "node generate && npm run babel && node-gyp configure build",
        "rebuildDebug": "node generate && npm run babel && node-gyp configure --debug build",
        "recompile": "node-gyp configure build",
        "recompileDebug": "node-gyp configure --debug build",
        "test": "npm run lint && node --expose-gc test",
        "xcodeDebug": "node-gyp configure -- -f xcode"
    },
    "vendorDependencies": {
        "libssh2": "1.7.0",
        "http_parser": "2.5.0"
    },
    "version": "0.18.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module nodegit](#apidoc.module.nodegit)



# <a name="apidoc.module.nodegit"></a>[module nodegit](#apidoc.module.nodegit)



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
