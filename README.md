# akhil-peyyala.github.io

Personal site — single page, built as plain HTML/CSS/JS (no build step).

## Deploy to GitHub Pages

1. Create a new repo on GitHub. For a user site, name it exactly `<your-username>.github.io`; for a project site, any name works and it'll be served at `<your-username>.github.io/<repo-name>`.
2. Upload everything in this folder (`index.html`, the `assets/` folder, and this README) to the repo — either via the GitHub web UI ("Add file → Upload files") or:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**, set **Source** to the `main` branch and `/ (root)` folder, then save.
4. GitHub gives you a live URL within a minute or two (shown on that same Pages settings screen).

## Before you publish

- **LinkedIn / GitHub links**: the two link placeholders in the contact section at the bottom of `index.html` currently point to `#`. Search for `target="_blank" rel="noopener"` and drop in your real URLs.
- **Resume file**: `assets/Akhil_Peyyala_Resume.pdf` is your current resume. Swap in updated versions under the same filename, or update the link in the contact section if you rename it.
- **Phone number**: currently shown in the contact row — remove the line if you'd rather keep it off a public page.

## Structure

```
index.html                 — the whole site (HTML + CSS + JS, no dependencies besides Google Fonts)
assets/img/profile.jpg      — hero portrait
assets/img/steak-hero.jpg   — Steak N' Bake feature shot
assets/img/steak-wiring.jpg — hardware close-up
assets/img/steak-team.jpg   — competition demo photo
assets/Akhil_Peyyala_Resume.pdf
```

## Adding more projects later

Duplicate the `<section id="projects">` block's inner `.proj-hero` / `.proj-gallery` pattern for each new project, or split into a separate Projects page when you're ready to go multi-page — the nav links are already set up to be easy to re-point at new pages instead of in-page anchors.
