# Minimal Linktree Template

This repo contains:
- `index.html`: pure HTML, no CSS (start here)
- `index-css-level-1.html`: very basic CSS (font, spacing)
- `index-css-level-2.html`: card layout + styled links
- `index-css-level-3.html`: variables, gradients, hover effects
- `Dockerfile`: static site image served by Nginx
- `.github/workflows/pages.yml`: deploys the site to GitHub Pages
- `.github/workflows/ghcr.yml`: builds and pushes image to GHCR (`ghcr.io/<owner>/<repo>`)

## Learning path for a 10th grader
1. Open `index.html` and learn core tags: `<html>`, `<head>`, `<body>`, headings, lists, links.
2. Open `index-css-level-1.html` and see how CSS changes layout basics.
3. Open `index-css-level-2.html` for classes and box styling.
4. Open `index-css-level-3.html` for more advanced styling patterns.

## GitHub setup (one-time)
1. In repository Settings -> Pages, set Source to **GitHub Actions**.
2. Ensure your default branch is `main` (or adjust workflow branch filters).
3. Push to `main` to trigger both workflows.

## Run locally with Docker
```bash
docker build -t linktree-template .
docker run --rm -p 8080:80 linktree-template
```
Then open `http://localhost:8080`.
