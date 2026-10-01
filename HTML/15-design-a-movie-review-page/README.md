# Responsive Web Design — HTML Series #15: Design a Movie Review Page

This exercise builds a simple movie review page using semantic HTML, an image, text content, an accessible visual rating, and a cast-members list.

## Files

- `index.html` — Complete movie review page.
- `README.md` — Detailed explanation and revision notes.

## 1. Page Structure

The document uses the standard HTML structure:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    ...
  </head>
  <body>
    ...
  </body>
</html>
```

### Important parts

- `<!DOCTYPE html>` declares an HTML5 document.
- `lang="en"` identifies the document language as English.
- `<head>` contains metadata and the page title.
- `<body>` contains visible page content.

## 2. Viewport Metadata

The page includes:

```html
<meta
  name="viewport"
  content="width=device-width, initial-scale=1.0"
/>
```

This helps the page display correctly on different screen sizes, especially mobile devices.

## 3. Semantic Main Content

The movie review is placed inside:

```html
<main>
  ...
</main>
```

`<main>` identifies the primary content of the page and gives the document a meaningful semantic structure.

## 4. Movie Heading

The main movie title uses an `<h1>`:

```html
<h1>Interstellar</h1>
```

There should generally be one primary `h1` describing the main subject of the page.

## 5. Movie Poster

The movie poster is displayed with an `<img>` element:

```html
<img
  src="https://image.tmdb.org/t/p/original/iolc5VLP4PFU0XvjTVRiCb80mUR.jpg"
  height="250"
  width="250"
  alt="Interstellar poster"
/>
```

### Important attributes

- `src` specifies the image URL.
- `width` controls the displayed width.
- `height` controls the displayed height.
- `alt` provides alternative text for users who cannot see the image.

### Accessibility

The `alt` attribute is important because screen readers can use it to describe the image.

## 6. Movie Description

The review description is placed inside a paragraph:

```html
<p>
  This movie is directed by Mr. Christopher Nolan and is based on
  science-fiction themes.
</p>
```

The `<p>` element is used for normal paragraphs of text.

## 7. Movie Rating

The rating is displayed using a paragraph containing bold text, stars, and the numerical rating:

```html
<p>
  <b>Movie Rating:</b>
  <span aria-hidden="true">⭐⭐⭐⭐⭐⭐⭐⭐⭐☆</span>
  (9.2/10)
</p>
```

### `<b>`

`<b>` draws attention to the text visually without adding the semantic meaning of strong importance.

### `<span>`

`<span>` is a generic inline element. Here it groups the star characters so accessibility attributes can be applied to them.

### `aria-hidden="true"`

The stars are decorative because the numerical rating `(9.2/10)` already communicates the rating.

Therefore:

```html
<span aria-hidden="true">⭐⭐⭐⭐⭐⭐⭐⭐⭐☆</span>
```

tells assistive technologies not to treat the decorative stars as meaningful text.

## 8. Cast Members Heading

The cast section uses:

```html
<h2>Cast Members</h2>
```

An `h2` is appropriate because it represents a subsection under the main movie heading.

## 9. Cast Members List

The cast members are presented using an unordered list:

```html
<ul>
  <li><b>X</b> as the main character.</li>
  <li><b>Y</b> as the main character.</li>
  <li><b>Z</b> as the main character.</li>
  <li><b>X</b> as the main character.</li>
</ul>
```

### `<ul>`

Creates an unordered/bulleted list.

### `<li>`

Represents one item inside a list.

The `<li>` elements must be placed inside a list container such as `<ul>` or `<ol>`.

## 10. HTML Cleanup Applied

A few small issues in the submitted code were cleaned before pushing.

### Corrected movie spelling

Original:

```html
<h1>Interstaller</h1>
```

Corrected:

```html
<h1>Interstellar</h1>
```

### Corrected director spelling

Original:

```
Chirstopher Nolan
```

Corrected:

```
Christopher Nolan
```

### Removed invalid `lenght` attribute

The original image contained:

```html
lenght="250"
```

`lenght` is not a valid HTML image attribute, so it was removed. The valid attributes are:

```html
width="250"
height="250"
```

## Quick Revision Map

| Concept | Example |
|---|---|
| Main content | `<main>` |
| Main heading | `<h1>` |
| Subheading | `<h2>` |
| Image | `<img>` |
| Image source | `src="..."` |
| Alternative text | `alt="..."` |
| Paragraph | `<p>` |
| Inline container | `<span>` |
| Hide decorative content from assistive tech | `aria-hidden="true"` |
| Unordered list | `<ul>` |
| List item | `<li>` |
| Bold visual text | `<b>` |

## One-Line Takeaway

**A movie review page combines semantic headings, accessible images, descriptive text, lists, and accessible handling of decorative rating symbols.**
