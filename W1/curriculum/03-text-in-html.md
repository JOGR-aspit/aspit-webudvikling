# Text in HTML

## Learning Objectives

By the end of this lesson, you will be able to:

- [ ] Understand the heading hierarchy (h1-h6) and when to use each level
- [ ] Create paragraphs with proper `<p>` tags
- [ ] Use `<strong>` for important/bold text and `<em>` for emphasized/italic text
- [ ] Add comments to HTML code with `<!-- -->`
- [ ] Write proper, semantic text content for webpages
- [ ] Explain the difference between semantic and non-semantic text formatting

## Prerequisites

**Required**: You should have completed:
- "How the Internet Works" (Lesson 01) - to understand how webpages are delivered
- "Basic HTML Structure" (Lesson 02) - to understand HTML tags and structure

**Estimated Reading Time**: 25-30 minutes

**What You'll Need**: A text editor (like VS Code) and a web browser

---

## Heading Tags

HTML provides six levels of headings, from most important (`<h1>`) to least important (`<h6>`). These headings create a visual and structural hierarchy for your content.

### Why Headings Matter

Headings are important for several reasons:

1. **Visual hierarchy** - They make your content scannable and easy to read
2. **Accessibility** - Screen readers use headings to navigate content
3. **SEO (Search Engine Optimization)** - Search engines use headings to understand your page structure
4. **Structure** - They organize your content into logical sections

### The Six Heading Levels

Here are all six heading levels:

```html
<!-- This is the main heading - most important -->
<h1>Main Title</h1>

<!-- This is a section heading -->
<h2>Section Title</h2>

<!-- This is a subsection heading -->
<h3>Subsection Title</h3>

<!-- This is a sub-subsection heading -->
<h4>Minor Section Title</h4>

<!-- This is a very specific section heading -->
<h5>Detailed Section Title</h5>

<!-- This is the least important heading level -->
<h6>Smallest Section Title</h6>
```

### How They Look in a Browser

When rendered by a browser, the headings look like this:

```
Main Title          ← h1 (largest, boldest)
================================================================================

Section Title         ← h2 (smaller than h1)
--------------------------------------------------------------------------------

Subsection Title     ← h3 (smaller than h2)
............................................................

Minor Section Title  ← h4 (smaller than h3)
..............................

Detailed Section    ← h5 (smaller than h4)
Title

Smallest Section    ← h6 (smallest)
Title
```

### When to Use Each Heading Level

Use headings to create a clear, logical structure:

| Level | When to Use | Example |
|-------|--------------|----------|
| **h1** | Main page title - use only once per page | `<h1>Welcome to My Website</h1>` |
| **h2** | Major sections of your page | `<h2>About Me</h2>` |
| **h3** | Subsections within major sections | `<h3>My Background</h3>` |
| **h4** | Details within subsections | `<h4>Education</h4>` |
| **h5** | Very specific details | `<h5>University Courses</h5>` |
| **h6** | Smallest possible section | `<h6>Course Details</h6>` |

### Proper Heading Hierarchy Example

Here's a well-structured webpage using headings:

```html
<!-- Main page title (one h1 per page) -->
<h1>My Personal Website</h1>

<!-- First major section -->
<h2>About Me</h2>
    <!-- Subsection of About -->
    <h3>My Background</h3>
    <p>I grew up in... (content)</p>

    <!-- Another subsection of About -->
    <h3>My Interests</h3>
    <p>I enjoy... (content)</p>

<!-- Second major section -->
<h2>My Projects</h2>
    <!-- Subsection of Projects -->
    <h3>Project One</h3>
    <p>Description of project one... (content)</p>

    <!-- Another subsection of Projects -->
    <h3>Project Two</h3>
    <p>Description of project two... (content)</p>

<!-- Third major section -->
<h2>Contact</h2>
<p>Get in touch at... (content)</p>
```

### Bad Heading Practices

**Don't skip heading levels**:

```html
<!-- BAD: Skips h2 -->
<h1>Main Title</h1>
<h3>This should be h2</h3>

<!-- GOOD: Uses h2 -->
<h1>Main Title</h1>
<h2>This is correct</h2>
```

**Don't use headings just for styling**:

```html
<!-- BAD: Using h3 just to make text smaller -->
<p>
    Regular paragraph text
    <h3>This is wrong - h3 is a heading, not a style</h3>
    More paragraph text
</p>

<!-- GOOD: Use CSS for styling (you'll learn this later) -->
<p>
    Regular paragraph text
    <span style="font-size: smaller;">This is the right way</span>
    More paragraph text
</p>
```

**Don't use more than one h1 per page**:

```html
<!-- BAD: Multiple h1 tags -->
<h1>My Website</h1>
<h1>Another Main Title</h1>

<!-- GOOD: One h1, use h2 for other main sections -->
<h1>My Website</h1>
<h2>About</h2>
<h2>Contact</h2>
```

### Success Criteria

You understand headings if you can:
- Name all six heading levels in order (h1 to h6)
- Explain when to use each heading level
- Write properly nested headings without skipping levels
- Identify bad heading usage (skipping levels, multiple h1s)

---

## Paragraphs

Paragraphs are the building blocks of text content on webpages. They group related sentences together.

### The `<p>` Tag

The `<p>` tag creates a paragraph of text:

```html
<!-- This creates a paragraph -->
<p>This is a paragraph of text.</p>
```

### How Paragraphs Work

When you use `<p>` tags:

1. The browser displays the text
2. It automatically adds spacing above and below the paragraph
3. Each `<p>` tag starts on a new line

**Example**:

```html
<p>This is the first paragraph.</p>
<p>This is the second paragraph.</p>
<p>This is the third paragraph.</p>
```

**What it looks like**:

```
This is the first paragraph.

This is the second paragraph.

This is the third paragraph.
```

Notice how the browser automatically adds space between paragraphs!

### Multiple Paragraphs in Sequence

You can have as many paragraphs as you need:

```html
<h1>My Story</h1>

<p>My name is Alex and I love web development. I started learning HTML last year and have been building websites ever since.</p>

<p>Web development is exciting because you can create something and share it with the world instantly. I enjoy seeing my ideas come to life on the screen.</p>

<p>In this website, I'll share my projects and what I've learned along the way. I hope you enjoy exploring my work!</p>
```

### Common Mistake: Using `<br>` Instead of `<p>`

**Don't use line breaks (`<br>`) to create paragraphs**:

```html
<!-- BAD: Using <br> for spacing -->
<p>This is paragraph one.</p>
<br><br>
<p>This is paragraph two.</p>

<!-- GOOD: Let browsers handle spacing automatically -->
<p>This is paragraph one.</p>
<p>This is paragraph two.</p>
```

The `<br>` tag (line break) is for forcing text to the next line within a paragraph. It's NOT for creating space between paragraphs.

### When to Use `<br>` (Line Break)

Use `<br>` only when you need to break a line within a paragraph:

```html
<p>
    My address is:<br>
    123 Main Street<br>
    Anytown, USA 12345
</p>
```

**What it looks like**:

```
My address is:
123 Main Street
Anytown, USA 12345
```

### Paragraphs with Headings

Paragraphs work perfectly with headings to structure content:

```html
<h1>Welcome to My Blog</h1>

<p>Hello! This is my first blog post. I'm excited to share my thoughts with you.</p>

<h2>Today's Topic</h2>

<p>Today I want to talk about something important: how to structure your HTML properly.</p>

<p>Using the right tags for the right purpose makes your code cleaner and your website more accessible.</p>

<h2>Why Structure Matters</h2>

<p>Good structure helps search engines understand your content. It also makes your website easier to navigate for people using screen readers.</p>
```

### Success Criteria

You understand paragraphs if you can:
- Explain what the `<p>` tag does
- Describe how browsers render paragraphs (spacing)
- Write multiple paragraphs in sequence
- Identify when to use `<br>` vs `<p>`

---

## Text Formatting

HTML provides tags for formatting text in ways that are meaningful (semantic) rather than just visual.

### Semantic vs Non-Semantic Tags

**Semantic tags** describe what the text means:
- `<strong>` = important text
- `<em>` = emphasized text

**Non-semantic tags** only describe how text looks:
- `<b>` = bold text
- `<i>` = italic text

**Always prefer semantic tags!** They help with accessibility and SEO.

### The `<strong>` Tag (Important Text)

Use `<strong>` for text that is important or should be strongly emphasized:

```html
<p><strong>Warning:</strong> Please read this carefully.</p>

<p>The <strong>most important</strong> thing is to keep practicing.</p>
```

**What it looks like** (bold text):

```
Warning: Please read this carefully.
The most important thing is to keep practicing.
```

Screen readers announce `<strong>` text with emphasis, so users know it's important.

### The `<b>` Tag (Bold Visual Only)

The `<b>` tag makes text bold but doesn't add meaning:

```html
<p>This text is <b>bold</b> but not important.</p>
```

**What it looks like** (bold text):

```
This text is bold but not important.
```

Screen readers treat `<b>` the same as regular text. There's no emphasis.

**When to use `<b>`**: Rarely. Use it only when you want bold text but no emphasis (e.g., product names, keywords).

**When to use `<strong>`**: Almost always. Use it for important information, warnings, or key points.

### Comparison: `<strong>` vs `<b>`

```html
<!-- GOOD: Semantic - important information -->
<p><strong>Important:</strong> Don't forget to save your work!</p>

<!-- AVOID: Non-semantic - just looks bold -->
<p><b>Important:</b> Don't forget to save your work!</p>
```

Both look the same in a browser (bold text), but `<strong>` is better because:
- Screen readers announce it as important
- Search engines know it's important
- The meaning is clear to everyone

### The `<em>` Tag (Emphasized Text)

Use `<em>` for text that should be emphasized or stressed:

```html
<p>I <em>really</em> love web development!</p>

<p>Please <em>don't</em> forget to submit your assignment.</p>
```

**What it looks like** (italic text):

```
I really love web development!
Please don't forget to submit your assignment.
```

Screen readers announce `<em>` text with emphasis, changing their tone.

### The `<i>` Tag (Italic Visual Only)

The `<i>` tag makes text italic but doesn't add meaning:

```html
<p>This text is <i>italic</i> but not emphasized.</p>
```

**What it looks like** (italic text):

```
This text is italic but not emphasized.
```

Screen readers treat `<i>` the same as regular text. There's no emphasis.

**When to use `<i>`**: For things that are conventionally italicized (book titles, foreign words, taxonomic names).

**When to use `<em>`**: For text that should be emphasized or stressed.

### Comparison: `<em>` vs `<i>`

```html
<!-- GOOD: Semantic - emphasized meaning -->
<p>I <em>truly</em> believe this is important.</p>

<!-- AVOID: Non-semantic - just looks italic -->
<p>I <i>truly</i> believe this is important.</p>
```

Both look the same in a browser (italic text), but `<em>` is better because:
- Screen readers emphasize the text
- The meaning is clear (stress/emphasis)
- It follows accessibility best practices

### When to Use Each Tag

| Tag | Purpose | When to Use |
|------|----------|-------------|
| `<strong>` | Important text | Warnings, key points, important information |
| `<b>` | Bold visual only | Product names, keywords (rarely) |
| `<em>` | Emphasized text | Stressed words, contrast, emphasis |
| `<i>` | Italic visual only | Book titles, foreign words, scientific names |

### Combining Strong and Em

You can combine `<strong>` and `<em>` for very important, strongly emphasized text:

```html
<p><strong><em>This is both important AND emphasized!</em></strong></p>
```

**What it looks like** (bold and italic):

```
This is both important AND emphasized!
```

### Real-World Example

Here's a complete example using all text formatting:

```html
<h1>Important Safety Guidelines</h1>

<p><strong>Warning:</strong> Please read these guidelines carefully before proceeding.</p>

<h2>General Safety</h2>

<p>Always wear protective equipment when working with tools. <em>Never</em> attempt repairs without proper training.</p>

<h2>Emergency Procedures</h2>

<p>If you encounter an emergency, follow these steps:</p>

<ol>
    <li>Stay calm</li>
    <li>Call emergency services at <strong>911</strong></li>
    <li>Evacuate the area if necessary</li>
</ol>

<p><em><strong>Remember:</strong></em> Your safety is the top priority!</p>
```

### Success Criteria

You understand text formatting if you can:
- Explain the difference between `<strong>` and `<b>`
- Explain the difference between `<em>` and `<i>`
- Choose the right tag for different situations
- Combine `<strong>` and `<em>` tags

---

## HTML Comments

Comments are notes you write in your code that browsers ignore. They don't appear on the webpage.

### What Are Comments?

Comments are:
- Notes to yourself (or other developers) about the code
- Completely ignored by browsers (not displayed on the webpage)
- Essential for maintaining and understanding your code

### Comment Syntax

HTML comments start with `<!--` and end with `-->`:

```html
<!-- This is a comment. Browsers will ignore this. -->
<p>This is visible content on the webpage.</p>
```

### Single-Line Comments

A comment on one line:

```html
<!-- This is a single-line comment -->
<p>This paragraph is visible.</p>
```

### Multi-Line Comments

Comments that span multiple lines:

```html
<!--
    This is a multi-line comment.
    I can write as much as I want here.
    The browser will ignore all of it.
-->
<p>This paragraph is still visible.</p>
```

### Commenting Out Code

You can use comments to temporarily disable code without deleting it:

```html
<!-- I'm working on this section, so I'll comment it out for now -->
<!--
<h2>Coming Soon</h2>
<p>This section is under construction.</p>
-->
<p>Check back later for updates!</p>
```

Only the last paragraph will be displayed. The commented-out section won't appear.

### Where to Use Comments

Use comments to:

1. **Explain complex code**:
```html
<!-- This navigation menu uses an unordered list for semantic structure -->
<nav>
    <ul>
        <li><a href="home.html">Home</a></li>
        <li><a href="about.html">About</a></li>
    </ul>
</nav>
```

2. **Mark sections**:
```html
<!-- ========== START: ABOUT SECTION ========== -->
<h2>About Me</h2>
<p>Content about me...</p>
<!-- ========== END: ABOUT SECTION ========== -->
```

3. **Add reminders**:
```html
<!-- TODO: Add more photos here later -->
<p>Photo gallery coming soon!</p>
```

4. **Credit sources**:
```html
<!-- Image source: https://unsplash.com/photos/example -->
<img src="photo.jpg" alt="Beautiful landscape">
```

### Comment Best Practices

1. **Keep comments concise and clear**:
```html
<!-- GOOD -->
<!-- Main page heading -->
<h1>Welcome to My Website</h1>

<!-- AVOID -->
<!-- This heading below is the main heading of the page and it should be the largest and most prominent text on the page -->
<h1>Welcome to My Website</h1>
```

2. **Comment why, not what**:
```html
<!-- GOOD -->
<!-- Using semantic HTML for accessibility -->
<nav>...</nav>

<!-- AVOID -->
<!-- This is a nav tag -->
<nav>...</nav>
```

3. **Keep comments up to date**:
Remove or update comments when the code changes. Outdated comments are confusing.

4. **Don't over-comment**:
Comment important or confusing parts, not obvious things:
```html
<!-- GOOD -->
<!-- Loop through all users and display their names -->
<ul id="user-list"></ul>

<!-- AVOID: This is obvious -->
<!-- This is a paragraph -->
<p>Hello world!</p>
```

### Success Criteria

You understand comments if you can:
- Write HTML comments using `<!-- -->`
- Create single-line and multi-line comments
- Comment out code temporarily
- Follow best practices for commenting

---

## Putting It All Together

Now let's create a complete blog post using all the text elements we've learned.

### Complete Example: Blog Post

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>My First Blog Post</title>
    </head>

    <body>
        <!-- Main page title - one h1 per page -->
        <h1>My First Blog Post</h1>

        <!-- Introduction paragraph -->
        <p>
            Hello! Welcome to my very first blog post. I'm excited to share my journey into web development with you.
            In this post, I'll talk about why I chose to learn HTML and what I've learned so far.
        </p>

        <!-- First major section -->
        <h2>Why I Started Learning Web Development</h2>

        <p>
            I've always been curious about how websites work. Every time I visited a beautiful website,
            I wondered: <em>"How do they create this?"</em>
        </p>

        <p>
            When I discovered that HTML is the foundation of every webpage, I knew I had to learn it.
            The idea that I could create something and share it with the entire world was incredibly exciting.
        </p>

        <!-- Second major section -->
        <h2>What I've Learned So Far</h2>

        <p>
            Over the past few weeks, I've been learning the fundamentals of HTML.
            Here are some of the key concepts I've mastered:
        </p>

        <ul>
            <li>HTML document structure (DOCTYPE, html, head, body)</li>
            <li>Heading hierarchy (h1 through h6)</li>
            <li>Paragraphs and how browsers render them</li>
            <li>Semantic text formatting (strong and em tags)</li>
            <li>HTML comments for code documentation</li>
        </ul>

        <!-- Third major section -->
        <h2>The Importance of Semantic HTML</h2>

        <p>
            One thing that really surprised me was the importance of using semantic HTML tags.
            It's not just about how the content looks - it's about <strong>what the content means</strong>.
        </p>

        <p>
            For example, using <code>&lt;strong&gt;</code> instead of <code>&lt;b&gt;</code> might seem like a small difference,
            but it matters for accessibility and search engine optimization.
            Screen readers announce <strong>important</strong> text differently, making the content accessible to everyone.
        </p>

        <!-- Fourth major section -->
        <h2>My Favorite Resources</h2>

        <p>
            Here are some resources that have helped me learn HTML:
        </p>

        <ul>
            <li><em>MDN Web Docs</em> - Excellent documentation</li>
            <li><em>W3Schools</em> - Great tutorials and examples</li>
            <li><em>freeCodeCamp</em> - Interactive coding challenges</li>
        </ul>

        <!-- Fifth major section -->
        <h2>What's Next</h2>

        <p>
            I'm currently working on learning about lists, links, and images in HTML.
            <strong>My next goal</strong> is to build my personal portfolio website using all the HTML skills I've learned.
        </p>

        <p>
            If you're just starting out with web development, <em>don't give up!</em>
            The learning curve is real, but it's also incredibly rewarding to see your creations come to life.
        </p>

        <!-- Closing paragraph -->
        <p>
            Thanks for reading my first blog post! I'll be sharing more updates as I continue my web development journey.
            <strong>Feel free to leave a comment below!</strong>
        </p>

        <!-- TODO: Add a comment section later -->
        <!-- <section id="comments">
            <h3>Comments</h3>
            <p>Comment section coming soon!</p>
        </section> -->

    </body>
</html>
```

### What This Page Will Look Like

When rendered in a browser, the page will display:

```
My First Blog Post
================================================================================

Hello! Welcome to my very first blog post. I'm excited to share my journey into web
development with you. In this post, I'll talk about why I chose to learn HTML
and what I've learned so far.

Why I Started Learning Web Development
--------------------------------------------------------------------------------

I've always been curious about how websites work. Every time I visited a beautiful
website, I wondered: "How do they create this?"

When I discovered that HTML is the foundation of every webpage, I knew I had to
learn it. The idea that I could create something and share it with the entire
world was incredibly exciting.

What I've Learned So Far
--------------------------------------------------------------------------------

Over the past few weeks, I've been learning the fundamentals of HTML. Here are
some of the key concepts I've mastered:

• HTML document structure (DOCTYPE, html, head, body)
• Heading hierarchy (h1 through h6)
• Paragraphs and how browsers render them
• Semantic text formatting (strong and em tags)
• HTML comments for code documentation

The Importance of Semantic HTML
--------------------------------------------------------------------------------

One thing that really surprised me was the importance of using semantic HTML tags.
It's not just about how the content looks - it's about what the content means.

For example, using <strong> instead of <b> might seem like a small difference,
but it matters for accessibility and search engine optimization. Screen readers announce
important text differently, making the content accessible to everyone.

My Favorite Resources
--------------------------------------------------------------------------------

Here are some resources that have helped me learn HTML:

• MDN Web Docs - Excellent documentation
• W3Schools - Great tutorials and examples
• freeCodeCamp - Interactive coding challenges

What's Next
--------------------------------------------------------------------------------

I'm currently working on learning about lists, links, and images in HTML. My next
goal is to build my personal portfolio website using all the HTML skills I've learned.

If you're just starting out with web development, don't give up! The learning
curve is real, but it's also incredibly rewarding to see your creations come
to life.

Thanks for reading my first blog post! I'll be sharing more updates as I continue
my web development journey. Feel free to leave a comment below!
```

### Key Features of This Example

1. **Proper heading hierarchy** - h1 for title, h2 for major sections
2. **Multiple paragraphs** - Organized logically with automatic spacing
3. **Semantic formatting** - `<strong>` for important text, `<em>` for emphasis
4. **Useful comments** - Explains code structure, marks TODO items
5. **Commented-out code** - Shows future plans without affecting current page

---

## Summary

In this lesson, you learned:

1. **Heading tags (h1-h6)** create a visual and structural hierarchy
   - Use h1 once per page for the main title
   - Use h2-h6 for sections and subsections
   - Don't skip heading levels
   - Don't use headings just for styling

2. **Paragraph tags (`<p>`)** group related sentences together
   - Browsers automatically add spacing between paragraphs
   - Use `<br>` only for line breaks within paragraphs, not for spacing

3. **Semantic text formatting** is better than visual-only formatting
   - `<strong>` for important text (better than `<b>`)
   - `<em>` for emphasized text (better than `<i>`)
   - Semantic tags help accessibility and SEO

4. **HTML comments** (`<!-- -->`) document your code
   - Browsers ignore comments
   - Use comments to explain complex code, mark sections, and add reminders
   - Keep comments concise, clear, and up to date

### Key Takeaways

- Always use semantic HTML tags (`<strong>`/`<em>` instead of `<b>`/`<i>`)
- Create a clear heading hierarchy for better accessibility and SEO
- Let browsers handle paragraph spacing automatically
- Use comments to make your code maintainable
- Good structure and semantics make your website accessible to everyone

---

## Next Steps

Now that you understand text elements in HTML, you're ready to learn:

**Next Topic**: Lists in HTML

In the next lesson, you'll learn:
- How to create unordered (bulleted) and ordered (numbered) lists
- When to use each type of list
- How to nest lists within lists
- Practical uses of lists (navigation menus, features, steps)

Lists are essential for organizing content and will be used in almost every webpage you create.

---

## Validation Checkpoint

Test your understanding by answering these questions:

### Question 1: How many h1 tags should you use per page?

**Answer**: You should use only ONE h1 tag per page. The h1 represents the main title of the page. Use h2, h3, etc. for other sections.

### Question 2: What is the difference between `<strong>` and `<b>`?

**Answer**: `<strong>` is a semantic tag that means "important text." Screen readers announce it with emphasis, and search engines treat it as important. `<b>` is a non-semantic tag that only makes text bold visually. Screen readers treat `<b>` the same as regular text. Always use `<strong>` for important information.

### Question 3: When should you use `<br>` vs `<p>`?

**Answer**: Use `<p>` (paragraph tags) to create separate paragraphs - browsers automatically add spacing. Use `<br>` (line break) only when you need to break a line within a single paragraph, such as for addresses or poetry. Don't use `<br>` to create space between paragraphs.

### Question 4: What is the difference between `<em>` and `<i>`?

**Answer**: `<em>` is a semantic tag that means "emphasized text." Screen readers announce it with emphasis. `<i>` is a non-semantic tag that only makes text italic visually. Use `<em>` when you want to emphasize text, and `<i>` only for things conventionally italicized (book titles, foreign words).

### Question 5: Why are HTML comments useful?

**Answer**: HTML comments are useful for:
- Explaining complex or confusing code
- Marking sections of your code
- Adding reminders or TODOs
- Temporarily disabling code (commenting out) without deleting it
- Documenting sources or credits

Browsers ignore comments, so they don't appear on the webpage, but they help you and other developers understand the code.

### Question 6: Is it okay to skip heading levels (like h1 to h3)?

**Answer**: No, it's not okay to skip heading levels. You should always use headings in order (h1, h2, h3, etc.). Skipping levels (like going from h1 to h3) breaks the logical hierarchy and can confuse screen readers and search engines. If a heading level doesn't feel right, it usually means your content structure needs adjustment.

---

## Common Confusion Points

### Confusion: "Why not just use `<b>` and `<i>`? They're shorter."

**Answer**: While `<b>` and `<i>` are shorter to type, they don't convey meaning. Semantic tags like `<strong>` and `<em>` tell screen readers and search engines what the text means. This makes your content accessible to everyone and helps with search engine optimization. Always prioritize accessibility over convenience!

### Confusion: "Can I use multiple h1 tags on one page?"

**Answer**: Technically, yes, the browser will display multiple h1 tags. But you shouldn't! Multiple h1 tags confuse screen readers (who assume there's only one main title) and search engines (who use h1 to understand your page's main topic). Use one h1 per page and h2-h6 for other sections.

### Confusion: "Do browsers add spacing around headings?"

**Answer**: Yes, browsers automatically add margin (spacing) around headings. The larger the heading level, the more spacing is typically added. This is automatic - you don't need to add extra space manually. Later, when you learn CSS, you can control this spacing yourself.

### Confusion: "Can I nest paragraphs inside paragraphs?"

**Answer**: No! Paragraphs cannot contain other paragraphs. If you try, the browser will automatically close the first `<p>` tag when it sees the second `<p>` tag. This is a common mistake. If you need to nest content, use `<div>` tags (which you'll learn about in future lessons) instead of `<p>` tags.

### Confusion: "Why write comments if browsers ignore them?"

**Answer**: Comments aren't for the browser - they're for you (and other developers)! Comments help you understand your code when you return to it later. They help other developers understand your code if they work on it. Even though browsers ignore comments, they're essential for writing maintainable, understandable code.

### Confusion: "Does `<strong>` always make text bold?"

**Answer**: Usually yes, browsers display `<strong>` text as bold by default. However, the purpose of `<strong>` is semantic (meaning important), not visual (looking bold). You could use CSS to make `<strong>` text appear differently (not bold) - the tag's meaning (important) would remain the same. The appearance is separate from the meaning!

---

**Great job!** You now understand how to work with text elements in HTML. You're ready to learn about lists in the next lesson!
