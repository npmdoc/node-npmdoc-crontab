# api documentation for  [crontab (v1.1.3)](https://github.com/dachev/node-crontab)  [![npm package](https://img.shields.io/npm/v/npmdoc-crontab.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-crontab) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-crontab.svg)](https://travis-ci.org/npmdoc/node-npmdoc-crontab)
#### A module for reading, creating, deleting, manipulating, and saving system cronjobs with node.js

[![NPM](https://nodei.co/npm/crontab.png?downloads=true)](https://www.npmjs.com/package/crontab)

[![apidoc](https://npmdoc.github.io/node-npmdoc-crontab/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-crontab_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-crontab/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-crontab/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-crontab/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Blagovest Dachev",
        "email": "blago@dachev.com",
        "url": "http://www.dachev.com"
    },
    "bugs": {
        "url": "https://github.com/dachev/node-crontab/issues"
    },
    "dependencies": {
        "underscore": "^1.6.0"
    },
    "description": "A module for reading, creating, deleting, manipulating, and saving system cronjobs with node.js",
    "devDependencies": {
        "vows": "0.7.0"
    },
    "directories": {},
    "dist": {
        "shasum": "5469a2a76c505d8b7808e5b769061ab26dca3420",
        "tarball": "https://registry.npmjs.org/crontab/-/crontab-1.1.3.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "gitHead": "775805ab542501f2025b20bdba2107d1b4271e54",
    "homepage": "https://github.com/dachev/node-crontab",
    "keywords": [
        "cron",
        "crontab",
        "schedule",
        "system",
        "run",
        "process"
    ],
    "licenses": [
        {
            "type": "GPL3",
            "url": "http://opensource.org/licenses/MIT"
        }
    ],
    "main": "./lib/index",
    "maintainers": [
        {
            "name": "blago",
            "email": "blago@dachev.com"
        }
    ],
    "name": "crontab",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/dachev/node-crontab.git"
    },
    "scripts": {
        "test": "test/runner.js"
    },
    "version": "1.1.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module crontab](#apidoc.module.crontab)
1.  [function <span class="apidocSignatureSpan">crontab.</span>load ()](#apidoc.element.crontab.load)



# <a name="apidoc.module.crontab"></a>[module crontab](#apidoc.module.crontab)

#### <a name="apidoc.element.crontab.load"></a>[function <span class="apidocSignatureSpan">crontab.</span>load ()](#apidoc.element.crontab.load)
- description and source-code
```javascript
load = function () {
  if (_.isString(arguments[0]) && _.isFunction(arguments[1])) {
    new CronTab(arguments[0], arguments[1]);
  }
  else if (_.isFunction(arguments[0])) {
    new CronTab('', arguments[0]);
  }
}
```
- example usage
```shell
...
'''bash
$ npm install crontab
'''

## Examples
### Kitchen sink
'''js
require('crontab').load(function(err, crontab) {
// create with string expression
var job = crontab.create('ls -la', '0 7 * * 1,2,3,4,5');

// create with Date
var job = crontab.create('ls -lh', new Date(1400373907766));

// create with comment
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
