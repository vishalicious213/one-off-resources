# Grid areas

Grid areas allow different parts of a grid to be given names which can then be assigned to html elements on the grid.

- [Example image 1](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-areas-1.jpg) 
    - Shows a grid with the `grid-template-rows` and `grid-template-columns` defined
    - Below it is `grid-template-areas` with a name for each grid item on a row in quotes
- [Example image 2](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-areas-2.jpg) 
    - Shows the grid items using their `grid-template-areas` names

## Step 1: Set up grid (rows and columns)

Set up the grid using `grid-template-rows` and `grid-template-columns` or the `grid-template` shorthand.

```css
.grid {
    display: grid;
    grid-template-rows: 50px 200px;
    grid-template-columns: 200px 200px, 350px;
}
```

## Step 2. Add grid-template-areas

Add `grid-template-areas` and name/label each grid element. The names will be assigned to html elements and, if they span multiple rows or columns, have to be placed as squares or rectangles, not odd shapes like "L".

```css
.grid {
    display: grid;
    grid-template-rows: 50px 200px;
    grid-template-columns: 200px 200px, 350px;
    grid-template-areas:
        "header  header  header"
        "sidebar content content";
}
```

## Step 3. Assign grid items to grid areas

Choose a selector, give it a `grid-area` and give it the name you want.

```css
.main-content {
    grid-area: content;
}
```
If any elements in the grid container are not included in the `grid-template-areas` they will be placed at the bottom of the grid, using implicit grid rows and grid columns.

- [Codepen: grid-template-areas](https://codepen.io/vishalicious/pen/OJomGee)