# npmtest-electron-compile

#### basic test coverage for  [electron-compile (v6.4.0)](https://github.com/paulcbetts/electron-compile)  [![npm package](https://img.shields.io/npm/v/npmtest-electron-compile.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-electron-compile) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-electron-compile.svg)](https://travis-ci.org/npmtest/node-npmtest-electron-compile)

#### Electron supporting package to compile JS and CSS in Electron applications

[![NPM](https://nodei.co/npm/electron-compile.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/electron-compile)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-electron-compile/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-electron-compile/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-electron-compile/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-electron-compile/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-electron-compile/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-electron-compile/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-electron-compile/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-electron-compile/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-electron-compile/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-electron-compile/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-electron-compile/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-electron-compile/build/test-report.html](https://npmtest.github.io/node-npmtest-electron-compile/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-electron-compile/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-electron-compile/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-electron-compile/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-electron-compile/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-electron-compile/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-electron-compile/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-electron-compile/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-electron-compile/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "electron-compile",
    "version": "6.4.0",
    "description": "Electron supporting package to compile JS and CSS in Electron applications",
    "scripts": {
        "doc": "esdoc -c ./esdoc.json",
        "compile": "cross-env NODE_ENV='production' git clean -xdf lib && babel -d lib/ src",
        "prepublish": "npm run compile",
        "start": "npm run compile && electron ./test-dist/electron-smoke-test.js",
        "test": "mocha --compilers js:babel-register test/*.js",
        "test-cov": "cross-env NODE_ENV='test' istanbul cover ./node_modules/mocha/bin/_mocha -- --compilers js:babel-register test/*.js"
    },
    "bin": {
        "electron-compile": "lib/cli.js",
        "electron-packager-compile": "lib/packager-cli.js"
    },
    "repository": {
        "type": "git",
        "url": "https://github.com/paulcbetts/electron-compile"
    },
    "keywords": [
        "electron"
    ],
    "author": "Paul Betts <paul@paulbetts.org>",
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/paulcbetts/electron-compile/issues"
    },
    "homepage": "https://github.com/paulcbetts/electron-compile",
    "main": "lib/index.js",
    "types": "types/index.d.ts",
    "engines": {
        "node": ">= 5.0"
    },
    "dependencies": {
        "@paulcbetts/mime-types": "^2.1.10",
        "@types/node": "^7.0.12",
        "btoa": "^1.1.2",
        "debug": "^2.5.1",
        "lru-cache": "^4.0.1",
        "mkdirp": "^0.5.1",
        "pify": "^2.3.0",
        "rimraf": "^2.5.4",
        "rxjs": "^5.1.1",
        "spawn-rx": "^2.0.3",
        "yargs": "^4.8.1"
    },
    "devDependencies": {
        "asar": "^0.12.1",
        "babel-cli": "^6.11.4",
        "babel-eslint": "^6.1.2",
        "babel-plugin-array-includes": "^2.0.3",
        "babel-plugin-istanbul": "^4.0.0",
        "babel-plugin-transform-async-to-generator": "^6.8.0",
        "babel-preset-es2016-node5": "^1.1.2",
        "babel-preset-react": "^6.11.1",
        "babel-register": "^6.11.6",
        "chai": "^3.5.0",
        "chai-as-promised": "^5.3.0",
        "cheerio": "^0.20.0",
        "cross-env": "^3.2.4",
        "electron-compilers": "^5.8.0",
        "electron-packager": "^7.5.1",
        "electron-prebuilt": "^1.3.3",
        "esdoc": "^0.4.8",
        "esdoc-es7-plugin": "0.0.3",
        "esdoc-plugin-async-to-sync": "^0.5.0",
        "eslint": "^3.3.0",
        "istanbul": "^0.4.5",
        "mocha": "^3.0.2"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
