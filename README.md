# Personal Page — Nishant Chandna

An academic-style personal homepage: research interests, publications, projects,
experience, honors, and education. Plain static HTML/CSS — no build step.

Styled after the Beautiful Jekyll aesthetic — Lora/Open Sans typography, teal
accent, top navbar, centered photo header, and a footer with social icons.

## Files

- `index.html` — the page
- `style.css` — styling
- `assets/profile.jpg` — profile photo (header avatar)
- `assets/Nishant_Resume.pdf` — CV, linked from the page

Fonts (Google Fonts: Lora + Open Sans) and icons (Font Awesome) load from CDNs.

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

- **Profile photo:** replace `assets/profile.jpg` (square image recommended).
- **Content:** all text lives directly in `index.html` under clearly-labelled
  sections (About, News, Publications, Projects, Experience, Honors, Education).
- **Accent colour / fonts:** edit the CSS variables at the top of `style.css`.
