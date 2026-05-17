# 📰 Newspaper Style Article Page

> A Times of India inspired newspaper layout built with **pure HTML5 & CSS3** — no JavaScript, no frameworks.

![screenshot](screenshot.png)

## 🔴 Live Demo
👉 [Click here to view the live project](https://suryaprakash9199.github.io/newspaper-style-article-page)

---

## 📁 Project Structure

```
newspaper-style-article-page/
├── index.html                        ← Main HTML file
├── newspaper-style-artical-page.css  ← All CSS styles
├── screenshot.png                    ← Project screenshot
└── README.md                         ← You are here
```

---

## ✨ Features

- 3-column newspaper layout using `display: inline-block`
- Drop cap effect using `::first-letter` pseudo-element
- Custom text selection color using `::selection`
- Hover animations on navigation buttons
- Centered logo using `position: absolute` + `transform: translateX(-50%)`
- Image text wrapping using `float: left`
- Google Fonts — Playfair Display & Lora
- Fully built with semantic HTML5 tags

---

## 🧱 HTML — Tags Used

### Structure Tags

| Tag | Purpose | Where Used |
|-----|---------|------------|
| `<html>` | Root element of the page | Wraps entire document |
| `<head>` | Contains metadata, links | CSS link, Google Fonts, title |
| `<body>` | Visible page content | All visible elements |
| `<title>` | Browser tab title | `<title>newspaper</title>` |

### Linking External Resources

```html
<!-- Google Fonts link in <head> -->
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Lora&display=swap" rel="stylesheet">

<!-- External CSS file link -->
<link rel="stylesheet" href="newspaper-style-artical-page.css">
```

### Heading Tags

| Tag | Size | Where Used |
|-----|------|------------|
| `<h1>` | Largest | "TIMES OF INDIA" logo |
| `<h3>` | Medium | Date and author name |
| `<h4>` | Small | Article main heading |

```html
<h1 class="logo">TIMES OF INDIA</h1>
<h3 class="date">Sunday, 17 may 2026</h3>
<h4>Maharashtra government gets cold feet...</h4>
```

### Layout & Grouping Tags

| Tag | Purpose | Where Used |
|-----|---------|------------|
| `<header>` | Top section of page | Logo + sign in/subscribe |
| `<div>` | Group elements | Navigation, columns, footer |
| `<hr>` | Horizontal rule / divider line | Between header sections |
| `<p>` | Paragraph text | Article content |

```html
<header class="main-header">
  <h1 class="logo">TIMES OF INDIA</h1>
  <div id="seventh">
    <a href="..." class="nav-btn">sign in</a>
    <a href="..." class="nav-btn">subscribe</a>
  </div>
</header>
```

### Interactive / Navigation Tags

| Tag | Purpose | Where Used |
|-----|---------|------------|
| `<a>` | Hyperlink | Nav links, sign in, subscribe |
| `<button>` | Clickable button | Navigation menu, footer |
| `<img>` | Image | Uber image in article |

```html
<!-- Button wrapping a link -->
<button>
  <a href="https://indianexpress.com/">Home</a>
</button>

<!-- Image with float -->
<img src="uber.png" alt="uber" width="150" height="150">

<!-- Anchor as styled button -->
<a href="..." class="nav-btn">sign in</a>
```

### Text Formatting

| Tag | Effect | Where Used |
|-----|--------|------------|
| `<br>` | Line break | Inside article heading paragraph |

---

## 🎨 CSS — Properties & Concepts Used

### 1. Pseudo-Elements

```css
/* Drop cap — big first letter of every paragraph */
p::first-letter {
  font-size: 3em;
  font-weight: bold;
  float: left;
  line-height: 1;
  margin-right: 6px;
  color: #c0392b;
}

/* First line — bold + italic */
p::first-line {
  font-weight: bold;
  font-style: italic;
}

/* Custom text selection highlight */
::selection {
  background: #c0392b;
  color: white;
}
```

**Theory:**
- `::first-letter` — targets only the very first character of an element
- `::first-line` — targets the entire first line (depends on screen width)
- `::selection` — styles the highlighted/selected text

---

### 2. Pseudo-Classes

```css
/* Button hover effect */
button:hover {
  background-color: yellow;
  color: red;
  box-shadow: 10px 10px 10px rgba(220, 4, 11, 0.3);
  transform: translateY(-5px);
}

/* Nav button hover */
.nav-btn:hover {
  transform: translateY(-3px);
}

/* Link hover */
a:hover {
  color: red;
}
```

**Theory:**
- `:hover` — triggers when mouse is over an element
- `:active` — triggers when element is being clicked
- `:checked` — for checkboxes/radio buttons (not used here but related)

---

### 3. Box Model

```css
/* Padding — space inside element */
button {
  padding: 10px 20px;  /* top-bottom: 10px, left-right: 20px */
}

/* Margin — space outside element */
img {
  margin-right: 15px;
  margin-bottom: 5px;
}

/* Border */
#first {
  border-right: 5px solid black;  /* column separator */
}

/* Box sizing */
* {
  box-sizing: border-box;  /* padding included in width calculation */
}
```

**Box Shadow:**
```css
button:hover {
  box-shadow: 10px 10px 10px rgba(220, 4, 11, 0.3);
  /* offset-x | offset-y | blur | color */
}
```

---

### 4. Display & Layout

```css
/* Flexbox — for header alignment */
.main-header {
  display: flex;
  align-items: center;
  padding: 10px 20px;
}

/* Inline-block — 3 column newspaper layout */
#first, #second, #third {
  display: inline-block;
  width: 400px;
  height: 200px;
  vertical-align: top;
}

/* Flex for sign-in/subscribe row */
#seventh {
  display: flex;
  gap: 15px;
}
```

**Theory:**
- `display: block` — takes full width, new line
- `display: inline` — stays in same line, no width/height
- `display: inline-block` — stays in same line but accepts width/height ✅ used here
- `display: flex` — modern layout, aligns children in row/column
- `display: none` — hides element completely

---

### 5. Positioning

```css
/* Centering logo absolutely */
.logo {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
}

/* Parent must be relative for absolute child to work */
.main-header {
  position: relative;
}

/* Centering date */
.date {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
}

/* Push author to right */
.author {
  margin-left: auto;
}
```

**Theory:**
- `position: static` — default, normal flow
- `position: relative` — shifted from its normal position, acts as anchor for absolute children
- `position: absolute` — removed from flow, positioned relative to nearest `relative` parent
- `position: fixed` — stays fixed on screen while scrolling

---

### 6. CSS Transform

```css
/* Move element upward on hover */
button:hover {
  transform: translateY(-5px);
}

/* Center element horizontally */
.logo {
  transform: translateX(-50%);
}
```

**Theory — Transform functions:**
| Function | What it does |
|----------|-------------|
| `translateX(n)` | Move horizontally |
| `translateY(n)` | Move vertically |
| `rotate(deg)` | Rotate element |
| `scale(n)` | Resize element |
| `skew(deg)` | Slant/tilt element |

---

### 7. CSS Transition

```css
.nav-btn {
  transition: transform 0.2s ease;
}

/* This means: animate 'transform' over 0.2 seconds with ease timing */
```

**Theory:**
```css
transition: property duration timing-function delay;
/* Example */
transition: all 0.3s ease-in-out 0s;
```

| Timing | Effect |
|--------|--------|
| `ease` | Slow start, fast middle, slow end |
| `linear` | Same speed throughout |
| `ease-in` | Starts slow |
| `ease-out` | Ends slow |

---

### 8. Typography & Fonts

```css
/* Google Fonts imported in HTML <head> */
body {
  font-family: 'Georgia', serif;
  font-size: 16px;
  line-height: 1.7;
  color: #111;
}

h1, h2 {
  font-family: 'Times New Roman', serif;
}

h1 {
  font-size: 50px;
  text-align: center;
  color: red;
}

h4 {
  font-size: 30px;
  font-style: italic;
}
```

---

### 9. Colors & Backgrounds

```css
/* Solid color */
button {
  background-color: rgba(31, 29, 29, 0.767);
  color: white;
}

/* Semi-transparent using rgba */
box-shadow: 10px 10px 10px rgba(220, 4, 11, 0.3);
/* rgba(red, green, blue, opacity) — opacity 0=transparent, 1=solid */

/* Hex color */
color: #c0392b;
```

---

### 10. Float

```css
/* Image floats left, text wraps around it */
img {
  float: left;
  margin-right: 15px;
  margin-bottom: 5px;
}

/* Drop cap also uses float */
p::first-letter {
  float: left;
}
```

**Theory:**
- `float: left` — element moves to left, others wrap around it
- `float: right` — element moves to right
- Used for: image + text wrapping, drop caps

---

### 11. Border Radius

```css
/* Pill-shaped buttons */
button {
  border-radius: 50px;
}

/* Slightly rounded nav buttons */
.nav-btn {
  border-radius: 5px;
}
```

---

### 12. Universal Selector & Reset

```css
/* Removes default browser spacing from ALL elements */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

**Theory:** Every browser adds default margin/padding to elements. This resets them so your design looks same on all browsers.

---

## 🔧 CSS Concepts Summary Table

| Concept | Property Used | Effect |
|---------|--------------|--------|
| Pseudo-element | `::first-letter` | Drop cap |
| Pseudo-element | `::first-line` | Bold italic first line |
| Pseudo-element | `::selection` | Red highlight on select |
| Pseudo-class | `:hover` | Button lift + color change |
| Box Model | `padding`, `margin`, `border` | Spacing and columns |
| Box Shadow | `box-shadow` | Shadow on hover |
| Display | `inline-block` | 3-column layout |
| Display | `flex` | Header alignment |
| Position | `absolute` + `relative` | Centered logo |
| Transform | `translateX`, `translateY` | Center + hover lift |
| Transition | `transition: transform 0.2s` | Smooth animation |
| Float | `float: left` | Image text wrap |
| Border Radius | `border-radius: 50px` | Pill buttons |
| Typography | `font-family`, `font-size` | Google Fonts |
| Color | `rgba()`, `#hex` | Transparent shadow |

---

## 👤 Author

**Surya Prakash**
- GitHub: [@SURYAPRAKASH9199](https://github.com/SURYAPRAKASH9199)
- Project created: May 17, 2026

---

## 📌 What I Learned

- How to build multi-column layouts without CSS Grid or Flexbox using `inline-block`
- How `::first-letter` creates drop caps like real newspapers
- How `position: absolute` + `transform: translateX(-50%)` perfectly centers an element
- How `float` allows text to wrap around images
- How pseudo-classes like `:hover` create interactive animations
- How Google Fonts are imported and applied

---

*Built with ❤️ using only HTML5 and CSS3*
