# npmdoc-i18next

#### api documentation for  [i18next (v8.0.0)](http://i18next.com)  [![npm package](https://img.shields.io/npm/v/npmdoc-i18next.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-i18next) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-i18next.svg)](https://travis-ci.org/npmdoc/node-npmdoc-i18next)

#### i18next internationalization framework

[![NPM](https://nodei.co/npm/i18next.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/i18next)

- [https://npmdoc.github.io/node-npmdoc-i18next/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-i18next/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-i18next/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-i18next/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-i18next/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-i18next/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jan Mühlemann",
        "url": "https://github.com/jamuhl"
    },
    "bugs": {
        "url": "https://github.com/i18next/i18next/issues"
    },
    "dependencies": {},
    "description": "i18next internationalization framework",
    "devDependencies": {
        "babel-cli": "6.22.2",
        "babel-core": "6.22.1",
        "babel-eslint": "7.1.1",
        "babel-plugin-external-helpers": "6.22.0",
        "babel-plugin-transform-es2015-classes": "6.22.0",
        "babel-plugin-transform-proto-to-assign": "6.22.0",
        "babel-preset-es2015": "6.22.0",
        "babel-preset-stage-0": "6.22.0",
        "babelify": "7.3.0",
        "browserify": "14.0.0",
        "browserify-istanbul": "2.0.0",
        "chai": "3.5.0",
        "coveralls": "2.11.16",
        "eslint": "3.15.0",
        "eslint-config-airbnb": "14.1.0",
        "eslint-plugin-import": "2.2.0",
        "eslint-plugin-jsx-a11y": "4.0.0",
        "eslint-plugin-react": "6.9.0",
        "i18next-browser-languagedetector": "1.0.1",
        "i18next-localstorage-cache": "0.3.0",
        "i18next-sprintf-postprocessor": "0.2.2",
        "i18next-xhr-backend": "1.3.0",
        "istanbul": "github:gotwarlost/istanbul#source-map",
        "karma": "1.4.1",
        "karma-browserify": "5.1.1",
        "karma-chai": "0.1.0",
        "karma-chrome-launcher": "2.0.0",
        "karma-cli": "1.0.1",
        "karma-coverage": "github:douglasduteil/karma-coverage#next",
        "karma-coveralls": "1.1.2",
        "karma-expect": "1.1.3",
        "karma-mocha": "1.3.0",
        "karma-phantomjs-launcher": "1.0.2",
        "karma-rollup-preprocessor": "3.0.3",
        "karma-sinon": "1.0.5",
        "karma-spec-reporter": "0.0.26",
        "mkdirp": "0.5.1",
        "mocha": "3.2.0",
        "phantomjs-prebuilt": "2.1.14",
        "rimraf": "2.5.4",
        "rollup": "0.41.4",
        "rollup-plugin-babel": "2.7.1",
        "rollup-plugin-node-resolve": "2.0.0",
        "rollup-plugin-uglify": "1.0.1",
        "sinon": "1.17.7",
        "watchify": "3.9.0",
        "yargs": "6.6.0"
    },
    "directories": {},
    "dist": {
        "shasum": "487ea70d422e98d0b9ff2246e44bd91d851a46b7",
        "tarball": "https://registry.npmjs.org/i18next/-/i18next-8.0.0.tgz"
    },
    "gitHead": "5f6a86d58222b2c209a8e92ef39c7e602b5d3eaa",
    "homepage": "http://i18next.com",
    "jsnext:main": "dist/es/index.js",
    "keywords": [
        "i18next",
        "internationalization",
        "i18n",
        "translation",
        "localization",
        "l10n",
        "globalization",
        "gettext"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "adrai"
        },
        {
            "name": "jamuhl"
        }
    ],
    "module": "dist/es/index.js",
    "name": "i18next",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/i18next/i18next.git"
    },
    "scripts": {
        "build": "npm run clean && npm run build:cjs && npm run build:es && npm run build:umd && npm run copy",
        "build:amd": "rollup -c rollup.config.js --format amd && rollup -c rollup.config.js --format umd --uglify",
        "build:cjs": "babel src --out-dir dist/commonjs",
        "build:es": "BABEL_ENV=jsnext babel src --out-dir dist/es",
        "build:iife": "rollup -c rollup.config.js --format iife && rollup -c rollup.config.js --format iife --uglify",
        "build:umd": "rollup -c rollup.config.js --format umd && rollup -c rollup.config.js --format umd --uglify",
        "clean": "rimraf dist && mkdirp dist",
        "copy": "cp ./dist/umd/i18next.min.js ./i18next.min.js && cp ./dist/umd/i18next.js ./i18next.js",
        "postversion": "git push && git push --tags",
        "preversion": "npm run test && npm run build && git push",
        "tdd": "karma start karma.conf.js",
        "tdd:compat": "karma start karma.backward.conf.js",
        "test": "npm run test:new && npm run test:compat",
        "test:compat": "karma start karma.backward.conf.js --singleRun",
        "test:new": "karma start karma.conf.js --singleRun"
    },
    "version": "8.0.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
