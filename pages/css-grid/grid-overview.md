# CSS Grid overview

- CSS Grid is a layout tool like CSS Flexbox
    - __Flexbox__ works with one dimension at a time (horizontal or vertical)
        - Flex containers can have either a row or a column, but not both inherently
    - __Grid__ creates a grid that works with the horizontal and vertical axes simultaneously
        - Grid containers can have both rows and columns at the same time

[CSS-Tricks: A Complete Guide to CSS Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)

## Setting up a basic grid

- Create a grid using `display: grid;` on a container
    - Margins no longer collapse
    - Direct children become `grid items`
    - [Codepen: display: grid](https://codepen.io/vishalicious/pen/qBMdzqW) example
- Flexbox only deals with one dimension, a row or column, we switch back and forth via `flex-direction`
- Grid deals with two dimensions - we explicitly create them and place items in the grid
    - [grid-template-columns](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-template-columns.jpg) defines columns (each gets a `width`)
        - example image shows 3 columns with widths of 200px, 200px and 350px
        - __css example__: `grid-template-columns: 200px 200px 350px;`
        - [Codepen: grid-template-columns](https://codepen.io/vishalicious/pen/YzOXoaG)
            - Note how in the Codepen example, there are 7 elements in the grid, an \<h1> and 6 \<p>'s. The grid has 3 columns and each element falls into a column - *rows are created automatically to accomodate the elements that exceed the 3 columns*.
    - [grid-template-rows](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-template-rows.jpg) defines rows (each gets a `height`)
        - example image builds on previous one and adds 2 rows with heights of 50px & 200px
        - __css example__: `grid-template-rows: 50px 200px;`
        - [Codepen: grid-template-rows](https://codepen.io/vishalicious/pen/BaOpjGz)
    - The shorthand for both `grid-template-columns` and `grid-template-rows` at the same time is `grid-template`.
        - Specify the __rows__ first followed by a `/` and then __columns__
        - __css example__: `grid-template: 100px 400px / 250px 250px 250px;`
        - [Codepen: grid-template](https://codepen.io/vishalicious/pen/oNPBbVR)

## Placing items on the grid

- Grid items can be explicitly placed on the grid
    - These properties are used on the `flex item`, __not__ on the `flex parent`:
        - `grid-column-start`
        - `grid-column-end`
        - `grid-row-start`
        - `grid-row-end`
    - [example image](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-template-columns-and-rows.jpg) shows `column lines` in __red__ and `row lines` in __yellow__
        - lines are numbered, starting at 1, not 0
        - [example image](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-template-placement-1.jpg) starting at row __1__ and ending at row __3__ & starting at column __2__ and ending at column __3__
        - [example image](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-template-placement-2.jpg) starting at row __2__ and ending at row __3__ & starting at column __1__ and ending at column __3__
        - Items can be placed in a __square__ or __rectangle__ shape - no odd shapes, like "__L__"
        - [Codepen: Placing items on the grid](https://codepen.io/vishalicious/pen/WNgRwJJ)
    - The shorthand for `grid-column-start` & `grid-column-end` and `grid-row-start` & `grid-row-end` is:
        - `grid-row: start / end;`
        - `grid-column: start / end;`
        - [This](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-template-placement-2.jpg) explicit placement can be shortened to [this](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-template-placement-3.jpg)
            - Another [example](https://github.com/vishalicious213/code-conspectus-v2/blob/main/img/grid-template-placement-4.jpg) using shorthand
    - __Overlap__ grid items by positioning them in common row or columns
        - [Codepen: Overlapping items on a grid](https://codepen.io/vishalicious/pen/OJoWEdO)
    - Grids can be counted backwards using negative numbers
        - The last row line or column line is -1, the one before it is -2, etc.
        - This is often used to make a row or column stretch across the entire row/column like this:
            - `grid-column: 1 / -1;`
            - This makes the element stretch from the 1st column line to the last column line without having to count the column lines to enter the ending line
            - Contain an item in a smaller area like this: `grid-column: 2 / -2;`
- `span` can be used to indicate how many rows or columns an element should stretch across
    - Starting on the 2nd column line, stretch across 2 columns: `grid-column: 2 / span 2;`
    - Get placed where applicable and stretch downward 2 rows: `grid-row: span 2;`
    - [Codepen: span across grid columns or rows](https://codepen.io/vishalicious/pen/yLxgZaK)