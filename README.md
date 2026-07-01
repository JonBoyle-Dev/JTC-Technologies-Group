# JTC Tech — Site Plan & README

## Overview

This is the main group landing site for **JTC Tech** — a portfolio of privacy-first AI tools and browser extensions. The site acts as the central hub linking all individual product sites.

**Live URL:** `https://jtctech.co.za/`

---

## File Structure

```
jtc-technologies/
├── index.html          ← Home page (hero + product grid + mission strip)
├── products.html       ← Full product portfolio with featured card
├── about.html          ← Origin story, values, timeline
├── contact.html        ← Contact form + product links
└── README.md           ← This file
```

---

## Pages (Current — 4 of 10 max)

| # | Page | File | Status | Purpose |
|---|------|------|--------|---------|
| 1 | Home | `index.html` | ✅ Done | Hero, product grid, pillars, mission |
| 2 | Products | `products.html` | ✅ Done | Full portfolio with featured card + filter bar |
| 3 | About | `about.html` | ✅ Done | Story, values, timeline |
| 4 | Contact | `contact.html` | ✅ Done | Contact form + product links |
| 5–10 | *Reserved* | — | 🔲 Pending | See roadmap below |

---

## Products Currently Linked

| Product | URL | Status | Category |
|---------|-----|--------|----------|
| Guardian AI | https://guardian.jtctech.co.za/ | Beta | Privacy / Data Protection |
| PromptForge | https://promptforge.jtctech.co.za/ | Coming Soon | Productivity / Prompt Engineering |
| Dark Pattern Detector | https://darkpattern.jtctech.co.za/ | Live | Consumer Protection / AI |

---

## Design System

### Colours
```css
--bg:         #080c12   /* Page background */
--bg-2:       #0d1420   /* Card / section background */
--bg-3:       #111c2e   /* Hover / elevated surface */
--cyan:       #00c8ff   /* Primary accent — links, highlights, borders */
--amber:      #f5a623   /* Secondary accent — warnings, beta badges */
--text:       #e8edf5   /* Primary text */
--text-muted: #7a90a8   /* Secondary / descriptive text */
```

### Typography
- **Display / Headings:** Bebas Neue (Google Fonts)
- **Body / UI:** Syne (Google Fonts)
- **Code / Labels / Mono:** DM Mono (Google Fonts)

### Status Badge Colours
```
Live        → #3dffa0 (green)
Beta        → #f5a623 (amber)
Coming Soon → muted grey
```

---

## Roadmap — Future Pages (Slots 5–10)

When you add new products, consider these page options:

| Slot | Suggested Page | When to Add |
|------|---------------|-------------|
| 5 | **Blog / Updates** — Release notes, dev logs, thinking-out-loud posts | When you have 2–3 things to share |
| 6 | **Individual Product Detail** — Deep-dive page for Guardian AI (or any flagship) | When a product grows complex enough to need its own landing page on the group site |
| 7 | **Open Source** — List of repos, contribution guides, licensing info | If/when any product goes fully open source with active contributors |
| 8 | **Press / Media Kit** — Logo downloads, screenshots, one-pager, quotes | If press coverage or partnerships become relevant |
| 9 | **Roadmap / Changelog** — Public-facing product roadmap | When you want community input or transparency about what's next |
| 10 | **Privacy Policy / Legal** | Before any serious user acquisition or if collecting any form data |

---

## Adding a New Product

When you launch a new tool, update these files:

### 1. `index.html`
Replace the `placeholder` card with the new product:
```html
<!-- Replace this placeholder card -->
<div class="product-card placeholder">...</div>

<!-- With a real product card -->
<div class="product-card" onclick="window.open('YOUR_URL','_blank')">
  <div class="card-header">
    <div class="card-icon">🔧</div>
    <span class="card-status status-live">Live</span>
  </div>
  <div class="card-title">New Tool Name</div>
  <div class="card-desc">Description here.</div>
  <div class="card-tags">
    <span class="tag">Category</span>
  </div>
  <a href="YOUR_URL" target="_blank" class="card-link">Visit site <span>→</span></a>
</div>
```

### 2. `products.html`
Same process — replace a placeholder in the `products-grid`.

### 3. All pages — Footer product list
Add to the "Products" `<ul>` in every footer:
```html
<li><a href="YOUR_URL" target="_blank">New Tool Name</a></li>
```

### 4. `contact.html`
Add to the product links section and the dropdown:
```html
<!-- Product link -->
<a href="YOUR_URL" target="_blank" class="product-link-item">
  <div class="pli-left">
    <div class="pli-icon">🔧</div>
    <div class="pli-name">New Tool Name</div>
  </div>
  <div class="pli-arrow">→</div>
</a>

<!-- Dropdown option -->
<option value="newtool">New Tool Name — question or feedback</option>
```

---

## GitHub Pages Deployment

1. Create a new repo: `jtc-technologies` (or `jtc-group`, etc.)
2. Push all four HTML files and this README to `main`
3. Go to **Settings → Pages → Source:** `main` branch, `/ (root)` folder
4. Site will be live at `https://jonboyle-dev.github.io/jtc-technologies/`

### Optional: Custom Domain
- Add a `CNAME` file to the repo root containing your domain (e.g. `jtctech.co.za`)
- Point your DNS A records to GitHub Pages IPs or use a CNAME to `jonboyle-dev.github.io`

---

## Contact Form Note

The contact form currently uses a `mailto:` link as the fallback (no backend required — works on GitHub Pages). Update the email address in `contact.html`:

```javascript
const to = 'hello@jtctech.co.za'; // ← Change this
```

For a proper form backend (no email client popup), options include:
- **Formspree** — free tier, just change `action` URL
- **Netlify Forms** — if you move to Netlify hosting
- **EmailJS** — client-side email sending

---

## Checklist Before Going Live

- [ ] Update contact email in `contact.html`
- [ ] Update LinkedIn URL in `contact.html` if different
- [ ] Add `favicon.ico` or `<link rel="icon">` to all pages
- [ ] Set up GitHub Pages
- [ ] Test all external product links
- [ ] Test on mobile (nav toggle, card stacking)
- [ ] Optional: Add Google Analytics or privacy-first alternative (Plausible, Fathom)
- [ ] Optional: Add `sitemap.xml` for SEO

---

*JTC Tech — Built in 🇿🇦*
