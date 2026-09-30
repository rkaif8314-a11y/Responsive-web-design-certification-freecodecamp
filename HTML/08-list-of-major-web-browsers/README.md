# List of Major Web Browsers

## What this exercise does

This exercise teaches the HTML description-list elements `dl`, `dt`, and `dd` by creating a list of major web browsers and descriptions for each one.

## Complete code walkthrough

### 1. Document setup

- `<!DOCTYPE html>` declares HTML5.
- `<html lang="en">` is the root element and identifies English as the page language.

### 2. Head

The head contains:

`<meta charset="UTF-8">`

Sets the document's character encoding.

`<meta name="viewport" content="width=device-width, initial-scale=1.0">`

Helps the page use the device's viewport correctly on different screen sizes.

`<title>List of Browsers and Descriptions</title>`

Sets the browser-tab title.

### 3. Main heading

`<h1>List of Major Web Browsers</h1>`

Introduces the page's main subject.

### 4. Description list

`<dl>`

Creates a description list.

Unlike `ul` or `ol`, a description list is designed for terms/names and their corresponding descriptions.

### 5. Description terms

Each browser name is written inside `<dt>`.

Examples:

- Google Chrome
- Firefox
- Safari
- Brave
- Arc

`dt` means description term.

### 6. Descriptions

Each explanation is written inside `<dd>`.

For example, the browser name is the term and the following `dd` provides information about that browser.

`dd` means description details/description.

The normal relationship is:

`dt → dd`

and this pattern can be repeated for multiple terms.

## Browser entries in this exercise

### Google Chrome

The `dt` contains the browser name and its `dd` explains that it is a browser developed by Google.

### Firefox

The `dt` identifies Firefox and its `dd` gives information about its development and history.

### Safari

The `dt` identifies Safari and its `dd` describes its relationship with Apple devices.

### Brave

The `dt` identifies Brave and its `dd` describes its Chromium-based nature and release information.

### Arc

The `dt` identifies Arc and its `dd` provides its description and release information.

## Key concepts learned

- `dl` = description list
- `dt` = description term
- `dd` = description/details
- The relationship between a term and its description
- Difference between a description list and a normal unordered/ordered list

## Quick memory trick

Think:

**DL = Description List**

**DT = Description Term**

**DD = Description Details**

So:

`<dl><dt>Term</dt><dd>Details</dd></dl>`
