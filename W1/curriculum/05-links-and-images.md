# Links and Images

## Learning Objectives

By the end of this lesson, you will be able to:

- [ ] Create links with `<a>` tags and `href` attributes
- [ ] Understand absolute vs relative file paths
- [ ] Add images to webpages with `<img>` tags
- [ ] Use alt text for accessibility
- [ ] Resize images with width and height attributes
- [ ] Make images clickable (image links)
- [ ] Link to different parts of the same page (anchor links)

## Prerequisites

**Required**: You should have completed:
- "How the Internet Works" (Lesson 01) - to understand how webpages are delivered
- "Basic HTML Structure" (Lesson 02) - to understand HTML tags and attributes
- "Text in HTML" (Lesson 03) - to understand text elements
- "Lists in HTML" (Lesson 04) - to understand lists (useful for navigation)

**Estimated Reading Time**: 30-35 minutes

**What You'll Need**: A text editor (like VS Code), a web browser, and some images to practice with

---

## Links (Anchor Tags)

Links are what make the web interconnected. They allow users to navigate between pages and websites.

### What Are Links?

Links (also called hyperlinks or anchors) are:
- Clickable elements that take you to another page
- The foundation of the internet's interconnectedness
- Created with the `<a>` tag (anchor tag)

**Every website you visit uses links** to connect its pages together!

### The `<a>` Tag and `href` Attribute

Links use the `<a>` tag with an `href` attribute:

```html
<!-- Basic link syntax -->
<a href="destination-url">Link text</a>
```

- `<a>` - The anchor tag (creates a link)
- `href` - The "hypertext reference" attribute (where link goes)
- Link text - What users click on (what they see)

### Basic Link Example

```html
<h1>Welcome to My Website</h1>

<p>
    Visit my <a href="about.html">about page</a> to learn more about me.
</p>

<p>
    Check out <a href="projects.html">my projects</a> to see what I've built.
</p>
```

**What it looks like in a browser**:

```
Welcome to My Website

Visit my about page to learn more about me.

Check out my projects to see what I've built.
```

The words "about page" and "my projects" are blue and underlined (default link styling). When you click them, you go to those pages.

### Linking to Other Pages on Your Site

To link to pages on the same website:

```html
<h1>My Website Navigation</h1>

<nav>
    <ul>
        <!-- All these links are to pages on the same site -->
        <li><a href="index.html">Home</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="projects.html">Projects</a></li>
        <li><a href="blog.html">Blog</a></li>
        <li><a href="contact.html">Contact</a></li>
    </ul>
</nav>
```

### Linking to External Websites

To link to other websites, use full URLs:

```html
<h1>Useful Resources</h1>

<p>Here are some great resources for learning HTML:</p>

<ul>
    <li><a href="https://developer.mozilla.org/en-US/docs/Learn/HTML">MDN Web Docs</a></li>
    <li><a href="https://www.w3schools.com/html/">W3Schools</a></li>
    <li><a href="https://www.freecodecamp.org/">freeCodeCamp</a></li>
</ul>
```

**Note**: External links start with `https://` or `http://`.

### Opening Links in New Tabs

To make a link open in a new tab or window:

```html
<a href="https://example.com" target="_blank">Visit Example</a>
```

- `target="_blank"` - Opens link in new tab/window
- Use this for external links (so users don't leave your site)

**Example**:

```html
<p>
    Check out my <a href="https://github.com" target="_blank">GitHub profile</a>
    for more projects!
</p>
```

### Email Links

You can create links that open an email client:

```html
<a href="mailto:email@example.com">Email Me</a>
```

- `mailto:` - Protocol that tells browser to open email client
- `email@example.com` - Email address

**Example**:

```html
<p>Questions? <a href="mailto:help@example.com">Contact us</a></p>
```

### Success Criteria

You understand links if you can:
- Write a basic link with `<a>` and `href`
- Link to pages on the same site
- Link to external websites
- Explain the `target="_blank"` attribute

---

## Understanding File Paths

File paths tell browsers where to find files (HTML pages, images, etc.). Understanding paths is crucial for linking.

### Why File Paths Matter

File paths matter because:
- Browsers need to know exactly where files are located
- Wrong path = broken link or missing image
- Different path types for different situations

### Absolute Paths

Absolute paths are **complete URLs** that include the domain name:

```html
<!-- Absolute paths - include full website address -->
<a href="https://www.example.com/about.html">About</a>
<a href="https://www.example.com/images/photo.jpg">Photo</a>
```

**When to use absolute paths**:
- Linking to external websites
- Linking to files on other domains
- When you want the full address

### Relative Paths

Relative paths are **shorter paths** that are relative to your current file location.

**Folder Structure Example**:
```
my-website/
├── index.html          ← Main page
├── about.html          ← About page
├── projects/
│   └── project1.html  ← In projects folder
└── images/
    └── logo.png       ← In images folder
```

#### 1. Same Folder

If file is in same folder as current page:

```html
<!-- From index.html to about.html (same folder) -->
<a href="about.html">About</a>
```

#### 2. Subfolder

If file is in a subfolder:

```html
<!-- From index.html to project1.html (in projects folder) -->
<a href="projects/project1.html">Project 1</a>
```

Use `/` between folder names and file names.

#### 3. Parent Folder

If file is in the parent folder (one level up):

```html
<!-- From projects/project1.html to index.html (parent folder) -->
<a href="../index.html">Home</a>
```

Use `../` to go up one folder level. Use `../../` to go up two levels.

#### 4. Root Folder

Starting from the root of your website:

```html
<!-- From any page to images/logo.png (starting at root) -->
<img src="/images/logo.png" alt="Logo">
```

Use `/` at the beginning to start from the root folder.

### Visual Example of File Paths

**Folder Structure**:
```
my-website/
│
├── index.html                ← You are here
├── about.html                ← Same folder: "about.html"
│
├── pages/                    ← Subfolder: "pages/contact.html"
│   └── contact.html
│
└── images/                   ← Subfolder: "images/photo.jpg"
    └── photo.jpg
```

**From index.html, links would be**:

```html
<!-- Same folder -->
<a href="about.html">About</a>

<!-- Subfolder -->
<a href="pages/contact.html">Contact</a>

<!-- Image in subfolder -->
<img src="images/photo.jpg" alt="Photo">
```

**From pages/contact.html, links would be**:

```html
<!-- Parent folder -->
<a href="../index.html">Home</a>

<!-- Same parent folder, different file -->
<a href="../about.html">About</a>

<!-- Images folder (go up one level, then into images) -->
<img src="../images/photo.jpg" alt="Photo">
```

### Common Path Mistakes

**1. Using backslashes instead of forward slashes**:

```html
<!-- WRONG: Uses backslash (\) -->
<a href="pages\about.html">About</a>

<!-- CORRECT: Uses forward slash (/) -->
<a href="pages/about.html">About</a>
```

**2. Forgetting folder names**:

```html
<!-- WRONG: Missing folder name -->
<a href="project1.html">Project 1</a>

<!-- CORRECT: Includes folder name -->
<a href="projects/project1.html">Project 1</a>
```

**3. Too many parent folder references**:

```html
<!-- WRONG: Goes up too many levels -->
<a href="../../../../index.html">Home</a>

<!-- CORRECT: Goes up right number of levels -->
<a href="../index.html">Home</a>
```

### Success Criteria

You understand file paths if you can:
- Explain the difference between absolute and relative paths
- Use relative paths for same-site links
- Use `../` to go to parent folders
- Identify common path mistakes

---

## Adding Images

Images make webpages visually engaging. The `<img>` tag is used to display images.

### The `<img>` Tag

The image tag is self-closing (no closing tag):

```html
<!-- Basic image syntax -->
<img src="image.jpg" alt="Description of image">
```

- `src` - The "source" attribute (where image file is located)
- `alt` - The "alternative text" attribute (description of image)
- **No closing tag needed** - `<img />` or just `<img>`

### Required Attributes

The `<img>` tag has two required attributes:

1. **`src` (source)** - Path to the image file
2. **`alt` (alternative text)** - Description of the image

```html
<!-- Both src and alt are required -->
<img src="photos/myphoto.jpg" alt="Photo of me standing by a lake">
```

### Basic Image Example

```html
<h1>About Me</h1>

<p>
    <img src="images/profile.jpg" alt="Profile photo of Alex">
</p>

<p>
    Hi! I'm Alex, a web developer who loves building beautiful websites.
    Welcome to my personal website!
</p>
```

**What it looks like**:

```
About Me

[PROFILE PHOTO]

Hi! I'm Alex, a web developer who loves building beautiful websites.
Welcome to my personal website!
```

### Image Sources: Local vs External

#### Local Images

Images stored on your website:

```html
<!-- Image in same folder -->
<img src="logo.png" alt="Website logo">

<!-- Image in subfolder -->
<img src="images/banner.jpg" alt="Website banner">
```

#### External Images

Images from other websites:

```html
<!-- Image from external website -->
<img src="https://example.com/images/photo.jpg" alt="External photo">
```

**Note**: External URLs use full web addresses (https://...).

### Image File Formats

Common image formats for websites:

| Format | When to Use | Notes |
|---------|---------------|--------|
| **.jpg / .jpeg** | Photographs | Good compression, small file size |
| **.png** | Graphics with transparency | Supports transparent backgrounds |
| **.gif** | Simple animations | Small file size, limited colors |
| **.svg** | Icons, logos | Scalable (vector graphics) |
| **.webp** | Modern web format | Better compression than jpg/png |

For now, focus on `.jpg` and `.png` - they're the most common.

### Success Criteria

You understand adding images if you can:
- Write a basic `<img>` tag with `src` and `alt`
- Use relative paths for local images
- Use absolute URLs for external images
- Name common image formats (.jpg, .png)

---

## Alt Text (Accessibility)

Alt text is one of the most important accessibility features in HTML. It's required and crucial for many users.

### What Is Alt Text?

Alt text (alternative text) is:
- A description of an image
- Read by screen readers for visually impaired users
- Displayed when images fail to load
- Used by search engines to understand image content

### Why Alt Text Matters

**1. Screen Readers**:

Visually impaired users use screen readers (software that reads webpage content aloud). Screen readers announce the alt text instead of the image.

**Without alt text**:
- Screen reader says: "Image" (unhelpful)
- User has no idea what the image shows

**With good alt text**:
- Screen reader says: "Image: Photo of a golden retriever puppy playing in a park"
- User understands the image content

**2. When Images Don't Load**:

Sometimes images fail to load (slow internet, broken link, etc.). When this happens, browsers display the alt text instead.

**Example**:
```
[Profile photo of Alex standing by a lake at sunset]

Hi! I'm Alex...
```

**3. Search Engine Optimization (SEO)**:

Search engines can't "see" images like humans can. They rely on alt text to understand what images show. Good alt text helps your images appear in image search results.

### Writing Good Alt Text

**Good alt text describes the image clearly and concisely**:

```html
<!-- GOOD: Descriptive -->
<img src="dog.jpg" alt="Golden retriever puppy playing in a park on a sunny day">

<!-- GOOD: Functional -->
<img src="search-icon.png" alt="Search button">

<!-- GOOD: Informative -->
<img src="chart.jpg" alt="Bar chart showing 50% increase in sales from 2023 to 2024">
```

### Bad Alt Text Examples

```html
<!-- BAD: Too vague -->
<img src="dog.jpg" alt="Image">

<!-- BAD: Unnecessary (screen reader already says "Image") -->
<img src="dog.jpg" alt="An image of a dog">

<!-- BAD: Too long -->
<img src="logo.jpg" alt="This is the company logo which we use on all our marketing materials and it features a blue circle with a white star inside it and our company name below in bold letters">

<!-- BAD: No alt text (completely inaccessible) -->
<img src="dog.jpg">
```

### When to Use Empty Alt Text

Sometimes images are purely decorative and don't need descriptions:

```html
<!-- Empty alt text: decorative spacer image -->
<img src="spacer.png" alt="">

<!-- Empty alt text: decorative divider -->
<img src="divider.jpg" alt="">
```

**Why use `alt=""`?**
- Tells screen readers "This image is decorative, skip it"
- Prevents screen reader from saying "Image" unnecessarily
- Still allows the image to be displayed for sighted users

### Images as Links (Alt Text for Links)

When an image is a link, the alt text should describe where the link goes:

```html
<!-- Image is a link to home page -->
<a href="index.html">
    <img src="logo.png" alt="Go to home page">
</a>
```

### Success Criteria

You understand alt text if you can:
- Explain why alt text is crucial for accessibility
- Write descriptive, concise alt text
- Identify bad alt text examples
- Know when to use empty alt text (`alt=""`)

---

## Resizing Images

Images should be properly sized for your webpage layout and performance.

### Why Resize Images?

**1. Page Load Speed**:

Large image files take longer to load. Resizing images to appropriate dimensions reduces file size and makes your website faster.

**2. Layout Control**:

You control how images fit into your webpage layout by setting their size.

**3. User Experience**:

Properly sized images look better and load faster, improving user experience.

### Width and Height Attributes

You can resize images using `width` and `height` attributes:

```html
<!-- Resize to 300 pixels wide, 200 pixels tall -->
<img src="photo.jpg" alt="My photo" width="300" height="200">
```

- `width` - Image width in pixels (px)
- `height` - Image height in pixels (px)

### Resizing Examples

```html
<!-- Large image -->
<img src="photo.jpg" alt="Large photo" width="800" height="600">

<!-- Medium image -->
<img src="photo.jpg" alt="Medium photo" width="400" height="300">

<!-- Small image (thumbnail) -->
<img src="photo.jpg" alt="Small photo" width="100" height="75">
```

**What they look like**:

```
Large image (800x600):
[===================================]
[                                     ]
[         LARGE PHOTO                ]
[                                     ]
[===================================]

Medium image (400x300):
[==================]
[                   ]
[    MEDIUM       ]
[                   ]
[==================]

Small image (100x75):
[=======]
[       ]
[ SMALL ]
[       ]
[=======]
```

### Just Width or Just Height

You can specify just width OR just height:

```html
<!-- Specify width only - height adjusts proportionally -->
<img src="photo.jpg" alt="Photo" width="400">

<!-- Specify height only - width adjusts proportionally -->
<img src="photo.jpg" alt="Photo" height="300">
```

Browser maintains aspect ratio (proportions) automatically.

### Aspect Ratio Warning

**Don't distort images by setting wrong proportions!**

```html
<!-- WRONG: Distorts image (unnatural proportions) -->
<img src="photo.jpg" alt="Distorted photo" width="400" height="400">

<!-- GOOD: Maintains aspect ratio (natural proportions) -->
<img src="photo.jpg" alt="Natural photo" width="400" height="300">
```

If you set both width and height, use the image's original aspect ratio to avoid distortion.

### Performance Note

**Resizing in HTML doesn't reduce file size!**

The `<img>` tag's `width` and `height` attributes only change display size. The image file itself is still the same size.

**Better approach**: Resize images with an image editor (like Paint, GIMP, or online tools) before adding them to your website. This reduces actual file size and improves performance.

You'll learn more about this when you study image optimization (future topic).

### Success Criteria

You understand image resizing if you can:
- Use `width` and `height` attributes to resize images
- Explain why specifying just width or just height works
- Identify distorted images (wrong aspect ratio)
- Understand that HTML resizing doesn't reduce file size

---

## Making Images Clickable (Image Links)

You can make an image a link by nesting it inside an `<a>` tag.

### How to Make an Image a Link

```html
<!-- Image link syntax -->
<a href="destination-url">
    <img src="image.jpg" alt="Link text description">
</a>
```

The `<img>` is nested inside the `<a>` tag.

### Basic Image Link Example

```html
<h1>Welcome to My Website</h1>

<!-- Clickable logo that goes to home page -->
<a href="index.html">
    <img src="logo.png" alt="Go to home page">
</a>
```

When users click the logo, they go to the home page.

### Common Use Cases

**1. Website Logo**:

```html
<nav>
    <!-- Logo links to home -->
    <a href="index.html">
        <img src="logo.png" alt="Website logo - Go to home">
    </a>

    <!-- Text navigation links -->
    <ul>
        <li><a href="about.html">About</a></li>
        <li><a href="contact.html">Contact</a></li>
    </ul>
</nav>
```

**2. Thumbnail Images**:

```html
<h1>My Photo Gallery</h1>

<p>Click on any photo to see it full-size:</p>

<!-- Thumbnail links to full-size image -->
<a href="photos/large/dog.jpg">
    <img src="photos/thumbnails/dog-small.jpg" alt="Photo of golden retriever puppy" width="150" height="100">
</a>
```

**3. Call-to-Action Images**:

```html
<h1>Download My App</h1>

<p>Click the button below to download:</p>

<!-- Image button links to download -->
<a href="downloads/app.exe">
    <img src="download-button.png" alt="Download button - Click to download app">
</a>
```

### Success Criteria

You understand image links if you can:
- Make an image clickable by nesting in `<a>` tag
- Identify common use cases for image links
- Write proper alt text for image links

---

## Putting It All Together

Now let's create a complete webpage using links and images.

### Complete Example: Portfolio Page

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>My Portfolio</title>
    </head>

    <body>
        <!-- Navigation with links -->
        <nav>
            <ul>
                <!-- Link to home page -->
                <li><a href="index.html">Home</a></li>
                <!-- Link to about page -->
                <li><a href="about.html">About</a></li>
                <!-- Link to projects page (current page - no link) -->
                <li><strong>Projects</strong></li>
                <!-- Link to contact page -->
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>

        <!-- Main page heading -->
        <h1>My Projects</h1>

        <p>Welcome to my project portfolio! Here are some things I've built:</p>

        <!-- Project 1 -->
        <article>
            <h2>Personal Website</h2>

            <!-- Project thumbnail (clickable) -->
            <a href="projects/website/index.html">
                <img src="images/thumbnails/website.jpg" alt="Thumbnail of personal website project" width="300" height="200">
            </a>

            <p>
                This is my first website! I built it using HTML and CSS to showcase
                my skills and share information about myself.
            </p>

            <!-- View project link -->
            <p>
                <a href="projects/website/index.html">View Project →</a>
            </p>
        </article>

        <hr>

        <!-- Project 2 -->
        <article>
            <h2>Recipe Blog</h2>

            <!-- Project thumbnail (clickable) -->
            <a href="projects/recipe-blog/index.html">
                <img src="images/thumbnails/blog.jpg" alt="Thumbnail of recipe blog project" width="300" height="200">
            </a>

            <p>
                A blog about cooking with beautiful photos of recipes. Features
                responsive design and an intuitive navigation menu.
            </p>

            <!-- View project link -->
            <p>
                <a href="projects/recipe-blog/index.html">View Project →</a>
            </p>
        </article>

        <hr>

        <!-- Project 3 -->
        <article>
            <h2>Product Landing Page</h2>

            <!-- Project thumbnail (clickable) -->
            <a href="projects/landing-page/index.html">
                <img src="images/thumbnails/landing.jpg" alt="Thumbnail of product landing page" width="300" height="200">
            </a>

            <p>
                A modern landing page for a fictional product. Includes
                call-to-action buttons, testimonials, and feature lists.
            </p>

            <!-- View project link -->
            <p>
                <a href="projects/landing-page/index.html">View Project →</a>
            </p>
        </article>

        <hr>

        <!-- Resources section with external links -->
        <h2>Learning Resources</h2>

        <p>
            Here are some resources that helped me learn web development:
        </p>

        <ul>
            <li>
                <!-- External link (opens in new tab) -->
                <a href="https://developer.mozilla.org/en-US/docs/Learn/HTML" target="_blank">
                    MDN Web Docs
                </a>
            </li>
            <li>
                <a href="https://www.w3schools.com/html/" target="_blank">
                    W3Schools HTML Tutorial
                </a>
            </li>
            <li>
                <a href="https://www.freecodecamp.org/" target="_blank">
                    freeCodeCamp
                </a>
            </li>
        </ul>

        <!-- Contact section with email link -->
        <h2>Contact Me</h2>

        <p>
            Have questions or want to work together?
            <!-- Email link -->
            <a href="mailto:contact@example.com">Send me an email!</a>
        </p>

        <!-- Social media links with icons -->
        <h2>Connect With Me</h2>

        <nav>
            <ul>
                <!-- Twitter link with icon -->
                <li>
                    <a href="https://twitter.com/myusername" target="_blank">
                        <img src="images/icons/twitter.png" alt="Twitter - Follow me" width="32" height="32">
                    </a>
                </li>
                <!-- GitHub link with icon -->
                <li>
                    <a href="https://github.com/myusername" target="_blank">
                        <img src="images/icons/github.png" alt="GitHub - View my code" width="32" height="32">
                    </a>
                </li>
                <!-- LinkedIn link with icon -->
                <li>
                    <a href="https://linkedin.com/in/myusername" target="_blank">
                        <img src="images/icons/linkedin.png" alt="LinkedIn - Connect with me" width="32" height="32">
                    </a>
                </li>
            </ul>
        </nav>

        <!-- Footer with copyright -->
        <hr>

        <footer>
            <p>© 2024 My Portfolio. Built with HTML & CSS.</p>
        </footer>

    </body>
</html>
```

### What This Page Will Look Like

When rendered in a browser, the page will display:

```
Home  About  [Projects]  Contact

My Projects
================================================================================

Welcome to my project portfolio! Here are some things I've built:

Personal Website
--------------------------------------------------------------------------------

[THUMBNAIL IMAGE]

This is my first website! I built it using HTML and CSS to showcase my skills
and share information about myself.

View Project →

Recipe Blog
--------------------------------------------------------------------------------

[THUMBNAIL IMAGE]

A blog about cooking with beautiful photos of recipes. Features responsive design
and an intuitive navigation menu.

View Project →

Product Landing Page
--------------------------------------------------------------------------------

[THUMBNAIL IMAGE]

A modern landing page for a fictional product. Includes call-to-action buttons,
testimonials, and feature lists.

View Project →

Learning Resources
--------------------------------------------------------------------------------

Here are some resources that helped me learn web development:

• MDN Web Docs
• W3Schools HTML Tutorial
• freeCodeCamp

Contact Me
--------------------------------------------------------------------------------

Have questions or want to work together? Send me an email!

Connect With Me
--------------------------------------------------------------------------------

[Twitter Icon]  [GitHub Icon]  [LinkedIn Icon]

--------------------------------------------------------------------------------

© 2024 My Portfolio. Built with HTML & CSS.
```

### Key Features of This Example

1. **Navigation links** - Links to pages on the same site
2. **Clickable images** - Thumbnails that link to project pages
3. **External links** - Links to other websites with `target="_blank"`
4. **Email links** - `mailto:` links for email
5. **Proper alt text** - Every image has descriptive alt text
6. **Image resizing** - Images have appropriate width and height
7. **Social icons** - Small images as links to social media

---

## Summary

In this lesson, you learned:

1. **Links (`<a>`)** connect webpages together
   - Use `href` attribute to specify destination
   - Link to pages on the same site (relative paths)
   - Link to external websites (absolute paths)
   - Use `target="_blank"` to open in new tab

2. **File paths** tell browsers where files are located
   - Absolute paths: Full URLs (https://...)
   - Relative paths: Relative to current file location
   - Same folder: `filename.html`
   - Subfolder: `folder/filename.html`
   - Parent folder: `../filename.html`
   - Root: `/filename.html`

3. **Images (`<img>`)** add visual content
   - Required attributes: `src` (source) and `alt` (alternative text)
   - Self-closing tag (no closing tag)
   - Common formats: .jpg, .png, .gif, .svg

4. **Alt text** is crucial for accessibility
   - Describes image content
   - Read by screen readers
   - Displayed when images fail to load
   - Used by search engines
   - Write descriptive, concise alt text
   - Use empty alt text (`alt=""`) for decorative images

5. **Image resizing** with `width` and `height`
   - Specify size in pixels
   - Maintain aspect ratio to avoid distortion
   - Resize with image editor for better performance

6. **Image links** make images clickable
   - Nest `<img>` inside `<a>` tag
   - Common use cases: logos, thumbnails, buttons

### Key Takeaways

- Links make the web interconnected and navigable
- Understand file paths to avoid broken links
- Always include alt text for accessibility
- Resize images appropriately for layout and performance
- Make images clickable for better user experience
- Use `target="_blank"` for external links

---

## Next Steps

Now that you understand links and images in HTML, you're ready to learn:

**Next Topic**: Classes and Semantic HTML

In the next lesson, you'll learn:
- How to add classes to HTML elements for styling
- Understanding semantic HTML elements (article, section, header, footer)
- When to use divs vs semantic elements
- How semantic HTML improves accessibility and SEO

Classes and semantic HTML are essential for building professional, accessible websites!

---

## Validation Checkpoint

Test your understanding by answering these questions:

### Question1: What is the difference between absolute and relative file paths?

**Answer**: Absolute paths are complete URLs that include the full website address (e.g., https://example.com/page.html). They're used for linking to external websites. Relative paths are shorter paths relative to your current file location (e.g., about.html, pages/contact.html, ../index.html). They're used for linking to pages and images on the same website.

### Question2: Why is alt text required for images?

**Answer**: Alt text is required because:
1. Screen readers (for visually impaired users) read alt text aloud to describe images
2. When images fail to load, browsers display alt text instead
3. Search engines use alt text to understand image content (SEO)
Without alt text, your website is inaccessible and images can't be understood by search engines.

### Question3: How do you link to a file in a parent folder?

**Answer**: To link to a file in the parent folder (one level up), use `../` at the beginning of the path. For example: `<a href="../index.html">Home</a>`. Use `../../` to go up two levels, `../../../` for three levels, etc.

### Question4: What does `target="_blank"` do on a link?

**Answer**: The `target="_blank"` attribute makes the link open in a new tab or window instead of the current tab. This is commonly used for external links so users don't leave your website when they click them.

### Question5: When should you use empty alt text (`alt=""`)?

**Answer**: Use empty alt text for purely decorative images that don't convey meaningful information (spacers, dividers, decorative elements). Empty alt text tells screen readers "This image is decorative, skip it," preventing unnecessary announcements. Never omit the alt attribute entirely - always include it, even if empty.

### Question6: Does resizing images with HTML attributes reduce file size?

**Answer**: No! Using `width` and `height` attributes on the `<img>` tag only changes display size. The actual image file remains the same size. To reduce file size (for faster loading), resize images with an image editor (Paint, GIMP, online tools) before adding them to your website.

---

## Common Confusion Points

### Confusion: "Why use relative paths instead of absolute paths for same-site links?"

**Answer**: Relative paths are better for same-site links because:
1. **They're shorter** and easier to write
2. **They work on any domain** - you can move your website to a different domain without breaking links
3. **They're easier to maintain** - less code to change if you reorganize folders

Use absolute paths only for external links to other websites.

### Confusion: "Do I need both width and height attributes on images?"

**Answer**: No, you can specify just width OR just height. The browser will automatically calculate the other dimension to maintain the image's aspect ratio (proportions). However, if you specify both, make sure they maintain the aspect ratio or the image will appear distorted.

### Confusion: "Why can't I see the images in my HTML file?"

**Answer**: You can't see images directly in your HTML code file - you need to open the HTML file in a web browser. The browser will display the images referenced by your `<img>` tags. Also, double-check that your file paths are correct and the image files exist in the specified locations.

### Confusion: "What if I forget the alt attribute on an image?"

**Answer**: The browser will still display the image, but your website will be less accessible. Screen readers won't know what the image shows. Search engines won't understand the image. If the image fails to load, users will see nothing instead of a description. Always include alt text!

### Confusion: "Can I link to files on my computer (C:\, D:\)?"

**Answer**: No, you shouldn't use local file paths (like C:\Users\Name\Documents\file.html). These paths work only on your computer. When you publish your website online, the links will be broken for everyone else. Use relative paths (file.html) or upload files to your web server and use relative paths.

### Confusion: "What's the difference between a broken image and missing alt text?"

**Answer**: A broken image is one that the browser can't find or load (wrong path, file doesn't exist, network error). The browser might display a "broken image" icon or nothing. Missing alt text means the image loads but has no description for screen readers. Both are problems - fix broken images and always add alt text!

---

**Great job!** You now understand how to work with links and images in HTML. You're ready to learn about classes and semantic HTML in the next lesson!
