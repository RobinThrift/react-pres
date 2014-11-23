title: [PRES TITLE]
author: Robin Thrift
twitter: RobinThrift
homepage: RobinThrift.com
shortcodes: true
css:
    - 'http://fonts.googleapis.com/css?family=Open+Sans:300italic,300,700|Ubuntu:400,700|Source+Code+Pro'
reveal:
    controls: true
    progress: true
    slideNumber: true
    history: true
    keyboard: true
    overview: true
    transition: 'linear'
    backgroundTransition: 'slide'

-- {
    background: 
        img: '#cb5243'
}

#[var title]

<div class="author-info">
    <h5>[var author]</h5>
    <a href="http://twitter.com/[var twitter]">@[var twitter]</a>
    <a href="http://[var homepage]">[var homepage]</a>
</div>

--

- this
- is
- a
- list

--

## Another Title

-- 

## A Title with some stuff
- a list
- for example

--

```js
var Metalsmith  = require('metalsmith'),
    markdown    = require('metalsmith-markdown'),
    shortcodes  = require('metalsmith-flexible-shortcodes');

Metalsmith(__dirname)
    .use(ignore([
        '_*', '.*',
        '**/_*', '**/.*'
    ]))    
    .use(slides.split())
    .use(markdown({
        gfm: true,
        tables: true,
        smartLists: true,
        smartypants: true,
    }));
```

-- 

```scss
// COLOURS
$body-bg: #fcfcfc;
$body-bg-accent: #f5f5f5;

$main: #cb5243;
$main-light: #d98275;
$main-contrast: #f5f4f2;

$main-font: #0e0e0e;

$divider: #c0c0c0;
```
