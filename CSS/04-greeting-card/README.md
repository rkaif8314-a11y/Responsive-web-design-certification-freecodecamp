# CSS Series 04 — Greeting Card

## What this exercise teaches

This project combines several CSS concepts in one interactive greeting card:

- Backgrounds and spacing
- Rounded corners and box shadows
- CSS transitions
- `transform: scale()` and `transform: skewX()`
- Pseudo-elements: `::before` and `::after`
- Flexbox with `display: flex`
- Link pseudo-classes: `:hover`, `:active`, `:focus`, `:visited`
- The `:target` pseudo-class

## Files

- `index.html` — greeting card structure and target sections.
- `styles.css` — visual styling, animations, link states, and target behavior.

## CSS walkthrough

### 1. Body

```css
body {
  font-family: Arial, sans-serif;
  padding: 40px;
  text-align: center;
  background-color: brown;
}
```

- `font-family` chooses the font.
- `padding` adds space inside the body.
- `text-align: center` centers text.
- `background-color` changes the page background.

### 2. Card

```css
.card {
  background-color: white;
  max-width: 400px;
  padding: 40px;
  margin: 0 auto;
  border-radius: 10px;
  box-shadow: 0 4px 8px gray;
  transition: transform 0.3s, background-color 0.3s ease;
}
```

- `max-width` limits the card width.
- `margin: 0 auto` centers the card.
- `border-radius` rounds corners.
- `box-shadow` creates a shadow.
- `transition` makes property changes smooth.

### 3. Hover + transform

```css
.card:hover {
  background-color: khaki;
  transform: scale(1.1);
}
```

`:hover` applies when the pointer is over the card.

`transform: scale(1.1)` makes the card 10% larger visually.

### 4. Pseudo-elements

```css
h1::before {
  content: "🥳 ";
}

h1::after {
  content: " 🥳";
}
```

- `::before` inserts generated content before the element's text.
- `::after` inserts generated content after it.
- `content` is required for these generated-content examples.

### 5. Message

```css
.message {
  font-size: 1.2em;
  margin-bottom: 20px;
}
```

`1.2em` makes the text 1.2 times the inherited font size.

### 6. Flexbox link container

```css
.card-links {
  margin-top: 20px;
  display: flex;
  justify-content: space-around;
}
```

- `display: flex` activates Flexbox.
- `justify-content: space-around` distributes horizontal space around the links.

### 7. Link styling

```css
.card-links a {
  text-decoration: none;
  font-size: 1em;
  padding: 10px 20px;
  border-radius: 5px;
  color: white;
  background-color: midnightblue;
  transition: background-color 0.3s ease;
}
```

This makes the links look like buttons. `padding` creates space inside, while `border-radius` rounds their corners.

### 8. Link states

```css
.card-links a:hover {
  background-color: orangered;
}

.card-links a:active {
  background-color: midnightblue;
}

.card-links a:focus {
  outline: 2px solid yellow;
}

.card-links a:visited {
  color: crimson;
}
```

- `:hover` — pointer is over the link.
- `:active` — link is being activated/clicked.
- `:focus` — link has focus, useful for keyboard navigation.
- `:visited` — browser considers the destination visited.

### 9. Hidden sections

```css
section {
  display: none;
}
```

`display: none` removes the section from the normal page display until another rule changes it.

### 10. Section hover

```css
section:hover {
  transform: skewX(10deg);
}
```

`skewX()` slants the element horizontally along the X-axis.

### 11. `:target` — important new pseudo-class

```css
section:target {
  display: block;
}
```

This works with the HTML links:

```html
<a href="#send">Send Card</a>
<section id="send">...</section>
```

Clicking `#send` changes the URL fragment to `#send`. Because the section has `id="send"`, it becomes the current target, so `section:target` applies and changes it from `display: none` to `display: block`.

## Important concepts learned

### Transition

```css
transition: background-color 0.3s ease;
```

Makes a CSS property change smoothly instead of instantly.

### Transform

```css
transform: scale(1.1);
transform: skewX(10deg);
```

Changes the visual geometry of an element without changing its normal document layout.

### Pseudo-element vs pseudo-class

```css
h1::before { }
```

`::before` is a **pseudo-element** because it creates generated content.

```css
.card:hover { }
```

`:hover` is a **pseudo-class** because it describes an element's state.

### Flexbox

```css
display: flex;
```

Turns an element into a flex container so its children can be arranged using Flexbox properties such as `justify-content`.

### `:target`

`:target` selects the element whose `id` matches the current URL fragment.

## Quick revision table

| CSS | Purpose |
|---|---|
| `box-shadow` | Adds a shadow |
| `transition` | Smooths property changes |
| `transform` | Visually transforms an element |
| `scale()` | Enlarges/reduces an element |
| `skewX()` | Slants an element horizontally |
| `::before` | Inserts generated content before |
| `::after` | Inserts generated content after |
| `display: flex` | Activates Flexbox |
| `justify-content` | Controls main-axis distribution |
| `outline` | Focus indicator |
| `display: none` | Hides an element |
| `:target` | Selects the current URL target |

## Common mistakes

- Forgetting the colon in `:hover`, `:active`, `:focus`, or `:target`.
- Confusing `::before` / `::after` with `:hover` / `:focus`.
- Forgetting the `content` property when using generated pseudo-element content.
- Writing `transform: scale` without parentheses and a value.
- Forgetting that `display: none` hides the section.
- Using `href="#send"` without a matching `id="send"`.
- Spelling `justify-content` incorrectly.
- Forgetting the semicolon at the end of a CSS declaration.

## Memory trick

**Pseudo-element = creates/targets a piece of an element**

`::before`, `::after`

**Pseudo-class = describes a state/condition**

`:hover`, `:active`, `:focus`, `:visited`, `:target`
