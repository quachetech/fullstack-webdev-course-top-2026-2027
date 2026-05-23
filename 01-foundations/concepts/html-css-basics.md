# HTML & CSS Basics

**Date Learned:** 23 May 2026 
**Related Lesson:** [Introduction to HTML & CSS](https://www.theodinproject.com/lessons/foundations-introduction-to-html-and-css) 

---

## Overview

HTML and CSS are the two foundational languages of the web. They work together
to produce every visual webpage a user sees in a browser — HTML providing the
raw structure and content, CSS providing the presentation and style. Neither
is a programming language in the traditional sense. Both are concerned
exclusively with how information is defined and displayed, not with logic or
computation.

---

## The Three Languages of the Web

Every webpage is built from a combination of three languages, each with a
distinct and non-overlapping role:

**HTML — HyperText Markup Language (The Builder)**
Defines all the content on a page. Headings, paragraphs, images, links, lists,
forms — everything that exists on a webpage is defined in HTML. It is the raw
data and structural skeleton from which a page is built. Without HTML there is
nothing to display.

**CSS — Cascading Style Sheets (The Artist)**
Adds styling to HTML elements, making content visually presentable. Colors,
fonts, spacing, layout, sizing, and visual hierarchy are all CSS concerns. CSS
takes the structure HTML defines and determines how it looks. Without CSS a
page is functional but unstyled — plain black text on a white background.

**JavaScript — (The Wizard)**
Adds interactivity and dynamic behavior to a page. Form validation, animations,
real-time updates, click events, and anything that responds to user input is
JavaScript's domain. Without JavaScript a page is static — it displays
information but does not respond or adapt.

---

## How They Work Together

The three languages occupy separate layers with a clear hierarchy:

```
JavaScript  →  Behavior   (what it does)
CSS         →  Presentation  (how it looks)
HTML        →  Structure   (what it is)
```

HTML is the required foundation. CSS needs HTML elements to style. JavaScript
needs HTML elements to manipulate. You can have HTML without CSS or JavaScript
and still have a functioning webpage. You cannot have CSS or JavaScript without
HTML — there would be nothing to work with.

---

## Key Distinctions

**HTML and CSS are not programming languages.** A programming language executes
logic — it makes decisions, runs loops, performs calculations. HTML and CSS do
none of this. HTML describes content. CSS describes appearance. They are markup
and styling languages respectively, concerned only with presenting information,
not processing it.

**Frontend web development** is the practice of building the part of a web
product that users see and interact with directly — the visual layer. HTML, CSS,
and JavaScript are the three tools of frontend development. The web browser is
the environment that reads these languages and translates them into the visual
webpages users experience.

**These languages are constantly evolving.** New HTML elements, CSS features,
and JavaScript capabilities are added regularly as the web matures. Mastering
the fundamentals provides a stable base from which to absorb new additions as
they emerge.

---

## Key Insight

The separation of concerns between HTML, CSS, and JavaScript is a deliberate
design principle. Structure, style, and behavior are kept in separate files and
separate languages so that each can be changed independently without breaking
the others. Redesigning the visual appearance of a page means editing CSS
without touching the HTML. Adding interactivity means writing JavaScript without
rewriting the structure. This modularity is what makes web development
maintainable at scale.

This also reframes what a webpage actually is: not a single monolithic thing,
but three layers of language working in concert — each doing one job, doing it
well, and handing off to the next.

---

## Connection to Previous Learning

Day 4 introduced the concept that a webpage is an HTML document. Day 7
identified HTML as the foundational structural language of the web and placed
CSS and JavaScript in their respective roles. Today's lesson formalizes and
names that architecture — giving the three-layer model its proper vocabulary
and making the distinction between markup languages and programming languages
explicit.

The foundation laid in the first weeks of this challenge was pointing here all
along.

---

**Status:** ✅ Day 57 Complete — HTML & CSS Basics  
**Next:** HTML foundations — elements, tags, and document structure.