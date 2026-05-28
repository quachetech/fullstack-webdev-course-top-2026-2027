# Concept Note: Lists
**Date:** 28 May 2026
**Related Lesson:** [Lists](https://www.theodinproject.com/lessons/foundations-lists)

---

## Overview

Lists are one of the most common structures on the web — navigation menus,
ingredients, instructions, rankings, and feature lists are all built with HTML
list elements. HTML provides two primary list types: unordered for items where
sequence doesn't matter, and ordered for items where it does.

---

## Unordered Lists — `<ul>`

Used when the order of items is not significant. Renders as a bulleted list
by default.

```html
<ul>
    <li>Apples</li>
    <li>Bread</li>
    <li>Milk</li>
</ul>
```

**Renders as:**
- Apples
- Bread
- Milk

The `<ul>` element wraps the entire list. Each individual item is wrapped in
an `<li>` (list item) element. The order in which items appear carries no
implied meaning — a shopping list where items can be picked up in any sequence
is a good example.

---

## Ordered Lists — `<ol>`

Used when the order of items is significant. Renders as a numbered list
by default.

```html
<ol>
    <li>Preheat the oven to 180°C</li>
    <li>Mix the dry ingredients</li>
    <li>Add the wet ingredients</li>
    <li>Pour into a baking tin and bake for 30 minutes</li>
</ol>
```

**Renders as:**
1. Preheat the oven to 180°C
2. Mix the dry ingredients
3. Add the wet ingredients
4. Pour into a baking tin and bake for 30 minutes

The `<ol>` element wraps the entire list. Each item is again wrapped in `<li>`.
The sequence is meaningful here — step 2 cannot happen before step 1.

---

## The List Item Element — `<li>`

`<li>` is used inside both `<ul>` and `<ol>`. It always functions as a child
of a list element and wraps individual list entries. It cannot be used
meaningfully outside of a list context.

---

## Structure at a Glance

| Element | Type | Default Rendering | Use When |
|---|---|---|---|
| `<ul>` | Unordered list | Bulleted | Order doesn't matter |
| `<ol>` | Ordered list | Numbered | Order matters |
| `<li>` | List item | — | Always, inside `<ul>` or `<ol>` |

---

## Key Insight

The choice between `<ul>` and `<ol>` is a semantic decision, not just a
visual one. Both can be styled to look identical with CSS, but the element
chosen communicates the nature of the content to the browser, search engines,
and assistive technologies. A numbered list built with `<ul>` and CSS numbers
looks ordered but isn't semantically ordered — the markup does not reflect the
meaning. Choosing `<ol>` for sequential content and `<ul>` for non-sequential
content is semantic HTML applied to lists.

---

## Connection to Previous Learning

**Day 57 (Elements & Tags):** Lists follow the same parent-child nesting
structure introduced with elements and tags. `<ul>` or `<ol>` is the parent,
`<li>` elements are the children — the same relationship pattern seen in the
boilerplate and in nested text elements.

**Day 62 (Working With Text):** Lists are text content and sit inside `<body>`
alongside paragraphs and headings. They can contain other text elements —
a list item can wrap `<strong>` or `<em>` just like a paragraph can.

---

**Status:** ✅ Day 62 — Lists (Concept Note Complete)
**Assignment:** Pending — four lists to be built and committed tomorrow.