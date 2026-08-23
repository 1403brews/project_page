# Personal Page — Nishant Chandna

An academic-style personal homepage: research interests, publications, projects,
experience, honors, and education. Plain static HTML/CSS — no build step.

Styled after the Beautiful Jekyll aesthetic — Lora/Open Sans typography, teal
accent, top navbar, centered photo header, and a footer with social icons.

Prose sits in a narrow reading column; Projects and Honors break out into
full-width bands, because a grid of media needs room that prose does not.
Project cards play their video while it is on screen (visibility rather than
hover, because phones have no hover and would otherwise show a black frame).
Clicking a card opens its video large with controls; award photos open the
same way.

## Files

- `index.html` — the page
- `style.css` — styling
- `assets/profile.jpg` — profile photo (header avatar)
- `assets/Nishant_Resume.pdf` — CV, linked from the page
- `assets/media/` — project and award media (five demo videos, a GIF, and award photos)

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
- **Project / award media:** drop files in `assets/media/` and point the
  corresponding `<img>`/`<video>` at them. Videos are H.264, scaled to 960px
  wide and stripped of audio, which keeps each one a few MB rather than tens.
  A project with no footage can use the `card-media-plain` treatment (a tinted
  panel with a Font Awesome glyph) instead of leaving an empty box.
- **Content:** all text lives directly in `index.html` under clearly-labelled
  sections (About, News, Publications, Projects, Experience, Honors, Education).
- **Accent colour / fonts:** edit the CSS variables at the top of `style.css`.

## Analytics

GitHub Pages serves the site with no analytics of its own, and GitHub's repo
traffic API (`Insights > Traffic`) counts views of the *repository* on
github.com, keeps only 14 days, and has no geography data at all — there is no
`traffic/countries` endpoint.

For visitor counts and countries on the actual site, `index.html` carries a
commented-out **Cloudflare Web Analytics** beacon. It is cookieless and free.
To turn it on:

1. dash.cloudflare.com → Analytics & Logs → Web Analytics → **Add a site**
2. Enter `1403brews.github.io` and copy the token it issues
3. In `index.html`, replace `PASTE_TOKEN_HERE` with that token and uncomment
   the `<script>` block
4. Commit and push; the dashboard starts filling within a few minutes

Reports live in the Cloudflare dashboard, not on the page.
