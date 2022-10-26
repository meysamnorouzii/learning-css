# CSS Basics

## Table Of Contents

1. <a href="#add-css">Add CSS</a>
2. <a href="#color">Color</a>
3. <a href="#background">Background</a>
4. <a href="#border">Border</a>
5. <a href="#margin">Margin</a>
6. <a href="#padding">Padding</a>
7. <a href="#width">Width</a>
8. <a href="#height">Height</a>
9. <a href="#box-model">Box Model</a>
10. <a href="#outline">Outline</a>
11. <a href="#text">Text</a>
12. <a href="#fonts">Fonts</a>
13. <a href="#links">Links</a>
14. <a href="#list">List</a>
15. <a href="#display">Display</a>
16. <a href="#max-width">Max-Width</a>
17. <a href="#position">Position</a>
18. <a href="#z-index">Z-Index</a>
19. <a href="#overflow">Overflow</a>
20. <a href="#float">Float</a>
21. <a href="#css-combinators">CSS Combinators</a>
22. <a href="#pseudo-classes">Pseudo-classes</a>
23. <a href="#pseudo-elements">Pseudo-elements</a>
24. <a href="#opacity">Opacity</a>
25. <a href="#css-attribute-selector">CSS [attribute] Selector</a>
26. <a href="#counter">Counter</a>
27. <a href="#units">Units</a>
28. <a href="#css-specificity">CSS Specificity</a>
29. <a href="#math-functions">Math Functions</a>
30. <a href="#gradient">Gradient</a>
31. <a href="#box-shadow">Box Shadow</a>
32. <a href="#transforms">Transforms</a>
33. <a href="#Transitions">Transitions</a>
34. <a href="#animations">Animations</a>
35. <a href="#object-properties">Object Properties</a>
36. <a href="#masking">Masking</a>
37. <a href="#multiple-columns">Multiple Columns</a>
38. <a href="#user-interface">User Interface</a>
39. <a href="#variables">Variables</a>
40. <a href="#box-sizing">Box Sizing</a>
41. <a href="#media-query">Media Query</a>
42. <a href="#flex-box">Flex Box</a>
43. <a href="#grid">Grid</a>

# Add CSS

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Document</title>
    <!-- External CSS -->
    <link rel="stylesheet" href="./style.css" />
    <!-- Internal CSS -->
    <style>
      h1 {
        color: blue;
      }
    </style>
  </head>

  <body>
    <h1>External CSS</h1>
    <!-- Inline CSS -->
    <h2 style="color: red">Inline CSS</h2>
  </body>
</html>
```

# Color

<code>
color: color|initial|inherit;
</code>

```css
h1 {
  color: tomato;
  /* color rgb(red, green, blue)*/
  color: rgb(255, 99, 71);
  /* color rgba(red, green, blue, alpha) */
  /* The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (not transparent at all): */
  color: rgb(255, 99, 71, 0);
  color: rgb(255, 99, 71, 0.5);
  color: rgb(255, 99, 71, 1);
  /* color hex #rrggbb #rgb */
  color: #ff6347;
  color: #f64;
  /* color hsl(hue, saturation, lightness) */
  color: hsl(0, 100%, 50%);
  /* color hsla(hue, saturation, lightness, alpha) */
  color: hsl(0, 100%, 50%, 0.5);
}
```

# Background

<code>
    background-color: color|transparent|initial|inherit;
</code>

```css
div {
  background-color: red;
  background-color: #bbff00;
  background-color: rgb(255, 255, 128);
  background-color: hsl(50, 33%, 25%);
  background-color: currentColor;
  background-color: transparent;
}
```

<code>
  background-image: url|none|initial|inherit;
</code>

```css
div {
  background-image: url("paper.gif");

  background-image: url(image1.png), url(image2.png), url(image3.png),
    url(image4.png);
  background-image: linear-gradient(to bottom, red, blue), url("catfront.png");
}
```

<code>
    background-repeat: repeat|repeat-x|repeat-y|no-repeat|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  background-repeat: repeat-x;
  background-repeat: repeat-y;
  background-repeat: repeat;
  background-repeat: space;
  background-repeat: round;
  background-repeat: no-repeat;

  /* Two-value syntax: horizontal | vertical */
  background-repeat: repeat space;
  background-repeat: repeat repeat;
  background-repeat: round space;
  background-repeat: no-repeat round;
}
```

<code>
    background-size: auto|length|cover|contain|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  background-size: cover;
  background-size: contain;

  /* One-value syntax */
  /* the width of the image (height becomes 'auto') */
  background-size: 50%;
  background-size: 3.2em;
  background-size: 12px;
  background-size: auto;

  /* Two-value syntax */
  /* first value: width of the image, second value: height */
  background-size: 50% auto;
  background-size: 3em 25%;
  background-size: auto 6px;
  background-size: auto auto;

  /* Multiple backgrounds */
  background-size: auto, auto; /* Not to be confused with `auto auto` */
  background-size: 50%, 25%, 25%;
  background-size: 6px, auto, contain;
}
```

<code>
   background-position: value;
</code>

```css
div {
  /* Keyword values */
  background-position: top;
  background-position: bottom;
  background-position: left;
  background-position: right;
  background-position: center;

  /* <percentage> values */
  background-position: 25% 75%;

  /* <length> values */
  background-position: 0 0;
  background-position: 1cm 2cm;
  background-position: 10ch 8em;

  /* Multiple images */
  background-position: 0 0, center;

  /* Edge offsets values */
  background-position: bottom 10px right 20px;
  background-position: right 3em bottom 10px;
  background-position: bottom 10px right;
  background-position: top right 10px;
}
```

<code>
   background-attachment: scroll|fixed|local|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  background-attachment: scroll;
  background-attachment: fixed;
  background-attachment: local;
}
```

<code>
   background-clip: border-box|padding-box|content-box|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  background-clip: border-box;
  background-clip: padding-box;
  background-clip: content-box;
  background-clip: text;
}
```

<code>
   background-origin: padding-box|border-box|content-box|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  background-origin: border-box;
  background-origin: padding-box;
  background-origin: content-box;
}
```

<code>
   background-blend-mode: normal|multiply|screen|overlay|darken|lighten|color-dodge|saturation|color|luminosity;
</code>

```css
div {
  /* Keyword values */
  background-blend-mode: multiply;
}
```

<code>
   background: bg-color bg-image position/bg-size bg-repeat bg-origin bg-clip bg-attachment initial|inherit;
</code>

```css
div {
  background-color: #ffffff;
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
  /* shortland */
  background: #ffffff url("img_tree.png") no-repeat right top;
}
```

# Border

<code>
border: border-width border-style border-color|initial|inherit;
</code>

```css
div {
  border: 5px solid red;
}
```

<code>
border-width: medium|thin|thick|length|initial|inherit;
</code>

```css
div {
  border-width: 1px;
  border-width: medium;
  border-width: thick;
  border-width: 25px 10px 4px 35px; /* 25px top, 10px right, 4px bottom and 35px left */

  border-top-width: 1px;
  border-right-width: 10px;
  border-bottom-width: 7px;
  border-left-width: 3px;
}
```

<code>
border-style: none|hidden|dotted|dashed|solid|double|groove|ridge|inset|outset|initial|inherit;
</code>

```css
div {
  border-style: dotted;
  border-style: dashed;
  border-style: solid;
  border-style: double;
  border-style: groove;
  border-style: ridge;
  border-style: inset;
  border-style: outset;
  border-style: none;
  border-style: hidden;

  border-top-style: dotted;
  border-right-style: solid;
  border-bottom-style: dotted;
  border-left-style: solid;
}
```

<code>
border-color: color|transparent|initial|inherit;
</code>

```css
div {
  border-color: royalblue;
  border-color: red green blue yellow; /* red top, green right, blue bottom and yellow left */

  border-top-color: red;
  border-right-color: blue;
  border-bottom-color: yellow;
  border-left-color: red;
}
```

<code>
border-radius: 1-4 length|% / 1-4 length|%|initial|inherit;
</code>

```css
div {
  border-radius: 4px;

  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
  border-bottom-left-radius: 5px;
  border-top-left-radius: 5px;
}
```

<code>
border-collapse: separate|collapse|initial|inherit;
</code>

```css
table {
  border-collapse: separate;
  border-collapse: collapse;
}
```

<code>
border-spacing: length|initial|inherit;
</code>

```css
table {
  border-spacing: 15px;
  border-spacing: 15px 50px;
}
```

<code>
border-image: source slice width outset repeat|initial|inherit;
</code>

```css
#borderimg {
  border-image: url(border.png) 30 round;
}
```

<code>
border-image-source: none|image|initial|inherit;

border-image-slice: number|%|fill|initial|inherit;

border-image-width: number|%|auto|initial|inherit;

border-image-outset: length|number|initial|inherit;

border-image-repeat: stretch|repeat|round|space|initial|inherit;
</code>

```css
#borderimg {
  border-image-source: url(border.png);
  border-image-slice: 30%;
  border-image-width: 10px;
  border-image-outset: 10px;
  border-image-repeat: repeat;
}
```

# Margin

<code>
margin: length|auto|initial|inherit;
</code>

```css
div {
  margin: 100px;
  margin: auto;
  /* 
    top and bottom margins are 25px
    right and left margins are 50px
 */
  margin: 25px 50px;
  /* 
    top margin is 25px
    right and left margins are 50px
    bottom margin is 75px 
  */
  margin: 25px 50px 75px;
  /* 
    top margin is 25px
    right margin is 50px
    bottom margin is 75px
    left margin is 100px
  */
  margin: 20px 0 0 0;

  margin-top: 100px;
  margin-bottom: 100px;
  margin-right: 150px;
  margin-left: 80px;
}
```

# Padding

<code>
padding: length|initial|inherit;
</code>

```css
div {
  padding: 25px;
  /* 
        top and bottom paddings are 25px
        right and left paddings are 50px
    */
  padding: 25px 50px;
  /* 
        top padding is 25px
        right and left paddings are 50px
        bottom padding is 75px
    */
  padding: 25px 50px 75px;
  /* 
        top padding is 25px
        right padding is 50px
        bottom padding is 75px
        left padding is 100px
    */
  padding: 25px 50px 75px 100px;

  padding-top: 50px;
  padding-right: 30px;
  padding-bottom: 50px;
  padding-left: 80px;
}
```

# Width

<code>
width: auto|value|initial|inherit;
</code>

```css
div {
  /* <length> values */
  width: 300px;
  width: 25em;

  /* <percentage> value */
  width: 75%;

  /* Keyword values */
  width: max-content;
  width: min-content;
  width: fit-content(20em);
  width: auto;
}
```

# height

<code>
height: auto|length|initial|inherit;
</code>

```css
div {
  /* <length> values */
  height: 120px;
  height: 10em;
  height: 100vh;

  /* <percentage> value */
  height: 75%;

  /* Keyword values */
  height: max-content;
  height: min-content;
  height: fit-content(20em);
  height: auto;
}
```

# Box Model

<img src="../box-model.png" alt="box model" />

# Outline

<code>
outline: outline-width outline-style outline-color|initial|inherit;
</code>

```css
div {
  outline: 1px solid red;
}
```

<code>
outline-width: medium|thin|thick|length|initial|inherit;
</code>

```css
div {
  outline-width: thick;
}
```

<code>
outline-style: none|hidden|dotted|dashed|solid|double|groove|ridge|inset|outset|initial|inherit;
</code>

```css
div {
  outline-style: dotted;
}
```

<code>
outline-color: invert|color|initial|inherit;
</code>

```css
div {
  outline-color: coral;
}
```

<code>
outline-offset: length|initial|inherit;
</code>

```css
div {
  outline: 4px solid red;
  outline-offset: 15px;
}
```

# Text

## Text Alignment

<code>
text-align: left|right|center|justify|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  text-align: start;
  text-align: end;
  text-align: left;
  text-align: right;
  text-align: center;
  text-align: justify;
  text-align: justify-all;
  text-align: match-parent;

  /* Character-based alignment in a table column */
  text-align: ".";
  text-align: "." center;

  /* Block alignment values (Non-standard syntax) */
  text-align: -moz-center;
  text-align: -webkit-center;
}
```

<code>
text-align-last: auto|left|right|center|justify|start|end|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  text-align-last: auto;
  text-align-last: start;
  text-align-last: end;
  text-align-last: left;
  text-align-last: right;
  text-align-last: center;
  text-align-last: justify;
}
```

<code>
direction: ltr|rtl|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  direction: ltr;
  direction: rtl;
}
```

<code>
unicode-bidi: normal|embed|bidi-override|initial|inherit;
</code>

```css
div {
  direction: rtl;
  /* Keyword values */
  unicode-bidi: normal;
  unicode-bidi: embed;
  unicode-bidi: isolate;
  unicode-bidi: bidi-override;
  unicode-bidi: isolate-override;
  unicode-bidi: plaintext;
}
```

<code>
vertical-align: baseline|length|sub|super|top|text-top|middle|bottom|text-bottom|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  vertical-align: baseline;
  vertical-align: sub;
  vertical-align: super;
  vertical-align: text-top;
  vertical-align: text-bottom;
  vertical-align: middle;
  vertical-align: top;
  vertical-align: bottom;

  /* <length> values */
  vertical-align: 10em;
  vertical-align: 4px;

  /* <percentage> values */
  vertical-align: 20%;
}
```

## Text Decoration

<code>
text-decoration-line: none|underline|overline|line-through|initial|inherit;
</code>

```css
div {
  /* Single keyword */
  text-decoration-line: none;
  text-decoration-line: underline;
  text-decoration-line: overline;
  text-decoration-line: line-through;
  text-decoration-line: blink;

  /* Multiple keywords */
  text-decoration-line: underline overline; /* Two decoration lines */
  text-decoration-line: overline underline line-through; /* Multiple decoration lines */
}
```

<code>
text-decoration-color: color|initial|inherit;
</code>

```css
div {
  /* <color> values */
  text-decoration-color: currentcolor;
  text-decoration-color: red;
  text-decoration-color: #00ff00;
  text-decoration-color: rgba(255, 128, 128, 0.5);
  text-decoration-color: transparent;
}
```

<code>
text-decoration-style: solid|double|dotted|dashed|wavy|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  text-decoration-style: solid;
  text-decoration-style: double;
  text-decoration-style: dotted;
  text-decoration-style: dashed;
  text-decoration-style: wavy;
}
```

<code>
text-decoration-thickness: auto|from-font|length/percentage|initial|inherit;
</code>

```css
div {
  /* Single keyword */
  text-decoration-thickness: auto;
  text-decoration-thickness: from-font;

  /* length */
  text-decoration-thickness: 0.1em;
  text-decoration-thickness: 3px;

  /* percentage */
  text-decoration-thickness: 10%;
}
```

<code>
text-decoration: text-decoration-line text-decoration-color text-decoration-style text-decoration-thickness|initial|inherit;
</code>

```css
div {
  text-decoration: underline overline dotted red;
}
```

## Text Transformation

<code>
text-transform: none|capitalize|uppercase|lowercase|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  text-transform: none;
  text-transform: capitalize;
  text-transform: uppercase;
  text-transform: lowercase;
  text-transform: full-width;
  text-transform: full-size-kana;
}
```

## Text Spacing

<code>
text-indent: length|initial|inherit;
</code>

```css
div {
  /* <length> values */
  text-indent: 3mm;
  text-indent: 40px;

  /* <percentage> value
   relative to the containing block width */
  text-indent: 15%;

  /* Keyword values */
  text-indent: 5em each-line;
  text-indent: 5em hanging;
  text-indent: 5em hanging each-line;
}
```

<code>
letter-spacing: normal|length|initial|inherit;
</code>

```css
div {
  /* Keyword value */
  letter-spacing: normal;

  /* <length> values */
  letter-spacing: 0.3em;
  letter-spacing: 3px;
  letter-spacing: 0.3px;
}
```

<code>
line-height: normal|number|length|initial|inherit;
</code>

```css
div {
  /* Keyword value */
  line-height: normal;

  /* Unitless values: use this number multiplied
by the element's font size */
  line-height: 3.5;

  /* <length> values */
  line-height: 3em;

  /* <percentage> values */
  line-height: 34%;
}
```

<code>
word-spacing: normal|length|initial|inherit;
</code>

```css
div {
  /* Keyword value */
  word-spacing: normal;

  /* <length> values */
  word-spacing: 3px;
  word-spacing: 0.3em;

  /* <percentage> values */
  word-spacing: 50%;
  word-spacing: 200%;
}
```

<code>
white-space: normal|nowrap|pre|pre-line|pre-wrap|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  white-space: normal;
  white-space: nowrap;
  white-space: pre;
  white-space: pre-wrap;
  white-space: pre-line;
  white-space: break-spaces;
}
```

## Text Shadow

<code>
text-shadow: h-shadow v-shadow blur-radius color|none|initial|inherit;
</code>

```css
div {
  /* offset-x | offset-y | blur-radius | color */
  text-shadow: 1px 1px 2px black;

  /* color | offset-x | offset-y | blur-radius */
  text-shadow: #fc0 1px 0 10px;

  /* offset-x | offset-y | color */
  text-shadow: 5px 5px #558abb;

  /* color | offset-x | offset-y */
  text-shadow: white 2px 5px;

  /* offset-x | offset-y
/* Use defaults for color and blur-radius */
  text-shadow: 5px 10px;
}
```

## Text Effects

<code>
text-overflow: clip|ellipsis|string|initial|inherit;
</code>

```css
p {
  text-overflow: clip;
  text-overflow: ellipsis ellipsis;
  text-overflow: ellipsis " [..]";
}
```

<code>
word-wrap: normal|break-word|initial|inherit;
</code>

```css
p {
  word-wrap: break-word;
}
```

<code>
word-break: normal|break-all|keep-all|break-word|initial|inherit;
</code>

```css
p {
  /* Keyword values */
  word-break: normal;
  word-break: break-all;
  word-break: keep-all;
  word-break: break-word; /* deprecated */
}
```

<code>
writing-mode: horizontal-tb|vertical-rl|vertical-lr;
</code>

```css
p {
  /* Keyword values */
  writing-mode: horizontal-tb;
  writing-mode: vertical-rl;
  writing-mode: vertical-lr;
}
```

# Fonts

<code>
font-family: family-name|generic-family|initial|inherit;
</code>

```css
div {
  /* A font family name and a generic family name */
  font-family: "Gill Sans Extrabold", sans-serif;
  font-family: "Goudy Bookletter 1911", sans-serif;

  /* A generic family name only */
  font-family: serif;
  font-family: sans-serif;
  font-family: monospace;
  font-family: cursive;
  font-family: fantasy;
  font-family: system-ui;
  font-family: ui-serif;
  font-family: ui-sans-serif;
  font-family: ui-monospace;
  font-family: ui-rounded;
  font-family: emoji;
  font-family: math;
  font-family: fangsong;
}
```

<code>
font-style: normal|italic|oblique|initial|inherit;
</code>

```css
div {
  font-style: normal;
  font-style: italic;
  font-style: oblique;
  font-style: oblique 10deg;
}
```

<code>
font-weight: normal|bold|bolder|lighter|number|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  font-weight: normal;
  font-weight: bold;

  /* Keyword values relative to the parent */
  font-weight: lighter;
  font-weight: bolder;

  /* Numeric keyword values */
  font-weight: 100;
  font-weight: 200;
  font-weight: 300;
  font-weight: 400; /* normal */
  font-weight: 500;
  font-weight: 600;
  font-weight: 700; /* bold */
  font-weight: 800;
  font-weight: 900;
}
```

<code>
font-variant: normal|small-caps|initial|inherit;
</code>

```css
div {
  font-variant: small-caps;
  font-variant: common-ligatures small-caps;
}
```

<code>
font-size:medium|xx-small|x-small|small|large|x-large|xx-large|smaller|larger|length|initial|inherit;
</code>

pixels/16=em

1vw = 1% of viewport width.

```css
div {
  /* <absolute-size> values */
  font-size: xx-small;
  font-size: x-small;
  font-size: small;
  font-size: medium;
  font-size: large;
  font-size: x-large;
  font-size: xx-large;
  font-size: xxx-large;

  /* <relative-size> values */
  font-size: smaller;
  font-size: larger;

  /* <length> values */
  font-size: 12px;
  font-size: 0.8em;

  /* <percentage> values */
  font-size: 80%;

  /* math value */
  font-size: math;
}
```

<code>
font: font-style font-variant font-weight font-size/line-height font-family|caption|icon|menu|message-box|small-caption|status-bar|initial|inherit;
</code>

```css
div {
  font: italic small-caps bold 12px/30px Georgia, serif;
}
```

## Web Fonts

    @font-face {
       font-properties
    }

```css
@font-face {
  font-family: "Open Sans";
  src: url("/fonts/OpenSans-Regular-webfont.woff2") format("woff2"), url("/fonts/OpenSans-Regular-webfont.woff")
      format("woff");
  font-weight: bold;
}
```

# Links

```css
/* unvisited link */
a:link {
  color: red;
}

/* visited link */
a:visited {
  color: green;
}

/* mouse over link */
a:hover {
  color: hotpink;
}

/* selected link */
a:active {
  color: blue;
}
```

<code>
cursor: value;
</code>

```css
a {
  /* Keyword value */
  cursor: auto;
  cursor: crosshair;
  cursor: default;
  cursor: e-resize;
  cursor: help;
  cursor: move;
  cursor: n-resize;
  cursor: ne-resize;
  cursor: nw-resize;
  cursor: pointer;
  cursor: progress;
  cursor: s-resize;
  cursor: se-resize;
  cursor: sw-resize;
  cursor: text;
  cursor: w-resize;
  cursor: wait;
  /* … */
  cursor: zoom-out;

  /* URL with mandatory keyword fallback */
  cursor: url(hand.cur), pointer;

  /* URL and coordinates, with mandatory keyword fallback */
  cursor: url(cursor_1.png) 4 12, auto;
  cursor: url(cursor_2.png) 2 2, pointer;

  /* URLs and fallback URLs (some with coordinates), with mandatory keyword fallback */
  cursor: url(cursor_1.svg) 4 5, url(cursor_2.svg), /* … ,*/ url(cursor_n.cur) 5
      5, progress;
}
```

# List

<code>
list-style-type: value;
</code>

```css
ul {
  /* Partial list of types */
  list-style-type: disc;
  list-style-type: circle;
  list-style-type: square;
  list-style-type: decimal;
  list-style-type: georgian;
  list-style-type: trad-chinese-informal;
  list-style-type: kannada;

  /* <string> value */
  list-style-type: "-";

  /* Identifier matching an @counter-style rule */
  list-style-type: custom-counter-style;

  /* Keyword value */
  list-style-type: none;
}
```

<code>
list-style-image: none|url|initial|inherit;
</code>

```css
ul {
  /* Keyword values */
  list-style-image: none;

  /* <url> values */
  list-style-image: url("starsolid.gif");

  /* valid image values */
  list-style-image: linear-gradient(to left bottom, red, blue);
}
```

<code>
list-style-position: inside|outside|initial|inherit;
</code>

```css
ul {
  /* Keyword values */
  list-style-position: inside;
  list-style-position: outside;
}
```

<code>
list-style: list-style-type list-style-position list-style-image|initial|inherit;
</code>

```css
ul {
  /* type */
  list-style: square;

  /* image */
  list-style: url("../img/shape.png");

  /* position */
  list-style: inside;

  /* type | position */
  list-style: georgian inside;

  /* type | image | position */
  list-style: lower-roman url("../img/shape.png") outside;

  /* Keyword value */
  list-style: none;

  list-style: square inside url("sqpurple.gif");
}
```

# Display

<code>
display: value;
</code>

```css
.box {
  /* precomposed values */
  display: block;
  display: inline;
  display: inline-block;
  display: flex;
  display: inline-flex;
  display: grid;
  display: inline-grid;
  display: flow-root;

  /* box generation */
  display: none;
  display: contents;

  /* two-value syntax */
  display: block flow;
  display: inline flow;
  display: inline flow-root;
  display: block flex;
  display: inline flex;
  display: block grid;
  display: inline grid;
  display: block flow-root;

  /* other values */
  display: table;
  display: table-row; /* all table elements have an equivalent CSS display value */
  display: list-item;
}
```

<code>
visibility: visible|hidden|collapse|initial|inherit;
</code>

```css
.box {
  /* Keyword values */
  visibility: visible;
  visibility: hidden;
  visibility: collapse;
}
```

# Max-Width

<code>
max-width: none|length|initial|inherit;
</code>

```css
div {
  /* <length> value */
  max-width: 3.5em;

  /* <percentage> value */
  max-width: 75%;

  /* Keyword values */
  max-width: none;
  max-width: max-content;
  max-width: min-content;
  max-width: fit-content(20em);
}
```

# Position

<code>
position: static|absolute|fixed|relative|sticky|initial|inherit;
</code>

```css
div {
  position: static;
  position: relative;
  position: absolute;
  position: fixed;
  position: sticky;
}
```

# Z-Index

<code>
z-index: auto|number|initial|inherit;
</code>

```css
div {
  /* Keyword value */
  z-index: auto;

  /* <integer> values */
  z-index: 0;
  z-index: 3;
  z-index: 289;
  z-index: -1; /* Negative values to lower the priority */
}
```

# Overflow

<code>
overflow: visible|hidden|clip|scroll|auto|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  overflow: visible;
  overflow: hidden;
  overflow: clip;
  overflow: scroll;
  overflow: auto;
  overflow: hidden visible;
}
```

<code>
overflow: visible|hidden|clip|scroll|auto|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  overflow: visible;
  overflow: hidden;
  overflow: clip;
  overflow: scroll;
  overflow: auto;
  overflow: hidden visible;
}
```

<code>
overflow-x: visible|hidden|scroll|auto|initial|inherit;

overflow-y: visible|hidden|scroll|auto|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  overflow-x: visible;
  overflow-x: hidden;
  overflow-x: clip;
  overflow-x: scroll;
  overflow-x: auto;
  overflow-x: hidden visible;
  /* Keyword values */
  overflow-y: visible;
  overflow-y: hidden;
  overflow-y: clip;
  overflow-y: scroll;
  overflow-y: auto;
  overflow-y: hidden visible;
}
```

<code>
overflow-wrap: normal|anywhere|break-word|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  overflow-wrap: normal;
  overflow-wrap: break-word;
  overflow-wrap: anywhere;
}
```

# Float

<code>
float: none|left|right|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  float: left;
  float: right;
  float: none;
  float: inline-start;
  float: inline-end;
}
```

<code>
clear: none|left|right|both|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  clear: none;
  clear: left;
  clear: right;
  clear: both;
  clear: inline-start;
  clear: inline-end;
}
```

# CSS Combinators

```css
/* Descendant Selector */
div p {
  background-color: yellow;
}

/* Child Selector (>) */
div > p {
  background-color: yellow;
}

/* Adjacent Sibling Selector (+) */
div + p {
  background-color: yellow;
}

/* General Sibling Selector (~) */
div ~ p {
  background-color: yellow;
}
```

# Pseudo-classes

    selector:pseudo-class {
      property: value;
    }

### Link

```css
a:active {
  background-color: yellow;
}

a:hover {
  background-color: yellow;
}

a:link {
  background-color: yellow;
}

a:visited {
  color: pink;
}

:target {
  border: 2px solid #d4d4d4;
  background-color: #e5eecc;
}
```

### Input

```css
input:checked {
  height: 50px;
  width: 50px;
}

input[type="text"]:disabled {
  background: #dddddd;
}

input[type="text"]:enabled {
  background: #ffff00;
}
input:focus {
  background-color: yellow;
}

input:in-range {
  border: 2px solid yellow;
}

input:invalid {
  border: 2px solid red;
}
input:valid {
  background-color: yellow;
}
input:optional {
  background-color: yellow;
}

input:out-of-range {
  border: 2px solid red;
}

input:read-only {
  background-color: yellow;
}

input:read-write {
  background-color: yellow;
}

input:required {
  background-color: yellow;
}
```

### Element

```css
p:empty {
  background: #ff0000;
}

p:first-child {
  background-color: yellow;
}

p:first-of-type {
  background: red;
}

p:lang(it) {
  background: yellow;
}

p:last-child {
  background: #ff0000;
}

p:last-of-type {
  background: #ff0000;
}

/* :not Selector */
:not(p) {
  background: #ff0000;
}

/*  */
/* Selects the second element of div siblings */
div:nth-child(2) {
  background: red;
}

/* Selects the second li element in a list */
li:nth-child(2) {
  background: lightgreen;
}

/* Selects every third element among any group of siblings */
:nth-child(3) {
  background: yellow;
}

p:nth-last-child(2) {
  background: red;
}

p:nth-last-of-type(2) {
  background: red;
}

/*  */
/* Selects the second element of div siblings */
div:nth-of-type(2) {
  background: red;
}

/* Selects the second li element in a list */
li:nth-of-type(2) {
  background: lightgreen;
}

/* Selects every third element among any group of siblings */
:nth-of-type(3) {
  background: yellow;
}

p:only-of-type {
  background: #ff0000;
}

p:only-child {
  background: #ff0000;
}
```

### Root

```css
:root {
  background: #ff0000;
}
```

# Pseudo-elements

    selector::pseudo-element {
      property: value;
    }

```css
p::after {
  content: " - Remember this";
}

p::before {
  content: "Read this: ";
}
p::first-letter {
  font-size: 200%;
  color: #8a2be2;
}

p::first-line {
  background-color: yellow;
}

::marker {
  color: red;
}

::selection {
  color: red;
  background: yellow;
}
```

# Opacity

<code>
  opacity: number|initial|inherit;
</code>

```css
div {
  opacity: 0.9;
  opacity: 90%;
}
```

# CSS [attribute] Selector

```css
/* [attribute="value"] */
a[target="_blank"] {
  background-color: yellow;
}

/* [attribute~="value"] like : "summer flower" or "flower" but not "summer-flower" */
[title~="flower"] {
  border: 5px solid yellow;
}

/* [attribute|="value"] like : "top" or "top-text" */
[class|="top"] {
  background: yellow;
}

/* [attribute^="value"]  starts with "top" */
[class^="top"] {
  background: yellow;
}

/* [attribute$="value"]  ends with "test" */
[class$="test"] {
  background: yellow;
}

/* [attribute*="value"]  contains "te" */
[class*="te"] {
  background: yellow;
}
```

# Counter

<code>
content: normal|none|counter|attr|string|open-quote|close-quote|no-open-quote|no-close-quote|url|initial|inherit;
</code>

```css
/* Keywords that cannot be combined with other values */
content: normal;
content: none;

/* <image> values */
content: url("http://www.example.com/test.png");
content: linear-gradient(#e66465, #9198e5);
content: image-set("image1x.png" 1x, "image2x.png" 2x);

/* alt text for generated content, added in the Level 3 specification */
content: url("http://www.example.com/test.png") / "This is the alt text";

/* <string> value */
content: "prefix";

/* <counter> values, optionally with <list-style-type> */
content: counter(chapter_counter);
content: counter(chapter_counter, upper-roman);
content: counters(section_counter, ".");
content: counters(section_counter, ".", decimal-leading-zero);

/* attr() value linked to the HTML attribute value */
content: attr(value string);

/* Language- and position-dependent keywords */
content: open-quote;
content: close-quote;
content: no-open-quote;
content: no-close-quote;

/* Except for normal and none, several values can be used simultaneously */
content: open-quote counter(chapter_counter);
```

<code>
counter-reset: none|name number|initial|inherit;
</code>

```css
/* Set "my-counter" to 0 */
counter-reset: my-counter;

/* Set "my-counter" to -3 */
counter-reset: my-counter -3;

/* Set reversed "my-counter" to "the number of peer elements" */
counter-reset: reversed(my-counter);

/* Set reversed "my-counter" to -1 */
counter-reset: reversed(my-counter) -1;

/* Set counter2 to 9 and reversed "counter1" and "counter3" to 1 and 4, respectively*/
counter-reset: reversed(counter1) 1 counter2 9 reversed(counter3) 4;

/* Cancel any reset that could have been set in less specific rules */
counter-reset: none;
```

<code>
counter-increment: none|id|initial|inherit;
</code>

```css
/* Increment "my-counter" by 1 */
counter-increment: my-counter;

/* Decrement "my-counter" by 1 */
counter-increment: my-counter -1;

/* Increment "counter1" by 1, and decrement "counter2" by 4 */
counter-increment: counter1 counter2 -4;

/* Do not increment/decrement anything: used to override less specific rules */
counter-increment: none;
```

```css
body {
  /* Set "my-sec-counter" to 0 */
  counter-reset: my-sec-counter;
}

h2::before {
  /* Increment "my-sec-counter" by 1 */
  counter-increment: my-sec-counter;
  content: "Section " counter(my-sec-counter) ". ";
}
```

# Units

1- Absolute Lengths

<ul>
  <li>cm - centimeters</li>
  <li>mm - millimeters</li>
  <li>in - inches (1in = 96px = 2.54cm)</li>
  <li>px - pixels (1px = 1/96th of 1in)</li>
  <li>pt - points (1pt = 1/72 of 1in)</li>
  <li>pc - picas (1pc = 12 pt)</li>
</ul>
2- Relative Lengths
<ul>
  <li>em - Relative to the font-size of the element (2em means 2 times the size of the current font)</li>
  <li>ex - Relative to the x-height of the current font (rarely used)</li>
  <li>ch - Relative to width of the "0" (zero)</li>
  <li>rem - Relative to font-size of the root element</li>
  <li>vw - Relative to 1% of the width of the viewport*</li>
  <li>vh - Relative to 1% of the height of the viewport*</li>
  <li>vmin - Relative to 1% of viewport's* smaller dimension</li>
  <li>vmax - Relative to 1% of viewport's* larger dimension</li>
  <li>% - Relative to the parent element</li>
</ul>

# CSS Specificity

    There are four categories which define the specificity level of     a selector:

    Inline styles - Example: <h1 style="color: pink;">
    IDs - Example: #navbar
    Classes, pseudo-classes, attribute selectors - Example: .test,    :hover, [href]
    Elements and pseudo-elements - Example: h1, :before

# Math Functions

<code>
The following operators can be used: + - * /
</code>

```css
div {
  /* calc(expression) */
  width: calc(100% - 100px);

  /* max(value1, value2, ...) */
  width: max(50%, 300px);

  /* min(value1, value2, ...) */
  width: min(50%, 100px);
}
```

# Gradient

<code>
background-image: linear-gradient(direction, color-stop1, color-stop2, ...);

background-image: linear-gradient(angle, color-stop1, color-stop2);
</code>

```css
#exm {
  /* A gradient tilted 45 degrees,
   starting blue and finishing red */
  background-image: linear-gradient(45deg, blue, red);

  /* A gradient going from the bottom right to the top left corner,
   starting blue and finishing red */
  background-image: linear-gradient(to left top, blue, red);

  /* Color stop: A gradient going from the bottom to top,
   starting blue, turning green at 40% of its length,
   and finishing red */
  background-image: linear-gradient(0deg, blue, green 40%, red);

  /* Color hint: A gradient going from the left to right,
   starting red, getting to the midpoint color
   10% of the way across the length of the gradient,
   taking the rest of the 90% of the length to change to blue */
  background-image: linear-gradient(0.25turn, red, 10%, blue);

  /* Multi-position color stop: A gradient tilted 45 degrees,
   with a red bottom-left half and a blue top-right half,
   with a hard line where the gradient changes from red to blue */
  background-image: linear-gradient(45deg, red 0 50%, blue 50% 100%);

  background-image: repeating-linear-gradient(red, yellow 10%, green 20%);
}
```

<code>

background-image: radial-gradient(shape size at position, start-color, ..., last-color);

</code>

```css
#exm {
  /* A gradient at the center of its container,
   starting red, changing to blue, and finishing green */
  background-image: radial-gradient(circle at center, red 0, blue, green 100%);

  background-image: radial-gradient(red, yellow, green);
  background-image: radial-gradient(red 5%, yellow 15%, green 60%);
  background-image: radial-gradient(circle, red, yellow, green);
  /* closest-side farthest-side closest-corner farthest-corner */
  background-image: radial-gradient(
    closest-side at 60% 55%,
    red,
    yellow,
    black
  );
  background-image: repeating-radial-gradient(red, yellow 10%, green 15%);
}
```

<code>

background-image: conic-gradient([from angle] [at position,] color [degree], color [degree], ...);
</code>

```css
#exm {
  /* A conic gradient rotated 45 degrees,
   starting blue and finishing red */
  background-image: conic-gradient(from 45deg, blue, red);

  /* A bluish purple box: the gradient goes from blue to red,
   but only the bottom right quadrant is visible, as the
   center of the conic gradient is at the top left corner */
  background-image: conic-gradient(from 90deg at 0 0, blue, red);

  /* Color wheel */
  background-image: conic-gradient(
    hsl(360, 100%, 50%),
    hsl(315, 100%, 50%),
    hsl(270, 100%, 50%),
    hsl(225, 100%, 50%),
    hsl(180, 100%, 50%),
    hsl(135, 100%, 50%),
    hsl(90, 100%, 50%),
    hsl(45, 100%, 50%),
    hsl(0, 100%, 50%)
  );

  /* Conic Gradient */
  background-image: conic-gradient(red, yellow, green);
  background-image: conic-gradient(red 45deg, yellow 90deg, green 210deg);
  background-image: conic-gradient(from 90deg, red, yellow, green);
  background-image: conic-gradient(at 60% 45%, red, yellow, green);
  background-image: repeating-conic-gradient(red 10%, yellow 20%);
}
```

# Box Shadow

<code>
box-shadow: none|h-offset v-offset blur spread color |inset|initial|inherit;
</code>

```css
#example1 {
  /* Keyword values */
  box-shadow: none;

  /* offset-x | offset-y | color */
  box-shadow: 60px -16px teal;

  /* offset-x | offset-y | blur-radius | color */
  box-shadow: 10px 5px 5px black;

  /* offset-x | offset-y | blur-radius | spread-radius | color */
  box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2);

  /* inset | offset-x | offset-y | color */
  box-shadow: inset 5em 1em gold;

  /* Any number of shadows, separated by commas */
  box-shadow: 3px 3px red, -1em 0 0.4em olive;
}
```

# Transforms

<code>
transform: none|transform-functions|initial|inherit;
</code>

```css
.box {
  /* Keyword values */
  transform: none;

  /* Function values */
  transform: matrix(1, 2, 3, 4, 5, 6);
  transform: matrix3d(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1);
  transform: perspective(17px);
  transform: rotate(0.5turn);
  transform: rotate3d(1, 2, 3, 10deg);
  transform: rotateX(10deg);
  transform: rotateY(10deg);
  transform: rotateZ(10deg);
  transform: translate(12px, 50%);
  transform: translate3d(12px, 50%, 3em);
  transform: translateX(2em);
  transform: translateY(3in);
  transform: translateZ(2px);
  transform: scale(2, 0.5);
  transform: scale3d(2.5, 1.2, 0.3);
  transform: scaleX(2);
  transform: scaleY(0.5);
  transform: scaleZ(0.3);
  transform: skew(30deg, 20deg);
  transform: skewX(30deg);
  transform: skewY(1.07rad);

  /* Multiple function values */
  transform: translateX(10px) rotate(10deg) translateY(5px);
  transform: perspective(500px) translate(10px, 0, 20px) rotateY(3deg);
}
```

<code>
transform-origin: x-axis y-axis z-axis|initial|inherit;
</code>

```css
.box {
  /* One-value syntax */
  transform-origin: 2px;
  transform-origin: bottom;

  /* x-offset | y-offset */
  transform-origin: 3cm 2px;

  /* x-offset-keyword | y-offset */
  transform-origin: left 2px;

  /* x-offset-keyword | y-offset-keyword */
  transform-origin: right top;

  /* y-offset-keyword | x-offset-keyword */
  transform-origin: top right;

  /* x-offset | y-offset | z-offset */
  transform-origin: 2px 30% 10px;

  /* x-offset-keyword | y-offset | z-offset */
  transform-origin: left 5px -3px;

  /* x-offset-keyword | y-offset-keyword | z-offset */
  transform-origin: right bottom 2cm;

  /* y-offset-keyword | x-offset-keyword | z-offset */
  transform-origin: bottom right 2cm;
}
```

<code>
transform-style: flat|preserve-3d|initial|inherit;
</code>

```css
.box {
  /* Keyword values */
  transform-style: flat;
  transform-style: preserve-3d;
}
```

<code>
perspective: length|none;
</code>

```css
.box {
  /* Keyword value */
  perspective: none;

  /* <length> values */
  perspective: 20px;
  perspective: 3.5em;
}
```

<code>
perspective-origin: x-axis y-axis|initial|inherit;
</code>

```css
.box {
  /* One-value syntax */
  perspective-origin: x-position;

  /* Two-value syntax */
  perspective-origin: x-position y-position;

  /* When both x-position and y-position are keywords,
   the following is also valid */
  perspective-origin: y-position x-position;
}
```

<code>
backface-visibility: visible|hidden|initial|inherit;
</code>

```css
.box {
  /* Keyword values */
  backface-visibility: visible;
  backface-visibility: hidden;
}
```

# Transitions

<code>
transition: property duration timing-function delay|initial|inherit;
</code>

```css
.box {
  /* Apply to 1 property */
  /* property name | duration */
  transition: margin-right 4s;

  /* property name | duration | delay */
  transition: margin-right 4s 1s;

  /* property name | duration | easing function */
  transition: margin-right 4s ease-in-out;

  /* property name | duration | easing function | delay */
  transition: margin-right 4s ease-in-out 1s;

  /* Apply to 2 properties */
  transition: margin-right 4s, color 1s;

  /* Apply to all changed properties */
  transition: all 0.5s ease-out;
}
```

<code>
transition-property: none|all|property|initial|inherit;
</code>

```css
.box {
  /* Keyword values */
  transition-property: none;
  transition-property: all;

  /* <custom-ident> values */
  transition-property: test_05;
  transition-property: -specific;
  transition-property: sliding-vertically;

  /* Multiple values */
  transition-property: test1, animation4;
  transition-property: all, height, color;
  transition-property: all, -moz-specific, sliding;
}
```

<code>
transition-duration: time|initial|inherit;
</code>

```css
.box {
  /* <time> values */
  transition-duration: 6s;
  transition-duration: 120ms;
  transition-duration: 1s, 15s;
  transition-duration: 10s, 30s, 230ms;
}
```

<code>
transition-timing-function: linear|ease|ease-in|ease-out|ease-in-out|step-start|step-end|steps(int,start|end)|cubic-bezier(n,n,n,n)|initial|inherit;
</code>

```css
.box {
  /* Keyword values */
  transition-timing-function: ease;
  transition-timing-function: ease-in;
  transition-timing-function: ease-out;
  transition-timing-function: ease-in-out;
  transition-timing-function: linear;
  transition-timing-function: step-start;
  transition-timing-function: step-end;

  /* Function values */
  transition-timing-function: steps(4, jump-end);
  transition-timing-function: cubic-bezier(0.1, 0.7, 1, 0.1);

  /* Steps Function keywords */
  transition-timing-function: steps(4, jump-start);
  transition-timing-function: steps(10, jump-end);
  transition-timing-function: steps(20, jump-none);
  transition-timing-function: steps(5, jump-both);
  transition-timing-function: steps(6, start);
  transition-timing-function: steps(8, end);

  /* Multiple timing functions */
  transition-timing-function: ease, step-start, cubic-bezier(0.1, 0.7, 1, 0.1);
}
```

<code>
transition-delay: time|initial|inherit;
</code>

```css
.box {
  /* <time> values */
  transition-delay: 3s;
  transition-delay: 2s, 4ms;
}
```

### Transition + Transformation

```css
.box {
  transition: width 2s, height 2s, transform 2s;
}

.box:hover {
  transform: rotate(180deg);
}
```

# Animations

<code>
@keyframes animationname {keyframes-selector {css-styles;}}
</code>

```css
@keyframes slidein {
  from {
    transform: translateX(0%);
  }

  to {
    transform: translateX(100%);
  }
}
```

<code>
animation: name duration timing-function delay iteration-count direction fill-mode play-state;
</code>

```css
.box {
  animation: mymove 5s infinite;

  /* @keyframes duration | easing-function | delay |
iteration-count | direction | fill-mode | play-state | name */
  animation: 3s ease-in 1s 2 reverse both paused slidein;

  /* @keyframes duration | easing-function | delay | name */
  animation: 3s linear 1s slidein;

  /* two animations */
  animation: 3s linear slidein, 3s ease-out 5s slideout;
}
```

<code>
animation-duration: time|initial|inherit;
</code>

```css
.box {
  /* Single animation */
  animation-duration: 6s;
  animation-duration: 120ms;

  /* Multiple animations */
  animation-duration: 1.64s, 15.22s;
  animation-duration: 10s, 35s, 230ms;
}
```

<code>
animation-timing-function: linear|ease|ease-in|ease-out|ease-in-out|step-start|step-end|steps(int,start|end)|cubic-bezier(n,n,n,n)|initial|inherit;
</code>

```css
.box {
  /* Keyword values */
  animation-timing-function: ease;
  animation-timing-function: ease-in;
  animation-timing-function: ease-out;
  animation-timing-function: ease-in-out;
  animation-timing-function: linear;
  animation-timing-function: step-start;
  animation-timing-function: step-end;

  /* Function values */
  animation-timing-function: cubic-bezier(0.1, 0.7, 1, 0.1);
  animation-timing-function: steps(4, end);

  /* Steps Function keywords */
  animation-timing-function: steps(4, jump-start);
  animation-timing-function: steps(10, jump-end);
  animation-timing-function: steps(20, jump-none);
  animation-timing-function: steps(5, jump-both);
  animation-timing-function: steps(6, start);
  animation-timing-function: steps(8, end);

  /* Multiple animations */
  animation-timing-function: ease, step-start, cubic-bezier(0.1, 0.7, 1, 0.1);
}
```

<code>
animation-delay: time|initial|inherit;
</code>

```css
.box {
  /* Single animation */
  animation-delay: 3s;
  animation-delay: 0s;
  animation-delay: -1500ms;

  /* Multiple animations */
  animation-delay: 2.1s, 480ms;
}
```

<code>
animation-iteration-count: number|infinite|initial|inherit;
</code>

```css
.box {
  /* Keyword value */
  animation-iteration-count: infinite;

  /* <number> values */
  animation-iteration-count: 3;
  animation-iteration-count: 2.4;

  /* Multiple values */
  animation-iteration-count: 2, 0, infinite;
}
```

<code>
animation-direction: normal|reverse|alternate|alternate-reverse|initial|inherit;
</code>

```css
.box {
  /* Single animation */
  animation-direction: normal;
  animation-direction: reverse;
  animation-direction: alternate;
  animation-direction: alternate-reverse;

  /* Multiple animations */
  animation-direction: normal, reverse;
  animation-direction: alternate, reverse, normal;
}
```

<code>
animation-fill-mode: none|forwards|backwards|both|initial|inherit;
</code>

```css
.box {
  /* Single animation */
  animation-fill-mode: none;
  animation-fill-mode: forwards;
  animation-fill-mode: backwards;
  animation-fill-mode: both;

  /* Multiple animations */
  animation-fill-mode: none, backwards;
  animation-fill-mode: both, forwards, none;
}
```

<code>
animation-play-state: paused|running|initial|inherit;
</code>

```css
.box {
  /* Single animation */
  animation-play-state: running;
  animation-play-state: paused;

  /* Multiple animations */
  animation-play-state: paused, running, running;
}
```

# Object Properties

<code>
object-fit: fill|contain|cover|scale-down|none|initial|inherit;
</code>

```css
.box {
  object-fit: contain;
  object-fit: cover;
  object-fit: fill;
  object-fit: none;
  object-fit: scale-down;
}
```

<code>
object-position: position|initial|inherit;
</code>

```css
.box {
  /* Keyword values */
  object-position: top;
  object-position: bottom;
  object-position: left;
  object-position: right;
  object-position: center;

  /* <percentage> values */
  object-position: 25% 75%;

  /* <length> values */
  object-position: 0 0;
  object-position: 1cm 2cm;
  object-position: 10ch 8em;

  /* Edge offsets values */
  object-position: bottom 10px right 20px;
  object-position: right 3em bottom 10px;
  object-position: top 0 right 10px;
}
```

# Masking

<code>
mask-image: none|image|url|initial|inherit;
</code>

```css
.box {
  /* Keyword value */
  mask-image: none;

  /* <mask-source> value */
  mask-image: url(masks.svg#mask1);

  /* <image> values */
  mask-image: linear-gradient(rgba(0, 0, 0, 1), transparent);
  mask-image: image(url(mask.png), skyblue);

  /* Multiple values */
  mask-image: image(url(mask.png), skyblue), linear-gradient(rgba(0, 0, 0, 1), transparent);
}
```

<code>
mask-repeat: repeat|repeat-x|repeat-y|space|round|no-repeat|initial|inherit;
</code>

```css
.box {
  /* One-value syntax */
  mask-repeat: repeat-x;
  mask-repeat: repeat-y;
  mask-repeat: repeat;
  mask-repeat: space;
  mask-repeat: round;
  mask-repeat: no-repeat;

  /* Two-value syntax: horizontal | vertical */
  mask-repeat: repeat space;
  mask-repeat: repeat repeat;
  mask-repeat: round space;
  mask-repeat: no-repeat round;

  /* Multiple values */
  mask-repeat: space round, no-repeat;
  mask-repeat: round repeat, space, repeat-x;
}
```

<code>
mask-mode: match-source|luminance|alpha|initial|inherit;
</code>

```css
.box {
  /* Keyword values */
  mask-mode: alpha;
  mask-mode: luminance;
  mask-mode: match-source;

  /* Multiple values */
  mask-mode: alpha, match-source;
}
```

<code>
mask-origin: border-box|content-box|padding-box|margin-box|fill-box|stroke-box|view-box|initial|inherit;
</code>

```css
.box {
  /* Keyword values */
  mask-origin: content-box;
  mask-origin: padding-box;
  mask-origin: border-box;
  mask-origin: margin-box;
  mask-origin: fill-box;
  mask-origin: stroke-box;
  mask-origin: view-box;

  /* Multiple values */
  mask-origin: padding-box, content-box;
  mask-origin: view-box, fill-box, border-box;

  /* Non-standard keyword values */
  -webkit-mask-origin: content;
  -webkit-mask-origin: padding;
  -webkit-mask-origin: border;
}
```

<code>
mask-position: value;
</code>

```css
.box {
  /* Keyword values */
  mask-position: top;
  mask-position: bottom;
  mask-position: left;
  mask-position: right;
  mask-position: center;

  /* <position> values */
  mask-position: 25% 75%;
  mask-position: 0px 0px;
  mask-position: 10% 8em;

  /* Multiple values */
  mask-position: top right;
  mask-position: 1rem 1rem, center;
}
```

<code>
mask-size: value;
</code>

```css
.box {
  /* Keywords syntax */
  mask-size: cover;
  mask-size: contain;

  /* One-value syntax */
  /* the width of the image (height set to 'auto') */
  mask-size: 50%;
  mask-size: 3em;
  mask-size: 12px;
  mask-size: auto;

  /* Two-value syntax */
  /* first value: width of the image, second value: height */
  mask-size: 50% auto;
  mask-size: 3em 25%;
  mask-size: auto 6px;
  mask-size: auto auto;

  /* Multiple values */
  /* Do not confuse this with mask-size: auto auto */
  mask-size: auto, auto;
  mask-size: 50%, 25%, 25%;
  mask-size: 6px, auto, contain;
}
```

# Multiple Columns

<code>
columns: auto|column-width column-count|initial|inherit;
</code>

```css
div {
  /* Column width */
  columns: 18em;

  /* Column count */
  columns: auto;
  columns: 2;

  /* Both column width and count */
  columns: 2 auto;
  columns: auto 12em;
  columns: auto auto;
}
```

<code>
column-count: number|auto|initial|inherit;
</code>

```css
div {
  /* Keyword value */
  column-count: auto;

  /* <integer> value */
  column-count: 3;
}
```

<code>
column-fill: balance|auto|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  column-fill: auto;
  column-fill: balance;
  column-fill: balance-all;
}
```

<code>
column-gap: length|normal|initial|inherit;
</code>

```css
div {
  /* Keyword value */
  column-gap: normal;

  /* <length> values */
  column-gap: 3px;
  column-gap: 2.5em;

  /* <percentage> value */
  column-gap: 3%;
}
```

<code>
column-rule: column-rule-width column-rule-style column-rule-color|initial|inherit;
</code>

```css
div {
  column-rule: dotted;
  column-rule: solid 8px;
  column-rule: solid blue;
  column-rule: thick inset blue;
}
```

<code>
column-rule-color: color|initial|inherit;
</code>

```css
div {
  /* <color> values */
  column-rule-color: red;
  column-rule-color: rgb(192, 56, 78);
  column-rule-color: transparent;
  column-rule-color: hsla(0, 100%, 50%, 0.6);
}
```

<code>
column-rule-style: none|hidden|dotted|dashed|solid|double|groove|ridge|inset|outset|initial|inherit;
</code>

```css
div {
  /* <'border-style'> values */
  column-rule-style: none;
  column-rule-style: hidden;
  column-rule-style: dotted;
  column-rule-style: dashed;
  column-rule-style: solid;
  column-rule-style: double;
  column-rule-style: groove;
  column-rule-style: ridge;
  column-rule-style: inset;
  column-rule-style: outset;
}
```

<code>
column-rule-width: medium|thin|thick|length|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  column-rule-width: thin;
  column-rule-width: medium;
  column-rule-width: thick;

  /* <length> values */
  column-rule-width: 1px;
  column-rule-width: 2.5em;
}
```

<code>
column-span: none|all|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  column-span: none;
  column-span: all;
}
```

<code>
column-width: auto|length|initial|inherit;
</code>

```css
div {
  /* Keyword value */
  column-width: auto;

  /* <length> values */
  column-width: 60px;
  column-width: 15.5em;
  column-width: 3.3vw;
}
```

# User Interface

<code>
resize: none|both|horizontal|vertical|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  resize: none;
  resize: both;
  resize: horizontal;
  resize: vertical;
  resize: block;
  resize: inline;
}
```

# Variables

<code>
var(--name, value)
</code>

```css
:root {
  --blue: #1e90ff;
  --white: #ffffff;
}

body {
  background-color: var(--blue);
}
```

# Box Sizing

<code>
box-sizing: content-box|border-box|initial|inherit;
</code>

```css
div {
  box-sizing: border-box;
  box-sizing: content-box;
}
* {
  box-sizing: border-box;
}
```

# Media Query

    @media not|only mediatype and (expressions) {
      CSS-Code;
    }

```html
<head>
  <link
    rel="stylesheet"
    media="screen and (min-width: 900px)"
    href="widescreen.css"
  />
  <link
    rel="stylesheet"
    media="screen and (max-width: 600px)"
    href="smallscreen.css"
  />
</head>
```

```css
@media screen and (min-width: 480px) {
  body {
    background-color: lightgreen;
  }
}

@media only screen and (orientation: landscape) {
  body {
    background-color: lightblue;
  }
}

@media screen {
  body {
    color: green;
  }
}

@media print {
  body {
    color: black;
  }
}

/* When the width is between 600px and 900px OR above 1100px - change the appearance of <div> */
@media screen and (max-width: 900px) and (min-width: 600px),
  (min-width: 1100px) {
  div.example {
    font-size: 50px;
    padding: 50px;
    border: 8px solid black;
    background: yellow;
  }
}
```

# Flex Box

## Flex Container

<code>
flex-direction: row|row-reverse|column|column-reverse|initial|inherit;
</code>

```css
div {
  /* The direction text is laid out in a line */
  flex-direction: row;

  /* Like <row>, but reversed */
  flex-direction: row-reverse;

  /* The direction in which lines of text are stacked */
  flex-direction: column;

  /* Like <column>, but reversed */
  flex-direction: column-reverse;
}
```

<code>
flex-wrap: nowrap|wrap|wrap-reverse|initial|inherit;
</code>

```css
div {
  flex-wrap: nowrap; /* Default value */
  flex-wrap: wrap;
  flex-wrap: wrap-reverse;
}
```

<code>
flex-flow: flex-direction flex-wrap|initial|inherit;
</code>

```css
div {
  /* flex-flow: <'flex-direction'> */
  flex-flow: row;
  flex-flow: row-reverse;
  flex-flow: column;
  flex-flow: column-reverse;

  /* flex-flow: <'flex-wrap'> */
  flex-flow: nowrap;
  flex-flow: wrap;
  flex-flow: wrap-reverse;

  /* flex-flow: <'flex-direction'> and <'flex-wrap'> */
  flex-flow: row nowrap;
  flex-flow: column wrap;
  flex-flow: column-reverse wrap-reverse;
}
```

<code>
justify-content: flex-start|flex-end|center|space-between|space-around|space-evenly|initial|inherit;
</code>

```css
div {
  /* Positional alignment */
  justify-content: center; /* Pack items around the center */
  justify-content: start; /* Pack items from the start */
  justify-content: end; /* Pack items from the end */
  justify-content: flex-start; /* Pack flex items from the start */
  justify-content: flex-end; /* Pack flex items from the end */
  justify-content: left; /* Pack items from the left */
  justify-content: right; /* Pack items from the right */

  /* Baseline alignment */
  /* justify-content does not take baseline values */

  /* Normal alignment */
  justify-content: normal;

  /* Distributed alignment */
  justify-content: space-between;
  justify-content: space-around;
  justify-content: space-evenly;
  justify-content: stretch;

  /* Overflow alignment */
  justify-content: safe center;
  justify-content: unsafe center;
}
```

<code>
align-items: stretch|center|flex-start|flex-end|baseline|initial|inherit;
</code>

```css
div {
  /* Basic keywords */
  align-items: normal;
  align-items: stretch;

  /* Positional alignment */
  /* align-items does not take left and right values */
  align-items: center; /* Pack items around the center */
  align-items: start; /* Pack items from the start */
  align-items: end; /* Pack items from the end */
  align-items: flex-start; /* Pack flex items from the start */
  align-items: flex-end; /* Pack flex items from the end */

  /* Baseline alignment */
  align-items: baseline;
  align-items: first baseline;
  align-items: last baseline; /* Overflow alignment (for positional alignment only) */
  align-items: safe center;
  align-items: unsafe center;
}
```

<code>
align-content: stretch|center|flex-start|flex-end|space-between|space-around|space-evenly|initial|inherit;
</code>

```css
div {
  /* Basic positional alignment */
  /* align-content does not take left and right values */
  align-content: center; /* Pack items around the center */
  align-content: start; /* Pack items from the start */
  align-content: end; /* Pack items from the end */
  align-content: flex-start; /* Pack flex items from the start */
  align-content: flex-end; /* Pack flex items from the end */

  /* Normal alignment */
  align-content: normal;

  /* Baseline alignment */
  align-content: baseline;
  align-content: first baseline;
  align-content: last baseline;

  /* Distributed alignment */
  align-content: space-between;
  align-content: space-around;
  align-content: space-evenly;
  align-content: stretch;

  /* Overflow alignment */
  align-content: safe center;
  align-content: unsafe center;
}
```

## Flex Items

<code>
order: number|initial|inherit;
</code>

```css
div {
  /* <integer> values */
  order: 5;
  order: -5;
}
```

<code>
flex-grow: number|initial|inherit;
</code>

```css
div {
  /* <number> values */
  flex-grow: 3;
  flex-grow: 0.6;
}
```

<code>
flex-shrink: number|initial|inherit;
</code>

```css
div {
  /* <number> values */
  flex-shrink: 2;
  flex-shrink: 0.6;
}
```

<code>
flex-basis: number|auto|initial|inherit;
</code>

```css
div {
  /* Specify <'width'> */
  flex-basis: 10em;
  flex-basis: 3px;
  flex-basis: 50%;
  flex-basis: auto;

  /* Intrinsic sizing keywords */
  flex-basis: max-content;
  flex-basis: min-content;
  flex-basis: fit-content;

  /* Automatically size based on the flex item's content */
  flex-basis: content;
}
```

<code>
flex: flex-grow flex-shrink flex-basis|auto|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  flex: auto;
  flex: initial;
  flex: none;

  /* One value, unitless number: flex-grow
flex-basis is then equal to 0. */
  flex: 2;

  /* One value, width/height: flex-basis */
  flex: 10em;
  flex: 30%;
  flex: min-content;

  /* Two values: flex-grow | flex-basis */
  flex: 1 30px;

  /* Two values: flex-grow | flex-shrink */
  flex: 2 2;

  /* Three values: flex-grow | flex-shrink | flex-basis */
  flex: 2 2 10%;
}
```

<code>
align-self: auto|stretch|center|flex-start|flex-end|baseline|initial|inherit;
</code>

```css
div {
  /* Keyword values */
  align-self: auto;
  align-self: normal;

  /* Positional alignment */
  /* align-self does not take left and right values */
  align-self: center; /* Put the item around the center */
  align-self: start; /* Put the item at the start */
  align-self: end; /* Put the item at the end */
  align-self: self-start; /* Align the item flush at the start */
  align-self: self-end; /* Align the item flush at the end */
  align-self: flex-start; /* Put the flex item at the start */
  align-self: flex-end; /* Put the flex item at the end */

  /* Baseline alignment */
  align-self: baseline;
  align-self: first baseline;
  align-self: last baseline;
  align-self: stretch; /* Stretch 'auto'-sized items to fit the container */

  /* Overflow alignment */
  align-self: safe center;
  align-self: unsafe center;
}
```

# Grid

<code>
row-gap: length|normal|initial|inherit;

column-gap: length|normal|initial|inherit;
</code>

```css
div {
  /* <length> values */
  row-gap: 20px;
  row-gap: 1em;
  row-gap: 3vmin;
  row-gap: 0.5cm;

  /* <percentage> value */
  row-gap: 10%;
}
```

<code>
gap: row-gap column-gap;
</code>

```css
div {
  /* One <length> value */
  gap: 20px;
  gap: 1em;
  gap: 3vmin;
  gap: 0.5cm;

  /* One <percentage> value */
  gap: 16%;
  gap: 100%;

  /* Two <length> values */
  gap: 20px 10px;
  gap: 1em 0.5em;
  gap: 3vmin 2vmax;
  gap: 0.5cm 2mm;

  /* One or two <percentage> values */
  gap: 16% 100%;
  gap: 21px 82%;

  /* calc() values */
  gap: calc(10% + 20px);
  gap: calc(20px + 10%) calc(10% - 5px);
}
```

<code>
grid-column-gap: length;

grid-row-gap: length;

grid-gap: grid-row-gap grid-column-gap;
</code>

```css
div {
  grid-row-gap: 50px;
  grid-column-gap: 50px;
  grid-gap: 50px;
}
```

<code>
grid-column-start: auto|span n|column-line;
</code>

```css
div {
  /* Keyword value */
  grid-column-start: auto;

  /* <custom-ident> value */
  grid-column-start: somegridarea;

  /* <integer> + <custom-ident> values */
  grid-column-start: 2;
  grid-column-start: somegridarea 4;

  /* span + <integer> + <custom-ident> values */
  grid-column-start: span 3;
  grid-column-start: span somegridarea;
  grid-column-start: span somegridarea 5;
}
```

<code>
grid-column-end: auto|span n|column-line;
</code>

```css
div {
  /* Keyword value */
  grid-column-end: auto;

  /* <custom-ident> values */
  grid-column-end: somegridarea;

  /* <integer> + <custom-ident> values */
  grid-column-end: 2;
  grid-column-end: somegridarea 4;

  /* span + <integer> + <custom-ident> values */
  grid-column-end: span 3;
  grid-column-end: span somegridarea;
  grid-column-end: 5 somegridarea span;
}
```

<code>
grid-row-end: auto|row-line|span n;
</code>

```css
div {
  /* Keyword value */
  grid-row-end: auto;

  /* <custom-ident> values */
  grid-row-end: somegridarea;

  /* <integer> + <custom-ident> values */
  grid-row-end: 2;
  grid-row-end: somegridarea 4;

  /* span + <integer> + <custom-ident> values */
  grid-row-end: span 3;
  grid-row-end: span somegridarea;
  grid-row-end: 5 somegridarea span;
}
```

<code>
grid-row-start: auto|row-line;
</code>

```css
div {
  /* Keyword value */
  grid-row-start: auto;

  /* <custom-ident> values */
  grid-row-start: somegridarea;

  /* <integer> + <custom-ident> values */
  grid-row-start: 2;
  grid-row-start: somegridarea 4;

  /* span + <integer> + <custom-ident> values */
  grid-row-start: span 3;
  grid-row-start: span somegridarea;
  grid-row-start: 5 somegridarea span;
}
```

<code>
grid-template-columns: none|auto|max-content|min-content|length|initial|inherit;
</code>

```css
div {
  /* Keyword value */
  grid-template-columns: none;

  /* <track-list> values */
  grid-template-columns: 100px 1fr;
  grid-template-columns: [linename] 100px;
  grid-template-columns: [linename1] 100px [linename2 linename3];
  grid-template-columns: minmax(100px, 1fr);
  grid-template-columns: fit-content(40%);
  grid-template-columns: repeat(3, 200px);
  grid-template-columns: subgrid;
  grid-template-columns: masonry;

  /* <auto-track-list> values */
  grid-template-columns: 200px repeat(auto-fill, 100px) 300px;
  grid-template-columns:
    minmax(100px, max-content)
    repeat(auto-fill, 200px) 20%;
  grid-template-columns:
    [linename1] 100px [linename2]
    repeat(auto-fit, [linename3 linename4] 300px)
    100px;
  grid-template-columns:
    [linename1 linename2] 100px
    repeat(auto-fit, [linename1] 300px) [linename3];
}
```

<code>
grid-template-rows: none|auto|max-content|min-content|length|initial|inherit;
</code>

```css
div {
  /* Keyword value */
  grid-template-rows: none;

  /* <track-list> values */
  grid-template-rows: 100px 1fr;
  grid-template-rows: [linename] 100px;
  grid-template-rows: [linename1] 100px [linename2 linename3];
  grid-template-rows: minmax(100px, 1fr);
  grid-template-rows: fit-content(40%);
  grid-template-rows: repeat(3, 200px);
  grid-template-rows: subgrid;
  grid-template-rows: masonry;

  /* <auto-track-list> values */
  grid-template-rows: 200px repeat(auto-fill, 100px) 300px;
  grid-template-rows:
    minmax(100px, max-content)
    repeat(auto-fill, 200px) 20%;
  grid-template-rows:
    [linename1] 100px [linename2]
    repeat(auto-fit, [linename3 linename4] 300px)
    100px;
  grid-template-rows:
    [linename1 linename2] 100px
    repeat(auto-fit, [linename1] 300px) [linename3];
}
```

<code>
  grid-column: grid-column-start / grid-column-end;
</code>

```css
div {
  grid-column: auto;

  /* with line numbers */
  grid-column: 1;
  grid-column: 1 / 3;
  grid-column: 1 / span 2;

  /* with line names */
  grid-column: main-start;
  grid-column: main-start / main-end;
}
```

<code>
  grid-row: grid-row-start / grid-row-end;
</code>

```css
div {
  /* Keyword values */
  grid-row: auto;
  grid-row: auto / auto;

  /* <custom-ident> values */
  grid-row: somegridarea;
  grid-row: somegridarea / someothergridarea;

  /* <integer> + <custom-ident> values */
  grid-row: somegridarea 4;
  grid-row: 4 somegridarea / 6;

  /* span + <integer> + <custom-ident> values */
  grid-row: span 3;
  grid-row: span somegridarea;
  grid-row: 5 somegridarea span;
  grid-row: span 3 / 6;
  grid-row: span somegridarea / span someothergridarea;
  grid-row: 5 somegridarea span / 2 span;
}
```

<code>
 grid-area: grid-row-start / grid-column-start / grid-row-end / grid-column-end | itemname;
</code>

```css
div {
  /* Keyword values */
  grid-area: auto;
  grid-area: auto / auto;
  grid-area: auto / auto / auto;
  grid-area: auto / auto / auto / auto;

  /* <custom-ident> values */
  grid-area: some-grid-area;
  grid-area: some-grid-area / another-grid-area;

  /* <integer> && <custom-ident>? values */
  grid-area: 4 some-grid-area;
  grid-area: 4 some-grid-area / 2 another-grid-area;

  /* span && [ <integer> || <custom-ident> ] values */
  grid-area: span 3;
  grid-area: span 3 / span some-grid-area;
  grid-area: 2 span / another-grid-area span;
}
```

<code>
grid-template-areas: none|itemnames;
</code>

```css
div {
  /* Keyword value */
  grid-template-areas: none;

  /* <string> values */
  grid-template-areas: "a b";
  grid-template-areas:
    "a b b"
    "a c d";
}
```

<code>
 grid-auto-columns: auto|max-content|min-content|length;
</code>

```css
div {
  /* Keyword values */
  grid-auto-columns: min-content;
  grid-auto-columns: max-content;
  grid-auto-columns: auto;

  /* <length> values */
  grid-auto-columns: 100px;
  grid-auto-columns: 20cm;
  grid-auto-columns: 50vmax;

  /* <percentage> values */
  grid-auto-columns: 10%;
  grid-auto-columns: 33.3%;

  /* <flex> values */
  grid-auto-columns: 0.5fr;
  grid-auto-columns: 3fr;

  /* minmax() values */
  grid-auto-columns: minmax(100px, auto);
  grid-auto-columns: minmax(max-content, 2fr);
  grid-auto-columns: minmax(20%, 80vmax);

  /* fit-content() values */
  grid-auto-columns: fit-content(400px);
  grid-auto-columns: fit-content(5cm);
  grid-auto-columns: fit-content(20%);

  /* multiple track-size values */
  grid-auto-columns: min-content max-content auto;
  grid-auto-columns: 100px 150px 390px;
  grid-auto-columns: 10% 33.3%;
  grid-auto-columns: 0.5fr 3fr 1fr;
  grid-auto-columns: minmax(100px, auto) minmax(max-content, 2fr) minmax(20%, 80vmax);
  grid-auto-columns: 100px minmax(100px, auto) 10% 0.5fr fit-content(400px);
}
```

<code>
grid-auto-flow: row|column|dense|row dense|column dense;
</code>

```css
div {
  /* Keyword values */
  grid-auto-flow: row;
  grid-auto-flow: column;
  grid-auto-flow: dense;
  grid-auto-flow: row dense;
  grid-auto-flow: column dense;
}
```

<code>
grid-auto-rows: auto|max-content|min-content|length;
</code>

```css
div {
  /* Keyword values */
  grid-auto-rows: min-content;
  grid-auto-rows: max-content;
  grid-auto-rows: auto;

  /* <length> values */
  grid-auto-rows: 100px;
  grid-auto-rows: 20cm;
  grid-auto-rows: 50vmax;

  /* <percentage> values */
  grid-auto-rows: 10%;
  grid-auto-rows: 33.3%;

  /* <flex> values */
  grid-auto-rows: 0.5fr;
  grid-auto-rows: 3fr;

  /* minmax() values */
  grid-auto-rows: minmax(100px, auto);
  grid-auto-rows: minmax(max-content, 2fr);
  grid-auto-rows: minmax(20%, 80vmax);

  /* fit-content() values */
  grid-auto-rows: fit-content(400px);
  grid-auto-rows: fit-content(5cm);
  grid-auto-rows: fit-content(20%);

  /* multiple track-size values */
  grid-auto-rows: min-content max-content auto;
  grid-auto-rows: 100px 150px 390px;
  grid-auto-rows: 10% 33.3%;
  grid-auto-rows: 0.5fr 3fr 1fr;
  grid-auto-rows: minmax(100px, auto) minmax(max-content, 2fr) minmax(20%, 80vmax);
  grid-auto-rows: 100px minmax(100px, auto) 10% 0.5fr fit-content(400px);
}
```

<code>
 grid: none|grid-template-rows / grid-template-columns|grid-template-areas|grid-template-rows / [grid-auto-flow] grid-auto-columns|[grid-auto-flow] grid-auto-rows / grid-template-columns|initial|inherit;
</code>

```css
div {
  /* <'grid-template'> values */
  grid: none;
  grid: "a" 100px "b" 1fr;
  grid: [linename1] "a" 100px [linename2];
  grid: "a" 200px "b" min-content;
  grid: "a" minmax(100px, max-content) "b" 20%;
  grid: 100px / 200px;
  grid: minmax(400px, min-content) / repeat(auto-fill, 50px);

  /* <'grid-template-rows'> /
   [ auto-flow && dense? ] <'grid-auto-columns'>? values */
  grid: 200px / auto-flow;
  grid: 30% / auto-flow dense;
  grid: repeat(3, [line1 line2 line3] 200px) / auto-flow 300px;
  grid: [line1] minmax(20em, max-content) / auto-flow dense 40%;

  /* [ auto-flow && dense? ] <'grid-auto-rows'>? /
   <'grid-template-columns'> values */
  grid: auto-flow / 200px;
  grid: auto-flow dense / 30%;
  grid: auto-flow 300px / repeat(3, [line1 line2 line3] 200px);
  grid: auto-flow dense 40% / [line1] minmax(20em, max-content);
}
```
