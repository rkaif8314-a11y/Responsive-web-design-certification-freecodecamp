# Heart Icon

## What this exercise does

This exercise creates a small heart icon using inline SVG inside an HTML document.

SVG stands for Scalable Vector Graphics. SVG describes graphics with elements and drawing instructions rather than storing the picture as a grid of pixels.

## Complete code walkthrough

### 1. HTML5 declaration

`<!DOCTYPE html>` declares the document as HTML5.

### 2. Root element

`<html lang="en">` creates the document root and identifies English as the language.

### 3. Head

`<meta charset="UTF-8">` sets UTF-8 character encoding.

`<title>Heart Icon</title>` sets the browser-tab title.

### 4. Body

`<body>` contains the visible page content.

### 5. SVG drawing area

`<svg fill="red" width="24" height="24" viewBox="0 0 24 24">` creates the SVG canvas.

- `fill="red"` sets the default fill color.
- `width="24"` sets the displayed width.
- `height="24"` sets the displayed height.
- `viewBox="0 0 24 24"` defines the internal coordinate system.

The viewBox values are:

`min-x min-y width height`

So `0 0 24 24` means the drawing coordinates run across a 24 × 24 coordinate system.

### 6. Path

`<path d="..."></path>` draws the heart.

The `d` attribute contains SVG path commands and coordinates. Those commands tell the browser how to construct the outline of the shape.

You do not need to memorize the long path string. The important relationship is:

`path` = shape

`d` = instructions for drawing that shape

### 7. Closing elements

The path is closed first, then the SVG element is closed, followed by the body and HTML document.

## Key concepts learned

- SVG inside HTML
- `svg` element
- `fill`
- `width` and `height`
- `viewBox`
- `path`
- `d` path data
- HTML document structure

## SVG memory trick

**SVG = drawing area**

**viewBox = coordinate system**

**path = shape**

**d = drawing instructions**

This foundation will make SVG icons and vector graphics easier to understand later.
