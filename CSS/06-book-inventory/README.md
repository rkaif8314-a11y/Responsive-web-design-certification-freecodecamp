# Book Inventory

## Overview

A CSS-focused FreeCodeCamp Book Inventory project. It combines semantic HTML tables with CSS attribute selectors, gradients, status badges, and a three-circle rating system.

## Files

- `index.html` — table structure, books, status labels, and rating markup.
- `styles.css` — table layout, row gradients, status badges, rating circles, and rating fills.

## Project Structure

```text
06-book-inventory/
├── index.html
├── styles.css
└── README.md
```

## HTML Walkthrough

### 1. Table structure

The page uses one `h1`, one `table`, one `thead`, and one `tbody`. The header contains five columns:

- Title
- Author
- Category
- Status
- Rate

Each book is represented by a `tr` inside `tbody`.

### 2. Row status classes

Each book row uses one of these classes:

```html
<tr class="read">
<tr class="to-read">
<tr class="in-progress">
```

These classes allow CSS to give each row a different gradient.

### 3. Status span

The Status cell contains a span with the exact `status` class:

```html
<span class="status">Read</span>
```

The text changes according to the row status.

### 4. Rating structure

Every Rate cell contains a `rate` span with three empty child spans:

```html
<span class="rate one">
  <span></span>
  <span></span>
  <span></span>
</span>
```

The first class is always `rate`. Optional second classes are `one`, `two`, or `three` for rated books.

## CSS Walkthrough

### Basic table styling

- `font-family` changes the page font.
- `margin` controls outside space.
- `padding` controls inside space.
- `width: 100%` makes the table use the available width.
- `border-collapse: collapse` joins table borders cleanly.
- `text-align: center` centers table content.

### Attribute selectors

This project deliberately uses attribute selectors required by the FreeCodeCamp tests.

```css
tr[class="read"]
```

Targets rows whose class is exactly `read`.

```css
span[class="status"]
```

Targets spans whose class is exactly `status`.

```css
span[class^="rate"]
```

The `^=` operator means the class value starts with `rate`. It therefore matches `rate`, `rate one`, `rate two`, and `rate three`.

```css
span[class~="one"]
```

The `~=` operator finds `one` as a separate class value.

### Linear gradients

`linear-gradient()` creates a smooth color transition. `to right` creates a horizontal gradient, while `to bottom` creates a vertical gradient.

### Inline-block

```css
span {
  display: inline-block;
}
```

`span` is normally inline. `inline-block` lets it remain inline while accepting controlled width and height. This is important for the rating circles.

### Status and rate sizing

```css
span[class="status"],
span[class^="rate"] {
  height: 24px;
  width: 110px;
  padding: 3px 8px;
}
```

The comma groups the two required attribute selectors so the same dimensions apply to both components.

### Rating circles

```css
span[class^="rate"] > span {
  border: 1px solid gray;
  border-radius: 50%;
  margin: 0 2px;
  height: 18px;
  width: 18px;
  background-color: lightgray;
}
```

The `>` combinator targets only the direct child spans of the rate container. Equal height and width make a square, and `border-radius: 50%` turns it into a circle.

### Rating fills

One rating fills the first circle:

```css
span[class~="one"] > span:first-child
```

Two ratings fill the first two circles:

```css
span[class~="two"] > span:nth-child(-n + 2)
```

Three ratings fill all three circles:

```css
span[class~="three"] > span
```

## Important CSS Concepts

| Concept | Meaning |
|---|---|
| `[class="x"]` | Exact class attribute match |
| `[class^="x"]` | Class attribute starts with `x` |
| `[class~="x"]` | Class list contains `x` as a separate value |
| `>` | Direct child selector |
| `:first-child` | Selects the first child |
| `:nth-child(-n + 2)` | Selects the first two children |
| `display: inline-block` | Inline element with controllable box dimensions |
| `border-radius: 50%` | Turns a square into a circle |
| `linear-gradient()` | Creates a gradient background |
| `padding` | Inner spacing |
| `margin` | Outer spacing |

## Common Mistakes

1. Writing `.status` instead of the required `span[class="status"]` selector.
2. Writing `.rate` instead of `span[class^="rate"]` when the exercise requires the attribute selector.
3. Putting `rate` after `one`, `two`, or `three`. The `rate` class must be first.
4. Forgetting all three empty child spans inside every rate element.
5. Forgetting `display: inline-block` on spans when controlling their dimensions.
6. Using `:nth-child(2)` when the goal is to select the first two children. This project uses `:nth-child(-n + 2)`.

## Quick Revision

```text
read       → row gradient + status styling
rate       → rating container
one        → first circle filled
two        → first two circles filled
three      → all three circles filled
^=         → starts with
~=         → contains a separate class value
>          → direct child
```

## Learning Outcome

This project practices CSS attribute selectors, descendant and direct-child selectors, pseudo-classes, gradients, box sizing, inline-block layout, and structured table styling while building a practical UI component.
