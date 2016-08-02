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

/*
[
    [
        "asd12",
        "asd23",
        "asd34"
    ],
    [
        "1",
        "2"
    ],
    [
        "2",
        "3"
    ],
    [
        "3",
        "4"
    ]
]
*/

console.log(JSON.stringify(
    
    RegEx.matchAll(/asd(\d)(\d)/g, text, RegEx.REGEXP_PATTERN_ORDER)
    
, null, 4));

/*
    Same as above
*/

console.log(
    
    JSON.stringify(RegEx.matchAll(/asd(\d)(\d)/g, text, RegEx.REGEXP_SET_ORDER)
    
, null, 4));

/*
[
    [
        "asd12",
        "1",
        "2"
    ],
    [
        "asd23",
        "2",
        "3"
    ],
    [
        "asd34",
        "3",
        "4"
    ]
]
*/
~~~