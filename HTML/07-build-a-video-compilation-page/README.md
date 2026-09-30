# Build a Video Compilation Page

## What this exercise does

This page introduces front-end web development and organizes three related topics — HTML, CSS, and JavaScript — into separate sections. Each section contains an embedded YouTube video.

## Complete code walkthrough

### 1. Document declaration and root

- `<!DOCTYPE html>` declares HTML5.
- `<html lang="en">` is the root element and identifies English as the document language.

### 2. Head

The `head` contains document metadata.

- `<meta charset="utf-8">` sets UTF-8 character encoding.
- `<title>Video Compilation Page</title>` sets the browser-tab title.

### 3. Body

`<body>` contains everything displayed on the page.

### 4. Main content

`<main>` identifies the primary content of the document.

Inside it:

`<h1>Front-End Web Development</h1>`

This is the main page heading.

The following `<p>` explains what front-end development means.

### 5. First section — HTML

`<section>` groups the content about HTML.

- `<h2>HTML</h2>` gives the section its heading.
- The paragraph explains HTML's role in page structure.
- The iframe embeds a YouTube video.

The iframe's `src` uses the YouTube embed URL format. Its `title` describes the embedded video, while `height` and `width` control its displayed size.

### 6. Second section — CSS

The second `section` follows the same semantic pattern:

- `h2` identifies CSS.
- `p` explains CSS.
- `iframe` embeds the video.

CSS is responsible for presentation such as layout, spacing, fonts, colors, and responsive styling.

### 7. Third section — JavaScript

The third `section` contains:

- an `h2` for JavaScript,
- a paragraph explaining JavaScript,
- an iframe for the video.

JavaScript is used to add behavior and interactivity to web pages.

### 8. Why sections are used

The three `section` elements make the document structure meaningful. Each section represents one related topic with its own heading and content.

## Key concepts learned

- Semantic `main` and `section`
- Heading hierarchy: `h1` → `h2`
- Paragraphs
- Embedded content with `iframe`
- YouTube embed URLs
- iframe titles and dimensions
- Organizing related information into semantic sections

## Revision checklist

Remember this structure:

`main → section → h2 + p + iframe`

That pattern is useful whenever a page is divided into multiple self-contained topics.
