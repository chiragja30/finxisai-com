# FinxisAI — finxisai.com (Website Restore)

Production website for **finxisai.com**, restored from a Hostinger Horizons
backup. The deployable site lives at the repo root (`index.html` + `assets/`),
so the repo can be served directly by any static host, GitHub Pages, Netlify,
Vercel, or re-uploaded to Hostinger's `public_html`.

## Contents

- `index.html` — SPA entry point
- `assets/` — compiled, minified JS + CSS build (~121 files)
- `.htaccess` — SPA rewrite (all non-file routes → `index.html`) + cache headers
- `robots.txt`, `sitemap.xml`, `llms.txt` — SEO / crawler files

## Important

These are **compiled production build** files, not the original source code.
The React/Vite source is not part of the Hostinger backup and is not in this
repo. To change the site, edit the source project and re-build, or edit the
built `assets/` directly (not recommended).

`index.html` loads Google Analytics (`G-M30YY328VS`), Calendly and Leadsy tags.

## Deploy

**Hostinger:** upload all repo files into the domain's `public_html/`.
**Static host / Pages:** serve from the repo root; ensure SPA fallback routes
unknown paths to `index.html` (the `.htaccess` does this on Apache).
