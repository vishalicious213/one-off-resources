# Formatting CSS Grid

## auto

In general, don't set a height when defining rows. Let the height dynamically adjust to match the content with the `auto` keyword.

- Setting `auto` in a column or row instead of defining a width or height will cause the row or column to adjust to the height or width of the contents. If there are multiple columns, the other columns in that row will take on the height of the tallest column. The same happens with rows.
    - [Example image 1](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-auto.jpg) shows a grid with 2 rows and 3 columns. The first row is 50px in height. The 2nd row's height is `auto`, so it will adjust to the content's height.
    - [Example image 2](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-auto-2.jpg) shows the height of content, to illustrate the height of the 2nd row.
- If a `grid-template-row` isn't defined, or if there are more rows than we have defined, __they will default to auto__.

## Positioning grid items

Like with flex items and containers, grid items can be positioned via the grid container or directly from the grid item itself.

### Positioning elements via the grid container

- `align-items` controls the __vertical position__ of a grid item that doesn't take up the entire height of a row
    - Flexbox uses `flex-start`, `flex-end` and so on - Grid does away with the `flex` prefix
        - `align-items: start;`
        - `align-items: end;`
        - `align-items: center;`
        - `align-items: baseline;`
    - [Example image 1](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-align-items.jpg) (start, end, center)
    - [Example image 2](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-align-items-2.jpg) (baseline)
- `justify-items` controls the __horizontal position__ of a grid item that doesn't take up the entire width of a column
    - `justify-items: end;`
    - `justify-items: start;`
    - `justify-items: center;`
    - `justify-items: stretch;` (default)
    - [Example image](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-justify-items.jpg) (start, end, center, stretch)

### Positioning elements via individual grid items

Grid items can be positioned using their own properties instead of properties defined in the parent grid container. Both `align-self` and `justify-self` can accept values of `start`, `center`, and `end`.

- `align-self`
- `justify-self`
- [Codepen: grid: align-self & justify-self](https://codepen.io/vishalicious/pen/xxaqLVL)

## Spacing

Adding space to the __outside edges__ of a grid is done by adding rows or columns where needed. For example, adding a 1em column to the right and left of the grid, or a 1em row to the top and bottom of a grid.

- `grid-template: 1em auto auto 150px 1em / 200px auto auto 1em;`
    - This places a 1em row at the top and bottom of the grid and a 1em column on the right end of the grid

### grid-gap

Adding space between rows and columns on a grid is accomplished via `grid-gap`. The gap adds a margin-like space in the row-line and column-line areas. It only affects the inside lines, not the borders of the grid.

- grid-column-gap: `grid-column-gap: 1em;`
- grid-row-gap: `grid-row-gap: 1em;`
- grid-gap shorthand: `grid-gap: 0 2em;`
    - The above example adds no space between rows and a 2em space between columns
- [Codepen: grid spacing & grid-gap](https://codepen.io/vishalicious/pen/MWqpOBg)