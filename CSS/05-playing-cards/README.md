# CSS Series #05 — Playing Cards

A Flexbox-based playing card layout built for the freeCodeCamp CSS curriculum. The project uses nested Flexbox containers to arrange multiple cards and position the left, middle, and right sections inside each card.

## Files

- `index.html` — page structure and four playing cards.
- `styles.css` — card styling and Flexbox layout.

## HTML Walkthrough

### Main container

```html
<main id="playing-cards">
```

The `main` element contains all playing cards. The required `id` is used by CSS to control the overall card layout.

### Card structure

Every `.card` contains exactly three `div` children:

```html
<div class="card">
  <div class="left">...</div>
  <div class="middle">...</div>
  <div class="right">...</div>
</div>
```

This structure is important for the freeCodeCamp tests and gives Flexbox three direct children to position.

## CSS Walkthrough

### 1. Page setup

```css
body {
  margin: 0;
  min-height: 100vh;
  background-color: #e8edf3;
  font-family: Arial, sans-serif;
}
```

- `margin: 0` removes the browser's default outer spacing.
- `min-height: 100vh` makes the page at least as tall as the viewport.
- `background-color` sets the page background.
- `font-family` sets the default font.

### 2. Main Flexbox container

```css
#playing-cards {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}
```

- `display: flex` turns the main element into a Flexbox container.
- `justify-content: center` centers its card children along the main axis.
- `gap: 20px` creates 20px of space between flex items.
- `flex-wrap: wrap` allows cards to move to another line when needed.

### 3. Card styling

```css
.card {
  width: 180px;
  height: 260px;
  background-color: white;
  border: 2px solid black;
  border-radius: 12px;
  display: flex;
  justify-content: space-between;
  padding: 15px;
  box-sizing: border-box;
  font-size: 24px;
  font-family: Georgia, serif;
}
```

- `width` and `height` define the card dimensions.
- `background-color` creates the card surface.
- `border` creates the outline.
- `border-radius` rounds the corners.
- `display: flex` makes the card's `.left`, `.middle`, and `.right` children flex items.
- `justify-content: space-between` distributes those three children across the card.
- `padding` creates space inside the card.
- `box-sizing: border-box` includes padding and border inside the declared width and height.
- `font-size` controls the suit and rank size.
- `font-family` gives the card a serif style.

### 4. Individual Flexbox item alignment

```css
.left {
  align-self: flex-start;
}

.right {
  align-self: flex-end;
}

.middle {
  align-self: center;
  display: flex;
  flex-direction: column;
}
```

`align-self` controls one flex item instead of every item.

- `.left` uses `flex-start`.
- `.middle` uses `center`.
- `.right` uses `flex-end`.

The `.middle` element is also a Flexbox container. `flex-direction: column` changes its children from a row into a vertical column.

## Important Flexbox Concepts

| Property | Purpose |
|---|---|
| `display: flex` | Creates a Flexbox container |
| `justify-content` | Positions items along the main axis |
| `justify-content: center` | Centers flex items |
| `justify-content: space-between` | Distributes space between items |
| `gap` | Adds consistent space between flex items |
| `flex-wrap` | Allows flex items to move to another line |
| `align-self` | Positions one individual flex item on the cross axis |
| `flex-start` | Aligns an item at the start |
| `center` | Centers an item |
| `flex-end` | Aligns an item at the end |
| `flex-direction: column` | Arranges flex children vertically |

## Nested Flexbox

This project demonstrates an important real-world CSS pattern: a Flexbox container can contain another Flexbox container.

```text
#playing-cards
    ↓
  Flexbox
    ↓
  .card .card .card .card
       ↓
   each card is also Flexbox
       ↓
 left / middle / right
       ↓
   .middle is Flexbox too
       ↓
      column
```

## Common Mistakes

1. Writing `justify-content: space-between` on `#playing-cards` instead of `.card`.
2. Using `align-items` when the requirement specifically asks for `align-self`.
3. Forgetting `display: flex` on `.middle` before using `flex-direction`.
4. Writing `flex-direction: columns` — the correct value is `column`.
5. Writing `flex-wrap: wraps` — the correct value is `wrap`.
6. Forgetting the `20px` value in `gap: 20px`.
7. Adding extra `div` children directly inside `.card`, which can fail the FCC structure test.

## Quick Revision

**Parent cards:**

```css
#playing-cards {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 20px;
}
```

**Inside each card:**

```css
.card {
  display: flex;
  justify-content: space-between;
}
```

**Individual positions:**

```css
.left { align-self: flex-start; }
.middle { align-self: center; }
.right { align-self: flex-end; }
```

**Vertical middle content:**

```css
.middle {
  display: flex;
  flex-direction: column;
}
```

## FreeCodeCamp Requirements Covered

- Main element with `id="playing-cards"`.
- At least three `.card` elements.
- Each card has a width and height.
- Each card has exactly three direct `div` children.
- Each card contains `.left`, `.middle`, and `.right`.
- `#playing-cards` uses Flexbox, centering, wrapping, and a 20px gap.
- `.card` uses Flexbox and `space-between`.
- `.left`, `.middle`, and `.right` use the required `align-self` values.
- `.middle` uses Flexbox with `flex-direction: column`.
