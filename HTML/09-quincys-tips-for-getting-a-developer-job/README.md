# Quincy's Tips for Getting a Developer Job

## What this exercise does

This exercise demonstrates semantic HTML for quotations and citations. It uses inline quotations, longer block quotations, source references, headings, paragraphs, and sections.

## Complete code walkthrough

### 1. Document setup

`<!DOCTYPE html>` declares HTML5.

`<html lang="en">` defines the root element and identifies English as the document language.

### 2. Head

The `head` contains:

- `meta charset="UTF-8"` for character encoding.
- `meta name="viewport"...` for responsive viewport behavior.
- `title` for the browser-tab title.

The metadata elements are HTML void elements, so they use the HTML syntax without a closing slash.

### 3. Page heading

`<h1>Quincy's Tips for Getting a Developer Job</h1>` creates the main heading.

### 4. Inline quotation with q

`<q cite="...">...</q>` is used for a short quotation that appears inside normal text.

The `cite` attribute stores the source URL associated with the quotation.

### 5. Main content

`<main>` wraps the primary content of the page.

This gives the document a clear semantic main-content landmark.

### 6. Sections and headings

Each topic is placed inside a `<section>` with an `<h2>`.

The heading hierarchy is:

`h1 → h2`

This makes the page easier to understand structurally.

### 7. Block quotation

`<blockquote cite="...">...</blockquote>` is used for longer quotations presented as separate blocks.

Its `cite` attribute identifies the source URL.

### 8. Citing the work

The first section uses the `<cite>` element around the title of the cited book.

Important distinction:

- `cite="URL"` is an attribute that stores a source URL.
- `<cite>Work Title</cite>` is an element identifying the title of a cited work.

### 9. Multiple paragraphs inside blockquote

The networking and reputation sections contain several `p` elements inside their `blockquote`.

This allows a longer quotation to contain separate paragraphs.

### 10. Em dash entity

`&mdash;` is an HTML character entity that displays an em dash before the author's name.

## Key concepts learned

- `q` for short inline quotations
- `blockquote` for longer quotations
- `cite` attribute for source URLs
- `cite` element for cited work titles
- Semantic `main` and `section`
- Heading hierarchy
- HTML entities such as `&mdash;`

## Important revision point

Do not confuse the two uses of `cite`:

`<q cite="URL">quote</q>`

uses `cite` as an attribute.

`<cite>Book Title</cite>`

uses `cite` as an HTML element.
