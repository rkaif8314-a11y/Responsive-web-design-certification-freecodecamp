# XYZ Bookstore Page

A beginner HTML project from the **freeCodeCamp Responsive Web Design** curriculum.

## Project Overview

This project builds the basic structure of a bookstore page using HTML. It demonstrates how `div` elements, classes, and IDs can be used to organize related content and create a clear page structure.

## Concepts Practiced

- HTML document structure
- Headings and paragraphs
- `div` elements for grouping content
- Classes with the `class` attribute
- Unique identifiers with the `id` attribute
- Buttons with the `button` element
- Organizing repeated card content
- Creating a container for action buttons

## Page Structure

The page contains:

1. **Bookstore heading** — introduces the XYZ Bookstore.
2. **Introduction paragraph** — describes the bookstore collection.
3. **Book cards** — two books with titles, descriptions, and Buy Now buttons.
4. **Checkout message** — tells the user to review selections.
5. **Action buttons** — View Cart and Checkout.

## HTML Structure

The main bookstore content is organized using:

```html
<div class="card-container">
  <div class="card" id="sally-adventure-book">
    ...
  </div>

  <div class="card" id="dave-cooking-book">
    ...
  </div>
</div>
```

### Classes

Classes such as `card`, `btn`, and `card-container` are used to identify groups of elements that can later be styled or targeted together with CSS.

### IDs

The book cards and action buttons use unique IDs such as:

- `sally-adventure-book`
- `dave-cooking-book`
- `view-cart-btn`
- `checkout-btn`

IDs are useful when a specific element needs to be uniquely identified.

## Project Structure

```text
BookstorePage/
├── index.html
└── README.md
```

## How to Run

Open `index.html` in any modern web browser.

## Learning Goal

The goal of this exercise is to practice structuring webpage content with `div` elements and using classes and IDs to organize and identify HTML elements. CSS can be added later to style the bookstore cards and buttons.
