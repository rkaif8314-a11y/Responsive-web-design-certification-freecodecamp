# Accessible Audio Controls

## Series

**Responsive Web Design — HTML Series #13**

This exercise creates a small audio-control interface and demonstrates how to make a range input more understandable to assistive technologies using ARIA.

## What this exercise teaches

- Semantic HTML buttons
- The `button` element
- The `range` input type
- `min`, `max`, and `value`
- Accessible naming with `aria-labelledby`
- Connecting multiple text elements to one control
- The relationship between `id` and `aria-labelledby`
- Basic accessibility thinking

---

## Complete code

The exercise is stored in `index.html`.

The HTML file contains comments explaining the important accessibility pieces.

## Code walkthrough

### 1. Document structure

```html
<!DOCTYPE html>
<html lang="en">
```

- `<!DOCTYPE html>` declares modern HTML.
- `lang="en"` identifies the document language.

### 2. Main heading

```html
<h1>Audio Controls</h1>
```

`h1` gives the page its main heading and tells users what the controls are for.

### 3. Play button

```html
<button type="button">Play</button>
```

The `button` element creates an interactive button.
`type="button"` explicitly makes this a normal button rather than a form-submit button.

### 4. Volume label and description

```html
<span id="volume-label">Volume</span>
<span id="volume-description">Adjust the sound level</span>
```

- `volume-label` identifies the control.
- `volume-description` explains what the user should do with it.

The important part is the `id` attribute. Each `id` provides a unique identifier that another HTML attribute can reference.

## 5. The range input

```html
<input type="range" min="0" max="100" value="50" aria-labelledby="volume-label volume-description" />
```

### `type="range"`

Creates a slider/range control.

### `min="0"`

Sets the lowest value.

### `max="100"`

Sets the highest value.

### `value="50"`

Sets the initial value to 50.

So the initial slider position represents **50 out of 100**.

## 6. Understanding `aria-labelledby`

```html
aria-labelledby="volume-label volume-description"
```

It tells assistive technologies to use the elements with these IDs to provide the accessible name/description for this control.

The connection is:

```text
aria-labelledby
      ↓
volume-label → "Volume"
      +
volume-description → "Adjust the sound level"
```

The IDs in `aria-labelledby` must match the IDs of existing elements.

## 7. Why accessibility matters

A sighted user can see the label and description next to the slider. Assistive technologies may need an explicit relationship between the control and its descriptive text. `aria-labelledby` provides that relationship.

Important pattern:

```text
Text element → id → aria-labelledby → Form control
```

## 8. Mute button

```html
<button type="button">Mute</button>
```

Together, the page demonstrates three common audio controls: Play, Volume slider, and Mute.

---

# Important revision points

## `type="range"`

Creates a slider. Common attributes:

```text
min   → minimum value
max   → maximum value
value → initial value
```

## `aria-labelledby`

Connects an element to existing visible text by referencing IDs.

```html
<span id="label">Volume</span>
<input aria-labelledby="label" />
```

Multiple IDs can be referenced:

```html
aria-labelledby="volume-label volume-description"
```

## `id` vs `aria-labelledby`

| Attribute | Purpose |
|---|---|
| `id` | Gives an element a unique identifier |
| `aria-labelledby` | References IDs that provide an accessible label |

Memory trick: **id = identifier; aria-labelledby = which element(s) describe/name me?**

## Common mistakes

### 1. Referencing an ID that does not exist

If `aria-labelledby="volume-text"` is used, an element with `id="volume-text"` must exist.

### 2. Misspelling an ID

`id="volume-label"` and `aria-labelledby="volume-label"` must match exactly.

### 3. Confusing `aria-labelledby` with `aria-label`

- `aria-label` provides an accessible label directly as a string.
- `aria-labelledby` points to another element's text using its ID.

Example:

```html
<input aria-label="Volume" />
<span id="volume-label">Volume</span>
<input aria-labelledby="volume-label" />
```

This exercise specifically demonstrates `aria-labelledby`.

## Quick revision map

```text
AUDIO CONTROLS
│
├── h1 → Audio Controls
│
├── button → Play
│
├── volume group
│   ├── span#volume-label
│   ├── span#volume-description
│   └── input[type="range"]
│       ├── min="0"
│       ├── max="100"
│       ├── value="50"
│       └── aria-labelledby
│
└── button → Mute
```

## One-line takeaway

**`aria-labelledby` makes the relationship between a control and its existing descriptive text explicit for assistive technologies.**

## Files

- `index.html` — complete commented accessible audio controls
- `README.md` — detailed accessibility explanation and revision notes