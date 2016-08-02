# regex-match-all

PHP-like regex match all

## Installation

`npm install --save regex-match-all`

The UMD build is in the dist directory.

Can be used both in node and browser.

### Usage
~~~js
'use strict';

const RegEx = require('../src/RegEx.js');

let text = 'asd12 dsa asd23 dsa asd34 dsa';

console.log(JSON.stringify(
    
    RegEx.matchAll(/asd(\d)(\d)/g, text)
    
, null, 4));
console.log(JSON.stringify(RegEx.matchAll(/asd(\d)(\d)/g, text, RegEx.REGEXP_PATTERN_ORDER), null, 4));
console.log(JSON.stringify(RegEx.matchAll(/asd(\d)(\d)/g, text, RegEx.REGEXP_SET_ORDER), null, 4));
~~~