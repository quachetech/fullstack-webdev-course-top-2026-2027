# Practice Note: Links & Images
**#190DaysTOPFoundations**
*Foundations Course | HTML & CSS Module*
11 June 2026

---

## Overview

This practical built a small two-page website demonstrating absolute links,
relative links, and image embedding using both relative paths from different
directory depths.

---

## Project Structure

```
links-images/
├── index.html
├── pages/
│   └── about.html
└── images/
    └── dog.jpg
```

---

## Step-by-Step Walkthrough

### 1. Create the Project Directory and Entry File

```bash
mkdir links-images
cd links-images
touch index.html
code index.html
```

Add the boilerplate and a main heading:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Links & Images</title>
    </head>
    <body>
        <h1>Homepage</h1>
    </body>
</html>
```

---

### 2. Add an Absolute Link

Add an anchor element pointing to an external page with `target="_blank"` and
`rel="noreferrer"` for security:

```html
<a href="https://www.theodinproject.com/about" target="_blank" rel="noreferrer">
    About The Odin Project
</a>
```

This is an **absolute link** — it includes the full scheme, domain, and path.
It opens in a new tab without giving the destination page access to this one.

---

### 3. Create the About Page

```bash
touch about.html
code about.html
```

Add boilerplate and a heading:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Links & Images</title>
    </head>
    <body>
        <h1>About Page</h1>
    </body>
</html>
```

Add a relative link to it from `index.html`:

```html
<a href="about.html">About</a>
```

---

### 4. Move About Page into a `/pages` Directory

```bash
mkdir pages
mv about.html pages/
```

The relative link in `index.html` must now be updated to reflect the new
location:

```html
<a href="./pages/about.html">About</a>
```

The `./` means "starting from the current directory" — the same logic used
when navigating directories in the terminal.

---

### 5. Add an Images Directory and Download the Image

```bash
mkdir images
```

Download the image from Unsplash, move it into `/images`, and rename it
`dog.jpg`.

---

### 6. Embed the Image in `index.html`

Start with just the `src` attribute, then progressively add `alt` and size
dimensions:

```html
<img src="./images/dog.jpg" alt="Black dog on yellow background" height="310" width="310">
```

The path `./images/dog.jpg` works because `index.html` and the `images/`
folder are in the same directory (`links-images/`).

---

### 7. Embed the Image in `about.html`

`about.html` lives inside `pages/` — one level deeper than `index.html`. To
reach the `images/` folder from inside `pages/`, the path must first go up one
level using `../`:

```html
<img src="../images/dog.jpg" alt="Black dog on yellow background" height="310" width="310">
```

`../` means "go up one directory." From `pages/`, going up one level lands
back in `links-images/`, where `images/` is accessible.

---

## Final Code

### `index.html`

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Links & Images</title>
    </head>
    <body>
        <h1>Homepage</h1>
        <a href="https://www.theodinproject.com/about" target="_blank" rel="noreferrer">
            About The Odin Project
        </a>
        <a href="./pages/about.html">About</a>
        <img src="./images/dog.jpg" alt="Black dog on yellow background" height="310" width="310">
    </body>
</html>
```

### `pages/about.html`

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Links & Images</title>
    </head>
    <body>
        <h1>About Page</h1>
        <img src="../images/dog.jpg" alt="Black dog on yellow background" height="310" width="310">
    </body>
</html>
```

---

## Key Observations

**Relative paths are positional.** The same image requires a different path
depending on where the file referencing it sits in the directory tree.
`index.html` uses `./images/dog.jpg` because it is at the same level as
`images/`. `about.html` uses `../images/dog.jpg` because it is one level
deeper inside `pages/` and must climb back up first. The path describes a
journey through the file system, not a fixed address.

**Moving a file breaks its links.** When `about.html` moved from
`links-images/` into `links-images/pages/`, the relative link in `index.html`
pointing to it immediately broke and had to be updated. This is a practical
lesson in why project structure decisions made early matter — reorganising
files later means updating every path that references them.

**Progressive attribute building.** Adding attributes to the `<img>` element
one at a time (`src` first, then `alt`, then dimensions) mirrors the practice
of building incrementally and testing at each step rather than writing
everything at once and debugging later.

---

## Connection to Previous Learning

**Days 31–33 (CLI — File System):** The `./` and `../` path notation used in
HTML relative paths is identical to the notation used in the terminal. `cd ..`
and `src="../images/dog.jpg"` are the same movement described in two different
contexts. The CLI groundwork makes HTML paths immediately readable.