# npmdoc-xml-js

#### api documentation for  [xml-js (v1.0.2)](https://github.com/nashwaan/xml-js#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-xml-js.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-xml-js) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-xml-js.svg)](https://travis-ci.org/npmdoc/node-npmdoc-xml-js)

#### A convertor between XML text and Javascript object / JSON text.

[![NPM](https://nodei.co/npm/xml-js.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/xml-js)

- [https://npmdoc.github.io/node-npmdoc-xml-js/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-xml-js/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-xml-js/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-xml-js/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-xml-js/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-xml-js/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Yousuf Almarzooqi"
    },
    "bin": {
        "xml-js": "./bin/cli.js"
    },
    "bugs": {
        "url": "https://github.com/nashwaan/xml-js/issues"
    },
    "dependencies": {
        "sax": "^1.2.1"
    },
    "description": "A convertor between XML text and Javascript object / JSON text.",
    "devDependencies": {
        "biased-opener": "^0.2.8",
        "browser-sync": "^2.18.6",
        "cash-cat": "^0.2.0",
        "codacy-coverage": "^2.0.0",
        "codeclimate-test-reporter": "^0.4.0",
        "coveralls": "^2.11.15",
        "cross-env": "^3.1.4",
        "globify": "^2.0.0",
        "istanbul": "^0.4.5",
        "jasmine": "^2.5.3",
        "node-inspector": "^0.12.8",
        "nodemon": "^1.11.0",
        "npm-run-all": "^4.0.1",
        "typescript": "^2.1.5",
        "watch": "^1.0.1"
    },
    "directories": {},
    "dist": {
        "shasum": "95bbe24591a91542ad852a1c4839d80c363db5b4",
        "tarball": "https://registry.npmjs.org/xml-js/-/xml-js-1.0.2.tgz"
    },
    "gitHead": "4261e1fde197a7d68a1ff3900b7033fb35fca0f9",
    "homepage": "https://github.com/nashwaan/xml-js#readme",
    "keywords": [
        "XML",
        "xml",
        "js",
        "JSON",
        "json",
        "cdata",
        "CDATA",
        "Javascript",
        "js2xml",
        "json2xml",
        "xml2js",
        "xml2json",
        "transform",
        "transformer",
        "transforming",
        "transformation",
        "convert",
        "convertor",
        "converting",
        "conversion",
        "parse",
        "parser",
        "parsing"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "nashwaan"
        }
    ],
    "name": "xml-js",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/nashwaan/xml-js.git"
    },
    "scripts": {
        "bundle:jasmine": "globify test/*_test.js --watch --verbose --list --outfile test/browse-jasmine/bundle.js",
        "coverage": "npm-run-all coverage:*",
        "coverage:a-step": "npm run istanbul",
        "coverage:codacy": "cross-env CODACY_PROJECT_TOKEN=0207815122ea49a68241d1aa435f21f1 cat ./test/browse-coverage/lcov.info | codacy-coverage",
        "coverage:codeclimate": "cross-env CODECLIMATE_REPO_TOKEN=60848a077f9070acf358b0c7145f0a2698a460ddeca7d8250815e75aa4333f7d codeclimate-test-reporter < test\\browse-coverage\\lcov.info",
        "coverage:coveralls": "cat ./test/browse-coverage/lcov.info | coveralls",
        "debug": "nodemon --inspect --watch lib/ --watch test/ --debug-brk test/index.js",
        "debug:jasmine": "nodemon --watch lib/ --watch test/ --debug-brk test/index.js",
        "debug:listener": "node-inspect",
        "debug:live": "browser-sync start --port 8080 --server --startPath ?port=5858 --files lib/ test/ --no-open --no-ui --no-online",
        "debug:open": "biased-opener --browser chrome http://localhost:8080/?port=5858",
        "deploy": "npm-run-all --serial coverage git:commit",
        "git:commit": "git add . && git commit -a -m \"Committed by npm script.\" && git push origin master",
        "git:push": "git push origin master",
        "istanbul": "istanbul cover --dir test/browse-coverage -x test/browse-** test/index.js",
        "jasmine": "jasmine JASMINE_CONFIG_PATH=./test/jasmine.json",
        "live": "npm-run-all --parallel live:* open:*",
        "live:istanbul": "browser-sync start --port 9992 --server test/browse-coverage/lcov-report/ --files test/browse-coverage/lcov-report/ --no-open --no-ui --no-online",
        "live:jasmine": "browser-sync start --port 9991 --server test/browse-jasmine/ --files test/browse-jasmine/ --no-open --no-ui --no-online",
        "open:istanbul": "biased-opener --browser chrome http://localhost:9992",
        "open:jasmine": "biased-opener --browser chrome http://localhost:9991",
        "pre-node6.3.1-debug": "npm-run-all --parallel debug:*",
        "prepublish": "npm run test",
        "start": "npm-run-all --parallel bundle:jasmine watch:istanbul live:* open:*",
        "test": "npm run jasmine && npm run test:types",
        "test:types": "tsc -p ./types",
        "watch:istanbul": "watch \"npm run istanbul\" lib/ test/ --ignoreDirectoryPattern=/browse-.+/",
        "watch:jasmine": "watch \"npm run jasmine\" lib/ test/",
        "xdebug:cli": "nodemon --watch lib/ --debug-brk index.js -- --help"
    },
    "types": "./types/index.d.ts",
    "version": "1.0.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
