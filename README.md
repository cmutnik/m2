# M2 HR Consulting Website

This is the website for M2 HR Consulting. It's a simple set of pages (no special software required to run it) designed to be hosted for free on **GitHub Pages**.

This guide is written for someone with no coding experience. Everything you need to publish and maintain the site is below.

---

## 1. Publishing the site on GitHub Pages

1. Go to this repository on GitHub.com.
2. Click **Settings** (top menu of the repository).
3. In the left sidebar, click **Pages**.
4. Under "Build and deployment" &rarr; "Source," choose **Deploy from a branch**.
5. Under "Branch," select **main** and folder **/ (root)**, then click **Save**.
6. Wait 1–2 minutes. GitHub will show a green box with your live website address (something like `https://yourusername.github.io/m2/`).

That's it — the site is live. Any time you save a change to a file (see below), the live site updates automatically within a minute or two.

---

## 2. What's in this website

| File | What it is |
|---|---|
| `index.html` | The Home page |
| `services.html` | The Services page |
| `about.html` | The About page |
| `team.html` | The Team page |
| `contact.html` | The Contact page |
| `404.html` | The page shown if a visitor follows a broken link |
| `css/styles.css` | Controls colors, fonts, and layout for the whole site |
| `js/main.js` | A small script that makes the mobile menu work |
| `assets/favicon.svg` | The small icon shown in the browser tab |

All the text you see on the site (headlines, paragraphs, names, etc.) is **placeholder content**. It's realistic so you can see how the finished site looks, but it should be replaced with M2's real information before the site goes live to clients.

---

## 3. How to edit text (no coding needed)

You can edit any page directly on GitHub.com — no software to install:

1. Open the file you want to edit (e.g., `index.html`) from the file list on GitHub.
2. Click the **pencil icon** (Edit this file) in the top-right of the file view.
3. Find the text you want to change. It will be sitting between HTML tags, like this:
   ```html
   <h1>Human-centered HR solutions for growing businesses.</h1>
   ```
   Only change the text between the `>` and `<` — leave the tags themselves alone.
4. Scroll to the bottom, add a short note describing your change (e.g., "Update homepage headline"), and click **Commit changes**.
5. Refresh the live site in a minute or two to see your update.

**Tip:** If you're ever unsure whether you changed something safely, click "Cancel changes" before committing — nothing is saved until you click **Commit changes**.

---

## 4. Common updates

### Update contact info (email, phone, address)
This appears in **two places on every page**: the footer near the bottom, and the Contact page (`contact.html`) has additional copies. Search each HTML file for:
- `hello@m2hrconsulting.com`
- `(555) 555-1234`
- `123 Main Street, Suite 400`

Replace each instance with the real information. Because this appears on every page, you'll need to repeat the change in `index.html`, `services.html`, `about.html`, `team.html`, `contact.html`, and `404.html`.

### Update the Team page
Open `team.html`. Each team member is one block that looks like this:

```html
<div class="card team-card">
  <div class="avatar" style="background:#0b2545;">JB</div>
  <h3>Jordan Blake</h3>
  <span class="team-role">Founder &amp; Principal Consultant</span>
  <p>10+ years leading HR functions for fast-growing companies...</p>
</div>
```

- Change `JB` to the person's initials, `Jordan Blake` to their name, the role text, and the bio.
- To add a real photo instead of the colored initials circle, replace the `<div class="avatar" ...>JB</div>` line with:
  ```html
  <img src="assets/team/jordan-blake.jpg" alt="Jordan Blake" class="avatar" style="object-fit:cover;">
  ```
  Upload the photo into a new `assets/team/` folder first (you can create folders when uploading files on GitHub).
- Copy/paste an entire block to add a new team member, or delete a block to remove one.

### Update Services
Open `services.html`. Each service is a `<div class="card">...</div>` block with an icon, a heading (`<h3>`), and a description (`<p>`). Edit the heading and paragraph text directly.

### Change colors or fonts
Open `css/styles.css` and look at the very top of the file — the `:root { ... }` section. These lines control the whole site's color scheme:

```css
--color-primary: #0b2545;   /* main dark navy */
--color-accent: #2ec4b6;    /* teal accent color */
```

Changing a value here updates that color everywhere on the site.

### Replace the logo
The current logo is a text-based "M²" mark. To use a real logo image instead:
1. Upload your logo file into the `assets` folder.
2. In every HTML file, find:
   ```html
   <span class="logo-mark">M<sup>2</sup></span>
   ```
3. Replace it with:
   ```html
   <img src="assets/your-logo-file.png" alt="M2 HR Consulting" style="height:40px;">
   ```

---

## 5. Getting help

If something looks broken after an edit, the safest fix is to undo your change:
1. Go to the file's page on GitHub and click **History**.
2. Find the version before your edit and click **Revert** (or copy its content back into the file).

You can always hand this repository to a developer to make larger changes — everything is plain HTML/CSS, so any web developer will be able to pick it up immediately.
