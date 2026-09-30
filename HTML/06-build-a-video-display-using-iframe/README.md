# Build a Video Display Using iframe

## What this exercise does

This exercise creates a simple HTML page that displays a YouTube video inside the page using the HTML `<iframe>` element.

The important idea is that an iframe lets one document embed another document or external resource inside a rectangular area of the current page.

## Complete code walkthrough

### 1. Document declaration

`<!DOCTYPE html>`

Tells the browser that this document uses modern HTML5.

### 2. Root HTML element

`<html lang="en">`

- `html` is the root element of the entire document.
- `lang="en"` tells browsers and assistive technologies that the page content is in English.

### 3. Head section

`<head>`

Contains information about the document that is not normally displayed as page content.

#### Character encoding

`<meta charset="UTF-8">`

UTF-8 allows the page to correctly represent a very large range of characters.

The repository validator expects HTML void elements such as `meta` to use the HTML form without a self-closing slash.

#### Page title

`<title>Display Videos in an iframe</title>`

Sets the text shown in the browser tab.

### 4. Body section

`<body>`

Contains the visible content of the page.

### 5. Main heading

`<h1>iframe Video Display</h1>`

Creates the main heading. A page normally uses `h1` for its primary topic.

### 6. iframe

The main element is:

`<iframe ...></iframe>`

An iframe creates an embedded browsing area.

#### `width="560"`

Sets the iframe width to 560 pixels.

#### `height="315"`

Sets the iframe height to 315 pixels.

#### `src="https://www.youtube.com/embed/I0_951_MPE0"`

Specifies the resource displayed inside the iframe.

For YouTube, the embed format is:

`https://www.youtube.com/embed/VIDEO_ID`

Here the video ID is `I0_951_MPE0`.

#### `title="Display Videos in an iframe"`

Provides an accessible name for the iframe. This is important because screen-reader users need to know what embedded content the iframe contains.

#### `allow="..."`

Lists browser capabilities that the embedded content may request, such as playback-related or encrypted-media functionality.

#### `referrerpolicy="strict-origin-when-cross-origin"`

Controls how much referrer information the browser sends when loading the embedded resource.

#### `allowfullscreen`

Allows the embedded video to use fullscreen mode when supported.

### 7. Closing the document

The `body` and `html` elements are closed to finish the document.

## Key concepts learned

- HTML document structure
- `head` vs `body`
- `meta charset`
- `title`
- `iframe`
- YouTube embed URLs
- iframe accessibility with `title`
- iframe sizing
- `allow`, `referrerpolicy`, and `allowfullscreen`

## Validation note

The repository's HTML quality check requires an iframe `title` attribute and the HTML-style syntax for void elements such as `meta`. This version follows those rules.
