# CSS Exercise: Inline-Block Navigation

## Learning Objectives

By completing this exercise, you will be able to:

- [ ] Create a horizontal navigation bar using `display: inline-block`
- [ ] Style navigation links with padding and hover effects
- [ ] Build a complete page layout with header, navigation, main content, and footer
- [ ] Understand how `inline-block` combines inline flow with block styling
- [ ] Use auto margins to center page containers

## Prerequisites

Before starting this exercise, you should have:

- Completed the "Block vs Inline Elements" lesson (11-block-vs-inline-elements.md)
- Completed the "The Box Model" lesson (10-the-box-model.md)
- Completed the "CSS Fundamentals" lesson (07-css-fundamentals.md)
- Know how to use padding, margin, border, and background-color

## What You'll Build

You will create a complete webpage layout with a horizontal navigation bar. The HTML structure is already written - it contains a header, navigation, main content area, and footer. Your job is to write CSS that:

1. Styles the page header with a dark background
2. Creates a horizontal navigation bar using `display: inline-block`
3. Styles navigation links with padding and hover effects
4. Centers the main content on the page
5. Creates a footer at the bottom

This exercise brings together block elements (for page sections) and inline-block (for navigation items).

## Tasks

1. **Open `styles.css`** - This file has base styles. You'll add the layout styles.

2. **Remove list styles from navigation** - Create a selector for `.nav-menu` and add properties to remove browser defaults
   - Think: What properties control the bullet points and spacing on lists?
   - Hint: You need to remove three things that browsers add by default

3. **Make list items inline-block** - Create a selector for `.nav-menu li` and add a display property
   - Think: How do you make block elements sit side by side while still accepting width/height?
   - Hint: The solution is in the exercise name!

4. **Style navigation links** - Create a selector for `.nav-menu a` and add inline-block with padding
   - Think: Why do links need special treatment for padding?
   - Hint: Links have default display type that ignores padding

5. **Add hover effects to links** - Create a selector for `.nav-menu a:hover` with background change
   - Think: How do you select elements when the mouse is over them?
   - Hint: Use a pseudo-class with no space before the colon

6. **Style the page header** - Create a selector for `.page-header` with dark background and centered text
   - Think: What properties control background color and text alignment?
   - Hint: Use the same dark blue color from the CSS fundamentals lesson

7. **Style the main content container** - Create a selector for `.container` with max width and centering
   - Think: How do you limit width and center content at the same time?
   - Hint: You need width, max-width, and the magic margin value

8. **Style the page footer** - Create a selector for `.page-footer` with dark background and semi-transparent text
   - Think: How do you make text semi-transparent?
   - Hint: Use rgba with alpha channel

## Why Inline-Block for Navigation?

```
REGULAR BLOCK ELEMENTS (stacking):
┌─────────────────────────────────────────┐
│ Home                                    │
└─────────────────────────────────────────┘
┌─────────────────────────────────────────┐
│ About                                   │
└─────────────────────────────────────────┘
┌─────────────────────────────────────────┐
│ Contact                                 │
└─────────────────────────────────────────┘


INLINE-BLOCK (horizontal navigation):
┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐
│  Home   │ │  About  │ │ Services│ │ Contact │
└─────────┘ └─────────┘ └─────────┘ └─────────┘
     ↑           ↑           ↑           ↑
  Same line, but each accepts padding!
```

**The problem with regular inline elements:**
- `<a>` tags are inline by default
- They ignore `width` and vertical `padding`
- Navigation links would have tiny click areas

**The solution with `inline-block`:**
- Links stay on the same line (inline behavior)
- Links accept `padding` for larger click areas (block behavior)
- Perfect for navigation menus!

## Expected Result

When you complete this exercise, your page will look like this:

```
┌────────────────────────────────────────────────────────────────┐
│                      PAGE HEADER (dark blue)                   │
│                  My Awesome Website                            │
├────────────────────────────────────────────────────────────────┤
│              NAVIGATION (inline-block items)                   │
│  ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐              │
│  │  Home   │ │  About  │ │Services │ │ Contact │              │
│  └─────────┘ └─────────┘ └─────────┘ └─────────┘              │
├────────────────────────────────────────────────────────────────┤
│                                                                │
│                      MAIN CONTENT                              │
│                    (centered container)                        │
│                                                                │
│  Welcome to My Website                                        │
│  ─────────────────────────                                    │
│                                                                │
│  This is a complete page layout demonstrating block and       │
│  inline-block elements working together.                      │
│                                                                │
│  The navigation above uses inline-block to create a           │
│  horizontal menu with clickable padding.                      │
│                                                                │
├────────────────────────────────────────────────────────────────┤
│                      PAGE FOOTER (dark blue)                   │
│              © 2024 My Awesome Website                        │
└────────────────────────────────────────────────────────────────┘
```

## How to Check Your Work

1. **Save `styles.css`**

2. **Open `index.html` in your web browser**

3. **Verify the page header**:
   - Should have **dark blue background** (#2c3e50)
   - Text should be **white and centered**
   - Should have **20px padding**

4. **Verify the navigation**:
   - Links should appear **horizontally** (side by side)
   - **No bullet points** should be visible
   - Links should have **padding** (larger clickable area)
   - **Hover** over a link - background should **darken** (#3d566e)

5. **Verify the main content**:
   - Container should be **centered on the page**
   - Should have **max-width of 800px**
   - Should have **space on the sides**

6. **Verify the footer**:
   - Should have **dark blue background**
   - Text should be **semi-transparent white**
   - Should be **centered**
   - Should have **space above it**

## Common Issues

### Issue: Navigation items are stacking vertically

**Possible cause:** You forgot `display: inline-block` on the list items.

**Fix:** Make sure list items are inline-block:
```css
/* WRONG - list items are block by default */
.nav-menu li {
    /* no display property = block */
}

/* RIGHT - inline-block makes them horizontal */
.nav-menu li {
    display: inline-block;
}
```

### Issue: The links don't have padding

**Possible cause:** You forgot `display: inline-block` on the links.

**Fix:** Links need inline-block to accept padding:
```css
/* Links are inline by default - ignore padding */
.nav-menu a {
    padding: 15px 20px;  /* Won't work without inline-block! */
}

/* RIGHT - inline-block allows padding */
.nav-menu a {
    display: inline-block;
    padding: 15px 20px;  /* Now it works! */
}
```

### Issue: Bullet points are still showing

**Possible cause:** You forgot `list-style: none` on the ul/ol.

**Fix:** Remove list styling:
```css
.nav-menu {
    list-style: none;  /* Removes bullet points */
    margin: 0;
    padding: 0;
}
```

### Issue: The hover effect isn't working

**Possible cause:** You might have used the wrong pseudo-class syntax.

**Fix:** Use `:hover` with no space before it:
```css
/* WRONG - space before :hover */
.nav-menu a :hover {
    background-color: #3d566e;
}

/* RIGHT - no space before :hover */
.nav-menu a:hover {
    background-color: #3d566e;
}
```

### Issue: The container isn't centered

**Possible cause:** You forgot the `auto` in margin or didn't set a width.

**Fix:** Auto margins need a width constraint:
```css
.container {
    max-width: 800px;  /* Must have width */
    margin: 30px auto; /* auto = center left/right */
}
```

### Issue: There are small gaps between navigation items

**Possible cause:** This is normal! HTML whitespace creates small gaps between inline-block elements.

**Note:** This is expected behavior. We'll learn better solutions with Flexbox in the next lesson! For now, the small gaps are fine.

## Time Estimate

~30 minutes
