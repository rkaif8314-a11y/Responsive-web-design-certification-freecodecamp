# CSS Series 01 — Design a Business Card

## Goal

This exercise introduces the core CSS ideas needed to style a simple business card: selectors, declarations, colors, fonts, the box model, spacing, sizing, text alignment, and descendant selectors.

## Files

- `index.html` — the HTML structure of the business card.
- `styles.css` — the CSS rules that style the page.

## CSS walkthrough

### 1. Styling the whole page

```css
body {
  background-color: rosybrown;
  font-family: Arial, sans-serif;
}
```

- `body` is the selector for the whole webpage body.
- `background-color` changes the page background.
- `font-family` sets the typeface.
- `Arial, sans-serif` means Arial is preferred; `sans-serif` is the fallback.

### 2. Styling the business card

```css
.business-card {
  width: 300px;
  background-color: white;
  padding: 20px;
  margin: 100px auto 0;
  text-align: center;
  font-size: 16px;
}
```

- `.business-card` selects the element whose class is `business-card`.
- `width: 300px` gives the card a fixed width.
- `background-color: white` makes the card white.
- `padding: 20px` adds space inside the card.
- `margin: 100px auto 0` gives 100px top margin, automatically centers the card horizontally, and gives 0 bottom margin.
- `text-align: center` centers the text.
- `font-size: 16px` sets the base text size.

### 3. Profile image

```css
.profile-image {
  max-width: 100%;
}
```

The image can use up to the full width of its parent, helping prevent it from overflowing the card.

### 4. Name

```css
.full-name {
  font-size: 24px;
  font-weight: bold;
}
```

The class selector targets the name paragraph. `font-size` controls size and `font-weight` controls thickness.

### 5. Designation

```css
.designation {
  font-size: 18px;
}
```

This makes the designation text 18 pixels tall.

### 6. Company

```css
.company {
  font-size: 16px;
}
```

This targets only the company paragraph and sets its font size.

### 7. All paragraphs

```css
p {
  margin: 5px 0;
}
```

The element selector `p` targets every paragraph.

The two values mean:
- `5px` = top and bottom margin.
- `0` = left and right margin.

### 8. All links

```css
a {
  text-decoration: none;
}
```

The `a` selector targets every link. `text-decoration: none` removes the default underline.

### 9. Portfolio link

```css
.portfolio-link {
  display: inline-block;
  margin: 10px 0;
}
```

- `display: inline-block` lets the link remain inline while accepting box-model sizing and spacing.
- `margin: 10px 0` adds 10px above and below the link and 0px on the sides.

### 10. Social-media section

```css
.social-media {
  margin-top: 20px;
}
```

This adds 20px of space above the social-media section.

### 11. Social heading

```css
.social-media h2 {
  font-size: 20px;
}
```

This is a descendant selector. It means: select an `h2` that is inside an element with the `social-media` class.

### 12. Social links

```css
.social-media a {
  margin: 0 5px;
}
```

This selects links inside `.social-media`. The links get 0px top/bottom margin and 5px left/right margin, creating space between them.

## CSS syntax to remember

Every CSS rule follows this pattern:

```css
selector {
  property: value;
}
```

Example:

```css
.business-card {
  width: 300px;
}
```

Think:

**Selector = WHO**  
**Property = WHAT**  
**Value = HOW MUCH / HOW**

## Key concepts from this exercise

### Class selector

A class in HTML:

```html
<div class="business-card">
```

is selected in CSS with:

```css
.business-card {
}
```

The dot `.` means class selector.

### Element selector

```css
p {
}
```

targets every `<p>` element.

### Descendant selector

```css
.social-media a {
}
```

targets `<a>` elements located inside `.social-media`.

### Box model

Remember:

**content → padding → border → margin**

- Padding = space inside the element.
- Border = visible boundary around the element.
- Margin = space outside the element.

## Common mistakes

- Forgetting the dot before a class selector, such as writing `business-card` instead of `.business-card`.
- Writing a class name differently in HTML and CSS.
- Confusing padding with margin.
- Forgetting the semicolon after a declaration.
- Using `.portfoilo-link` or another misspelling when the HTML class is `.portfolio-link`.
- Using `.socail-media` instead of `.social-media`.
- Forgetting to connect `styles.css` in the HTML `<head>`.

## Quick revision

| CSS | Purpose |
|---|---|
| `background-color` | Background color |
| `font-family` | Font choice |
| `width` | Element width |
| `padding` | Inside spacing |
| `margin` | Outside spacing |
| `text-align` | Text alignment |
| `font-size` | Text size |
| `font-weight` | Text thickness |
| `max-width` | Maximum width |
| `display` | Element display behavior |
| `text-decoration` | Text decoration such as underline |

## Revision takeaway

This project combines the basic CSS building blocks: **selectors + properties + values + box model + typography + spacing + descendant selectors**.
