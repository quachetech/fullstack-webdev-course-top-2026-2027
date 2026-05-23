# Elements & Tags

**Date Learned:** 23 May 2026 
**Related Lesson:** [Elements and Tags](https://www.theodinproject.com/lessons/foundations-elements-and-tags) 

---

## Overview

HTML defines the structure and content of webpages through a system of
elements and tags. Every piece of content on a webpage — paragraphs, headings,
lists, images, links — is represented by an HTML element. Tags are the syntax
that marks where each element begins and ends, telling the browser how to
interpret and format the content contained within them.

---

## Elements & Tags

An **HTML element** is a piece of content wrapped in opening and closing tags.
A **tag** is the markup syntax that defines the element — a keyword enclosed
in angle brackets `<>`.

### Anatomy of an Element

```html
<p>I am a paragraph.</p>
```

| Part | What it is |
|---|---|
| `<p>` | Opening tag — signals where the element begins and what type it is |
| `I am a paragraph.` | Content — what is wrapped and displayed |
| `</p>` | Closing tag — signals where the element ends |

The closing tag is identical to the opening tag with one addition: a forward
slash `/` before the keyword.

**Opening tag** — required for all elements:
```html
<p>
```

**Closing tag** — required for most elements:
```html
</p>
```

---

## Why Tags Matter

Tags do more than mark boundaries. They tell the browser what *type* of content
it is reading, which determines how that content is interpreted, formatted, and
rendered visually. A heading tag produces a heading. A paragraph tag produces
a paragraph. A link tag produces a clickable link.

Using the correct tag for the content it wraps matters for two reasons beyond
visual presentation:

**SEO (Search Engine Optimisation)** — Search engines read HTML tags to
understand the content and hierarchy of a page. Using semantic tags correctly
improves how a page is indexed and ranked.

**Accessibility** — Users who rely on assistive technology such as screen
readers depend on correct HTML tags to navigate and consume content. A page
that uses the right tags is a page that works for everyone.

This practice of using the tag that accurately describes the content it
contains is called **semantic HTML**.

---

## Void Elements

Most HTML elements wrap content between an opening and closing tag. Void
elements are the exception — they have only an opening tag and no closing tag
because they contain no content to wrap.

**Examples:**
```html
<img>   <!-- displays an image -->
<br>    <!-- inserts a line break -->
<hr>    <!-- inserts a horizontal rule -->
<input> <!-- creates a form input field -->
```

Void elements are sometimes written with a self-closing forward slash:
```html
<br />
<img />
```

This syntax is valid and browsers render it correctly, but current HTML
standards consider it obsolete. The preferred modern syntax omits the trailing
slash:
```html
<br>
<img>
```

---

## Key Insight

HTML has a finite set of predefined tags — you do not invent your own. Each
tag exists because it describes a specific type of content or structure. This
is the foundation of semantic HTML: the tag chosen should reflect the *meaning*
of the content, not just its appearance. A heading is not a heading because it
looks big and bold — it is a heading because it is marked with a heading tag.
The visual presentation follows from the semantic choice, not the other way
around.

This distinction matters enormously for SEO and accessibility, and it becomes
increasingly important as projects scale. Writing semantic HTML from the
beginning is the habit that pays dividends later.

---

## Connection to Previous Learning

Day 4 identified a webpage as an HTML document. Day 57's earlier concept note
on HTML & CSS Basics established HTML as the structural layer — The Builder.
This lesson fills in the mechanics of how HTML builds: through elements defined
by tags, each one telling the browser what the content is and how to handle it.

The vocabulary is now in place. Elements. Tags. Opening. Closing. Void.
Semantic. These are the building blocks of everything that follows.

---

**Status:** ✅ Day 57 Complete — Elements & Tags
**Next:** HTML document structure — the full skeleton of a webpage.