# api documentation for  [normalizr (v3.2.2)](https://github.com/paularmstrong/normalizr)  [![npm package](https://img.shields.io/npm/v/npmdoc-normalizr.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-normalizr) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-normalizr.svg)](https://travis-ci.org/npmdoc/node-npmdoc-normalizr)
#### Normalizes and denormalizes JSON according to schema for Redux and Flux applications

[![NPM](https://nodei.co/npm/normalizr.png?downloads=true)](https://www.npmjs.com/package/normalizr)

[![apidoc](https://npmdoc.github.io/node-npmdoc-normalizr/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-normalizr_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-normalizr/build/apidoc.html)

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
            "name": "paularmstrong",
            "email": "paul@spaceyak.com"
        }
    ],
    "name": "normalizr",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module normalizr](#apidoc.module.normalizr)
1.  [function <span class="apidocSignatureSpan">normalizr.</span>denormalize (input, schema, entities)](#apidoc.element.normalizr.denormalize)
1.  [function <span class="apidocSignatureSpan">normalizr.</span>normalize (input, schema)](#apidoc.element.normalizr.normalize)
1.  object <span class="apidocSignatureSpan">normalizr.</span>schema

#### [module normalizr.schema](#apidoc.module.normalizr.schema)
1.  [function <span class="apidocSignatureSpan">normalizr.schema.</span>Array ()](#apidoc.element.normalizr.schema.Array)
1.  [function <span class="apidocSignatureSpan">normalizr.schema.</span>Entity (key)](#apidoc.element.normalizr.schema.Entity)
1.  [function <span class="apidocSignatureSpan">normalizr.schema.</span>Object (definition)](#apidoc.element.normalizr.schema.Object)
1.  [function <span class="apidocSignatureSpan">normalizr.schema.</span>Union (definition, schemaAttribute)](#apidoc.element.normalizr.schema.Union)
1.  [function <span class="apidocSignatureSpan">normalizr.schema.</span>Values ()](#apidoc.element.normalizr.schema.Values)



# <a name="apidoc.module.normalizr"></a>[module normalizr](#apidoc.module.normalizr)

#### <a name="apidoc.element.normalizr.denormalize"></a>[function <span class="apidocSignatureSpan">normalizr.</span>denormalize (input, schema, entities)](#apidoc.element.normalizr.denormalize)
- description and source-code
```javascript
function denormalize(input, schema, entities) {
  if (!input) {
    return input;
  }

  return getUnvisit(entities)(input, schema);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.normalizr.normalize"></a>[function <span class="apidocSignatureSpan">normalizr.</span>normalize (input, schema)](#apidoc.element.normalizr.normalize)
- description and source-code
```javascript
function normalize(input, schema) {
  if (!input || (typeof input === 'undefined' ? 'undefined' : _typeof(input)) !== 'object') {
    throw new Error('Unexpected input given to normalize. Expected type to be "object", found "' + (typeof input === 'undefined' ? '
undefined' : _typeof(input)) + '".');
  }

  var entities = {};
  var addEntity = addEntities(entities);

  var result = visit(input, input, null, schema, addEntity);
  return { entities: entities, result: result };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.normalizr.schema"></a>[module normalizr.schema](#apidoc.module.normalizr.schema)

#### <a name="apidoc.element.normalizr.schema.Array"></a>[function <span class="apidocSignatureSpan">normalizr.schema.</span>Array ()](#apidoc.element.normalizr.schema.Array)
- description and source-code
```javascript
function ArraySchema() {
  _classCallCheck(this, ArraySchema);

  return _possibleConstructorReturn(this, (ArraySchema.__proto__ || Object.getPrototypeOf(ArraySchema)).apply(this, arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.normalizr.schema.Entity"></a>[function <span class="apidocSignatureSpan">normalizr.schema.</span>Entity (key)](#apidoc.element.normalizr.schema.Entity)
- description and source-code
```javascript
function EntitySchema(key) {
  var definition = arguments.length > 1 && arguments[1] !== undefined ? arguments[1] : {};
  var options = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : {};

  _classCallCheck(this, EntitySchema);

  if (!key || typeof key !== 'string') {
    throw new Error('Expected a string key for Entity, but found ' + key + '.');
  }

  var _options$idAttribute = options.idAttribute,
      idAttribute = _options$idAttribute === undefined ? 'id' : _options$idAttribute,
      _options$mergeStrateg = options.mergeStrategy,
      mergeStrategy = _options$mergeStrateg === undefined ? function (entityA, entityB) {
    return _extends({}, entityA, entityB);
  } : _options$mergeStrateg,
      _options$processStrat = options.processStrategy,
      processStrategy = _options$processStrat === undefined ? function (input) {
    return _extends({}, input);
  } : _options$processStrat;


  this._key = key;
  this._getId = typeof idAttribute === 'function' ? idAttribute : getDefaultGetId(idAttribute);
  this._idAttribute = idAttribute;
  this._mergeStrategy = mergeStrategy;
  this._processStrategy = processStrategy;
  this.define(definition);
}
```
- example usage
```shell
...

We have two nested entity types within our 'article': 'users' and 'comments'. Using various 'schema', we can normalize all three
 entity types down:

'''js
import { normalize, schema } from 'normalizr';

// Define a users schema
const user = new schema.Entity('users');

// Define your comments schema
const comment = new schema.Entity('comments', {
  commenter: user
});

// Define your article
...
```

#### <a name="apidoc.element.normalizr.schema.Object"></a>[function <span class="apidocSignatureSpan">normalizr.schema.</span>Object (definition)](#apidoc.element.normalizr.schema.Object)
- description and source-code
```javascript
function ObjectSchema(definition) {
  _classCallCheck(this, ObjectSchema);

  this.define(definition);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.normalizr.schema.Union"></a>[function <span class="apidocSignatureSpan">normalizr.schema.</span>Union (definition, schemaAttribute)](#apidoc.element.normalizr.schema.Union)
- description and source-code
```javascript
function UnionSchema(definition, schemaAttribute) {
  _classCallCheck(this, UnionSchema);

  if (!schemaAttribute) {
    throw new Error('Expected option "schemaAttribute" not found on UnionSchema.');
  }
  return _possibleConstructorReturn(this, (UnionSchema.__proto__ || Object.getPrototypeOf(UnionSchema)).call(this, definition, schemaAttribute
));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.normalizr.schema.Values"></a>[function <span class="apidocSignatureSpan">normalizr.schema.</span>Values ()](#apidoc.element.normalizr.schema.Values)
- description and source-code
```javascript
function ValuesSchema() {
  _classCallCheck(this, ValuesSchema);

  return _possibleConstructorReturn(this, (ValuesSchema.__proto__ || Object.getPrototypeOf(ValuesSchema)).apply(this, arguments));
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
