# CSS Exercise: Centered Layout

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Use auto margins to center elements horizontally
- [ ] Combine padding, border, and margin properties
- [ ] Create spacing between elements using margin
- [ ] Build a complete page layout using the box model
- [ ] Apply `box-sizing: border-box` globally

## Prerequisites

Before starting this exercise, you should have:

- Completed the "The Box Model" lesson (10-the-box-model.md)
- Completed the "Card with Borders" (Medium) exercise
- Understand CSS selectors and the box model

## What You'll Build

You will create a complete centered page layout with:

- A **header** at the top
- Three **cards** in the content area
- A **footer** at the bottom
- Everything **centered** on the page using auto margins

This exercise brings together everything you've learned about padding, border, and margin!

## Tasks

1. **Open `styles.css`** - This file is empty. You'll write everything from scratch.

2. **Set box-sizing globally** - Write a universal selector to make all elements use border-box sizing
   - Think: Which selector targets ALL elements, including pseudo-elements?
   - Hint: This affects how width, padding, and border are calculated

3. **Style the page body** - Remove default browser spacing and set basic page properties
   - Think: What properties control the default spacing around the page?
   - Hint: Reset margins, padding, set a font, and a light background color

4. **Center the main container** - Create a responsive centered wrapper with max width
   - Think: How do you center an element without using flexbox or grid?
   - Hint: You need width, max-width, and margin properties
   - Goal: 90% width on small screens, max 800px, perfectly centered

5. **Style the header** - Create a page header with dark background and centered text
   - Think: What properties control background color, text color, spacing, and text alignment?
   - Hint: Remember to add space below the header
   - Hint: Dark blue background with white text works well

6. **Style the header title** - Remove the default margin and set appropriate font size
   - Think: Why do headings have extra space around them by default?
   - Hint: Set margin to 0 and choose a nice font size

7. **Style the cards** - Create white card components with borders and spacing
   - Think: How do you create content boxes with inner spacing and borders?
   - Hint: Use background, padding, border, and margin-bottom
   - Hint: Add slightly rounded corners for a modern look

8. **Style card titles** - Make card headings stand out with proper spacing and color
   - Think: How do you control the spacing around headings and make them readable?
   - Hint: Remove default margins and set appropriate size/color

9. **Style card content** - Make paragraphs readable with proper line height and color
   - Think: What makes text comfortable to read in a card?
   - Hint: Adjust line height and use a muted color for text

10. **Create a featured card variant** - Make one card special with accent styling
    - Think: How do you style elements with multiple classes?
    - Hint: The selector has NO space between the classes
    - Hint: Green accent border and light green background work well

11. **Style the footer** - Create a page footer similar to the header but smaller
    - Think: What properties make a footer similar to the header but with different spacing?
    - Hint: Same background color as header but with space above
    - Hint: Centered text with appropriate padding

12. **Style footer text** - Make footer text smaller without extra spacing
    - Think: How do you control text size and remove default paragraph margins?
    - Hint: Set a smaller font size and reset margins

## Auto Margin Centering Explained

```css
.container {
    width: 80%;        /* Must have a width! */
    margin: 0 auto;    /* 0 = top/bottom, auto = left/right */
}
```

**How it works**:

- `auto` tells the browser: "calculate the remaining space and split it equally"
- If the viewport is 1000px wide and your container is 800px wide...
- The browser calculates: 1000 - 800 = 200px remaining
- It splits 200px equally: 100px on the left, 100px on the right
- Result: perfectly centered!

```
┌────────────────────────────────────────────────────────┐
│                     VIEWPORT                           │
│                                                        │
│    ← 100px →  ┌──────────────────┐  ← 100px →         │
│               │                  │                    │
│               │   .container     │                    │
│               │   (800px wide)   │                    │
│               │                  │                    │
│               └──────────────────┘                    │
│                    ↑                                   │
│              margin: 0 auto                            │
│         (auto calculates equal sides)                  │
└────────────────────────────────────────────────────────┘
```

## Expected Result

When you complete this exercise, your page will look like this:

```
┌────────────────────────────────────────────────────────────────┐
│                                                                │
│   ┌────────────────────────────────────────────────────────┐   │
│   │                    MY WEBSITE                           │   │
│   │              (dark blue #2c3e50 header)                 │   │
│   └────────────────────────────────────────────────────────┘   │
│                           ↑ 30px margin                        │
│   ┌────────────────────────────────────────────────────────┐   │
│   │                                                        │   │
│   │   Card 1: Introduction                                 │   │
│   │   ─────────────────────                                │   │
│   │   This is the first card. It has a white               │   │
│   │   background and a light gray border.                  │   │
│   │   (padding: 20px, border: 1px solid #ddd)              │   │
│   │                                                        │   │
│   └────────────────────────────────────────────────────────┘   │
│                           ↑ 20px margin                        │
│   ┌────────────────────────────────────────────────────────┐   │
│   ┃                                                        │   │
│   ┃   Card 2: Featured Card                                │   │
│   ┃   ─────────────────────                                │   │
│   ┃   This card has a green left border and a              │   │
│   ┃   light green background. It stands out!               │   │
│   ┃   (border-left: 4px solid #27ae60)                     │   │
│   ┃                                                        │   │
│   └────────────────────────────────────────────────────────┘   │
│                           ↑ 20px margin                        │
│   ┌────────────────────────────────────────────────────────┐   │
│   │                                                        │   │
│   │   Card 3: Regular Card                                 │   │
│   │   ─────────────────────                                │   │
│   │   Another regular card with the same styling           │   │
│   │   as the first one.                                    │   │
│   │                                                        │   │
│   └────────────────────────────────────────────────────────┘   │
│                           ↑ 30px margin                        │
│   ┌────────────────────────────────────────────────────────┐   │
│   │              © 2024 My Website                         │   │
│   │              (dark blue #2c3e50 footer)                │   │
│   └────────────────────────────────────────────────────────┘   │
│                                                                │
└────────────────────────────────────────────────────────────────┘
```

## How to Check Your Work

1. **Save both files** (`index.html` and `styles.css`)

2. **Open `index.html` in your web browser**

3. **Verify the container is centered**:
   - The content should be **centered** on the page
   - There should be **equal space** on the left and right
   - The content should be **no wider than 800px**

4. **Verify the header**:
   - Should have a **dark blue background** (#2c3e50)
   - Text should be **white** and **centered**
   - Should have **space below** (30px margin)

5. **Verify the cards**:
   - Should have **white backgrounds** and **light gray borders**
   - Should have **20px of space inside** (padding)
   - Should have **20px gap between** each card (margin)
   - The **featured card** should have a **green left border** and **light green background**

6. **Verify the footer**:
   - Should have a **dark blue background** like the header
   - Should have **space above** (30px margin)
   - Text should be **centered** and **white**

7. **Resize your browser window**:
   - The container should **shrink and grow** with the window
   - At very wide windows, it should **stop at 800px**
   - Everything should stay **centered** at all sizes

## Common Issues

### Issue: The container isn't centering

**Possible cause:** You forgot to add `width` or used `width: auto`.

**Fix:** Auto margins only work with a defined width:

```css
/* WON'T CENTER - no width */
.container {
    margin: 0 auto;
}

/* WILL CENTER - has width */
.container {
    width: 90%;
    margin: 0 auto;
}
```

### Issue: There's no space between my cards

**Possible cause:** You forgot `margin-bottom` on the cards.

**Fix:** Add margin to create gaps:

```css
.card {
    margin-bottom: 20px;  /* Space between cards */
}
```

### Issue: The featured card styles aren't applying

**Possible cause:** Wrong selector format (space vs no space).

**Fix:** No space between classes for chained selector:

```css
/* WRONG - space means descendant */
.card .featured { }

/* RIGHT - no space means both classes on same element */
.card.featured { }
```

### Issue: The page has unwanted white space around the edges

**Possible cause:** Browsers add default margin to the body.

**Fix:** Reset body margin and padding:

```css
body {
    margin: 0;
    padding: 0;
}
```

### Issue: The header or footer has extra space around the text

**Possible cause:** Headings (`h1`, `h2`) have default margins.

**Fix:** Reset heading margins:

```css
.header h1 {
    margin: 0;
}
```

### Issue: My container is wider than 800px on large screens

**Possible cause:** You forgot `max-width`.

**Fix:** Add both `width` and `max-width`:

```css
.container {
    width: 90%;        /* Percentage for small screens */
    max-width: 800px;  /* Limit for large screens */
}
```

## Time Estimate

~30 minutes
