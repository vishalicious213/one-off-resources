# Basic Responsive CSS Grid Layout

This is a traditional CSS grid layout. At screen sizes under 768px, it has the following layout:

![](../img/css-grid-sm-layout.jpg)

Above 768px, it looks like this:

![](../img/css-grid-lg-layout.jpg)

A live example is published [here](https://codepen.io/vishalicious/pen/MWeZxZv?editors=1100).

## Code

__HTML__

```html
<div class="wrapper">
    <div class="header">Header</div>
    <div class="sidebar">Sidebar</div>
    <div class="content">Content</div>
    <div class="footer">Footer</div>
</div>
```

__CSS__

```css
.header {
    grid-area: hd;
}
.footer {
    grid-area: ft;
}
.content {
    grid-area: main;
}
.sidebar {
    grid-area: sd;
}

.wrapper {
    display: grid;
    grid-auto-rows: minmax(100px, auto);
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr auto 1fr;
    grid-template-areas: 
      "hd hd sd"
      "main main main"
      "ft ft ft";
}

@media (min-width: 768px) {
    .wrapper {
        grid-template-columns: repeat(9, 1fr);
        grid-template-areas: 
          "sd sd hd   hd   hd   hd   hd   hd   hd"
          "sd sd main main main main main main main"
          "sd sd ft   ft   ft   ft   ft   ft   ft";
    }
}

* {box-sizing: border-box;}

.wrapper {
    border: 2px solid red;
    margin: 0 auto;
}

.wrapper > div {
    border: 1px solid orange;
    padding: 1em;
    margin: .25rem;
}

```

## Resources
* [MDN: Grid template areas](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Grid_Template_Areas)