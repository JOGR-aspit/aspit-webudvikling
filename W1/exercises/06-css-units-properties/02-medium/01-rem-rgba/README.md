# CSS Exercise: rem Units, RGBA & Text Properties

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Use rem units for scalable font sizes
- [ ] Use RGBA colors to add transparency
- [ ] Apply `text-transform` to change text case
- [ ] Apply `letter-spacing` to adjust letter spacing
- [ ] Understand why rem is preferred over px for text

## Prerequisites

Before starting this exercise, you should have:

- Completed the "CSS Units and Properties" lesson (09-css-units-and-properties.md)
- Completed the "Pixel Units & Color Formats" (Easy) exercise
- Understand the difference between px and rem units

## What You'll Build

You will style a blog quote card with a semi-transparent overlay. You'll use rem units for accessible sizing and RGBA for transparency effects. You'll also apply text properties to create a professional typographic style.

## Tasks

1. **Open `styles.css`** - This file is empty. You'll write all the CSS from scratch.

2. **Style the page body**
   - Selector: `body`
   - Declarations:
     - `font-family: Georgia, serif;`
     - `background-color: #1a1a2e;` (dark blue background)
     - `color: #ffffff;` (white text)
     - `margin: 0;`
     - `padding: 2rem;`

3. **Style the quote card container**
   - Selector: `.quote-card`
   - Declarations:
     - `background-color: rgba(255, 255, 255, 0.1);` (semi-transparent white at 10%)
     - `border-left: 4px solid #e94560;` (pink/red accent border)
     - `padding: 2rem;`

4. **Style the quote text**
   - Selector: `.quote-text`
   - Declarations:
     - `font-size: 1.5rem;` (1.5 × base size = 24px)
     - `font-style: italic;`
     - `line-height: 1.6;`
     - `color: rgba(255, 255, 255, 0.9);` (white at 90% opacity)
     - `text-indent: 1.5rem;` (indent first line)
     - `margin: 0;`

5. **Style the author name**
   - Selector: `.author`
   - Declarations:
     - `font-size: 1rem;` (base size = 16px)
     - `color: #e94560;` (pink/red accent)
     - `text-transform: uppercase;` (ALL CAPS)
     - `letter-spacing: 0.1em;` (wider letter spacing)
     - `margin-top: 1rem;`

6. **Style the author title**
   - Selector: `.author-title`
   - Declarations:
     - `font-size: 0.875rem;` (smaller text = 14px)
     - `color: rgba(255, 255, 255, 0.6);` (white at 60% opacity - more faded)

## rem Unit Reminder

| rem Value | Calculation | Result (if base = 16px) |
|-----------|-------------|-------------------------|
| `1rem` | 1 × 16px | 16px |
| `1.5rem` | 1.5 × 16px | 24px |
| `2rem` | 2 × 16px | 32px |
| `0.875rem` | 0.875 × 16px | 14px |

## RGBA Syntax Reminder

```css
rgba(red, green, blue, alpha)
```

- `red`: 0-255
- `green`: 0-255
- `blue`: 0-255
- `alpha`: 0-1 (0 = invisible, 1 = solid)

**Examples**:
- `rgba(255, 255, 255, 0.1)` = white at 10% opacity
- `rgba(255, 255, 255, 0.9)` = white at 90% opacity
- `rgba(0, 0, 0, 0.5)` = black at 50% opacity

## Expected Result

When you complete this exercise, your quote card will look like this:

```
┌─────────────────────────────────────────────────┐
│ ▌                                                │
│ ▌  "The only way to do great work is to         │
│ ▌   love what you do."                          │
│ ▌                                                │
│ ▌   (italic text, 1.5rem, slightly transparent) │
│ ▌                                                │
│ ▌   STEVE JOBS                                   │
│ ▌   (uppercase, letter-spacing, pink accent)     │
│ ▌                                                │
│ ▌   Co-founder, Apple Inc.                       │
│ ▌   (smaller, more faded text)                   │
│ │                                                │
└─────────────────────────────────────────────────┘
(Dark blue page background #1a1a2e,
 semi-transparent card background rgba(255,255,255,0.1),
 pink accent border #e94560)
```

## How to Check Your Work

1. **Save both files** (`index.html` and `styles.css`)

2. **Open `index.html` in your web browser**

3. **Verify the page background**:
   - Should be **dark blue** (#1a1a2e)
   - Should have **padding** around the edges (2rem)

4. **Verify the quote card**:
   - Should have a **semi-transparent white background** (you can see it's lighter than the page)
   - Should have a **pink/red left border** (4px thick)

5. **Verify the quote text**:
   - Should be **italic**
   - Should be **1.5rem** (larger than normal)
   - Should be **slightly transparent** white (90%)
   - First line should be **indented**

6. **Verify the author name**:
   - Should be **ALL UPPERCASE**
   - Should have **wider letter spacing**
   - Should be **pink/red** color

7. **Verify the author title**:
   - Should be **smaller** than the author name
   - Should be **more faded** (60% opacity)

## Common Issues

### Issue: The background is solid white, not transparent

**Possible cause:** You used `rgb()` instead of `rgba()`, or forgot the alpha value.

**Fix:** RGBA needs 4 values (red, green, blue, alpha):
```css
/* WRONG - no alpha (transparency) */
background-color: rgb(255, 255, 255);

/* RIGHT - with alpha for transparency */
background-color: rgba(255, 255, 255, 0.1);
```

### Issue: The author name isn't uppercase

**Possible cause:** You typed the HTML in caps instead of using CSS.

**Fix:** Use `text-transform: uppercase;` in CSS:
```css
/* The HTML should be normal case */
<p class="author">Steve Jobs</p>

/* CSS makes it uppercase */
.author {
    text-transform: uppercase;
}
```

### Issue: The letter spacing didn't change

**Possible cause:** You forgot the unit (em) after the number.

**Fix:** Letter spacing needs a unit:
```css
/* WRONG */
letter-spacing: 0.1;

/* RIGHT */
letter-spacing: 0.1em;
```

### Issue: The rem values look the same as px

**Possible cause:** This is actually correct! 1rem = 16px by default.

**Fix:** No fix needed! The benefit of rem is that it scales if the user changes their browser's font size setting. Test it by changing your browser's default font size.

## Time Estimate

~20 minutes
