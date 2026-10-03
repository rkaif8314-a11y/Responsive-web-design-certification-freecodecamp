# Technical Documentation Page

## Overview

A FreeCodeCamp Responsive Web Design project that builds a technical documentation page for web development. The page uses a fixed navigation sidebar, section anchors, documentation content, code examples, lists, and a responsive mobile layout.

## Folder

```text
CSS/07-technical-documentation/
├── index.html
├── styles.css
└── README.md
```

## HTML Walkthrough

### 1. Page foundation

- `<!DOCTYPE html>` declares an HTML5 document.
- `<html lang="en">` sets the document language.
- `<head>` contains metadata, the page title, and the stylesheet link.
- `<body>` contains the visible page content.

### 2. Navigation

```html
<nav id="navbar">
  <header>Web Development</header>
  <a class="nav-link" href="#Introduction">Introduction</a>
</nav>
```

`nav` groups navigation links. Each link uses `href="#Section_ID"`, which jumps to the element with the matching `id`.

Example:

```text
href="#HTML_Basics"
        ↓
id="HTML_Basics"
```

This is why clicking a navbar item moves to its corresponding section.

### 3. Main documentation

```html
<main id="main-doc">
```

`main` represents the primary content of the page.

### 4. Documentation sections

Each topic is a `section` with the required `main-section` class and a unique `id`.

```html
<section class="main-section" id="HTML_Basics">
  <header>HTML Basics</header>
  <p>...</p>
</section>
```

The first child is the section's `header`, which is important for the FreeCodeCamp tests.

### 5. Lists

```html
<ul>
  <li>HTML for structure</li>
  <li>CSS for presentation</li>
</ul>
```

- `ul` creates an unordered list.
- `li` creates an individual list item.

### 6. Code examples

```html
<code>&lt;h1&gt;Hello World&lt;/h1&gt;</code>
```

`code` represents computer code. `&lt;` and `&gt;` display `<` and `>` as text instead of being interpreted as HTML tags.

## CSS Walkthrough

### 1. Body styling

```css
body {
  margin: 0;
  font-family: Arial, sans-serif;
  color: black;
  background-color: white;
}
```

- `margin: 0` removes the browser's default outer margin.
- `font-family` controls the font.
- `color` controls text color.
- `background-color` controls the page background.

### 2. Fixed navbar

```css
#navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 250px;
  height: 100vh;
}
```

- `position: fixed` keeps the navbar attached to the viewport.
- `top: 0` places it at the top.
- `left: 0` places it at the left edge.
- `width: 250px` gives it a fixed sidebar width.
- `height: 100vh` makes it the full viewport height.
- `vh` means viewport height.

### 3. Overflow

```css
overflow-y: auto;
```

Allows vertical scrolling inside the navbar when its content is taller than the available height.

### 4. Descendant selectors

```css
#navbar header { }
.main-section header { }
```

A space between selectors means the second element is a descendant of the first.

### 5. Link styling and pseudo-class

```css
.nav-link:hover {
  background-color: lightgray;
}
```

`:hover` applies the rule while the pointer is over the link.

### 6. Main content positioning

```css
#main-doc {
  margin-left: 250px;
  padding: 30px;
  max-width: 900px;
}
```

`margin-left` leaves room for the fixed navbar. `padding` creates inner space. `max-width` prevents the documentation from becoming excessively wide.

### 7. Code block styling

```css
.main-section code {
  display: block;
  padding: 15px;
  margin: 15px 0;
  background-color: lightgray;
  border-radius: 5px;
  border-left: 4px solid gray;
  font-family: monospace;
}
```

- `display: block` puts each code example on its own line.
- `padding` creates space inside the code box.
- `margin: 15px 0` adds vertical outside space.
- `border-radius` rounds the corners.
- `border-left` adds a visual accent on the left.
- `monospace` uses equal-width characters, common for code.

### 8. Responsive design

```css
@media (max-width: 768px) {
  #navbar {
    position: relative;
    width: 100%;
    height: auto;
  }
}
```

The media query applies different CSS when the viewport is 768px wide or smaller.

On smaller screens:

- the navbar becomes part of normal page flow with `position: relative`;
- it uses `width: 100%`;
- its height becomes automatic;
- the main content resets `margin-left` to `0`.

## New HTML Tags / Concepts

| Tag / Concept | Purpose |
|---|---|
| `nav` | Navigation area |
| `main` | Main page content |
| `section` | Groups related content |
| `header` | Introductory heading/content |
| `ul` | Unordered list |
| `li` | List item |
| `code` | Computer code content |
| `href="#id"` | Jumps to a matching ID |
| `id` | Unique identifier for an element |

## New CSS Concepts

| CSS | Meaning |
|---|---|
| `position: fixed` | Fixes an element relative to the viewport |
| `position: relative` | Keeps an element in normal flow while allowing positioning context |
| `top` / `left` | Offset a positioned element |
| `100vh` | 100% of viewport height |
| `overflow-y: auto` | Adds vertical scrolling when necessary |
| `margin-left` | Creates outside space on the left |
| `max-width` | Limits maximum width |
| `:hover` | Applies styles when the pointer is over an element |
| `display: block` | Makes an element behave as a block |
| `border-left` | Styles only the left border |
| `font-family: monospace` | Uses a code-friendly font family |
| `@media` | Applies CSS conditionally based on device/viewport conditions |

## Common Mistakes

1. Making the navbar links' `href` values different from the section `id` values.
2. Forgetting the `#` in `href="#Introduction"`.
3. Using spaces in an `id` when the navigation expects underscores.
4. Forgetting that every `.main-section` must start with a `header`.
5. Forgetting `id="main-doc"` on the `main` element.
6. Forgetting `id="navbar"` on the navigation element.
7. Writing `Arail` instead of `Arial` in `font-family`.
8. Forgetting `margin-left: 250px` when the navbar is fixed on desktop.
9. Forgetting to reset `margin-left` on smaller screens.
10. Forgetting `display: block` when the code examples need to behave like separate boxes.

## Quick Revision

```text
nav       → navigation
main      → main content
section   → related content group
header    → section heading
ul        → unordered list
li        → list item
code      → code example
#id       → jump to matching id
fixed     → stays attached to viewport
100vh     → full viewport height
:hover    → mouse-over state
@media    → responsive CSS
```

## Memory Trick

```text
NAV → MAIN → SECTION → HEADER → CONTENT

href="#X" → id="X"

Desktop  → fixed sidebar + margin-left
Mobile   → relative navbar + margin-left: 0
```

## Project Learning Outcome

This project combines semantic HTML structure, anchor navigation, fixed positioning, descendant selectors, pseudo-classes, code blocks, lists, and responsive media queries into one complete documentation page.
