# Writing, Publishing & GitHub Guide
### For Angela — A Complete Beginner's Reference

---

## Part 1 — Understanding the Structure

Your blog is made of plain text files. There are seven of them:

```
blog/
├── index.html           ← Your home page
├── published.html       ← Section I
├── poetry.html          ← Section II
├── books.html           ← Section III
├── world.html           ← Section IV
├── contemplations.html  ← Section V
└── style.css            ← All the visual design (don't edit this)
```

**HTML files** are the pages people read. You edit them to add content.
**style.css** controls colours, fonts, and layout. You generally leave this alone.

---

## Part 2 — Adding a New Entry

### Adding an Essay or Contemplation (Published, World, Contemplations)

Open the relevant HTML file and find the comment block that looks like this:

```html
<!-- Example entry — replace with your own:
<li class="entry">
  ...
</li>
-->
```

Copy everything between `<!--` and `-->`, paste it **above** the `</ul>` tag,
then remove the `<!--` and `-->` wrappers. Fill in your content:

```html
<li class="entry">
  <div class="entry-meta">
    <span class="tag">Essay</span> May 2026
  </div>
  <h2><a href="#">The Title of My Essay</a></h2>
  <p class="entry-excerpt">
    A short description — one or two sentences about what this piece holds.
  </p>
  <a href="#" class="read-more">Read &rarr;</a>
</li>
```

If the full essay is on another page, replace both `#` with the filename, e.g. `href="my-essay.html"`.
If it's published externally, use the full URL: `href="https://www.publication.com/my-essay"`.

Also **remove** the placeholder block when you have real entries:
```html
<div class="placeholder">...</div>   ← delete this when you have content
```

---

### Adding a Poem

Open `poetry.html` and find the example comment. Copy, paste above the placeholder, remove the comment wrappers, and fill in:

```html
<div class="poem">
  <div class="entry-meta"><span class="tag">Poem</span> June 2026</div>
  <div class="poem-title">The Name of the Poem</div>
  <div class="poem-body">First line of the poem,
second line continues here.

A blank line creates a stanza break.
The spacing will appear exactly as you type it.</div>
</div>
```

**Important for poetry:** line breaks inside `.poem-body` are preserved exactly as written. Type your poem naturally.

---

### Adding a Long Piece (its own page)

1. Create a new file in the blog folder, e.g. `my-essay.html`
2. Copy the entire contents of `contemplations.html` into it
3. Change the `<title>` tag and `<h1>` to your essay's title
4. Replace the `<ul class="entry-list">` section with your essay text, like this:

```html
<main class="main-content">
  <h1 class="page-title">Title of My Essay</h1>
  <div class="page-rule"></div>
  <div class="entry-meta"><span class="tag">Essay</span> June 2026</div>

  <p>First paragraph of my essay goes here...</p>
  <p>Second paragraph...</p>
</main>
```

5. Link to it from the section page:  `<a href="my-essay.html">Title</a>`

---

## Part 3 — GitHub for Beginners

### What GitHub is (simply)

GitHub is a website that stores your files online. When your files are there,
GitHub can serve them as a live website. Think of it as a filing cabinet
that also has a "publish" button.

Your website address will be: **https://angelaxucx233.github.io**

---

### First-time setup (do this once)

**Step 1 — Create an account** at github.com if you haven't already.
Your username is `angelaxucx233`.

**Step 2 — Create the repository**
- Go to github.com → click the **+** button top right → **New repository**
- Name it exactly: `angelaxucx233.github.io`
- Set to **Public**
- Click **Create repository**

**Step 3 — Upload your files**
- On the empty repository page, click **"uploading an existing file"**
- Open your `blog` folder on your computer
- Select all 7 files (Cmd+A on Mac) and drag them onto the GitHub page
- Scroll down → type "First upload" in the message box → click **Commit changes**

**Step 4 — Turn on GitHub Pages**
- Go to your repository → **Settings** tab (top of the page)
- Left sidebar → click **Pages**
- Under "Branch" → select **main** → click **Save**
- Wait 1–3 minutes → your site is live ✓

---

### Updating the site after editing (every time you add new writing)

This is the process you will repeat whenever you add something:

1. **Edit** the HTML file on your computer (open it in any text editor — TextEdit on Mac works, or download VS Code for a nicer experience)
2. **Go to** github.com/angelaxucx233/angelaxucx233.github.io
3. **Click on** the file you changed (e.g. `poetry.html`)
4. **Click the pencil icon** ✏️ (top right of the file view) — this opens the editor
5. **Paste your updated content** directly, or make the edit here
6. Scroll down → **Commit changes** → done

**Or upload a new version of the whole file:**
- On the repository page, click **Add file** → **Upload files**
- Drop in your updated file — GitHub will replace the old one automatically
- Click **Commit changes**

Your site updates within about 30 seconds.

---

### Key vocabulary

| Word | What it means |
|------|---------------|
| **Repository** (repo) | Your folder of files on GitHub |
| **Commit** | Saving a version of your file with a short description |
| **Branch** | A version of your repo — you will almost always use `main` |
| **GitHub Pages** | The feature that turns your repo into a live website |
| **Deploy** | The process of making your latest changes live on the website |

---

### Things you don't need to worry about yet

- Git commands in the Terminal (this is for later)
- Branches, pull requests, forks (these are for collaborative coding)
- Jekyll, frameworks, build tools — your site is plain HTML and doesn't need them

---

## Part 4 — Viewing Your Site Locally (Before Publishing)

To preview your site on your own computer before pushing to GitHub:

- Open the `blog` folder in Finder
- Double-click `index.html`
- It will open in your browser

**Note:** When viewing locally, the fonts may not load (they come from Google's servers). The layout, colours, and structure will all look correct. The fonts will appear normally on the live GitHub Pages site.

---

## Part 5 — Quick Reference Card

| Task | Where to go |
|------|-------------|
| Add a poem | Edit `poetry.html` |
| Add an essay | Edit `world.html` or `contemplations.html` |
| Add a published piece | Edit `published.html` |
| Add a book note | Edit `books.html` |
| Change the home page | Edit `index.html` |
| Change colours / fonts | Edit `style.css` (ask for help with this) |
| See your live site | https://angelaxucx233.github.io |
| See your repo | https://github.com/angelaxucx233/angelaxucx233.github.io |

---

*Written May 2026. Keep this file in your blog folder for reference.*
