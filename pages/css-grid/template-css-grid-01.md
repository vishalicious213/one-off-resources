# CSS Grid - Single Column Layout

This simple grid has 3 rows. The 'header' and 'footer' rows take up as much space as their content needs. The 'content' row is 1fr is size. The code is a simplified version of an example from YouTube (see Resources).

![](../img/css-grid-01.jpg)

A live example is published [here](https://codepen.io/vishalicious/pen/YzGErKB?editors=1100).

## Code

__HTML__

```html
<section class='container'>
  <div class='box-1 boxes'>Header</div>
  <div class='box-2 boxes'>Content</div>
  <div class='box-3 boxes'>Footer</div>
</section>
```

__CSS__

```css
* {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
}

body {
  font-family: sans-serif;
  font-size: 2rem;
}

.container {
  display: grid;
  height: 100vh;
  grid-gap: .5rem;
  grid-template-rows: auto 1fr auto;
}

.boxes {
  display: grid;
  place-items: center;
  border: 2px solid red;
}
```

## Resources
* [Mastering CSS Grid Model in 2021🔥 - Build 5 Layouts || CSS 2021](https://www.youtube.com/watch?v=OtpDP8k-2iM)