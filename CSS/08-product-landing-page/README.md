# Product Landing Page — NOVA X1

## Overview

This project is a responsive product landing page for a fictional premium wireless audio product called **NOVA X1**.

The project practices the main requirements of the freeCodeCamp Product Landing Page exercise while focusing on clean HTML structure, Flexbox layouts, fixed navigation, forms, embedded media, pricing cards, selectors, hover states, and responsive design.

## Folder Structure

```text
CSS/08-product-landing-page/
├── index.html
├── styles.css
└── README.md
```

## Main Sections

1. Fixed header and navigation
2. Hero section
3. Email signup form
4. Features section
5. Embedded product demo
6. Pricing cards
7. Responsive mobile layout
8. Footer

## HTML Walkthrough

### 1. Header

```html
<header id="header">
```

`header` creates the introductory/header area of the page.

The required freeCodeCamp image element is:

```html
<img id="header-img" ...>
```

The navigation uses:

```html
<nav id="nav-bar">
  <a class="nav-link" href="#features">Features</a>
  <a class="nav-link" href="#demo">Demo</a>
  <a class="nav-link" href="#pricing">Pricing</a>
</nav>
```

The `href="#features"` pattern connects a navigation link to an element whose `id` is `features`. This creates in-page navigation.

### 2. Main and Hero

```html
<main>
  <section id="hero">
```

`main` contains the primary content of the page. `section` groups related content into a meaningful page section.

### 3. Email Form

```html
<form id="form" action="https://www.freecodecamp.org/email-submit">
```

Important form concepts:

- `id="form"` identifies the form.
- `action` defines where the form submission is sent.
- `input type="email"` provides email-format validation.
- `name="email"` gives the submitted field a name.
- `placeholder` provides a hint inside the input.
- `type="submit"` creates a submission control.

### 4. Features

The three feature cards are placed inside:

```html
<div class="features-container">
```

Each card uses the reusable class `feature-card`.

### 5. Embedded Video

```html
<iframe id="video" ...></iframe>
```

`iframe` embeds external content inside the webpage.

Important attributes:

- `id="video"` identifies the required video element.
- `src` specifies the embedded content URL.
- `title` provides an accessible description.
- `allowfullscreen` allows fullscreen playback.

### 6. Pricing Cards

The pricing section contains three reusable cards:

- CORE
- PRO
- ULTRA

The PRO card has two classes:

```html
class="pricing-card featured"
```

This allows a special style using a compound selector.

### 7. Footer

```html
<footer>
```

`footer` contains information associated with the bottom of the webpage.

---

## CSS Concepts

### 1. Universal Selector and Box Sizing

```css
* {
  box-sizing: border-box;
}
```

`*` selects every element.

`box-sizing: border-box` makes the declared width and height include padding and border. This makes responsive sizing easier to control.

**Memory trick:** `border-box` = padding + border stay inside the declared size.

### 2. Fixed Navigation

```css
#header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}
```

- `position: fixed` keeps the header attached to the viewport.
- `top: 0` places it at the top.
- `left: 0` places it against the left edge.
- `width: 100%` makes it span the available width.
- `z-index: 10` keeps it above the page content.

### 3. Flexbox

Flexbox is used repeatedly in this project.

```css
display: flex;
```

It creates a flexible layout for child elements.

```css
justify-content: center;
```

Controls positioning along the main axis.

```css
align-items: center;
```

Controls alignment on the cross axis.

```css
gap: 30px;
```

Creates space between flex items.

```css
flex: 1;
```

Allows flex items to share available space.

```css
flex-direction: column;
```

Stacks flex items vertically.

**Memory trick:**

- `row` = side by side
- `column` = top to bottom
- `gap` = space between
- `flex: 1` = share space

### 4. Text Styling

```css
font-size
font-weight
letter-spacing
line-height
text-align
```

These properties control text size, thickness, letter spacing, line spacing, and alignment.

### 5. Box Model

```css
margin
padding
border
width
height
```

Remember:

- `padding` = inside space
- `border` = edge around an element
- `margin` = outside space

### 6. Hover State

```css
.nav-link:hover {
  color: orange;
}
```

`:hover` is a pseudo-class that applies styles while the pointer is over the element.

### 7. Compound Selector

```css
.pricing-card.featured {
```

This selects an element that has **both** `pricing-card` and `featured` classes.

### 8. Direct Child Selector

```css
.pricing-card > p:not(.price)
```

`>` means direct child.

`:not(.price)` excludes elements having the `price` class.

So this selector targets the card's description paragraph while excluding the price paragraph.

### 9. Responsive Design

```css
@media (max-width: 700px) {
```

A media query changes the layout when the viewport becomes 700px wide or smaller.

In this project it:

- stacks the header contents,
- reduces text sizes,
- stacks the email form,
- stacks feature cards,
- stacks pricing cards,
- reduces video height,
- reduces section spacing.

---

## Important New Tags / Features

| Tag / Feature | Purpose |
|---|---|
| `header` | Page header area |
| `nav` | Navigation area |
| `main` | Primary page content |
| `section` | Groups related content |
| `form` | Collects/submits input |
| `input` | User input/control |
| `iframe` | Embeds external content |
| `ul` | Unordered list |
| `li` | List item |
| `button` | Interactive button |
| `footer` | Bottom page information |
| `@media` | Responsive CSS |

## Common Mistakes to Remember

### 1. Class-name mismatch

If HTML has:

```html
<div class="features-container">
```

CSS must use:

```css
.features-container {
```

Not `.feature-container`.

### 2. Fixed header width

A fixed header with padding can overflow when using the default box model. `box-sizing: border-box` prevents this sizing problem.

### 3. Form attributes

The email field should have:

```html
type="email"
name="email"
placeholder="..."
```

And the form must use the required action URL.

### 4. Navigation targets

The navigation target must match the section ID exactly:

```html
href="#pricing"
```

matches:

```html
id="pricing"
```

### 5. Keep footer inside body

The `<footer>` belongs inside `<body>`, after the main content.

---

## Quick Revision

```text
Fixed navbar  → position: fixed
Flexbox       → display: flex
Space         → gap
Share space   → flex: 1
Inside space  → padding
Outside space → margin
Rounded edge  → border-radius
Hover effect  → :hover
Both classes  → .a.b
Direct child  → .a > .b
Exclude class → :not(.class)
Responsive    → @media
Sizing        → box-sizing: border-box
```

## freeCodeCamp Requirement Checklist

- [x] `header#header`
- [x] `img#header-img` inside the header
- [x] `nav#nav-bar` inside the header
- [x] Three `.nav-link` elements
- [x] Navigation links point to page sections
- [x] Embedded `#video`
- [x] `form#form`
- [x] `input#email`
- [x] Email placeholder
- [x] Email input uses `type="email"`
- [x] `input#submit`
- [x] Submit input uses `type="submit"`
- [x] Required form action URL
- [x] Fixed navigation
- [x] Media query
- [x] Flexbox

## Project Learning Outcome

This project combines the CSS concepts learned in the previous exercises with a complete multi-section responsive webpage. The main new skills are fixed navigation, embedded media, forms, reusable cards, compound selectors, direct-child selectors, responsive Flexbox layouts, media queries, and box sizing.
