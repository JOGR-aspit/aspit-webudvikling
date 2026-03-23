# CSS Exercise: Pixel Units & Color Formats

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Use pixel (px) units for font-size and border
- [ ] Write named colors (`red`, `blue`, `white`, etc.)
- [ ] Write hex colors (`#FF0000`, `#333333`, etc.)
- [ ] Understand when to use px units

## Prerequisites

Before starting this exercise, you should have:

- Completed the "CSS Units and Properties" lesson (09-css-units-and-properties.md)
- Completed the "CSS Fundamentals" lesson (07-css-fundamentals.md)
- Know how to write CSS rules with selectors and declarations

## What You'll Build

You will style a simple product card. The HTML is already written for you. Your job is to write CSS that uses pixel units and different color formats to create a visually appealing card.

## Tasks

1. **Open `styles.css`** - This file has selectors ready for you. You'll fill in the declarations.

2. **Style the card container** - Inside the `.product-card` selector, add:
   - `background-color: #ffffff;` (white background using hex)
   - `border: 2px solid #333333;` (dark gray border, 2 pixels thick)

3. **Style the product title** - Inside the `.product-title` selector, add:
   - `color: #2c3e50;` (dark blue-gray using hex)
   - `font-size: 24px;` (24 pixels tall)

4. **Style the product description** - Inside the `.product-description` selector, add:
   - `color: #666666;` (medium gray using hex)
   - `font-size: 16px;` (16 pixels tall)

5. **Style the price** - Inside the `.price` selector, add:
   - `color: green;` (green color using named color)
   - `font-size: 20px;` (20 pixels tall)

6. **Style the sale badge** - Inside the `.sale-badge` selector, add:
   - `background-color: red;` (red background using named color)
   - `color: white;` (white text using named color)
   - `font-size: 12px;` (12 pixels tall - small text)

## Unit Syntax Reminder

| Unit | Syntax | Example |
|------|--------|---------|
| **px** | `numberpx` (no space!) | `font-size: 16px;` |

**Common mistakes**:
- `16 px` (space between number and px) - WRONG!
- `16px` (no space) - CORRECT!

## Color Format Reminder

| Format | Syntax | Example |
|--------|--------|---------|
| **Named** | `colorname` | `color: red;` |
| **Hex** | `#RRGGBB` | `color: #FF0000;` |

## Expected Result

When you complete this exercise, your card will look like this:

```
┌────────────────────────────────────┐
│                           [SALE]   │
│                            (red bg,│
│                         white text)│
│                                    │
│   Wireless Headphones              │
│   (dark blue-gray #2c3e50, 24px)   │
│                                    │
│   High-quality wireless headphones │
│   with noise cancellation.         │
│   (medium gray #666666, 16px)      │
│                                    │
│   $99.99                           │
│   (green, 20px)                    │
│                                    │
└────────────────────────────────────┘
(white background #ffffff,
 2px dark gray border #333333)
```

## How to Check Your Work

1. **Save both files** (`index.html` and `styles.css`)

2. **Open `index.html` in your web browser**

3. **Verify the card container**:
   - Should have a **white background**
   - Should have a **dark gray border** that's **2 pixels thick**

4. **Verify the product title**:
   - Should be **dark blue-gray** color
   - Should be **24 pixels** tall

5. **Verify the product description**:
   - Should be **medium gray** color
   - Should be **16 pixels** tall

6. **Verify the price**:
   - Should be **green** color
   - Should be **20 pixels** tall

7. **Verify the sale badge**:
   - Should have a **red background**
   - Should have **white text**
   - Should be **12 pixels** tall (small)

## Common Issues

### Issue: My font sizes aren't changing

**Possible cause:** You put a space between the number and `px`.

**Fix:** Remove the space:
```css
/* WRONG */
font-size: 24 px;

/* RIGHT */
font-size: 24px;
```

### Issue: My hex color isn't working

**Possible cause:** You forgot the `#` symbol at the start.

**Fix:** Hex colors MUST start with `#`:
```css
/* WRONG */
color: 2c3e50;

/* RIGHT */
color: #2c3e50;
```

### Issue: The border isn't showing

**Possible cause:** You only wrote the width, not the full border shorthand.

**Fix:** The `border` property needs three values:
```css
/* WRONG */
border: 2px;

/* RIGHT */
border: 2px solid #333333;
/*       ↑      ↑      ↑
    width style  color   */
```

### Issue: The colors look wrong

**Possible cause:** You might have a typo in the hex code.

**Fix:** Hex codes use numbers 0-9 and letters A-F only:
```css
/* WRONG - 'G' is not valid in hex */
color: #GGGGGG;

/* RIGHT */
color: #666666;
```

## Time Estimate

~10 minutes
