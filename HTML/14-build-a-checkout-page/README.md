# Responsive Web Design — HTML Series #14: Build a Checkout Page

This exercise builds a simple checkout page containing a shopping-cart section and an accessible payment-information form.

## Files

- `index.html` — Complete checkout page.
- `README.md` — Explanation and revision notes.

## 1. Overall Page Structure

The page uses:

- `<!DOCTYPE html>` to declare an HTML5 document.
- `<html lang="en">` as the root element and language declaration.
- `<head>` for document metadata.
- `<body>` for visible page content.
- `<h1>` for the main page heading.
- Two `<section>` elements to separate the cart and payment information.

The main heading is:

```html
<h1>Checkout</h1>
```

Each section has its own `<h2>`.

## 2. Shopping Cart Section

The first section contains the product currently in the cart:

```html
<section>
  <h2>Your Cart</h2>

  <img
    src="https://cdn.freecodecamp.org/curriculum/labs/cube.jpg"
    alt="Image of puzzle"
  />

  <p>Puzzle</p>
  <p>22.99$</p>
</section>
```

### Important concepts

- `src` tells the browser where the image is located.
- `alt` provides alternative text describing the image.
- `<p>` elements contain the product name and price.

## 3. Payment Information Section

The second section begins with:

```html
<section>
  <h2>Payment Information</h2>
```

The exercise requires the payment form to be inside this second section.

The form is created with:

```html
<form>
  ...
</form>
```

## 4. Labels and Form Inputs

A label should be associated with its input.

For the cardholder name:

```html
<label for="card-name">
  Cardholder Name
  <span aria-hidden="true">*</span>
</label>

<input
  type="text"
  id="card-name"
  name="card-name"
  required
/>
```

The important connection is:

```
label for="card-name"
        ↓
input id="card-name"
```

The `name` attribute identifies the field when form data is submitted.

## 5. Required Fields

A required input uses the boolean `required` attribute:

```html
<input type="text" required />
```

The browser will require the user to enter a value before submitting the form.

This exercise uses required fields for:

- Cardholder Name
- Card Number
- Expiry Date
- CVV

## 6. The Visual Required Indicator

Each required label contains:

```html
<span aria-hidden="true">*</span>
```

The asterisk visually communicates that the field is required.

### Why `aria-hidden="true"`?

The asterisk is only a visual indicator. `aria-hidden="true"` prevents assistive technologies such as screen readers from unnecessarily announcing it as part of the label.

## 7. Card Number Help Text

The card number input is connected to explanatory text using `aria-describedby`:

```html
<input
  type="text"
  id="card-number"
  name="card-number"
  aria-describedby="card-number-help"
  required
/>

<p id="card-number-help">
  Please enter your 16-digit card number without spaces or dashes.
</p>
```

The connection is:

```
aria-describedby="card-number-help"
              ↓
id="card-number-help"
```

This allows the help text to be associated with the card number field for users of assistive technology.

### Important placement rule

The help paragraph is placed immediately after the card number input, as required by the exercise.

## 8. Expiry Date

The expiry field uses a text input with an `MM/YY` placeholder:

```html
<label for="expiry-date">
  Expiry Date
  <span aria-hidden="true">*</span>
</label>

<input
  type="text"
  id="expiry-date"
  name="expiry-date"
  placeholder="MM/YY"
  required
/>
```

The `placeholder` gives the user an example of the expected format.

## 9. CVV

The CVV field is another required text input:

```html
<label for="cvv">
  CVV
  <span aria-hidden="true">*</span>
</label>

<input
  type="text"
  id="cvv"
  name="cvv"
  required
/>
```

## 10. Submit Button

The form uses:

```html
<button type="submit">Place Order</button>
```

`type="submit"` makes the button submit the form.

## 11. Important HTML Corrections from the Original Code

The original exercise code had a few things worth correcting for clean HTML:

### Input elements are void elements

Do not write:

```html
<input ...></input>
```

Use:

```html
<input ... />
```

An `input` element does not have a closing tag.

### Keep IDs and names consistent

The original code used the typo `expirt-date`. The cleaned version uses:

```html
id="expiry-date"
name="expiry-date"
```

The label's `for` value matches the input's `id`.

### Submit button

The original button used:

```html
<button type="button">Place Order</button>
```

For a form submission, the cleaned version uses:

```html
<button type="submit">Place Order</button>
```

## Quick Revision Map

| Concept | Example |
|---|---|
| Section | `<section>` |
| Form | `<form>` |
| Label | `<label for="card-name">` |
| Text input | `<input type="text">` |
| Required field | `required` |
| Visual required mark | `<span aria-hidden="true">*</span>` |
| Input name | `name="card-name"` |
| Accessible help text | `aria-describedby` |
| Help text ID | `id="card-number-help"` |
| Placeholder | `placeholder="MM/YY"` |
| Submit button | `<button type="submit">` |

## One-Line Takeaway

**A good checkout form combines correct label-input associations, required-field indicators, and accessible help text using `aria-describedby`.**
