# 📰 Newspaper Style Article Page

> A pixel-perfect, Times of India inspired newspaper layout — crafted entirely with **pure HTML5 & CSS3**.  
> No JavaScript. No frameworks. No shortcuts. Just clean, handwritten code.
---

## 🔴 Live Demo
👉 [Click here to view the live project](https://suryaprakash9199.github.io/newspaper-style-article-page)

---

## 💡 About This Project

This project is a hands-on demonstration of core CSS concepts applied to a real-world design challenge — replicating the layout and feel of a professional newspaper website.

The goal was simple: **build something that looks like it was made by a developer who actually understands CSS** — not someone who just copied Stack Overflow.

Every element — the centered logo, the drop caps, the 3-column layout, the hover animations — was intentionally placed using specific CSS techniques, not luck.

---

## 📁 File Structure

```
newspaper-style-article-page/
├── newspaper-style-artical-page.html   ← Main HTML structure
├── newspaper-style-artical-page.css    ← All styling
├── Screenshot 2026-05-17 144217.png    ← Project screenshot 1
├── Screenshot 2026-05-17 144335.png    ← Project screenshot 2
└── README.md                           ← Project documentation
```

---

## ✨ Key Features

- **3-Column Newspaper Layout** — built using `display: inline-block` and `vertical-align`, replicating how real newspaper columns work
- **Drop Cap Effect** — `::first-letter` pseudo-element creates the classic large first letter seen in editorial writing
- **Custom Text Selection** — `::selection` changes highlight color to match the brand theme
- **First Line Styling** — `::first-line` makes the opening line of every article bold and italic
- **Perfectly Centered Logo** — achieved using `position: absolute` combined with `transform: translateX(-50%)` — a professional centering technique
- **Image Text Wrapping** — `float: left` makes the Uber image sit naturally inside the article text
- **Smooth Hover Animations** — buttons lift upward with `transform: translateY()` and `transition` for a polished feel
- **Pill-shaped Navigation** — `border-radius: 50px` gives the nav buttons a modern rounded look
- **Google Fonts Integration** — Playfair Display for headings, Lora for body — both chosen to match newspaper typography
- **CSS Reset** — universal selector resets all browser defaults for consistent cross-browser rendering

---

## 🧱 HTML Concepts Used

| Concept | Theory |
|---------|--------|
| Semantic Structure | `<header>`, `<div>`, `<p>`, `<hr>` used meaningfully to define page sections |
| Heading Hierarchy | `<h1>` for logo, `<h3>` for date/author, `<h4>` for article heading — correct heading order maintained |
| Hyperlinks | `<a>` tags connect to real Indian Express pages for Home, World, India, Business, etc. |
| Buttons | `<button>` wraps navigation links with custom styling |
| External Resources | Google Fonts and CSS file linked via `<link rel="stylesheet">` in `<head>` |
| Image Embedding | `<img>` with `alt`, `width`, `height` attributes — accessibility and layout both considered |
| Inline Text | `<br>` used for controlled line breaks inside paragraphs |

---

## 🎨 CSS Concepts Used

### Pseudo-Elements
These target specific parts of elements without adding extra HTML tags.

| Pseudo-Element | What It Does Here |
|---------------|-------------------|
| `::first-letter` | Creates the large red drop cap on paragraph openings |
| `::first-line` | Makes the first line of every paragraph bold and italic |
| `::selection` | Changes the highlight color to red + white when user selects text |

---

### Pseudo-Classes
These apply styles based on user interaction or element state.

| Pseudo-Class | What It Does Here |
|-------------|-------------------|
| `:hover` | Buttons change color, lift up, and glow when mouse hovers |
| `a:hover` | Navigation links turn red when hovered |

---

### Box Model
Every element in CSS is a box. This project uses all four parts of the box model.

| Property | Where Used |
|----------|-----------|
| `padding` | Inside spacing for buttons and nav items |
| `margin` | Gap between image and text, between elements |
| `border` | `border-right` creates the vertical column dividers |
| `box-sizing: border-box` | Ensures padding does not break the column widths |
| `box-shadow` | Red glow shadow appears on button hover |

---

### Display & Layout

| Property | What It Does Here |
|----------|-------------------|
| `display: inline-block` | Creates the 3-column newspaper layout |
| `display: flex` | Aligns header items (logo, sign in, subscribe) in a row |
| `vertical-align: top` | Keeps all 3 columns aligned from the top |
| `gap` | Adds space between flex items in the header |
| `margin-left: auto` | Pushes the author name to the far right |

---

### Positioning

| Property | Where Used |
|----------|-----------|
| `position: relative` | Set on header so absolute children position relative to it |
| `position: absolute` | Used on logo and date to center them precisely |
| `left: 50%` + `transform: translateX(-50%)` | The correct professional technique to center any element |
| `z-index: 1` | Keeps the sign-in buttons above the absolute logo |

---

### CSS Transform

| Function | Where Used |
|----------|-----------|
| `translateX(-50%)` | Horizontal centering of logo and date |
| `translateY(-5px)` | Buttons lift upward on hover |

---

### CSS Transition

Smooth animation is added to button hover effects. Without transition, the hover change is instant and jarring. With transition, it feels smooth and professional.

| Property | Value | Effect |
|----------|-------|--------|
| `transition` | `transform 0.2s ease` | Nav buttons smoothly lift on hover |

---

### Float

| Property | Where Used |
|----------|-----------|
| `float: left` | Uber image floats left so article text naturally wraps around it |
| `float: left` on `::first-letter` | Drop cap letter sits to the left while text flows beside it |

---

### Typography

| Property | Where Used |
|----------|-----------|
| `font-family` | Georgia/serif for body, Times New Roman for headings, Playfair Display + Lora from Google Fonts |
| `font-size` | 50px logo, 30px article heading, 20px body text |
| `font-style: italic` | Article main heading styled italic |
| `font-weight: bold` | Drop cap and first-line emphasis |
| `text-align: center` | Logo and navigation centered |
| `line-height` | Controls spacing between lines of text |
| `text-decoration` | Underline on sign in / subscribe buttons |

---

### Colors & Transparency

| Format | Where Used |
|--------|-----------|
| Named colors — `red`, `white`, `black` | Logo, link colors |
| Hex — `#c0392b`, `#555` | Drop cap red, border colors |
| RGBA — `rgba(220, 4, 11, 0.3)` | Semi-transparent red glow on box-shadow |

---

### Border & Border Radius

| Property | Where Used |
|----------|-----------|
| `border-right: 5px solid black` | Creates vertical dividers between the 3 columns |
| `border-radius: 50px` | Pill-shaped navigation buttons |
| `border-radius: 5px` | Slightly rounded sign-in/subscribe buttons |
| `border: 2px solid #555` | Outline on nav buttons |

---

## 📊 Complete CSS Properties Summary Table

| Category | Properties Used |
|----------|----------------|
| Pseudo-Elements | `::first-letter`, `::first-line`, `::selection` |
| Pseudo-Classes | `:hover` |
| Box Model | `margin`, `padding`, `border`, `box-shadow`, `box-sizing` |
| Display | `inline-block`, `flex` |
| Positioning | `relative`, `absolute`, `z-index` |
| Transform | `translateX()`, `translateY()` |
| Transition | `transition`, `ease` timing function |
| Float | `float: left` |
| Typography | `font-family`, `font-size`, `font-style`, `font-weight`, `text-align`, `line-height` |
| Colors | Hex, RGBA, named colors |
| Borders | `border`, `border-right`, `border-radius` |
| Layout | `width`, `height`, `vertical-align`, `gap`, `margin-left: auto` |
| Reset | Universal selector `*` with margin, padding, box-sizing |

---

## 🧠 What I Learned Building This

- How real newspaper column layouts work without CSS Grid
- Why `position: absolute` + `transform: translateX(-50%)` is the right way to center an element
- How `::first-letter` and `::first-line` give editorial-style polish without extra HTML
- How `float` was used for layouts before Flexbox — and still works perfectly for image wrapping
- How `box-sizing: border-box` prevents columns from breaking when padding is added
- How `rgba()` enables transparent colors for subtle effects like shadows
- How Google Fonts are loaded via `<link>` in `<head>` and applied in CSS

---

## 👤 Author

**Surya Prakash**
- GitHub: [@SURYAPRAKASH9199](https://github.com/SURYAPRAKASH9199)

---

*Built with ❤️ using only HTML5 and CSS3 — May 2026*
