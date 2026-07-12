# arashmparsa.github.io

Personal academic site for Arash Parsa — a plain static site (no build step) that
GitHub Pages serves directly.

## Deploy (one time, ~2 minutes)

1. Create a new **public** repo on GitHub named exactly:
   `arashmparsa.github.io`
2. Put every file in this folder at the **root** of that repo (index.html must be
   at the top level, not inside a subfolder).
3. Push:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/arashmparsa/arashmparsa.github.io.git
   git push -u origin main
   ```
4. In the repo: **Settings → Pages → Build and deployment → Source: Deploy from a
   branch**, branch `main` / `/ (root)`. Save.
5. Wait ~1 minute, then visit **https://arashmparsa.github.io**

## Add your photo
Drop a square-ish image at `assets/img/headshot.jpg`, then in `index.html` find the
`<div class="monogram">AP</div>` line and replace it with:
```html
<img src="assets/img/headshot.jpg" alt="Arash Parsa">
```
(The instructions are also in a comment right above that line.)

## Edit content
- Text lives directly in the four HTML files (`index`, `publications`, `projects`, `cv`).
- All styling is in `assets/css/style.css`. Colors are CSS variables at the top.
- Résumés live in `assets/pdf/` — replace those files (keep the names) to update the
  download buttons.

## Structure
```
index.html          About (landing)
publications.html   Publications
projects.html       Projects
cv.html             CV + résumé downloads
assets/css/style.css
assets/img/         (drop headshot.jpg here)
assets/pdf/         résumé PDFs
.nojekyll           tells GitHub Pages to serve files as-is
```
