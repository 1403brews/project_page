# Personal Page — Nishant Chandna

An academic-style personal homepage: research interests, publications, projects,
experience, honors, and education. Plain static HTML/CSS — no build step.

## Files

- `index.html` — the page
- `style.css` — styling (light + dark mode)
- `assets/Nishant_Resume.pdf` — CV, linked from the page

## Preview locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy

Works as-is on any static host:

- **GitHub Pages** — Settings → Pages → deploy from the default branch (root). The
  site is served from `index.html`.
- **Vercel** — import the repo; no framework, output directory is the repo root.

## Customize

- **Profile photo:** drop a square image at `assets/profile.jpg` and follow the
  comment near the top of `index.html` to swap the monogram avatar for the photo.
- **Content:** all text lives directly in `index.html` under clearly-labelled
  sections (About, News, Publications, Projects, Experience, Honors, Education).
