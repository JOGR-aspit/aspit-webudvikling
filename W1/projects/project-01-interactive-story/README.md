# Project 1: Interactive Story (Choose Your Own Adventure)

## What You'll Build

In this project, you'll create a **multi-page interactive story** where readers make choices that determine what happens next. This is like those "Choose Your Own Adventure" books where you decide which path to take!

Your story will have:
- Multiple pages connected by links
- Choices that lead to different story paths
- Different endings based on choices
- Images to set the atmosphere
- Proper HTML structure throughout

---

## Learning Objectives

After completing this project, you will be able to:

- [ ] Create a multi-page website with proper file organization
- [ ] Use links to connect pages and create navigation
- [ ] Apply semantic HTML elements to structure content
- [ ] Add images with descriptive alt text
- [ ] Use lists to present choices and information
- [ ] Write HTML comments to document your code
- [ ] Test a complete website with multiple linked pages

---

## Prerequisites

Before starting this project, you should have completed:

- [ ] Article 02: Basic HTML Structure
- [ ] Article 03: Text in HTML
- [ ] Article 04: Lists in HTML
- [ ] Article 05: Links and Images
- [ ] Article 06: Classes and Semantic HTML

---

## Project Requirements

Your interactive story **must include**:

### Structure Requirements

| Requirement | Minimum | Details |
|-------------|---------|---------|
| Story pages | 5 pages | Start page + at least 4 additional pages |
| Images | 2 images | With descriptive alt text |
| Endings | 2 endings | Different outcomes based on choices |
| Lists | 2 lists | Ordered or unordered (choices, items, clues, etc.) |

### HTML Requirements

- [ ] Proper HTML document structure (DOCTYPE, html, head, body)
- [ ] Title tags with page-specific titles
- [ ] Semantic HTML elements (`<header>`, `<main>`, `<section>`, `<article>`, `<footer>`)
- [ ] Heading hierarchy (h1 for main title, h2 for sections)
- [ ] Paragraphs for story text
- [ ] Links to navigate between pages
- [ ] Images with `src` and `alt` attributes
- [ ] HTML comments explaining your structure

### File Requirements

- [ ] All files use **kebab-case** naming (e.g., `dark-forest.html`, not `DarkForest.html`)
- [ ] Main page is named `index.html`
- [ ] Images are stored in an `images/` folder
- [ ] All file names are descriptive and consistent

---

## Getting Started

### Step 1: Plan Your Story

**Before writing any code**, plan your story on paper or in a text document. Answer these questions:

1. **What is your story about?** (fantasy adventure, mystery, survival, sci-fi, etc.)
2. **Who is the main character?** (the reader, a specific character, etc.)
3. **What is the goal?** (find treasure, solve a mystery, escape, survive, etc.)
4. **What choices will the reader make?**
5. **How many endings will there be?**

#### Story Planning Template

Copy this template and fill it in:

```
STORY TITLE: _______________________

THEME: _______________________

MAIN CHARACTER: _______________________

GOAL: _______________________

PAGE STRUCTURE:
- index.html (Start): What happens first?
  - Choice A leads to: _______________
  - Choice B leads to: _______________
- _______________.html: What happens?
  - Choice leads to: _______________
- _______________.html: What happens?
  - Choice leads to: _______________
- _______________.html (Ending 1): What's the outcome?
- _______________.html (Ending 2): What's the outcome?

IMAGES NEEDED:
1. _______________ (for page: _______________)
2. _______________ (for page: _______________)
```

### Step 2: Set Up Your Files

1. Create a new folder for your project (e.g., `my-interactive-story/`)
2. Inside that folder, create:
   - `index.html` (your start page)
   - `images/` folder for your images
   - Additional HTML files as needed

### Step 3: Create Your Pages

Use the starter files in `starter-files/` as templates:

1. Open `starter-files/index.html`
2. Save a copy to your project folder
3. Edit the content to match your story
4. Repeat for each page in your story

### Step 4: Connect Your Pages

Make sure every page has:

1. **Links to other pages** using `<a>` tags
2. **Consistent navigation** (readers should always know their options)
3. **Clear choices** presented in a list

### Step 5: Add Images

1. Find or create images for your story
2. Save them in your `images/` folder
3. Add them to your pages using `<img>` tags
4. **Always include descriptive alt text**

### Step 6: Test Everything

1. Open `index.html` in your browser
2. Click every link to make sure it works
3. Follow every story path to every ending
4. Check that all images display correctly
5. Verify all pages have proper structure

---

## File Structure Example

Your project should look like this:

```
my-interactive-story/
├── index.html              <!-- Start page -->
├── forest-path.html        <!-- Story page 1 -->
├── village.html            <!-- Story page 2 -->
├── cave.html               <!-- Story page 3 -->
├── treasure-ending.html    <!-- Ending 1 -->
├── escape-ending.html      <!-- Ending 2 -->
└── images/
    ├── forest.jpg          <!-- Image for forest page -->
    └── treasure.jpg        <!-- Image for treasure page -->
```

---

## Code Example

Here's an example of how a story page should be structured:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>The Dark Forest - Your Story</title>
</head>
<body>
    <!-- Page header with story title -->
    <header>
        <h1>The Dark Forest</h1>
    </header>

    <!-- Main story content -->
    <main>
        <!-- Story section -->
        <section>
            <h2>What Happens</h2>

            <p>You stand at the edge of a dark forest. The trees tower above you, blocking out most of the sunlight. You can hear strange sounds coming from deep within.</p>

            <p>A <strong>wise old owl</strong> perched on a nearby branch hoots and seems to be watching you carefully.</p>
        </section>

        <!-- Image section -->
        <section>
            <img src="images/dark-forest.jpg" alt="A dark, mysterious forest with tall trees and fog rolling through. An owl watches from a branch." width="400">
        </section>

        <!-- Choices section -->
        <section>
            <h2>What Do You Do?</h2>

            <ul>
                <li><a href="forest-path.html">Enter the forest carefully</a></li>
                <li><a href="village.html">Go back to the village</a></li>
                <li><a href="index.html">Start over</a></li>
            </ul>
        </section>
    </main>

    <!-- Page footer -->
    <footer>
        <p><em>Your Adventure Story</em> - Page 2</p>
    </footer>
</body>
</html>
```

---

## Theme Ideas

Not sure what your story should be about? Here are some ideas:

### Mystery
- A valuable item has been stolen. Find the thief!
- Strange things are happening in town. Investigate!
- A secret message leads to hidden treasure.

### Fantasy Adventure
- You must find a magical artifact to save your village.
- A dragon threatens the kingdom. Can you stop it?
- Discover a portal to another world.

### Survival
- You're stranded on an island. Find a way home!
- Lost in a cave system. Find the exit!
- Trapped in a haunted house. Escape before dawn!

### Sci-Fi
- Your spaceship has crashed on an alien planet.
- You discover a secret laboratory with strange experiments.
- A time machine sends you to the past. Can you return?

### Horror (Mild)
- A mysterious letter leads to an old mansion.
- Strange noises in your house at night. Investigate!
- A cursed object has been found. What do you do?

---

## Success Criteria Checklist

Before submitting your project, verify:

### Structure
- [ ] Project has at least 5 HTML pages
- [ ] All pages have proper HTML document structure
- [ ] All pages use semantic HTML elements
- [ ] Files are named using kebab-case

### Content
- [ ] Story has a clear beginning, middle, and endings
- [ ] Story has at least 2 different endings
- [ ] Each page has clear heading hierarchy
- [ ] Story text uses paragraphs properly
- [ ] Text uses `<strong>` and `<em>` for emphasis

### Links and Navigation
- [ ] All links work correctly
- [ ] Every page has navigation options
- [ ] Reader can always make a choice
- [ ] There's a way to start over

### Images
- [ ] At least 2 images are included
- [ ] All images have descriptive alt text
- [ ] Images are stored in an `images/` folder
- [ ] Images are appropriately sized

### Lists
- [ ] At least 2 lists are used (choices, items, etc.)
- [ ] Lists use proper `<ul>` or `<ol>` tags
- [ ] List items are clear and readable

### Code Quality
- [ ] HTML comments explain the structure
- [ ] Code is properly indented
- [ ] No broken links or missing images
- [ ] All pages have descriptive titles

---

## Troubleshooting

### My links don't work!

1. **Check the file name** - Make sure the `href` matches the exact file name (including .html)
2. **Check for typos** - `forest.html` is different from `forrest.html`
3. **Check the path** - If files are in different folders, you need the correct path

### My images don't show!

1. **Check the file path** - Images in a folder need `images/filename.jpg`
2. **Check the file name** - Must match exactly (case-sensitive!)
3. **Check the file exists** - Make sure the image file is actually there

### My page looks wrong!

1. **Check for missing closing tags** - Every `<p>` needs a `</p>`
2. **Check for typos in tag names** - `<h1>` not `<h1`
3. **Check nesting** - Tags should close in reverse order they opened

### I don't know what to write!

1. **Start simple** - Write a basic story first, add details later
2. **Use a template** - Copy the example structure
3. **Look at the example solution** - See how it's organized
4. **Ask for help** - Your instructor can help brainstorm ideas

---

## Need More Help?

- **Review the curriculum** - Articles 02-06 cover all the concepts
- **Check the starter files** - Use the templates provided
- **Look at the example solution** - See a complete working story
- **Ask your instructor** - Don't hesitate to ask questions!

---

## What's Next?

After completing this project, you'll be ready to:

1. Learn CSS to style your web pages
2. Add visual design to make your stories more engaging
3. Create more complex multi-page websites

**Good luck with your interactive story!**

---

**Estimated Time**: 4-6 hours
**Difficulty**: Beginner
**Focus**: HTML only (no CSS or JavaScript)
