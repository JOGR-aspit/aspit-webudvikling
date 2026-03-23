# CSS Exercise: Viewport Units & Combined Properties

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Use viewport height (`vh`) for full-screen sections
- [ ] Use percentage (`%`) for flexible widths
- [ ] Combine multiple units (rem, vh, %, px) appropriately
- [ ] Use all three color formats (named, hex, RGBA) together
- [ ] Apply `text-transform`, `letter-spacing`, and `text-indent` together
- [ ] Choose the right unit for each property

## Prerequisites

Before starting this exercise, you should have:

- Completed the "CSS Units and Properties" lesson (09-css-units-and-properties.md)
- Completed the "Pixel Units & Color Formats" (Easy) exercise
- Completed the "rem Units, RGBA & Text Properties" (Medium) exercise

## What You'll Build

You will create a full-height hero section with a semi-transparent overlay. This combines all the concepts from the lesson: viewport units, percentage widths, rem units, multiple color formats, and text properties.

## Tasks

1. **Open `styles.css`** - This file is empty. You'll write all the CSS from scratch.

2. **Style the page body** - Remove default spacing
   - Selector: `body`
   - Declarations:
     - `margin: 0;`
     - `padding: 0;`
     - `font-family: Arial, sans-serif;`

3. **Style the hero section** - Full viewport height
   - Selector: `.hero`
   - Declarations:
     - `height: 100vh;` (full viewport height)
     - `width: 100%;` (full width)
     - `background-color: #2c3e50;` (dark blue)
     - `display: flex;`
     - `flex-direction: column;`
     - `justify-content: center;`
     - `align-items: center;`

4. **Style the hero title** - Large, spaced, uppercase
   - Selector: `.hero-title`
   - Declarations:
     - `font-size: 3rem;` (large text)
     - `color: white;` (named color)
     - `text-transform: uppercase;` (ALL CAPS)
     - `letter-spacing: 0.15em;` (wide letter spacing)
     - `margin: 0;`

5. **Style the hero subtitle** - Semi-transparent
   - Selector: `.hero-subtitle`
   - Declarations:
     - `font-size: 1.25rem;` (medium text)
     - `color: rgba(255, 255, 255, 0.8);` (white at 80% opacity)
     - `margin-top: 1rem;`

6. **Style the description paragraph** - With text indent
   - Selector: `.hero-description`
   - Declarations:
     - `font-size: 1rem;` (base size)
     - `color: rgba(255, 255, 255, 0.7);` (white at 70% opacity)
     - `text-align: center;`
     - `text-indent: 2rem;` (indent first line)
     - `max-width: 600px;` (don't get too wide)
     - `line-height: 1.6;`
     - `margin-top: 1.5rem;`

7. **Style the call-to-action button**
   - Selector: `.cta-button`
   - Declarations:
     - `background-color: #e94560;` (pink/red accent)
     - `color: white;`
     - `font-size: 1.125rem;`
     - `text-transform: uppercase;`
     - `letter-spacing: 0.1em;`
     - `border: none;`
     - `padding: 1rem 2rem;`

## Unit Selection Guide

| Property | Recommended Unit | Why |
|----------|-----------------|-----|
| `font-size` | `rem` | Accessible, scalable |
| `height` (full screen) | `vh` | Fills viewport |
| `width` (flexible) | `%` | Responsive |
| `border` | `px` | Precise control |
| `letter-spacing` | `em` | Relative to font size |
| `text-indent` | `rem` or `em` | Consistent spacing |

## Color Format Selection Guide

| Situation | Recommended Format |
|-----------|-------------------|
| Common colors | Named: `white`, `black`, `red` |
| Precise colors | Hex: `#2c3e50` |
| Transparency needed | RGBA: `rgba(255, 255, 255, 0.8)` |

## Expected Result

When you complete this exercise, your hero section will fill the entire screen:

```
┌────────────────────────────────────────────────────────────────┐
│                                                                │
│                                                                │
│                                                                │
│              WELCOME TO MY WEBSITE                             │
│         (3rem, uppercase, letter-spacing: 0.15em)              │
│              (white text)                                      │
│                                                                │
│         A Journey Into Modern Web Design                       │
│    (1.25rem, rgba(255,255,255,0.8) - 80% opacity)              │
│                                                                │
│        "Discover the art of creating beautiful                 │
│         and functional websites using HTML and CSS."           │
│       (1rem, centered, text-indent, 70% opacity)               │
│                                                                │
│              [ GET STARTED ]                                   │
│       (pink button, uppercase, letter-spacing)                 │
│                                                                │
│                                                                │
│                                                                │
└────────────────────────────────────────────────────────────────┘
        (height: 100vh - fills entire viewport)
        (dark blue background #2c3e50)
```

## How to Check Your Work

1. **Save both files** (`index.html` and `styles.css`)

2. **Open `index.html` in your web browser**

3. **Verify the hero fills the screen**:
   - The `.hero` section should fill the **entire viewport height**
   - Try resizing your browser window - it should always fill the visible area

4. **Verify the title**:
   - Should be **large** (3rem)
   - Should be **ALL UPPERCASE**
   - Should have **wide letter spacing**
   - Should be **white**

5. **Verify the subtitle**:
   - Should be **medium size** (1.25rem)
   - Should be **slightly transparent** (80% opacity)
   - Should be **below** the title with space

6. **Verify the description**:
   - Should be **centered**
   - Should have **indented first line**
   - Should be **more transparent** (70% opacity)
   - Should have a **maximum width** (doesn't stretch across whole screen)

7. **Verify the button**:
   - Should have **pink/red background**
   - Should be **uppercase**
   - Should have **letter spacing**
   - Should have **padding** (inner space)

8. **Test responsiveness**:
   - Resize your browser window
   - The hero should always fill the viewport height
   - Text should remain centered

## Common Issues

### Issue: The hero doesn't fill the screen

**Possible cause:** You forgot `height: 100vh;` or used a different unit.

**Fix:** Use viewport height:
```css
/* WRONG */
height: 100%;
height: 100px;
height: 100rem;

/* RIGHT */
height: 100vh;
```

### Issue: The text is too wide

**Possible cause:** You forgot `max-width` on the description.

**Fix:** Add a maximum width:
```css
.hero-description {
    max-width: 600px;
    /* This prevents text from stretching across the whole screen */
}
```

### Issue: The button doesn't look right

**Possible cause:** Buttons have default styles you need to override.

**Fix:** Remove the default border and add your styles:
```css
.cta-button {
    border: none;           /* Remove default border */
    padding: 1rem 2rem;     /* Add inner space */
    background-color: #e94560;
    color: white;
}
```

### Issue: I used `100vw` and now there's a horizontal scrollbar

**Possible cause:** `100vw` includes the scrollbar width.

**Fix:** Use `width: 100%;` instead of `100vw`:
```css
/* Can cause scrollbar */
width: 100vw;

/* Better - no scrollbar */
width: 100%;
```

### Issue: The layout doesn't center

**Possible cause:** You're missing the flexbox properties.

**Fix:** Make sure you have all three:
```css
.hero {
    display: flex;            /* Enable flexbox */
    flex-direction: column;   /* Stack items vertically */
    justify-content: center;  /* Center vertically */
    align-items: center;      /* Center horizontally */
}
```

## Time Estimate

~30 minutes
