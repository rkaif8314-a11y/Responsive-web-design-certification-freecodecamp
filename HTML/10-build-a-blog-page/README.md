# Build a Blog Page

## What this exercise does

This exercise builds a complete semantic HTML blog page for Mr. Whiskers. It includes a header, navigation, image, about section, multiple blog articles, and a contact section in the footer.

## Complete code walkthrough

### 1. Document setup

`<!DOCTYPE html>` declares HTML5.

`<html lang="en">` creates the root element and identifies English as the document language.

### 2. Head

`<title>Mr. Whiskers' Blog</title>` sets the browser-tab title.

`<meta charset="UTF-8">` sets UTF-8 character encoding.

### 3. Header

`<header>` contains introductory content and navigation for the blog.

### 4. Main heading

`<h1>Welcome to Mr. Whiskers' Blog Page!</h1>` is the main page heading.

### 5. Figure, image, and caption

`<figure>` groups the image and its caption.

The `img` element displays the image. Its `src` attribute gives the image URL, while `alt` provides alternative text for accessibility.

`<figcaption>` gives the figure a visible caption.

The relationship is:

`figure → img + figcaption`

### 6. Navigation

`<nav>` identifies the navigation area.

Inside it, `<ul>` creates an unordered list and each `<li>` contains an anchor.

The fragment links work like this:

- `href="#about"` targets `id="about"`.
- `href="#posts"` targets `id="posts"`.
- `href="#contact"` targets `id="contact"`.

The `#` tells the browser that the target is an element ID in the current page.

### 7. Main content

`<main>` contains the primary blog content.

### 8. About section

`<section id="about">` groups the introduction to the author and gives the section the ID used by the About navigation link.

It contains an `h2` heading and two paragraphs.

### 9. Posts section

`<section id="posts">` groups the blog posts and matches the Posts navigation link.

### 10. Article elements

Each post is wrapped in `<article>`.

An article represents a self-contained piece of content.

Each article contains an `h3` title and two paragraphs.

The three articles are:

1. Mr. Whiskers' First Day Home
2. Mr. Whiskers' First Bath
3. Mr. Whiskers' First Birthday Party

### 11. Footer

`<footer>` contains information at the end of the page.

Here it contains the Contact section.

### 12. Contact section

`<section id="contact">` matches the Contact navigation link.

It contains an `h2` heading and an `address` element.

### 13. Address element

`<address>` represents contact information associated with the page or author.

### 14. Telephone link

`<a href="tel:5555555555">...</a>` creates a telephone link.

The displayed number uses `&#8209;`, a non-breaking hyphen, so the number's groups stay together and the repository validator accepts the telephone formatting.

### 15. Email link

`<a href="mailto:fake@email.com">...</a>` creates an email link.

The `mailto:` scheme tells compatible applications that the destination is an email address.

## Complete semantic structure

Think of the page as:

`header → nav`

`main → about + posts → articles`

`footer → contact → address`

## Key concepts learned

- Semantic `header`, `nav`, `main`, `section`, `article`, `footer`, and `address`
- `figure` and `figcaption`
- Accessible image `alt` text
- Internal navigation with IDs and fragment links
- Self-contained content with `article`
- `tel:` and `mailto:` links
- HTML character entities
- Relationship between semantic structure and accessibility

## Revision checklist

You should be able to explain:

1. Why `nav` is used for navigation.
2. How `href="#posts"` connects to `id="posts"`.
3. Why `alt` text is used on images.
4. Why each post is an `article`.
5. Why contact information can use `address`.
6. The difference between `section` and `article`.
