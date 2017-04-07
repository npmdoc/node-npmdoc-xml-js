# api documentation for  [xml-js (v1.0.2)](https://github.com/nashwaan/xml-js#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-xml-js.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-xml-js) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-xml-js.svg)](https://travis-ci.org/npmdoc/node-npmdoc-xml-js)
#### A convertor between XML text and Javascript object / JSON text.

[![NPM](https://nodei.co/npm/xml-js.png?downloads=true)](https://www.npmjs.com/package/xml-js)

[![apidoc](https://npmdoc.github.io/node-npmdoc-xml-js/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-xml-js_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-xml-js/build/apidoc.html)

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
            "name": "nashwaan",
            "email": "ysf953@gmail.com"
        }
    ],
    "name": "xml-js",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module xml-js](#apidoc.module.xml-js)
1.  [function <span class="apidocSignatureSpan">xml-js.</span>js2xml (js, options)](#apidoc.element.xml-js.js2xml)
1.  [function <span class="apidocSignatureSpan">xml-js.</span>json2xml (json, options)](#apidoc.element.xml-js.json2xml)
1.  [function <span class="apidocSignatureSpan">xml-js.</span>xml2js (xml, userOptions)](#apidoc.element.xml-js.xml2js)
1.  [function <span class="apidocSignatureSpan">xml-js.</span>xml2json (xml, userOptions)](#apidoc.element.xml-js.xml2json)
1.  object <span class="apidocSignatureSpan">xml-js.</span>common

#### [module xml-js.common](#apidoc.module.xml-js.common)
1.  [function <span class="apidocSignatureSpan">xml-js.common.</span>copyOptions (options)](#apidoc.element.xml-js.common.copyOptions)
1.  [function <span class="apidocSignatureSpan">xml-js.common.</span>ensureFlagExists (item, options)](#apidoc.element.xml-js.common.ensureFlagExists)
1.  [function <span class="apidocSignatureSpan">xml-js.common.</span>ensureKeyExists (key, options)](#apidoc.element.xml-js.common.ensureKeyExists)
1.  [function <span class="apidocSignatureSpan">xml-js.common.</span>ensureSpacesExists (options)](#apidoc.element.xml-js.common.ensureSpacesExists)
1.  [function <span class="apidocSignatureSpan">xml-js.common.</span>getCommandLineHelp (command, requiredArgs, optionalArgs)](#apidoc.element.xml-js.common.getCommandLineHelp)
1.  [function <span class="apidocSignatureSpan">xml-js.common.</span>mapCommandLineArgs (requiredArgs, optionalArgs)](#apidoc.element.xml-js.common.mapCommandLineArgs)
1.  [function <span class="apidocSignatureSpan">xml-js.common.</span>sanitize (text)](#apidoc.element.xml-js.common.sanitize)



# <a name="apidoc.module.xml-js"></a>[module xml-js](#apidoc.module.xml-js)

#### <a name="apidoc.element.xml-js.js2xml"></a>[function <span class="apidocSignatureSpan">xml-js.</span>js2xml (js, options)](#apidoc.element.xml-js.js2xml)
- description and source-code
```javascript
js2xml = function (js, options) {
    'use strict';
    options = validateOptions(options);
    var xml = '';
    if (options.compact) {
        xml = writeElementsCompact(js, options, 0, true);
    } else {
        if (js[options.declarationKey]) {
            xml += writeDeclaration(js[options.declarationKey], options);
        }
        if (js[options.elementsKey] && js[options.elementsKey].length) {
            xml += writeElements(js[options.elementsKey], options, 0, !xml);
        }
    }
    return xml;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xml-js.json2xml"></a>[function <span class="apidocSignatureSpan">xml-js.</span>json2xml (json, options)](#apidoc.element.xml-js.json2xml)
- description and source-code
```javascript
json2xml = function (json, options) {
    'use strict';
    if (json instanceof Buffer) {
        json = json.toString();
    }
    var js = null;
    if (typeof (json) === 'string') {
        try {
            js = JSON.parse(json);
        } catch (e) {
            throw new Error("The JSON structure is invalid");
        }
    } else {
        js = json;
    }
    return js2xml(js, options);
}
```
- example usage
```shell
...

To convert JavaScript object to XML text, use 'js2xml()'. To convert JSON text to XML text, use 'json2xml()'.

'''js
var convert = require('xml-js');
var json = require('fs').readFileSync('test.json', 'utf8');
var options = {ignoreText: true, spaces: 4};
var result = convert.json2xml(json, options);
console.log(result);
'''

### Options for Converting JS object / JSON → XML

The below options are applicable for both 'js2xml()' and 'json2xml()' functions.
...
```

#### <a name="apidoc.element.xml-js.xml2js"></a>[function <span class="apidocSignatureSpan">xml-js.</span>xml2js (xml, userOptions)](#apidoc.element.xml-js.xml2js)
- description and source-code
```javascript
xml2js = function (xml, userOptions) {

    var parser = pureJsParser ? sax.parser(true, {}) : parser = new expat.Parser('UTF-8');
    var result = {};
    currentElement = result;

    options = validateOptions(userOptions);

    if (pureJsParser) {
        parser.onopentag = onStartElement;
        parser.ontext = onText;
        parser.oncomment = onComment;
        parser.onclosetag = onEndElement;
        parser.onerror = onError;
        parser.oncdata = onCdata;
        parser.onprocessinginstruction = onDeclaration;
    } else {
        parser.on('startElement', onStartElement);
        parser.on('text', onText);
        parser.on('comment', onComment);
        parser.on('endElement', onEndElement);
        parser.on('error', onError);
        //parser.on('startCdata', onStartCdata);
        //parser.on('endCdata', onEndCdata);
        //parser.on('entityDecl', onEntityDecl);
    }

    if (pureJsParser) {
        parser.write(xml).close();
    } else {
        if (!parser.parse(xml)) {
            throw new Error('XML parsing error: ' + parser.getError());
        }
    }

    if (result[options.elementsKey]) {
        var temp = result[options.elementsKey];
        delete result[options.elementsKey];
        result[options.elementsKey] = temp;
        delete result.text;
    }

    return result;

}
```
- example usage
```shell
...

To convert XML text to JavaScript object, use 'xml2js()'. To convert XML text to JSON text, use 'xml2json()'.

'''js
var convert = require('xml-js');
var xml = require('fs').readFileSync('test.xml', 'utf8');
var options = {ignoreText: true, alwaysChildren: true};
var result = convert.xml2js(xml, options); // or convert.xml2json(xml, options)
console.log(result);
'''

### Options for Converting XML → JS object / JSON

The below options are applicable for both 'xml2js()' and 'xml2json()' functions.
...
```

#### <a name="apidoc.element.xml-js.xml2json"></a>[function <span class="apidocSignatureSpan">xml-js.</span>xml2json (xml, userOptions)](#apidoc.element.xml-js.xml2json)
- description and source-code
```javascript
xml2json = function (xml, userOptions) {
    'use strict';
    var options, js, json, parentKey;
    options = validateOptions(userOptions);
    js = xml2js(xml, options);
    parentKey = 'compact' in options && options.compact ? '_parent' : 'parent';
    if ('addParent' in options && options.addParent) {
        json = JSON.stringify(js, function (k, v) { return k === parentKey? '_' : v; }, options.spaces);
    } else {
        json = JSON.stringify(js, null, options.spaces);
    }
    return json.replace(/\u2028/g, '\\u2028').replace(/\u2029/g, '\\u2029');
}
```
- example usage
```shell
...
var xml =
'<?xml version="1.0" encoding="utf-8"?>' +
'<note importance="high" logged="true">' +
'    <title>Happy</title>' +
'    <todo>Work</todo>' +
'    <todo>Play</todo>' +
'</note>';
var result1 = convert.xml2json(xml, {compact: true, spaces: 4});
var result2 = convert.xml2json(xml, {compact: false, spaces: 4});
console.log(result1, '\n', result2);
'''

To see the result of this code, see the output above in *Synopsis* section.

Or [run and edit](https://runkit.com/587874e079a2f60013c1f5ac/587874e079a2f60013c1f5ad) this code live in the browser.
...
```



# <a name="apidoc.module.xml-js.common"></a>[module xml-js.common](#apidoc.module.xml-js.common)

#### <a name="apidoc.element.xml-js.common.copyOptions"></a>[function <span class="apidocSignatureSpan">xml-js.common.</span>copyOptions (options)](#apidoc.element.xml-js.common.copyOptions)
- description and source-code
```javascript
copyOptions = function (options) {
    var key, copy = {};
    for (key in options) {
        if (options.hasOwnProperty(key)) {
            copy[key] = options[key];
        }
    }
    return copy;
}
```
- example usage
```shell
...




var common = require('./common');

function validateOptions (userOptions) {
var options = common.copyOptions(userOptions);
common.ensureFlagExists('ignoreDeclaration', options);
common.ensureFlagExists('ignoreAttributes', options);
common.ensureFlagExists('ignoreText', options);
common.ensureFlagExists('ignoreComment', options);
common.ensureFlagExists('ignoreCdata', options);
common.ensureFlagExists('compact', options);
common.ensureFlagExists('fullTagEmptyElement', options);
...
```

#### <a name="apidoc.element.xml-js.common.ensureFlagExists"></a>[function <span class="apidocSignatureSpan">xml-js.common.</span>ensureFlagExists (item, options)](#apidoc.element.xml-js.common.ensureFlagExists)
- description and source-code
```javascript
ensureFlagExists = function (item, options) {
    if (!(item in options) || typeof options[item] !== 'boolean') {
        options[item] = false;
    }
}
```
- example usage
```shell
...



var common = require('./common');

function validateOptions (userOptions) {
var options = common.copyOptions(userOptions);
common.ensureFlagExists('ignoreDeclaration', options);
common.ensureFlagExists('ignoreAttributes', options);
common.ensureFlagExists('ignoreText', options);
common.ensureFlagExists('ignoreComment', options);
common.ensureFlagExists('ignoreCdata', options);
common.ensureFlagExists('compact', options);
common.ensureFlagExists('fullTagEmptyElement', options);
common.ensureSpacesExists(options);
...
```

#### <a name="apidoc.element.xml-js.common.ensureKeyExists"></a>[function <span class="apidocSignatureSpan">xml-js.common.</span>ensureKeyExists (key, options)](#apidoc.element.xml-js.common.ensureKeyExists)
- description and source-code
```javascript
ensureKeyExists = function (key, options) {
    if (!(key + 'Key' in options) || typeof options[key + 'Key'] !== 'string') {
        options[key + 'Key'] = options.compact ? '_' + key : key;
    }
}
```
- example usage
```shell
...
common.ensureFlagExists('ignoreCdata', options);
common.ensureFlagExists('compact', options);
common.ensureFlagExists('fullTagEmptyElement', options);
common.ensureSpacesExists(options);
if (typeof options.spaces === 'number') {
    options.spaces = Array(options.spaces + 1).join(' ');
}
common.ensureKeyExists('declaration', options);
common.ensureKeyExists('attributes', options);
common.ensureKeyExists('text', options);
common.ensureKeyExists('comment', options);
common.ensureKeyExists('cdata', options);
common.ensureKeyExists('type', options);
common.ensureKeyExists('name', options);
common.ensureKeyExists('elements', options);
...
```

#### <a name="apidoc.element.xml-js.common.ensureSpacesExists"></a>[function <span class="apidocSignatureSpan">xml-js.common.</span>ensureSpacesExists (options)](#apidoc.element.xml-js.common.ensureSpacesExists)
- description and source-code
```javascript
ensureSpacesExists = function (options) {
    if (!('spaces' in options) || (typeof options.spaces !== 'number' && typeof options.spaces !== 'string')) {
        options.spaces = 0;
    }
}
```
- example usage
```shell
...
common.ensureFlagExists('ignoreDeclaration', options);
common.ensureFlagExists('ignoreAttributes', options);
common.ensureFlagExists('ignoreText', options);
common.ensureFlagExists('ignoreComment', options);
common.ensureFlagExists('ignoreCdata', options);
common.ensureFlagExists('compact', options);
common.ensureFlagExists('fullTagEmptyElement', options);
common.ensureSpacesExists(options);
if (typeof options.spaces === 'number') {
    options.spaces = Array(options.spaces + 1).join(' ');
}
common.ensureKeyExists('declaration', options);
common.ensureKeyExists('attributes', options);
common.ensureKeyExists('text', options);
common.ensureKeyExists('comment', options);
...
```

#### <a name="apidoc.element.xml-js.common.getCommandLineHelp"></a>[function <span class="apidocSignatureSpan">xml-js.common.</span>getCommandLineHelp (command, requiredArgs, optionalArgs)](#apidoc.element.xml-js.common.getCommandLineHelp)
- description and source-code
```javascript
getCommandLineHelp = function (command, requiredArgs, optionalArgs) {
    var reqArgs = requiredArgs.reduce(function (res, arg) {return res + ' <' + arg.arg + '>';}, '');
    var output = 'Usage: ' + command + reqArgs + ' [options]' + '\n';
    requiredArgs.forEach(function (argument) {
        output += '  <' + argument.arg + '>' + Array(20 - argument.arg.length).join(' ') + argument.desc + '\n';
    });
    output += '\nOptions:' + '\n';
    optionalArgs.forEach(function (argument) {
        output += '  --' + argument.arg + Array(20 - argument.arg.length).join(' ') + argument.desc + '\n';
    });
    return output;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xml-js.common.mapCommandLineArgs"></a>[function <span class="apidocSignatureSpan">xml-js.common.</span>mapCommandLineArgs (requiredArgs, optionalArgs)](#apidoc.element.xml-js.common.mapCommandLineArgs)
- description and source-code
```javascript
mapCommandLineArgs = function (requiredArgs, optionalArgs) {
    var options = {}, r, o, a = 2;
    for (r = 0; r < requiredArgs.length; r += 1) {
        if (a < process.argv.length && process.argv[a].substr(0, 1) !== '-' && process.argv[a] !== 'JASMINE_CONFIG_PATH=./jasmine
.json') {
            options[requiredArgs[r].option] = process.argv[a++];
        } else {
            break;
        }
    }
    for (; a < process.argv.length; a += 1) {
        for (o = 0; o < optionalArgs.length; o += 1) {
            if (optionalArgs[o].alias === process.argv[a].slice(1) || optionalArgs[o].arg === process.argv[a].slice(2)) {
                break;
            }
        }
        if (o < optionalArgs.length) {
            switch (optionalArgs[o].type) {
                case 'file': case 'string': case 'number':
                    if (a + 1 < process.argv.length) {
                        a += 1;
                        options[optionalArgs[o].option] = (optionalArgs[o].type === 'number' ? Number(process.argv[a]) : process
.argv[a]);
                    }
                    break;
                case 'flag':
                    options[optionalArgs[o].option] = true; break;
            }
        }
    }
    return options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xml-js.common.sanitize"></a>[function <span class="apidocSignatureSpan">xml-js.common.</span>sanitize (text)](#apidoc.element.xml-js.common.sanitize)
- description and source-code
```javascript
sanitize = function (text) {
    return text.replace(/&/g, "&amp;").replace(/</g, "&lt;").replace(/>/g, "&gt;").replace(/"/g, "&quot;").replace(/'/g, "&#39;");
}
```
- example usage
```shell
...
if (options.trim) {
    text = text.trim();
}
if (options.nativeType) {
    text = nativeType(text);
}
if (options.sanitize) {
    text = common.sanitize(text);
}
addField('text', text, options);
}

function onComment (comment) {
if (options.ignoreComment) {
    return;
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
