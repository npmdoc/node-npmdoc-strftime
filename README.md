# api documentation for  [strftime (v0.10.0)](http://samhuri.net/proj/strftime)  [![npm package](https://img.shields.io/npm/v/npmdoc-strftime.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-strftime) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-strftime.svg)](https://travis-ci.org/npmdoc/node-npmdoc-strftime)
#### strftime for JavaScript

[![NPM](https://nodei.co/npm/strftime.png?downloads=true)](https://www.npmjs.com/package/strftime)

[![apidoc](https://npmdoc.github.io/node-npmdoc-strftime/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-strftime_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-strftime/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-strftime/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-strftime/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Sami Samhuri",
        "email": "sami@samhuri.net"
    },
    "bugs": {
        "url": "https://github.com/samsonjs/strftime/issues",
        "email": "sami@samhuri.net"
    },
    "contributors": [
        {
            "name": "Alexandr Nikitin",
            "url": "https://github.com/alexandrnikitin"
        },
        {
            "name": "Andrew Pirondini of iFixit",
            "url": "https://github.com/andrewjpiro"
        },
        {
            "name": "Andrew Schaaf",
            "email": "andrew@andrewschaaf.com",
            "url": "https://github.com/andrewschaaf"
        },
        {
            "name": "Ayman Nedjmeddine",
            "url": "https://github.com/IOAyman"
        },
        {
            "name": "Cory Heslip",
            "url": "https://github.com/cheslip"
        },
        {
            "name": "Forbes Lindesay",
            "url": "https://github.com/ForbesLindesay"
        },
        {
            "name": "John Zwinck",
            "url": "https://github.com/jzwinck"
        },
        {
            "name": "Joost Hietbrink",
            "url": "https://github.com/joost"
        },
        {
            "name": "Kevin Jin",
            "url": "https://github.com/Kevin-Jin"
        },
        {
            "name": "Michael J.",
            "url": "https://github.com/michaeljayt"
        },
        {
            "name": "Peter deHaan",
            "url": "https://github.com/pdehaan"
        },
        {
            "name": "Rob Colburn",
            "email": "rob@robcolburn.com",
            "url": "https://github.com/robcolburn"
        },
        {
            "name": "Ryan Regalado",
            "url": "https://github.com/d48"
        },
        {
            "name": "Ryan Stafford",
            "url": "https://github.com/ryanstafford"
        },
        {
            "name": "Sami Samhuri",
            "email": "sami@samhuri.net",
            "url": "https://github.com/samsonjs"
        },
        {
            "name": "Stian Grytøyr",
            "url": "https://github.com/stiang"
        },
        {
            "name": "TJ Holowaychuk",
            "url": "https://github.com/tj"
        },
        {
            "name": "w0den",
            "url": "https://github.com/w0den"
        }
    ],
    "dependencies": {},
    "description": "strftime for JavaScript",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "b3f0fa419295202a5a289f6d6be9f4909a617193",
        "tarball": "https://registry.npmjs.org/strftime/-/strftime-0.10.0.tgz"
    },
    "engines": {
        "node": ">=0.2.0"
    },
    "gitHead": "793ecfb7b492da0818c60ca205e86799027d4c1d",
    "homepage": "http://samhuri.net/proj/strftime",
    "license": "MIT",
    "main": "./strftime.js",
    "maintainers": [
        {
            "name": "sjs",
            "email": "sami@samhuri.net"
        }
    ],
    "name": "strftime",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/samsonjs/strftime.git"
    },
    "scripts": {},
    "version": "0.10.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module strftime](#apidoc.module.strftime)
1.  [function <span class="apidocSignatureSpan">strftime.</span>localize (locale)](#apidoc.element.strftime.localize)
1.  [function <span class="apidocSignatureSpan">strftime.</span>localizeByIdentifier (localeIdentifier)](#apidoc.element.strftime.localizeByIdentifier)
1.  [function <span class="apidocSignatureSpan">strftime.</span>timezone (timezone)](#apidoc.element.strftime.timezone)
1.  [function <span class="apidocSignatureSpan">strftime.</span>utc ()](#apidoc.element.strftime.utc)



# <a name="apidoc.module.strftime"></a>[module strftime](#apidoc.module.strftime)

#### <a name="apidoc.element.strftime.localize"></a>[function <span class="apidocSignatureSpan">strftime.</span>localize (locale)](#apidoc.element.strftime.localize)
- description and source-code
```javascript
localize = function (locale) {
    return new Strftime(locale || _locale, _customTimezoneOffset, _useUtcBasedDate);
}
```
- example usage
```shell
...
            c: '%a %b %d %X %Y',
            r: '%I:%M:%S %p',
            T: '%H:%M:%S',
            v: '%e-%b-%Y',
            x: '%D'
        }
    }
    var strftimeIT = strftime.localize(it_IT)
    console.log(strftimeIT('%B %d, %Y %H:%M:%S')) // => aprile 28, 2011 18:21:08
    console.log(strftimeIT('%B %d, %Y %H:%M:%S', new Date(1307472705067))) // => giugno 7, 2011 18:51:45
'''

Some locales are bundled and can be used like so:

'''JavaScript
...
```

#### <a name="apidoc.element.strftime.localizeByIdentifier"></a>[function <span class="apidocSignatureSpan">strftime.</span>localizeByIdentifier (localeIdentifier)](#apidoc.element.strftime.localizeByIdentifier)
- description and source-code
```javascript
localizeByIdentifier = function (localeIdentifier) {
    var locale = Locales[localeIdentifier];
    if (!locale) {
        warn('[WARNING] No locale found with identifier "' + localeIdentifier + '".');
        return strftime;
    }
    return strftime.localize(locale);
}
```
- example usage
```shell
...
    console.log(strftimeIT('%B %d, %Y %H:%M:%S', new Date(1307472705067))) // => giugno 7, 2011 18:51:45
'''

Some locales are bundled and can be used like so:

'''JavaScript
    var strftime = require('strftime') // not required in browsers
    var strftimeIT = strftime.localizeByIdentifier('it_IT')
    console.log(strftimeIT('%B %d, %Y %H:%M:%S')) // => aprile 28, 2011 18:21:08
    console.log(strftimeIT('%B %d, %Y %H:%M:%S', new Date(1307472705067))) // => giugno 7, 2011 18:51:45
'''

_The [full list of bundled locales](#locales) is below._

Time zones can be passed in as an offset from GMT in minutes.
...
```

#### <a name="apidoc.element.strftime.timezone"></a>[function <span class="apidocSignatureSpan">strftime.</span>timezone (timezone)](#apidoc.element.strftime.timezone)
- description and source-code
```javascript
timezone = function (timezone) {
    var customTimezoneOffset = _customTimezoneOffset;
    var useUtcBasedDate = _useUtcBasedDate;

    var timezoneType = typeof timezone;
    if (timezoneType === 'number' || timezoneType === 'string') {
        useUtcBasedDate = true;

        // ISO 8601 format timezone string, [-+]HHMM
        if (timezoneType === 'string') {
            var sign = timezone[0] === '-' ? -1 : 1,
                hours = parseInt(timezone.slice(1, 3), 10),
                minutes = parseInt(timezone.slice(3, 5), 10);

            customTimezoneOffset = sign * ((60 * hours) + minutes) * 60 * 1000;
            // in minutes: 420
        }
        else if (timezoneType === 'number') {
            customTimezoneOffset = timezone * 60 * 1000;
        }
    }

    return new Strftime(_locale, customTimezoneOffset, useUtcBasedDate);
}
```
- example usage
```shell
...

_The [full list of bundled locales](#locales) is below._

Time zones can be passed in as an offset from GMT in minutes.

'''JavaScript
    var strftime = require('strftime') // not required in browsers
    var strftimePDT = strftime.timezone(-420)
    var strftimeCEST = strftime.timezone(120)
    console.log(strftimePDT('%B %d, %y %H:%M:%S', new Date(1307472705067))) // => June 07, 11 11:51:45
    console.log(strftimeCEST('%F %T', new Date(1307472705067))) // => 2011-06-07 20:51:45
'''

Alternatively you can use the timezone format used by ISO 8601, '+HHMM' or '-HHMM'.
...
```

#### <a name="apidoc.element.strftime.utc"></a>[function <span class="apidocSignatureSpan">strftime.</span>utc ()](#apidoc.element.strftime.utc)
- description and source-code
```javascript
utc = function () {
    return new Strftime(_locale, _customTimezoneOffset, true);
}
```
- example usage
```shell
...
var strftime = require('./strftime.js');

var start = 1478415600 * 1000; // 2016-11-06 00:00:00 -0700 (PDT)
// var start = 1477782000 * 1000; // 2016-10-30 00:00:00 +0200 (Europe/Amsterdam)
var tenMinutes = 10 * 60 * 1000;
for (var i = 0; i < 18; i++) {
    var t = start + (i * tenMinutes);
    console.log('strftime.utc()("%F %T %z", ' + t + ') = ' + strftime.utc()('%F %T %z', new Date(t)));
}

// var strftime = require('./strftime.js'), su = strftime.utc();
// var start = new Date("2016-10-30 02:30:00");
// var tenMinutes = 10 * 60 * 1000, fmt = '%F %T %z';
// for (var i = 0; i < 18; i++) {
//     var t = new Date(+start + (i * tenMinutes));
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
