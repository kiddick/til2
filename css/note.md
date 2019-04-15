## Specifity
```css
body {
    background-color: aqua;
}
body {
    background-color: goldenrod;
}
/* second section will be applied first -- down has priority */
.class {
    background-color: goldenrod;
}
/* .class is even more specific */
#id {
    background-color: goldenrod;
}
/* has highest specifity */

/* https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity */
/* Specificity calculator */
/* http://specificity.keegan.st/ */
```

## Width & Height

```html
<html>
    <head>
        <link rel="stylesheet" href="instructor.css">
        <link rel="stylesheet" href="index.css">
    </head>
    <body>
        <section id="inline">
            <span>inline</span>
            <a>inline</a>
            <b>inline</b>
            <em>inline</em>
        </section>
        <section id="block"> 
            <div>block</div>
            <nav>nav</nav>
            <aside>main</aside>
            <main>main</main>
        </section>
    </body>
</html>
```

W&H couldn't be applied to inline elemens. Takes as much space as needed.
Block elemet always starts from new line.

```css
#inline * {
    display: inline-block;
    width: 200px;
    height: 100px;
}
/* do not start from new line but w&h still could be applied */
```
It takes procents, pixelsm ems (relative to current font size).

## Length units
rem -- relative to default font size (doesn't inherit from current element)

## Padding

```css
padding: 25px
/* all sides */
padding: 25px 10px;
/* (above, below) *(right, left) */
padding: 5px 10px 15px 20px;
/* clock rule (top, right, bottom, left) */
/* margin have same syntax */
box-sizing
```

## Borders
```css
.box {
    background-color: lightgray;
    width: 100px;
    height: 100px;
    padding: 10px;
    box-sizing: border-box;
    border-style: solid;
    border-color: lightgreen;
    border-width: 10px;
}

border: 10px solid lightgreen;
/* compacted */
```

## Visibility
```css
.box {
    margin: 20px;
}
.hidden {
    display: none; 
    /* totally removes */
    visibility: hidden;
    opacity: .5;
}
```

## Fonts
```css
@import url('https://fonts.googleapis.com/css?family=Black+Han+Sans');
body {
    background-color: #3D85C6;
    color: rgba(0,0,0,.8);
    height: 95vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.font {
    font-family: 'Black Han Sans', arial, sans-serif;
    font-size: 30px;
    font-weight: bold;
    font-style: italic;
    font: italic bold 40px 'Black Han Sans', arial, sans-serif;
}
/* https:google.com/fonts */
```

## Course link
https://scrimba.com/g/gintrotocss