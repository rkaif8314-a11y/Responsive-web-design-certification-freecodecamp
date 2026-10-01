# CSS Series 02 — Todo List Link States

## What this exercise teaches

This project practices CSS selectors and the five important link pseudo-classes:

- `:link` — unvisited link
- `:visited` — visited link
- `:hover` — mouse is over the link
- `:focus` — link has keyboard/focus attention
- `:active` — link is being clicked

It also reinforces the box model, attribute selectors, child selectors, spacing, and text styling.

## Files

- `index.html` — Todo list structure.
- `styles.css` — visual styling and link-state behavior.

## CSS walkthrough

### 1. Body

```css
body {
  background-color: #f4f1ea;
  font-family: Arial, sans-serif;
  color: #222;
  max-width: 600px;
  margin: 60px auto;
  padding: 20px;
}
```

- `background-color` changes the page background.
- `font-family` chooses the font. Arial is preferred and `sans-serif` is the fallback.
- `color` sets the default text color.
- `max-width` limits the content width.
- `margin: 60px auto` adds top/bottom spacing and centers the content horizontally.
- `padding` adds space inside the element.

### 2. Heading

```css
h1 {
  text-align: center;
  margin-bottom: 30px;
}
```

`text-align: center` centers the heading. `margin-bottom` creates space below it.

### 3. Todo list

```css
.todo-list {
  padding: 0;
  list-style-type: none;
}
```

- `.todo-list` is a class selector.
- `padding: 0` removes default list padding.
- `list-style-type: none` removes the default bullets.

### 4. Direct-child selector

```css
.todo-list > li {
  background-color: white;
  margin-bottom: 20px;
  padding: 20px;
  border-radius: 8px;
}
```

The `>` symbol means **direct child**. It selects only `li` elements directly inside `.todo-list`.

- `background-color` sets the item background.
- `margin-bottom` separates items.
- `padding` creates inner space.
- `border-radius` rounds corners.

### 5. Attribute selector

```css
input[type="checkbox"] {
  margin-right: 8px;
}
```

This selects an `input` only when its `type` attribute equals `checkbox`.

### 6. Label

```css
label {
  font-weight: bold;
}
```

`font-weight: bold` makes the todo label thicker.

### 7. Sub-list

```css
.sub-item {
  margin-top: 10px;
  padding-left: 25px;
}
```

The nested resource list gets top spacing and is moved inward using left padding.

### 8. Removing link decoration

```css
a {
  text-decoration: none;
}
```

The `a` element selector targets links. `text-decoration: none` removes the default underline.

## 9. Link pseudo-classes

### `:link`

```css
.sub-item-link:link {
  color: #2563eb;
}
```

Applies to an unvisited link.

### `:visited`

```css
.sub-item-link:visited {
  color: #7c3aed;
}
```

Applies after the link has been visited.

### `:hover`

```css
.sub-item-link:hover {
  color: red;
}
```

Applies when the mouse pointer is over the link.

### `:focus`

```css
.sub-item-link:focus {
  outline: 2px solid #16a34a;
  outline-offset: 3px;
}
```

Applies when the link has focus, including keyboard navigation. The outline provides a visible focus indicator.

### `:active`

```css
.sub-item-link:active {
  color: #dc2626;
}
```

Applies while the link is being activated/clicked.

## Important selector types learned

### Class selector

```css
.todo-list { }
```

The `.` selects a class.

### Element selector

```css
a { }
```

Selects every `a` element.

### Attribute selector

```css
input[type="checkbox"] { }
```

Selects elements based on an attribute value.

### Direct-child selector

```css
.todo-list > li { }
```

Selects only direct `li` children.

### Pseudo-class

```css
.sub-item-link:hover { }
```

Selects an element according to its current state.

## Link-state revision map

| Selector | Meaning |
|---|---|
| `:link` | Unvisited |
| `:visited` | Visited |
| `:hover` | Mouse over |
| `:focus` | Focused / keyboard navigation |
| `:active` | Being clicked |

## Important properties learned

| Property | Purpose |
|---|---|
| `background-color` | Background color |
| `font-family` | Font |
| `color` | Text color |
| `max-width` | Maximum width |
| `margin` | Outside spacing |
| `padding` | Inside spacing |
| `text-align` | Text alignment |
| `list-style-type` | List marker style |
| `border-radius` | Rounded corners |
| `font-weight` | Text thickness |
| `text-decoration` | Underline/decoration |
| `outline` | Focus indicator |
| `outline-offset` | Distance between element and outline |

## Common mistakes

- Forgetting the `.` before a class selector.
- Writing `todo-list` instead of `.todo-list`.
- Confusing `>` with a normal descendant selector.
- Spelling `text-decoration` incorrectly.
- Spelling pseudo-classes incorrectly: `:hover`, `:focus`, `:active`, `:visited`, `:link`.
- Forgetting the colon before a pseudo-class.
- Forgetting the closing `}`.
- Forgetting the semicolon after a declaration.

## Quick memory trick

**L V H F A**

**L**ink → **V**isited → **H**over → **F**ocus → **A**ctive

The most important new CSS concept in this exercise is **pseudo-classes: styling an element according to its state**.
