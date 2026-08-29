# GitHub Pages Setup — tsaha.github.io/astro

## Files
```
astro/
├── index.html      ← landing page
├── research.html   ← research + publications
├── cv.html         ← CV
├── beyond.html     ← personal / photography
└── style.css       ← shared styles (all pages use this)
```

---

## Step 1: Create the repository

1. Go to github.com, sign in
2. Click **New repository**
3. Name it: `astro`  (this gives you `tsaha.github.io/astro`)
4. Set to **Public**
5. Click **Create repository**

---

## Step 2: Upload files

### Via Git (recommended)
```bash
git clone https://github.com/tsaha/astro
cd astro
# copy the astro/ folder contents here (index.html, research.html, cv.html, beyond.html, style.css)
git add .
git commit -m "Initial site"
git push origin main
```

### Via GitHub web interface
Upload all files from the `astro/` folder directly into the repository root.

---

## Step 3: Enable GitHub Pages

1. Repository → **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: `main`, folder: `/ (root)`
4. Save

Site goes live at `https://tsaha.github.io/astro` within ~60 seconds.

---

## Step 4: Fill in your content

### index.html
- Replace `your@email.ac.in` with your actual email
- Replace Google Scholar, ORCID, GitHub, ADS URLs
- Check the institution/position line in the hero eyebrow

### research.html
- Fill in your actual publications (title, authors, journal, year, links)
- Adjust the research topic descriptions if needed

### cv.html
- Fill in talks, schools, and publication entries
- Add `cv.pdf` to the repository for the download button to work

### beyond.html
- Add photos by replacing `<div class="photo-slot">` with `<img>` tags:
```html
<!-- Before -->
<div class="photo-slot"><span class="photo-slot-city">Warsaw · 01</span><span>drop photo here</span></div>

<!-- After -->
<div class="photo-slot" style="padding:0; overflow:hidden;">
  <img src="photos/warsaw-01.jpg" alt="Warsaw" style="width:100%;height:100%;object-fit:cover;" />
</div>
```
Upload your photos to a `photos/` folder in the repository.

---

## Step 5: Add profile photo

Upload `photo.jpg` (candid half-body shot) to the repository. Then in `index.html`, replace:

```html
<div class="photo-wrap"> ... </div>
```
with:
```html
<img src="photo.jpg" alt="Tathagata Saha" style="width:260px;height:360px;object-fit:cover;border-radius:2px;border:1px solid rgba(255,255,255,0.1);" />
```

And replace the `about-photo` placeholder div similarly.

---

## Updating the site later

Every `git push` to `main` triggers an automatic rebuild. 
You can also edit files directly in the GitHub web editor.
