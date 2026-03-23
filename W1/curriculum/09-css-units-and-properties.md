# CSS Units and Properties

## Learning Objectives

By the end of this lesson, you will be able to:

- [ ] Explain what CSS units are and why they matter
- [ ] Use absolute units (px) for precise measurements
- [ ] Use relative units (%, em, rem) for flexible sizing
- [ ] Use viewport units (vh, vw) for screen-based sizing
- [ ] Choose the right unit for different situations
- [ ] Use different color formats (named, hex, rgb, rgba)
- [ ] Apply additional text properties (letter-spacing, word-spacing, text-transform)
- [ ] Understand when to use each unit type

## Prerequisites

**Required**: You should have completed:
- "How the Internet Works" (Lesson 01) - to understand how webpages are delivered
- "Basic HTML Structure" (Lesson 02) - to understand HTML tags and structure
- "Text in HTML" (Lesson 03) - to understand text elements
- "Lists in HTML" (Lesson 04) - to understand lists
- "Links and Images" (Lesson 05) - to understand links and images
- "Classes and Semantic HTML" (Lesson 06) - to understand classes
- "CSS Fundamentals" (Lesson 07) - to understand CSS basics
- "CSS Selectors" (Lesson 08) - to understand how to target elements

**Estimated Reading Time**: 35-40 minutes

**What You'll Need**: A text editor (like VS Code) and a web browser

---

## What Are CSS Units?

CSS units tell the browser **how much** of something to apply. When you write `font-size: 16px`, the `px` is the unit.

### Why Units Matter

Every measurement in CSS needs a unit:

```css
h1 {
    font-size: 32px;      /* px = pixels (unit) */
    color: blue;          /* blue = named color (no unit needed) */
}
```

- **Properties that need units**: `font-size`, `width`, `height`, `margin`, `padding`
- **Properties that don't need units**: `color`, `font-weight`, `text-align`

### The Measurement Analogy

Think of CSS units like measuring tools in real life:

| Real Life | CSS | When to Use |
|-----------|-----|-------------|
| **Ruler** (fixed length) | `px` (pixels) | Precise, fixed sizes |
| **Percentage of a pizza** | `%` (percentage) | Relative to container |
| **Your hand span** | `em` | Relative to parent's size |
| **A standard ruler everyone has** | `rem` | Relative to root (consistent) |
| **Screen size** | `vh`, `vw` | Relative to viewport |

Each tool has a purpose - you wouldn't measure a room with a teaspoon!

### Success Criteria

You understand CSS units if you can:
- Explain what CSS units are
- Identify which properties need units
- Use the measurement analogy

---

## Absolute Units: Pixels (px)

**Pixels (px)** are the most common absolute unit. One pixel is one tiny dot on your screen.

### What Is a Pixel?

```
A pixel is the smallest dot your screen can display.

Your entire screen is made of millions of tiny dots (pixels).
When you set font-size: 16px, the text is 16 dots tall.

Example: A 16px letter 'A' on screen:
█
██
█ █
████
█   █
█   █
↑
16 pixels tall
```

### Pixel Syntax

```css
selector {
    property: valuepx;
}
```

- `value` - A number (no decimals needed, but allowed)
- `px` - The unit (must come immediately after the number)
- **No space** between number and `px`

### Pixel Examples

```css
/* Font size in pixels */
h1 {
    font-size: 32px;    /* Heading is 32 pixels tall */
}

p {
    font-size: 16px;    /* Paragraph text is 16 pixels tall */
}

/* Border width in pixels */
.highlight {
    border-width: 2px;   /* Border is 2 pixels thick */
}

/* Small precise values */
.icon {
    font-size: 14px;     /* Small text */
}
```

### When to Use Pixels

**Use pixels when**:
- You need precise, fixed sizes
- Creating borders (1px, 2px, etc.)
- Small text that shouldn't change
- Icons or small elements

**Don't use pixels when**:
- You want text to scale with user preferences
- Creating responsive layouts (use % or rem instead)
- Building accessible websites (use rem instead)

### Pixel Pros and Cons

**Pros**:
- Precise and predictable
- Easy to understand
- Works the same everywhere

**Cons**:
- Doesn't scale with user preferences
- Not flexible for responsive design
- Can be too small on high-resolution screens

### Success Criteria

You understand pixels if you can:
- Explain what a pixel is
- Write pixel values correctly (number + px, no space)
- Identify when to use pixels

---

## Relative Units

Relative units are **relative to something else**. They change based on context.

### Percentage (%)

**Percentage** is relative to the **parent element**.

#### Percentage Syntax

```css
selector {
    property: value%;
}
```

- `value` - A number
- `%` - The unit (no space between number and %)

#### Percentage Examples

```css
/* Image width as percentage of container */
img {
    width: 100%;    /* Image fills 100% of its container */
}

.thumbnail {
    width: 50%;     /* Image fills 50% of its container */
}

/* Text size as percentage of parent */
.small-text {
    font-size: 80%;    /* 80% of parent's font size */
}

.large-text {
    font-size: 150%;   /* 150% of parent's font size */
}
```

#### How Percentage Works

```
Parent container is 400px wide
┌────────────────────────────────────┐
│                                    │
│   Child at 100% = 400px           │
│   ┌────────────────────────────┐  │
│   │                            │  │
│   └────────────────────────────┘  │
│                                    │
│   Child at 50% = 200px            │
│   ┌──────────────────┐            │
│   │                  │            │
│   └──────────────────┘            │
│                                    │
│   Child at 25% = 100px            │
│   ┌──────────┐                    │
│   │          │                    │
│   └──────────┘                    │
│                                    │
└────────────────────────────────────┘
```

#### When to Use Percentage

**Use percentage when**:
- Creating flexible, responsive layouts
- Making images scale with their container
- Creating fluid width elements

**Example**:
```css
/* Responsive image */
.article-image {
    width: 100%;     /* Always fills container, whatever size it is */
}

/* Half-width element */
.sidebar {
    width: 50%;      /* Always half of parent */
}
```

---

### em Unit

**em** is relative to the **parent element's font-size**.

#### em Syntax

```css
selector {
    property: valueem;
}
```

- `1em` = The parent element's font-size
- `2em` = Twice the parent's font-size
- `0.5em` = Half the parent's font-size

#### How em Works

```css
/* Parent element */
.parent {
    font-size: 20px;
}

/* Child with em */
.child {
    font-size: 1em;    /* 1 × 20px = 20px */
}

.child-large {
    font-size: 2em;    /* 2 × 20px = 40px */
}

.child-small {
    font-size: 0.75em; /* 0.75 × 20px = 15px */
}
```

#### em Calculation Example

```
Parent has font-size: 16px

Child with 1em     = 1 × 16px = 16px
Child with 1.5em   = 1.5 × 16px = 24px
Child with 2em     = 2 × 16px = 32px
Child with 0.5em   = 0.5 × 16px = 8px
```

#### The em Compounding Problem

**Problem**: em values compound (multiply) when nested!

```html
<div style="font-size: 16px;">
    Parent (16px)
    <div style="font-size: 1.5em;">
        Child (1.5 × 16px = 24px)
        <div style="font-size: 1.5em;">
            Grandchild (1.5 × 24px = 36px!) ← Oops! Not what we wanted
        </div>
    </div>
</div>
```

This is why `rem` is often preferred (see next section).

#### When to Use em

**Use em when**:
- Sizing should relate to parent's text size
- Creating scalable components
- You want elements to scale together

**Example**:
```css
.button {
    font-size: 16px;
    padding: 0.5em 1em;    /* Padding scales with font size */
}

/* If you later change font-size to 20px,
   padding automatically increases too! */
```

---

### rem Unit

**rem** stands for **root em**. It's relative to the **root element's font-size** (the `<html>` element).

#### rem Syntax

```css
selector {
    property: valuerem;
}
```

- `1rem` = The root element's font-size (usually 16px)
- `2rem` = Twice the root's font-size
- `0.5rem` = Half the root's font-size

#### How rem Works

```css
/* Default: html element has font-size: 16px */

h1 {
    font-size: 2rem;    /* 2 × 16px = 32px */
}

p {
    font-size: 1rem;    /* 1 × 16px = 16px */
}

.small {
    font-size: 0.875rem; /* 0.875 × 16px = 14px */
}
```

#### rem vs em Comparison

```
ROOT (html): font-size: 16px
│
├── PARENT: font-size: 2rem (32px)
│   │
│   ├── CHILD with 1em: 1 × 32px = 32px (relative to parent)
│   │
│   └── CHILD with 1rem: 1 × 16px = 16px (relative to root!)
```

**rem always refers to the root, not the parent!**

#### Why rem is Preferred

**rem solves the compounding problem**:

```html
<html style="font-size: 16px;">
    Root (16px)
    <div style="font-size: 1.5rem;">
        Child (1.5 × 16px = 24px)
        <div style="font-size: 1.5rem;">
            Grandchild (1.5 × 16px = 24px) ← Same! Predictable!
        </div>
    </div>
</html>
```

#### When to Use rem

**Use rem when**:
- You want consistent, predictable sizing
- Creating accessible websites (respects user preferences)
- Avoiding the em compounding problem
- Most font sizing

**Example**:
```css
/* Good practice: Use rem for font sizes */
body {
    font-size: 1rem;     /* Base text size */
}

h1 {
    font-size: 2rem;     /* Double the base */
}

h2 {
    font-size: 1.5rem;   /* 1.5× the base */
}

h3 {
    font-size: 1.25rem;  /* 1.25× the base */
}
```

---

### Success Criteria for Relative Units

You understand relative units if you can:
- Explain the difference between %, em, and rem
- Calculate em and rem values
- Explain the em compounding problem
- Choose between em and rem

---

## Viewport Units: vh and vw

**Viewport units** are relative to the **browser window size** (the viewport).

### What Is the Viewport?

The **viewport** is the visible area of your webpage in the browser window.

```
┌─────────────────────────────────────────┐
│ Browser chrome (tabs, address bar)      │
├─────────────────────────────────────────┤
│                                         │
│         THIS IS THE VIEWPORT            │
│                                         │
│    ← Viewport Width (vw) →              │
│                                         │
│    ↑                                    │
│    Viewport Height (vh)                 │
│    ↓                                    │
│                                         │
│                                         │
└─────────────────────────────────────────┘
```

### vh (Viewport Height)

**vh** = 1% of the viewport height

- `1vh` = 1% of viewport height
- `100vh` = 100% of viewport height (full screen height)

```css
/* Full-height section */
.hero {
    height: 100vh;    /* Takes up entire viewport height */
}

/* Half-height section */
.half-screen {
    height: 50vh;     /* Takes up half the viewport height */
}
```

### vw (Viewport Width)

**vw** = 1% of the viewport width

- `1vw` = 1% of viewport width
- `100vw` = 100% of viewport width (full screen width)

```css
/* Responsive font size */
.title {
    font-size: 5vw;    /* Font scales with screen width */
}

/* Quarter-width element */
.quarter {
    width: 25vw;       /* 25% of viewport width */
}
```

### When to Use Viewport Units

**Use vh when**:
- Creating full-screen sections
- Making elements fill the visible height

**Use vw when**:
- Creating responsive typography
- Elements should scale with screen width

**Example**:
```css
/* Full-screen hero section */
.hero {
    height: 100vh;           /* Full viewport height */
    width: 100%;             /* Full container width */
}

/* Hero title that scales with screen */
.hero-title {
    font-size: 8vw;          /* Big on large screens, small on phones */
}
```

### Caution with Viewport Units

**Be careful**:
- `100vw` includes the scrollbar, which can cause horizontal overflow
- Text scaled with `vw` can become very small on phones
- Always test on different screen sizes!

---

## Unit Comparison Table

### Quick Reference

| Unit | Relative To | Best For | Example |
|------|-------------|----------|---------|
| **px** | Fixed size | Borders, small precise values | `border: 1px solid black;` |
| **%** | Parent element | Flexible layouts, images | `width: 50%;` |
| **em** | Parent's font-size | Scalable components | `padding: 1em;` |
| **rem** | Root font-size | Font sizes, spacing | `font-size: 1.5rem;` |
| **vh** | Viewport height | Full-screen sections | `height: 100vh;` |
| **vw** | Viewport width | Responsive text | `font-size: 5vw;` |

### When to Use Each Unit

```css
/* FONT SIZES: Use rem */
body { font-size: 1rem; }
h1 { font-size: 2.5rem; }

/* WIDTHS: Use % for flexible, px for fixed */
.container { width: 100%; }
.sidebar { width: 30%; }
.icon { width: 32px; }

/* HEIGHTS: Use vh for full-screen, auto for content */
.hero { height: 100vh; }
.content { height: auto; }

/* BORDERS: Use px */
.card { border: 1px solid gray; }

/* SPACING: Use rem for consistency */
.section { margin-top: 2rem; }
```

### Success Criteria

You can choose units if you can:
- Match the right unit to the right use case
- Explain why rem is preferred for font sizes
- Know when to use px vs relative units

---

## Expanding Color Values

You've used named colors like `red`, `blue`, and `yellow`. Now let's learn more ways to specify colors.

### Named Colors

CSS has **147 named colors** built in.

```css
h1 {
    color: red;           /* Basic named color */
    background-color: blue;
}

.highlight {
    background-color: yellow;
}

.special {
    color: tomato;        /* Less common named color */
    background-color: cornsilk;
}
```

**Pros**: Easy to remember, readable
**Cons**: Limited selection, hard to match designs

### Hex Colors (Hexadecimal)

**Hex colors** use 6 characters (0-9, A-F) to specify colors.

#### Hex Syntax

```css
selector {
    color: #RRGGBB;
}
```

- `RR` = Red value (00 to FF)
- `GG` = Green value (00 to FF)
- `BB` = Blue value (00 to FF)

#### Hex Examples

```css
h1 {
    color: #FF0000;    /* Red (FF red, 00 green, 00 blue) */
}

p {
    color: #000000;    /* Black (00 red, 00 green, 00 blue) */
}

.highlight {
    background-color: #FFFF00;    /* Yellow */
}

.dark-text {
    color: #333333;    /* Dark gray */
}
```

#### Hex Shorthand

If both characters are the same, you can shorten it:

```css
/* Long form → Shorthand */
#FF0000 → #F00     /* Red */
#00FF00 → #0F0     /* Green */
#0000FF → #00F     /* Blue */
#FFFFFF → #FFF     /* White */
#000000 → #000     /* Black */
#333333 → #333     /* Dark gray */
```

#### Common Hex Colors

| Color | Hex | Shorthand |
|-------|-----|-----------|
| Black | #000000 | #000 |
| White | #FFFFFF | #FFF |
| Red | #FF0000 | #F00 |
| Green | #00FF00 | #0F0 |
| Blue | #0000FF | #00F |
| Yellow | #FFFF00 | #FF0 |
| Cyan | #00FFFF | #0FF |
| Magenta | #FF00FF | #F0F |
| Gray | #808080 | (can't shorten) |

---

### RGB Colors

**RGB** stands for Red, Green, Blue. Each value is 0-255.

#### RGB Syntax

```css
selector {
    color: rgb(red, green, blue);
}
```

- `red` = 0 to 255
- `green` = 0 to 255
- `blue` = 0 to 255

#### RGB Examples

```css
h1 {
    color: rgb(255, 0, 0);       /* Red (255 red, 0 green, 0 blue) */
}

p {
    color: rgb(0, 0, 0);         /* Black */
}

.highlight {
    background-color: rgb(255, 255, 0);    /* Yellow */
}

.dark-text {
    color: rgb(51, 51, 51);      /* Dark gray */
}
```

#### RGB vs Hex Comparison

```css
/* These are the SAME color: */
color: #FF0000;
color: rgb(255, 0, 0);

/* These are the SAME color: */
color: #336699;
color: rgb(51, 102, 153);
```

---

### RGBA Colors (With Transparency!)

**RGBA** adds **Alpha** (transparency) to RGB.

#### RGBA Syntax

```css
selector {
    color: rgba(red, green, blue, alpha);
}
```

- `red` = 0 to 255
- `green` = 0 to 255
- `blue` = 0 to 255
- `alpha` = 0 to 1 (0 = invisible, 1 = solid)

#### Alpha Values

| Alpha | Meaning |
|-------|---------|
| 1 | Fully visible (solid) |
| 0.9 | 90% visible |
| 0.75 | 75% visible |
| 0.5 | 50% visible (semi-transparent) |
| 0.25 | 25% visible |
| 0 | Invisible |

#### RGBA Examples

```css
/* Semi-transparent background */
.overlay {
    background-color: rgba(0, 0, 0, 0.5);    /* Black at 50% opacity */
}

/* Slightly transparent text */
.faded-text {
    color: rgba(0, 0, 0, 0.7);    /* Dark gray at 70% opacity */
}

/* Semi-transparent red */
.light-red {
    background-color: rgba(255, 0, 0, 0.3);    /* Red at 30% opacity */
}
```

#### RGBA Practical Example

```html
<div class="card">
    <h2>Card Title</h2>
    <p>Card content goes here.</p>
</div>
```

```css
.card {
    /* Semi-transparent white background */
    background-color: rgba(255, 255, 255, 0.9);

    /* Or semi-transparent black for dark overlay */
    /* background-color: rgba(0, 0, 0, 0.8); */
}
```

---

### Success Criteria for Colors

You understand color values if you can:
- Use named colors, hex, and RGB interchangeably
- Explain the difference between RGB and RGBA
- Create semi-transparent colors with RGBA
- Use hex shorthand when possible

---

## More Text Properties

Let's learn more properties to style text.

### letter-spacing

**letter-spacing** controls the space between letters.

```css
selector {
    letter-spacing: value;
}
```

- `normal` = Default spacing
- `value` = A length (usually in em or px)

```css
h1 {
    letter-spacing: 0.1em;    /* Slightly wider spacing */
}

.spaced-out {
    letter-spacing: 0.25em;   /* Very wide spacing */
}

.tight {
    letter-spacing: -0.05em;  /* Tighter spacing (negative) */
}
```

**When to use**: Headlines, creative effects, readability adjustments

---

### word-spacing

**word-spacing** controls the space between words.

```css
selector {
    word-spacing: value;
}
```

```css
p {
    word-spacing: 0.5em;    /* More space between words */
}

.tight-words {
    word-spacing: -0.1em;   /* Less space between words */
}
```

**When to use**: Adjusting readability, creative typography

---

### text-transform

**text-transform** changes the capitalization of text.

```css
selector {
    text-transform: value;
}
```

| Value | Effect | Example |
|-------|--------|---------|
| `none` | No change | "Hello World" |
| `uppercase` | ALL CAPS | "HELLO WORLD" |
| `lowercase` | all lowercase | "hello world" |
| `capitalize` | First Letter Of Each Word | "Hello World" |

```css
h1 {
    text-transform: uppercase;    /* ALL CAPS */
}

nav a {
    text-transform: capitalize;   /* Capitalize Each Word */
}

.subtitle {
    text-transform: lowercase;    /* all lowercase */
}
```

**When to use**: Navigation menus, headings, consistent styling

---

### text-indent

**text-indent** indents the first line of text.

```css
selector {
    text-indent: value;
}
```

```css
p {
    text-indent: 2em;    /* Indent first line by 2em */
}

article p {
    text-indent: 1.5rem; /* Indent first line by 1.5rem */
}
```

**When to use**: Paragraphs in articles (like in books and newspapers)

---

### font-style

**font-style** makes text italic or normal.

```css
selector {
    font-style: value;
}
```

| Value | Effect |
|-------|--------|
| `normal` | Normal text |
| `italic` | Italic text |
| `oblique` | Slanted text (rarely used) |

```css
em {
    font-style: italic;    /* Make emphasized text italic */
}

.quote {
    font-style: italic;    /* Style quotes as italic */
}

.no-italic {
    font-style: normal;    /* Remove italic from element */
}
```

**Note**: The `<em>` HTML tag already makes text italic, but you can control it with CSS.

---

### Success Criteria for Text Properties

You understand text properties if you can:
- Use letter-spacing and word-spacing
- Transform text case with text-transform
- Indent first lines with text-indent
- Control italic styling with font-style

---

## Putting It All Together

Let's create a complete webpage using units, colors, and text properties.

### Complete Example: Styled Article Page

**File: index.html**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS Units and Properties - Demo</title>

    <!-- Link to external CSS file -->
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <!-- Hero section with full viewport height -->
    <header class="hero">
        <h1 class="hero-title">Understanding CSS Units</h1>
        <p class="hero-subtitle">A Complete Guide for Beginners</p>
    </header>

    <!-- Main content -->
    <main class="content">
        <article class="article">
            <h2 class="article-title">Why Units Matter</h2>

            <p class="article-text">
                CSS units determine how elements are sized on your webpage.
                Choosing the right unit makes your website flexible and
                accessible to all users.
            </p>

            <p class="article-text">
                Pixels (px) give you precise control, while relative units
                like rem and em adapt to user preferences. Viewport units
                (vh and vw) let you create full-screen experiences.
            </p>

            <!-- Highlighted box -->
            <div class="highlight-box">
                <h3 class="highlight-title">Pro Tip</h3>
                <p class="highlight-text">
                    Use rem for font sizes and spacing. It respects user
                    preferences and avoids the em compounding problem!
                </p>
            </div>

            <h3 class="section-title">Color Values</h3>

            <p class="article-text">
                CSS offers multiple ways to specify colors. Named colors
                are easy to remember, while hex and RGB give you precise
                control over every shade.
            </p>

            <!-- Color examples -->
            <div class="color-demo">
                <div class="color-box color-red">Red</div>
                <div class="color-box color-green">Green</div>
                <div class="color-box color-blue">Blue</div>
                <div class="color-box color-transparent">Semi-transparent</div>
            </div>
        </article>
    </main>

    <!-- Footer -->
    <footer class="footer">
        <p class="copyright">© 2024 CSS Learning Guide</p>
    </footer>
</body>
</html>
```

**File: styles.css**
```css
/* ============================================
   ROOT STYLES
   Using rem? This is what it's relative to!
   ============================================ */
html {
    font-size: 16px;    /* 1rem = 16px (default) */
}

/* ============================================
   BODY STYLES
   ============================================ */
body {
    font-family: Arial, sans-serif;
    color: #333333;
    background-color: #f5f5f5;
    margin: 0;
    padding: 0;
}

/* ============================================
   HERO SECTION
   Using vh for full viewport height
   ============================================ */
.hero {
    /* Full viewport height */
    height: 100vh;

    /* Center content */
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    /* Background with semi-transparent overlay */
    background-color: #2c3e50;

    /* Text color */
    color: #ffffff;
}

.hero-title {
    /* Large responsive font size */
    font-size: 3rem;
    font-weight: bold;

    /* Wide letter spacing for effect */
    letter-spacing: 0.1em;

    /* Uppercase transformation */
    text-transform: uppercase;

    margin: 0;
}

.hero-subtitle {
    font-size: 1.25rem;
    color: rgba(255, 255, 255, 0.8);    /* Semi-transparent white */
    margin-top: 0.5rem;
}

/* ============================================
   MAIN CONTENT
   Using % for flexible width
   ============================================ */
.content {
    width: 90%;           /* 90% of viewport */
    max-width: 800px;     /* But never wider than 800px */
    margin: 2rem auto;    /* Center with auto margins */
}

.article {
    background-color: #ffffff;
    padding: 2rem;
}

/* ============================================
   ARTICLE TYPOGRAPHY
   Using rem for all sizes
   ============================================ */
.article-title {
    font-size: 1.75rem;
    color: #2c3e50;
    text-transform: capitalize;
    margin-top: 0;
}

.article-text {
    font-size: 1rem;
    line-height: 1.6;

    /* Indent first line like a book */
    text-indent: 1.5rem;

    margin-bottom: 1rem;
}

.section-title {
    font-size: 1.25rem;
    color: #2c3e50;
    margin-top: 2rem;
}

/* ============================================
   HIGHLIGHT BOX
   Using rgba for transparency
   ============================================ */
.highlight-box {
    /* Semi-transparent blue background */
    background-color: rgba(52, 152, 219, 0.15);

    /* Solid blue left border */
    border-left: 4px solid #3498db;

    padding: 1rem;
    margin: 1.5rem 0;
}

.highlight-title {
    font-size: 1rem;
    font-weight: bold;
    color: #2980b9;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    margin: 0 0 0.5rem 0;
}

.highlight-text {
    font-size: 0.9rem;
    font-style: italic;
    color: #34495e;
    margin: 0;
}

/* No indent for highlight text */
.highlight-text {
    text-indent: 0;
}

/* ============================================
   COLOR DEMO BOXES
   Showing different color formats
   ============================================ */
.color-demo {
    display: flex;
    gap: 1rem;
    margin-top: 1rem;
}

.color-box {
    width: 25%;           /* Each box is 25% of container */
    padding: 1rem;
    text-align: center;
    font-size: 0.875rem;
    font-weight: bold;
    text-transform: uppercase;
    letter-spacing: 0.05em;
}

/* Named color */
.color-red {
    background-color: red;
    color: white;
}

/* Hex color */
.color-green {
    background-color: #27ae60;
    color: white;
}

/* RGB color */
.color-blue {
    background-color: rgb(52, 152, 219);
    color: white;
}

/* RGBA color (semi-transparent) */
.color-transparent {
    background-color: rgba(0, 0, 0, 0.7);
    color: white;
}

/* ============================================
   FOOTER
   ============================================ */
.footer {
    background-color: #2c3e50;
    color: rgba(255, 255, 255, 0.7);
    text-align: center;
    padding: 1.5rem;
    margin-top: 2rem;
}

.copyright {
    font-size: 0.875rem;
    margin: 0;
}
```

### What This Page Looks Like

```
┌────────────────────────────────────────────────────────────┐
│                                                            │
│                                                            │
│              UNDERSTANDING CSS UNITS                       │
│         (3rem, uppercase, letter-spacing)                  │
│                                                            │
│           A Complete Guide for Beginners                   │
│         (1.25rem, semi-transparent white)                  │
│                                                            │
│                (100vh - full viewport height)              │
│                                                            │
├────────────────────────────────────────────────────────────┤
│                                                            │
│   Why Units Matter                                         │
│   (1.75rem, capitalized)                                   │
│   ─────────────────────────────────────────────            │
│                                                            │
│       CSS units determine how elements are sized           │
│       on your webpage. (text-indent: 1.5rem)               │
│                                                            │
│       Pixels (px) give you precise control...              │
│                                                            │
│   ┌──────────────────────────────────────────────┐        │
│   │ PRO TIP                                      │        │
│   │ Use rem for font sizes and spacing. It       │        │
│   │ respects user preferences and avoids the     │        │
│   │ em compounding problem!                      │        │
│   │ (rgba background, solid border, italic text) │        │
│   └──────────────────────────────────────────────┘        │
│                                                            │
│   Color Values                                             │
│   ─────────────────────────────────────────────            │
│                                                            │
│   ┌────────┐ ┌────────┐ ┌────────┐ ┌────────┐            │
│   │  RED   │ │ GREEN  │ │  BLUE  │ │SEMI-   │            │
│   │        │ │        │ │        │ │TRANS   │            │
│   │(named) │ │ (hex)  │ │ (rgb)  │ │(rgba)  │            │
│   └────────┘ └────────┘ └────────┘ └────────┘            │
│                                                            │
├────────────────────────────────────────────────────────────┤
│                                                            │
│              © 2024 CSS Learning Guide                     │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

### Key Features in This Example

1. **Units used**:
   - `rem` for all font sizes and spacing
   - `%` for flexible widths
   - `vh` for full-screen hero
   - `px` for borders

2. **Color formats used**:
   - Named colors: `red`, `white`
   - Hex colors: `#2c3e50`, `#27ae60`
   - RGB colors: `rgb(52, 152, 219)`
   - RGBA colors: `rgba(255, 255, 255, 0.8)`

3. **Text properties used**:
   - `text-transform: uppercase` for hero title
   - `letter-spacing` for wide letter effect
   - `text-indent` for paragraph first lines
   - `font-style: italic` for highlight text

---

## Summary

In this lesson, you learned:

### CSS Units

1. **px (pixels)**: Absolute unit, precise and fixed
   - Use for: borders, small precise values
   - Example: `border: 1px solid black;`

2. **% (percentage)**: Relative to parent element
   - Use for: flexible layouts, responsive images
   - Example: `width: 50%;`

3. **em**: Relative to parent's font-size
   - Use for: scalable components
   - Warning: Can compound when nested!
   - Example: `padding: 1em;`

4. **rem**: Relative to root font-size (usually 16px)
   - Use for: font sizes, spacing (preferred!)
   - No compounding problem
   - Example: `font-size: 1.5rem;`

5. **vh**: Viewport height (1vh = 1% of viewport height)
   - Use for: full-screen sections
   - Example: `height: 100vh;`

6. **vw**: Viewport width (1vw = 1% of viewport width)
   - Use for: responsive typography
   - Example: `font-size: 5vw;`

### Color Values

1. **Named colors**: `red`, `blue`, `tomato`
2. **Hex colors**: `#FF0000`, `#F00` (shorthand)
3. **RGB colors**: `rgb(255, 0, 0)`
4. **RGBA colors**: `rgba(255, 0, 0, 0.5)` (with transparency!)

### Text Properties

1. **letter-spacing**: Space between letters
2. **word-spacing**: Space between words
3. **text-transform**: `uppercase`, `lowercase`, `capitalize`
4. **text-indent**: Indent first line of text
5. **font-style**: `italic`, `normal`

### Key Takeaways

- Use **rem** for font sizes (accessible, predictable)
- Use **%** for flexible widths
- Use **px** for borders and precise values
- Use **vh** for full-height sections
- **RGBA** adds transparency to colors
- **text-transform** is better than typing in ALL CAPS

---

## Next Steps

Now that you understand CSS units and properties, you're ready for:

**Upcoming Topics**:
- CSS Box Model (margin, padding, border in detail)
- CSS Layout (display, positioning)
- Responsive Design

**Practice**:
- Try the exercises for this lesson
- Experiment with different units
- Test your page at different browser sizes

---

## Validation Checkpoint

Test your understanding by answering these questions:

### Question 1: What's the difference between px and rem?

**Answer**: **px** is an absolute unit that's always the same size (one pixel on screen). **rem** is a relative unit based on the root element's font-size (usually 16px). Use px for precise, fixed values like borders. Use rem for font sizes and spacing because it respects user preferences and scales properly.

### Question 2: What's the difference between em and rem?

**Answer**: **em** is relative to the **parent element's** font-size, while **rem** is relative to the **root (html) element's** font-size. The key difference: em can compound when nested (1.5em inside 1.5em = 2.25em), but rem always stays consistent. Use rem for predictable, accessible sizing.

### Question 3: How do you make a section fill the entire viewport height?

**Answer**: Use `height: 100vh;`. The `vh` unit stands for viewport height, and 100vh means 100% of the viewport height.

```css
.hero {
    height: 100vh;    /* Full viewport height */
}
```

### Question 4: What's the difference between RGB and RGBA?

**Answer**: **RGB** specifies a color using Red, Green, and Blue values (0-255 each). **RGBA** adds an **Alpha** channel for transparency (0 = invisible, 1 = solid).

```css
color: rgb(255, 0, 0);        /* Solid red */
color: rgba(255, 0, 0, 0.5);  /* Semi-transparent red (50% opacity) */
```

### Question 5: How do you convert text to uppercase using CSS?

**Answer**: Use the `text-transform` property with the value `uppercase`:

```css
h1 {
    text-transform: uppercase;
}
```

This is better than typing your HTML in ALL CAPS because:
- Screen readers read it correctly
- You can change it easily in CSS
- It keeps your HTML clean

---

## Common Confusion Points

### Confusion: "When should I use em vs rem?"

**Answer**: **Use rem for most things, em for special cases.**

| Use rem when | Use em when |
|--------------|-------------|
| Font sizes | Component-internal spacing |
| Margins between elements | Elements that should scale with their own font-size |
| Padding in most cases | Typography components (icons next to text) |
| Any time you want predictability | You specifically want the compounding effect |

**Why rem is usually better**:
- No compounding problem
- Predictable sizing
- Respects user's browser font-size setting
- Easier to calculate and debug

### Confusion: "Why doesn't my percentage work?"

**Answer**: Percentage is relative to the **parent element**. Common reasons percentages don't work:

1. **Parent has no size defined**: If parent has `height: auto`, child's `height: 50%` won't work
2. **Wrong property**: Some properties don't accept percentages
3. **Typo**: Check for `%` after the number (no space!)

```css
/* This won't work if parent has no defined height */
.child {
    height: 50%;    /* Parent needs a height! */
}

/* This works - parent has defined height */
.parent {
    height: 400px;
}
.child {
    height: 50%;    /* Now this is 200px */
}
```

### Confusion: "What's the difference between px and relative units?"

**Answer**:

| px (Absolute) | rem, em, % (Relative) |
|---------------|----------------------|
| Always the same size | Changes based on context |
| User can't easily override | Respects user preferences |
| Precise and predictable | Flexible and adaptable |
| Good for borders, icons | Good for fonts, layouts |

**Accessibility tip**: Using relative units (especially rem) makes your website accessible to users who increase their browser's font size for better readability.

### Confusion: "When should I use vh/vw?"

**Answer**:

**Good uses of vh**:
- Full-screen hero sections: `height: 100vh;`
- Half-screen sections: `height: 50vh;`
- Sticky headers: `height: 10vh;`

**Good uses of vw**:
- Responsive typography (with caution): `font-size: 5vw;`
- Elements that should scale with screen width

**Caution**:
- `100vw` can cause horizontal scrollbars (includes scrollbar width)
- Very small vw values on phones can make text unreadable
- Always test on different screen sizes!

**Better approach for responsive text**:
```css
/* Use clamp() for min/max limits (advanced) */
h1 {
    font-size: clamp(1.5rem, 5vw, 3rem);
    /* Minimum 1.5rem, preferred 5vw, maximum 3rem */
}
```

### Confusion: "How do I know which color format to use?"

**Answer**:

| Format | Use When |
|--------|----------|
| Named | Quick prototyping, common colors |
| Hex | Most common, easy to copy from design tools |
| RGB | When you need to calculate colors |
| RGBA | When you need transparency |

**Recommendation**: Use **hex** for solid colors, **RGBA** when you need transparency.

```css
/* Solid colors - use hex */
color: #333333;
background-color: #ffffff;

/* Transparency needed - use RGBA */
background-color: rgba(0, 0, 0, 0.5);    /* Semi-transparent overlay */
color: rgba(255, 255, 255, 0.8);         /* Slightly faded text */
```

---

**Great job!** You now understand CSS units, color values, and text properties. You can create flexible, accessible websites with proper sizing and beautiful typography. Practice using different units to see how they behave!
