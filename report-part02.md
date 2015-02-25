# Using SVG for web-design. Part 2

## Patterns
`use` element `<use xlink:href="#arrow" transform="translate(20 0) scale(0.5)"/>`

`defs` uses for stored hidden content.
`<defs> <!-- some elements go here --> </defs>`
Create pattern is SVG put it to `pattern` element, ant then put everything to `defs` element

```xml
<defs>
    <pattern id="Pattern01" width="10" height="10" patternUnits="userSpaceOnUse"> <!-- userSpaceOnUse | objectBoundingBox -->
        <rect width="10" height="10" fill="#FFFFFF" stroke="#000000" stroke-width="0.1"/>
    </pattern>
</defs>
<rect id="Background" x="0" y="0" width="100%" height="100%"
 fill="url(#Pattern01)" stroke-width="0.5" stroke="#000000" />
```

## Masks
```xml
<clipPath id="clip">
        <rect x="0" y="0" rx="15" ry="15" width="710" height="625" fill="none" stroke="#000" stroke-width="0"/>
    </clipPath>
```
`clipPath` doesn't support `g` and `use`
## Filters

http://codepen.io/progers/pen/eAasl

## Animation
Ways to create animation:
    * Declarative animation
    * Scripting
Declarative Animation with SVG
SMIL (Synchronized Multimedia Integration Language) by W3C
    * "smile"
    * markup not scripting
    * SMIL 3.0 since 2008

animate
    attributeName
    dur
    values
    repeatCount

animateTransform
    attributeName
    type
    from
    to
    repeatCount

animateMotion
    rotate
    repeatCount
    mpath


http://www.w3.org/TR/SMIL/smil-attributes-index.html
http://www.w3.org/TR/SMIL/smil-elements-index.html

Why not SMIL
http://caniuse.com/#feat=svg-smil




## Libraries

### JQuery SVG

### Raphaël JS ['ræfeɪəl]

### Snap.svg

### D3.js

### Pergola

## General things

### Embedding SVG to HTML
