# Concept Note: Links & Images
**Date:** 11 June 2026
**Related Lesson:** [Links and Images](http://theodinproject.com/lessons/foundations-links-and-images)

---

## Overview

Links are what make the web a web — without them, HTML pages would be isolated
documents with no connections between them. Images are among the most common
types of embedded content on any webpage. Both are handled through specific
HTML elements with attributes that point to external or internal resources.

---

## Links — The Anchor Element `<a>`

The anchor element creates a clickable link in HTML.

```html
<a>I am a link</a>
```

On its own, this renders as plain text with no functionality. For a link to
work it needs the `href` attribute.

---

### The `href` Attribute

`href` stands for **hypertext reference**. It provides the destination the
link points to. Without it the anchor element is decorative only.

```html
<a href="https://www.example.com">I am a link</a>
```

When `href` is present the link renders as blue and underlined by default.
Anchor elements can link to any kind of internet resource — not only HTML
documents.

---

### The `target` Attribute

Controls where the linked resource opens. Without it the default value is
`_self`, which opens the link in the current tab.

To open in a new tab:

```html
<a href="https://www.example.com" target="_blank" rel="noreferrer">
    I am a link
</a>
```

---

### The `rel` Attribute

Describes the relationship between the current page and the linked resource.
When using `target="_blank"` it is important to include appropriate `rel`
values for security:

| Value | Effect |
|---|---|
| `noopener` | Prevents the new tab from accessing the original page, blocking tabnabbing phishing attacks. Modern browsers apply this automatically for `target="_blank"` links. |
| `noreferrer` | Same protection as `noopener` plus prevents details about the original page from being passed to the destination page. |

Best practice when linking externally with `target="_blank"`:

```html
<a href="https://www.example.com" target="_blank" rel="noreferrer">
    External Link
</a>
```

---

## Absolute vs Relative Links

### Absolute Links

Links to pages or resources on other websites. They include the full path
from scheme to domain to resource:

```
scheme://domain/path
```

```html
<a href="https://www.theodinproject.com">The Odin Project</a>
```

---

### Relative Links

Links to other pages within the same website. They use only the file path
relative to the current page's location in the directory structure — no scheme
or domain required.

```html
<a href="./pages/about.html">About</a>
```

The `./` means "starting from the current directory." The path navigates
through the file system to the target file the same way CLI paths do.

---

## Images — The `<img>` Element

The `<img>` element embeds images into an HTML document. It is a **void
element** — it has no closing tag and wraps no content.

```html
<img src="./images/bird.jpg" alt="A small brown bird on a branch">
```

---

### The `src` Attribute

Tells the browser where the image file is located. Accepts both absolute and
relative paths.

**Absolute path** — image hosted on an external server:

```html
<img src="https://www.theodinproject.com/mstile-310x310.png">
```

**Relative path** — image stored within the project's own directory:

```html
<img src="./images/bird.jpg">
```

The relative path is written relative to the current file's position in the
directory tree. If the HTML file and the `images` folder are in the same
directory, `./images/filename.jpg` reaches the image correctly.

---

### The `alt` Attribute

Provides alternative text describing the image. This text serves two purposes:

- **Fallback display** — shown in place of the image if it fails to load
- **Accessibility** — read aloud by screen readers for users relying on
  assistive technologies

```html
<img src="./images/bird.jpg" alt="A small brown bird perched on a branch">
```

Always write `alt` text that describes what the image shows clearly and
concisely. An image without `alt` text is an accessibility gap.

---

### Size Attributes

It is good practice to specify image dimensions directly on the element:

```html
<img src="./images/bird.jpg" alt="A small brown bird" width="500" height="300">
```

**Why this matters:** When the browser loads a page it begins rendering content
before images have fully downloaded. Without declared dimensions it does not
know how much space to reserve for each image, causing content to shift and
jump as images load — a poor user experience. Declared dimensions allow the
browser to reserve the correct space immediately, keeping the layout stable.

---

## Key Insight

Relative paths for both links and images connect directly to the file system
and CLI knowledge built in earlier lessons. Navigating to `./pages/about.html`
in an `href` attribute uses the same logic as `cd ./pages` in the terminal —
the `./` means "from here." The directory tree that was navigated by hand in
the CLI lessons is the same structure that HTML relative paths traverse. The
two skill sets are the same mental model expressed in different contexts.

---

## Connection to Previous Learning

**Day 57 (Elements & Tags):** Introduced attributes as name-value pairs inside
opening tags. Links and images are the first intensive application of that
concept — `href`, `target`, `rel`, `src`, `alt`, `width`, and `height` are
all attributes doing specific work on their respective elements.

**Day 5 (URLs):** Absolute links follow the URL structure established early
in the challenge — `scheme://domain/path`. The distinction between absolute
and relative paths here mirrors the distinction between absolute and relative
file paths covered in the CLI lessons.

**Days 31–33 (CLI — File System):** Relative paths in HTML navigate the
directory tree using the same logic as relative paths in the terminal.
`./images/bird.jpg` in HTML and `cd ./images` in the terminal are the same
concept in two different environments.

---

**Status:** ✅ Links & Images — Concept Note Complete