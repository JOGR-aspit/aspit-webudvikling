# Project: Game Landing Page

## Overview

In this project, you'll create a **promotional landing page** for an upcoming video game you're excited about. This is a real-world task - game companies create landing pages to build hype, share information, and encourage pre-orders before a game releases.

Your landing page will include:
- A hero section with the game title and tagline
- Features section highlighting what makes the game exciting
- Screenshots or artwork gallery
- Release date and platform information
- Links to pre-order or learn more

---

## Learning Objectives

By completing this project, you will be able to:

- [ ] Create a complete, well-structured HTML document from scratch
- [ ] Use semantic HTML elements to organize content meaningfully
- [ ] Style your page with CSS including selectors, properties, and values
- [ ] Apply the CSS box model to control spacing and layout
- [ ] Use appropriate CSS units for fonts, spacing, and sizes
- [ ] Style text and headings for visual hierarchy
- [ ] Create a responsive layout that looks good on different screens

---

## Prerequisites

Before starting this project, you should have completed:

- [ ] Article 01: How the Internet Works
- [ ] Article 02: Basic HTML Structure
- [ ] Article 03: Text in HTML
- [ ] Article 04: Lists in HTML
- [ ] Article 05: Links and Images
- [ ] Article 06: Classes and Semantic HTML
- [ ] Article 07: CSS Fundamentals
- [ ] Article 08: CSS Selectors

---

## Project Scope

- **Time Estimate**: ~1-2 days
- **Difficulty**: Beginner
- **Topics Covered**: HTML structure, semantic elements, CSS fundamentals, selectors, box model, styling

---

## Requirements

### Functional Requirements

Your landing page **must include**:

| Requirement | Details |
|-------------|---------|
| **Hero section** | Game title, tagline, and call-to-action button |
| **Features section** | At least 3 features of the game (what makes it fun/unique) |
| **Gallery section** | At least 3 images (screenshots, artwork, or character art) |
| **Info section** | Release date, platforms (PC, PlayStation, Xbox, Switch, etc.) |
| **Footer** | Copyright notice and social/official links |
| **Navigation** | Links to each section (anchor links) |

### Technical Requirements

You must build your page using:

- [ ] Proper HTML document structure (DOCTYPE, html, head, body)
- [ ] Semantic HTML elements (header, nav, main, section, footer)
- [ ] Heading hierarchy (one h1, h2 for sections, etc.)
- [ ] CSS using element, class, and ID selectors appropriately
- [ ] External CSS file (linked with `<link>` tag)
- [ ] Box model properties (margin, padding, border)
- [ ] Text styling properties (color, font-size, font-family, etc.)
- [ ] At least one list (ordered or unordered)
- [ ] Images with descriptive alt text
- [ ] Consistent naming using kebab-case

---

## Milestones

### Milestone 1: Structure and Content

**Goal**: Create the HTML structure with all content, no styling yet.

**Tasks**:

1. **Set up your project folder**
   - Create a folder named `game-landing-page/`
   - Inside, create `index.html` and `styles.css`
   - Create an `images/` folder for your game images

2. **Write the HTML document structure**
   - Add `<!DOCTYPE html>`, `<html>`, `<head>`, and `<body>` tags
   - Add `<meta charset="UTF-8">` in the head
   - Add a `<title>` tag with your game's name
   - Link your CSS file: `<link rel="stylesheet" href="styles.css">`

3. **Create the header with navigation**
   - Add a `<header>` element
   - Inside the header, add an `<h1>` with the game title
   - Add a `<nav>` element with links to: Features, Gallery, Info
   - Use anchor links like `href="#features"` to jump to sections

4. **Create the hero section**
   - Add a `<section id="hero">` element
   - Include an `<h2>` with an exciting tagline
   - Add a paragraph describing what the game is about
   - Add a "Pre-Order Now" button link

5. **Create the features section**
   - Add a `<section id="features">` element
   - Add an `<h2>` heading: "Features"
   - Create an unordered list (`<ul>`) with at least 3 game features
   - Each feature should be a `<li>` with descriptive text

6. **Create the gallery section**
   - Add a `<section id="gallery">` element
   - Add an `<h2>` heading: "Gallery"
   - Add at least 3 `<img>` tags with `src` and `alt` attributes
   - Wrap each image in a `<figure>` element with a `<figcaption>` caption

7. **Create the info section**
   - Add a `<section id="info">` element
   - Add an `<h2>` heading: "Release Information"
   - Add a paragraph with the release date
   - Add an unordered list of platforms (PC, PlayStation, etc.)

8. **Create the footer**
   - Add a `<footer>` element
   - Include a copyright notice with `©` symbol
   - Add a link to the game's official website

**Verify your work**:
- [ ] Open `index.html` in your browser - you should see all content
- [ ] Content is unstyled (plain text and images) - this is correct for Milestone 1
- [ ] Navigation links jump to the correct sections when clicked
- [ ] All images display (or show alt text if image files don't exist yet)
- [ ] Use the browser's developer tools (F12) to check for HTML errors

---

### Milestone 2: CSS Styling - Colors and Typography

**Goal**: Add colors, fonts, and basic text styling.

**Tasks**:

1. **Set up your CSS file**
   - Open `styles.css`
   - Add a comment at the top with your name and the project name
   - Start with a reset: `* { margin: 0; padding: 0; box-sizing: border-box; }`
   - Add a `body` selector with `font-family: Arial, sans-serif;` and `line-height: 1.6;`

2. **Style the header**
   - Create a `header` selector
   - Add a background color: `background-color: #1a1a2e;` (dark blue)
   - Add text color: `color: #ffffff;` (white)
   - Add padding: `padding: 20px;`
   - Center the text: `text-align: center;`

3. **Style the navigation**
   - Create a `nav` selector
   - Add `margin-top: 15px;`
   - Style the `nav a` links:
     - `color: #00d9ff;` (cyan)
     - `text-decoration: none;` (remove underline)
     - `margin: 0 15px;` (space between links)

4. **Style the hero section**
   - Create a `#hero` selector
   - Add a different background color: `background-color: #16213e;`
   - Add padding: `padding: 60px 20px;`
   - Center align text: `text-align: center;`
   - Style the `#hero h2`:
     - `font-size: 2.5rem;`
     - `color: #e94560;` (accent color)
     - `margin-bottom: 20px;`

5. **Style the features section**
   - Create a `#features` selector with `padding: 40px 20px;`
   - Style `#features h2` with `color: #1a1a2e;` and `text-align: center;`
   - Style `#features ul` with `max-width: 600px;` and `margin: 20px auto;`
   - Style `#features li` with `margin-bottom: 10px;` and `font-size: 1.1rem;`

6. **Style the gallery section**
   - Create a `#gallery` selector with `padding: 40px 20px;` and `background-color: #f0f0f0;`
   - Style `#gallery h2` with `text-align: center;` and `color: #1a1a2e;`
   - Style `#gallery figure` with `display: inline-block;`, `margin: 10px;`, and `text-align: center;`
   - Style `#gallery img` with `max-width: 300px;` and `border: 3px solid #1a1a2e;`

7. **Style the info section**
   - Create an `#info` selector with `padding: 40px 20px;`
   - Style `#info h2` with `color: #1a1a2e;`
   - Style `#info ul` with `list-style-type: none;` and `padding: 0;`

8. **Style the footer**
   - Create a `footer` selector
   - Add `background-color: #1a1a2e;`, `color: #ffffff;`, `text-align: center;`, and `padding: 20px;`

**Verify your work**:
- [ ] Refresh your browser - the page should now have colors and styling
- [ ] Header and footer have dark backgrounds with white text
- [ ] Hero section has the accent color for the heading
- [ ] Navigation links are cyan and not underlined
- [ ] Gallery images have borders and are side by side
- [ ] Text is readable with good contrast

---

### Milestone 3: Spacing, Layout, and Polish

**Goal**: Use the box model for spacing, add hover effects, and finalize the design.

**Tasks**:

1. **Add spacing between sections**
   - After each section's background color, check that sections have visual separation
   - Add `margin` to sections if needed to create gaps
   - Ensure padding inside sections allows content to breathe

2. **Style the pre-order button**
   - Give the hero link a class: `class="cta-button"`
   - Create a `.cta-button` selector:
     - `display: inline-block;`
     - `background-color: #e94560;`
     - `color: #ffffff;`
     - `padding: 15px 30px;`
     - `text-decoration: none;`
     - `border-radius: 5px;`
     - `font-weight: bold;`

3. **Add hover effects**
   - Create a `.cta-button:hover` selector
   - Change the background: `background-color: #ff6b6b;`
   - Create a `nav a:hover` selector
   - Add `text-decoration: underline;`

4. **Style the gallery captions**
   - Create a `#gallery figcaption` selector
   - Add `font-size: 0.9rem;`, `color: #555;`, and `margin-top: 5px;`

5. **Add a border to the info section**
   - Update the `#info` selector
   - Add `border: 2px solid #1a1a2e;`
   - Add `border-radius: 10px;`
   - Add `max-width: 600px;` and `margin: 40px auto;`

6. **Improve mobile responsiveness**
   - Add a media query at the end of your CSS:
     ```css
     @media (max-width: 600px) {
         #hero h2 { font-size: 1.8rem; }
         #gallery img { max-width: 100%; }
     }
     ```

7. **Find and add real images**
   - Search for images of your chosen game (official screenshots, artwork)
   - Save them to your `images/` folder
   - Update the `src` attributes in your HTML
   - Make sure each `alt` text describes what's in the image

8. **Final review**
   - Check all spacing (padding and margin) looks consistent
   - Verify text contrast is readable
   - Test all links work correctly
   - View the page at different browser widths (resize the window)

**Verify your work**:
- [ ] All sections have appropriate spacing (nothing looks crowded)
- [ ] The pre-order button looks clickable and has a hover effect
- [ ] Navigation links show underline on hover
- [ ] Gallery images display with captions below
- [ ] Info section is centered with a border and rounded corners
- [ ] Page looks good when browser window is resized (mobile-friendly)
- [ ] All images load correctly with descriptive alt text
- [ ] Code is well-commented and organized

---

## Starter Files

The following starter files are provided in the `starter-files/` folder:

- **index.html**: Basic HTML document structure with semantic sections already set up
- **styles.css**: Started CSS file with reset and body styles
- **images/**: Empty folder for you to add your game images

**What you need to do**:
- Fill in the content (game title, features, etc.) in the HTML
- Complete the CSS styling following the milestone tasks
- Add your own images to the images folder

---

## Success Criteria

Before submitting your project, verify:

### Structure
- [ ] HTML has proper document structure (DOCTYPE, html, head, body)
- [ ] Semantic HTML elements are used (header, nav, main, section, footer)
- [ ] Heading hierarchy is correct (one h1, h2 for sections)
- [ ] All tags are properly closed

### Content
- [ ] Hero section includes game title, tagline, and CTA button
- [ ] Features section has at least 3 features in a list
- [ ] Gallery section has at least 3 images with captions
- [ ] Info section includes release date and platforms
- [ ] Footer has copyright and link
- [ ] Navigation links work as anchor links

### Styling
- [ ] External CSS file is linked correctly
- [ ] Element, class, and ID selectors are used appropriately
- [ ] Box model properties (margin, padding, border) are used
- [ ] Text styling (color, font-size, font-family) is applied
- [ ] At least one hover effect is included
- [ ] Colors have good contrast for readability

### Code Quality
- [ ] Code is properly indented
- [ ] HTML comments explain sections
- [ ] CSS comments explain major style groups
- [ ] File names use kebab-case
- [ ] Images have descriptive alt text

---

## Common Issues

### Issue: My CSS isn't working!

**Possible cause**: The CSS file isn't linked correctly in the HTML.

**Fix**: Check that your `<link>` tag in the HTML head points to the correct file: `<link rel="stylesheet" href="styles.css">`. Make sure the file name matches exactly.

---

### Issue: Navigation links don't jump to sections.

**Possible cause**: Anchor links are missing the `#` or section IDs don't match.

**Fix**: Ensure links use `#` followed by the section ID (e.g., `href="#features"`). Each section must have a matching `id` attribute (e.g., `<section id="features">`).

---

### Issue: Images aren't displaying.

**Possible cause**: The image path is wrong or files aren't in the correct folder.

**Fix**: Make sure images are in the `images/` folder and use the correct path: `src="images/your-image.jpg"`. Check that file names match exactly (including uppercase/lowercase).

---

### Issue: My colors don't look good together.

**Possible cause**: Colors may have poor contrast or clash.

**Fix**: Use a color scheme generator or stick to the suggested colors in this project. Ensure text contrast is high enough for readability (dark text on light backgrounds, light text on dark backgrounds).

---

### Issue: Sections are too close together or too crowded.

**Possible cause**: Padding or margin isn't applied correctly.

**Fix**: Use the box model: `padding` adds space inside an element, `margin` adds space outside. Add `padding` to sections for internal breathing room, and `margin` between sections for separation.

---

### Issue: My page looks different when I resize the browser.

**Possible cause**: Fixed widths don't adapt to different screen sizes.

**Fix**: Use percentages or `max-width` instead of fixed pixel widths. Add the media query from Milestone 3 to handle smaller screens.

---

## Extension Ideas

Want to add more? Try these optional enhancements:

- Add more sections: "Story", "Characters", "Reviews", or "FAQ"
- Create a gradient background for the hero section
- Add transitions for smoother hover effects
- Include a "Subscribe for Updates" form (HTML only, styling only)
- Add a video trailer section using an iframe
- Create a dark/light theme toggle (advanced - requires JavaScript)
- Add smooth scrolling behavior to the page

---

**Time Estimate**: ~1-2 days
**Difficulty**: Beginner
**Focus**: HTML structure, semantic elements, CSS fundamentals, selectors, box model
