# Working With Text
**Date:** 28 May 2026
**Related Lesson:** [Working With Text](https://www.theodinproject.com/lessons/foundations-working-with-text)

---

## Overview

Most content on the web is text-based. HTML provides dedicated text elements
that allow content to be structured, organised, and formatted meaningfully.
Without them, text placed directly into the `<body>` collapses into a single
unformatted block — impossible to organise into headings, paragraphs, or any
readable hierarchy.

---

## Text Elements

### Paragraphs — `<p>`

Wraps text into a paragraph block.

```html
<p>This is a paragraph of text.</p>
```

Without `<p>` tags, the browser compresses all text into one continuous line
regardless of how it is laid out in the HTML file. The paragraph element
restores that separation and makes text organizable.

---

### Headings — `<h1>` through `<h6>`

HTML provides six levels of headings, decreasing in size and importance from
`<h1>` to `<h6>`.

```html
<h1>Main Page Heading</h1>
<h2>Section Heading</h2>
<h3>Subsection Heading</h3>
<h4>Sub-subsection Heading</h4>
<h5>Minor Heading</h5>
<h6>Smallest Heading</h6>
```

Headings establish **content hierarchy** on the page. `<h1>` is reserved for
the main heading of the overall page — there should typically be only one per
page. Subsequent heading levels organise content into sections and subsections
in descending order of importance.

Correct heading hierarchy matters for both **SEO** (search engines use headings
to understand page structure) and **accessibility** (screen readers use headings
to navigate content).

---

### Bold — `<strong>`

Makes text bold and semantically marks it as important.

```html
<p>This is <strong>very important</strong> information.</p>
```

The visual effect (bold) and the semantic meaning (important) are both
delivered. Assistive technologies recognise `<strong>` and communicate the
emphasis to users who rely on them.

---

### Italic — `<em>`

Makes text italic and semantically places emphasis on it.

```html
<p>You should <em>always</em> validate your HTML.</p>
```

As with `<strong>`, the semantic layer matters as much as the visual. `<em>`
tells the browser and assistive technologies that this text carries emphasis,
not just a style preference.

---

## Nesting & Relationships

Elements are commonly nested within one another. Nesting creates
**parent-child relationships** between elements.

```html
<p>This paragraph contains <strong>bold</strong> and <em>italic</em> text.</p>
```

Here `<strong>` and `<em>` are children of `<p>`. Elements at the same level
of nesting are called **siblings**.

**From the boilerplate:**
- `<html>` is the parent of both `<head>` and `<body>`
- `<head>` and `<body>` are siblings — they sit at the same level within `<html>`
- Everything inside `<body>` is nested within it as children

**Indentation is best practice** when nesting. It makes the level of nesting
visually clear and keeps code readable for collaborators and future reference.

```html
<body>
    <h1>Main Heading</h1>
    <p>A paragraph with <strong>bold text</strong> inside it.</p>
</body>
```

---

## HTML Comments

Comments are notes written in the HTML file that are not rendered by the
browser and not visible to the user. They exist purely for developer context.

```html
<!-- This is an HTML comment -->

<!-- Navigation section begins here -->
<nav>
    ...
</nav>
```

**Use cases:**
- Explaining what a section of code does
- Leaving notes for collaborators or future self
- Temporarily disabling code without deleting it

**VS Code shortcut:** `Ctrl + /` toggles a comment on the selected line.

---

## VS Code Shortcuts Worth Knowing

**Lorem Ipsum placeholder text:** Type `lorem` and press `Enter` in VS Code
to generate a block of dummy placeholder text. Useful for filling out page
layouts during development before real content is available.

**Comment toggle:** `Ctrl + /` on any line creates or removes an HTML comment.

---

## Key Insight

The distinction between `<strong>` and simply making text bold with CSS, or
between `<em>` and making text italic with CSS, comes down to semantics.
A CSS style changes appearance only. A semantic HTML element changes both
appearance and meaning — it communicates intent to the browser, to search
engines, and to assistive technologies. This is the principle of semantic HTML
in practice: choose the element that describes what the content *is*, not just
how it should *look*.

---

## Connection to Previous Learning

**Day 57 (Elements & Tags):** Introduced the concept that the correct tag
should reflect the meaning of the content — semantic HTML. Today's text
elements are the first direct application of that principle. `<strong>` and
`<em>` are semantic choices, not just visual ones.

**Day 61 (HTML Boilerplate):** The parent-child and sibling relationships
introduced in the boilerplate (`<html>` → `<head>` + `<body>`) are the same
structural logic used when nesting text elements within `<body>`.

---

**Status:** ✅ Day 62 — Working With Text (Concept Note Complete)