# Creating Tags
## 1. Your 3-page structure (baseline)

You will have:

* `index.html` → entry page
* `blog.html` → all posts (chronological)
* `tags.html` → tag index (your “map”)

---

## 2. How tags work in your system

Tags are just:

* words attached to a post (like `css`, `layout`)
* and links pointing to sections in `tags.html`

They are NOT pages themselves.

---

## 3. STEP-BY-STEP: Adding a new blog post with tags

Whenever you write a new post, follow this exact process:

---

### Step 1: Create the post ID

Use this format:

```
post-YYYY-MM-DD-title
```

Example:

```
post-2026-06-04-layout-notes
```

---

### Step 2: Write your post using this template

Copy this every time:

```html
<article id="post-YYYY-MM-DD-title">
  <h2>TITLE HERE</h2>

  <p>
    Write your content here.
  </p>

  <div class="tags">
    <a href="./tags.html#tag1">#tag1</a>
    <a href="./tags.html#tag2">#tag2</a>
  </div>
</article>
```

---

### Step 3: Add your tags (important rule)

Pick simple lowercase tags:

* css
* layout
* journal
* typography

Then replace:

```html
<a href="./tags.html#tag1">#tag1</a>
```

with:

```html
<a href="./tags.html#css">#css</a>
<a href="./tags.html#layout">#layout</a>
```

---

### Step 4: Add the post to `blog.html`

Just paste the full `<article>` into `blog.html` in the right chronological position.

---

### Step 5: Register tags in `tags.html`

Now update your tag index.

#### Example structure:

```html
<h2 id="css">CSS</h2>
<ul>
  <li><a href="./blog.html#post-2026-06-04-layout-notes">Layout Notes</a></li>
</ul>

<h2 id="layout">Layout</h2>
<ul>
  <li><a href="./blog.html#post-2026-06-04-layout-notes">Layout Notes</a></li>
</ul>
```

---

## 4. RULES (important to keep it clean)

#### Rule 1: IDs are unique

* one post = one id
* never reuse IDs

---

#### Rule 2: Tags are lowercase

Keep it consistent:

* `css` not `CSS`
* `layout` not `Layout`

---

#### Rule 3: Tags page is the only “organized view”

* blog.html = chronological
* tags.html = grouped

Never mix responsibilities.

---

#### Rule 4: Every tag must exist in tags.html

If you add:

```html
#javascript
```

You MUST also add:

```html
<h2 id="javascript">JavaScript</h2>
```

---

## 5. Full reusable template (save this somewhere)

This is your “copy every time” block:

```html
<!-- POST TEMPLATE -->
<article id="post-YYYY-MM-DD-title">
  <h2>TITLE HERE</h2>

  <p>
    Write your post here...
  </p>

  <div class="tags">
    <a href="./tags.html#tag1">#tag1</a>
    <a href="./tags.html#tag2">#tag2</a>
  </div>
</article>
```

---

## 6. Mental model (this makes everything click)

Think of your system like this:

* **blog.html = timeline**
* **tags.html = map**
* **tags = labels that connect both**

So every post is just:

> a point in time + a few labels that connect it to the map