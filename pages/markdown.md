# What is Markdown:

- Lightweight markup language with a plain text formatting syntax
- No tags, very readable syntax
- Can be converted to HTML/XHTML and other formats
- GitHub has an extended Markdown that includes tables

### What is it used for?

- Readme files (Github)
- Blog posts (Gatsby)
- Static site generators (Gatsby)

### VS Code extension

- Auto-Open Markdown Preview
- Shows the preview in 2nd pane in VS Code


## Headings

- Use a hashtag. Each one increments heading type.

```md
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

## Italics

- Wrap text with asterisks or underscores

```md
*This text* is italic
_This text_ is italic
```
*This text* is italic

## Strong (Bold)

- Wrap text with double-underlines

```md
__This text__ is strong/bold
```
__This text__ is strong/bold

## Strikethrough

- Wrap text with double-tildes

```md
~~This text~~ is struckthrough
```
~~This text~~ is struckthrough

## Horizontal Rule (line across page)

- use three dashes or underscores

```md
---
___
```
---

## Escaping (to show asterisks, etc.)

- Preface char wih a backslash

```md
\*This text\* shows asterisks instead of being italic
```
\*This text\* shows asterisks instead of being italic

## Blockquotes

- Preface with a greater-than sign
- Gives a block square at first column and a lighter shade background

```md
> This is a quote
```
> This is a quote

## Links

- The text to turn into a link is wrapped in brackets
- The URL follows, wrapped in parenthesis
[Code Conspectus](https://vish213-code.netlify.app/)

- To add a tooltip, add a space after URL and text in quotes
[Code Conspectus](https://vish213-code.netlify.app/ "Code Conspectus")

### Link in the same document

- Use same format as above (brackets around text, parenthesis for link)
- Start link with a hashtag, VS Code will show headers to link to
- If manually typing links:
    - No space between hashtag and text
    - All text must be lowercase
    - Spaces must be dashes


## Unordered Lists

- Preface each line with an asterisk
- Nested list - tab over and add asterisk

```md
* Item 1
* Item 2
* Item 3
    * Nested Item 1
    * Nested Item 2
```
* Item 1
* Item 2
* Item 3
    * Nested Item 1
    * Nested Item 2

## Ordered Lists

- Preface each line with "1."
- It will auto-increment

```md
1. Item 1
1. Item 2
1. Item 3
```
1. Item 1
1. Item 2
1. Item 3

## Inline Code Block

- Use back-ticks

```md
`<p>This is a code block</p>`
```
`<p>This is a code block</p>`

## Images

- Just like a link. Text is in brackets, URL is in quotes.
- Preface with an exclamation point
- This will show the image directly in the markdown file

```md
![Markdown Logo](https://markdown-here.com/icon256.png)
```

## RESOURCES

- [YouTube: Markdown Crash Course / Traversy Media](https://www.youtube.com/watch?v=HUBNt18RFbo)