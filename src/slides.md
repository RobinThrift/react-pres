title: React to the Flux
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

## What?

--

## React.js and Flux

--

## What is React?

[fragment]
#### "A JAVASCRIPT LIBRARY FOR BUILDING USER INTERFACES"
[/fragment]

-- {
    background:
        img: 'img/react_logo.png'
        size: 100px
        position: 5% 10%
}

- Declarative
- One-Way
- Immutable
- Virtual Dom Diffing

-- 

## One Step at a time...

--

## React is Declarative
[fragment]
#### Everything is a component
[/fragment]

[fragment]
##### No Templates!
[/fragment]
--

### What do they look like?

[fragment]
```js
React.createClass({
    render: function() {
        return (
            <div>Hello World, at {new Date().toString()}</div>
        );
    }
});
```
[/fragment]

[fragment]
```js
React.createClass({
    render: function() {
        return React.createElement("div", null, 
            "Hello World, at " + (new Date().toString()));
    }
});
```
##### boring...
[/fragment]

--

### Also...

- Mixins
- No jumping between files
- Simpler
- Easier to maintain

--

### Why?

- Reusable
- Encapsulated
- Single-Concern-Pattern

[fragment]
- Testable
[/fragment]


--

## Immutability

--

- `render()` is called on every update
- no "bindings"

--

## Virtual Dom Diffing

-- {
    transition: fade
}

![](img/dom_simple.png)

-- {
    transition: fade
}

![](img/dom_marked.png)


-- {
    transition: fade
}

![](img/dom_removed.png)

--

![](img/dom_diff.png)

--

![](img/dom_marked.png)
