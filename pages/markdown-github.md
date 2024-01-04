# Additional Markdown syntax for GitHub Markdown files:

The following syntax extends Markdown on __GitHub__. Some other platforms, like __Discord__ and __Slack__ also support this syntax.

## Code Blocks (multi-line)

Use triple back-ticks before and after the lines of code

```md
    ```
    npm install
    npm start
    ```
```

Example:

```
    npm install
    npm start
```

- Can optionally add code language after opening back-ticks
- This adds text highlighting (colors, etc.) for coding languages

```md
    ```bash
    npm install
    npm start
    ```
```

Examples:

```bash
*This is a Markdown example*
npm install
npm start
```

```html
<!-- This is an HTML example -->
<div>Here's a div</div>
```

```css
/* This is a CSS example */
h1 {
    font-size: 1.5rem;
    font-weight: 1.25;
}

.container {
    display: flex;
    margin: 0;
    padding: 0;
}
```

```javascript
// This is a JavaScript example
function add(num1, num2) {
    return num1 + num2
}
```

This is the list of languages supported by Markdown for code blocks:

- [Markdown Supported Languages](https://github.com/jincheng9/markdown_supported_languages)

## Tables

- Use pipes to separate columns
- Use dashes for bold lines to separate columns
- Light dashes to separate lines automatically added

```md
| Name     | Email          |
| -------- | -------------- |
| John Doe | john@gmail.com |
| Jane Doe | jane@gmail.com |
```

Example:

| Name     | Email          |
| -------- | -------------- |
| John Doe | john@gmail.com |
| Jane Doe | jane@gmail.com |


## Task Lists (checkboxes)

- Preface with asterisk and brackets with space or "x" in-between
    - Space indicates incomplete task
    - "x" indicates complete task

```md
* [x] Task 1
* [x] Task 2
* [ ] Task 3

```

Example:

* [x] Task 1
* [x] Task 2
* [ ] Task 3


## RESOURCES

- [YouTube: Markdown Crash Course / Traversy Media](https://www.youtube.com/watch?v=HUBNt18RFbo)