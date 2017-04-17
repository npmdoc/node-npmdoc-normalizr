# api documentation for  [normalizr (v3.2.2)](https://github.com/paularmstrong/normalizr)  [![npm package](https://img.shields.io/npm/v/npmdoc-normalizr.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-normalizr) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-normalizr.svg)](https://travis-ci.org/npmdoc/node-npmdoc-normalizr)
#### Normalizes and denormalizes JSON according to schema for Redux and Flux applications

[![NPM](https://nodei.co/npm/normalizr.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/normalizr)

- [https://npmdoc.github.io/node-npmdoc-normalizr/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-normalizr/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-normalizr/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-normalizr/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-normalizr/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-normalizr/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Paul Armstrong"
    },
    "bugs": {
        "url": "https://github.com/paularmstrong/normalizr/issues"
    },
    "contributors": [
        {
            "name": "Dan Abramov"
        }
    ],
    "dependencies": {},
    "description": "Normalizes and denormalizes JSON according to schema for Redux and Flux applications",
    "devDependencies": {
        "babel-cli": "^6.18.0",
        "babel-eslint": "^7.1.1",
        "babel-preset-es2015": "^6.18.0",
        "babel-preset-es2015-rollup": "^3.0.0",
        "babel-preset-stage-1": "^6.16.0",
        "coveralls": "^2.11.15",
        "eslint": "^3.12.2",
        "flow-bin": "^0.37.1",
        "immutable": "^3.8.1",
        "jest": "^18.0.0",
        "mkdirp": "^0.5.1",
        "npm-run-all": "^3.1.2",
        "rimraf": "^2.5.4",
        "rollup": "^0.37.0",
        "rollup-plugin-babel": "^2.7.1",
        "rollup-plugin-filesize": "^1.0.1",
        "rollup-plugin-uglify": "^1.0.1",
        "typescript": "^2.1.4",
        "typescript-definition-tester": "0.0.5"
    },
    "directories": {},
    "dist": {
        "shasum": "542e915a260ca53279b76a63fb554185e9225f90",
        "tarball": "https://registry.npmjs.org/normalizr/-/normalizr-3.2.2.tgz"
    },
    "files": [
        "dist/",
        "index.d.ts",
        "LICENSE",
        "README.md"
    ],
    "gitHead": "e9ba85b8f9044b2aa97f4b28bd1de19dbe8df4e9",
    "homepage": "https://github.com/paularmstrong/normalizr",
    "keywords": [
        "flux",
        "redux",
        "normalize",
        "denormalize",
        "api",
        "json"
    ],
    "license": "MIT",
    "main": "dist/src/index.js",
    "maintainers": [
        {
            "name": "paularmstrong"
        }
    ],
    "name": "normalizr",
    "optionalDependencies": {},
    "repository": {
        "url": "git+https://github.com/paularmstrong/normalizr.git",
        "type": "git"
    },
    "scripts": {
        "build": "npm run clean && mkdirp dist && npm-run-all --parallel build:development build:production build:node",
        "build:development": "NODE_ENV=development rollup -c",
        "build:node": "babel src/*.js -d dist && babel src/schemas/*.js -d dist",
        "build:production": "NODE_ENV=production rollup -c",
        "clean": "rimraf dist",
        "flow": "flow src; test $? -eq 0 -o $? -eq 2",
        "lint": "eslint ./ --fix",
        "prebuild": "npm run clean",
        "prepublish": "npm run build",
        "test": "jest",
        "test:coverage": "npm run test -- --coverage && cat ./coverage/lcov.info | coveralls"
    },
    "typings": "index.d.ts",
    "version": "3.2.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
