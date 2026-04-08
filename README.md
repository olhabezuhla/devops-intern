# Minimal Linktree Template

This repo contains:
- `index.html`: a minimal linktree-style page template
- `Dockerfile`: static site image served by Nginx
- `.github/workflows/pages.yml`: deploys the site to GitHub Pages
- `.github/workflows/ghcr.yml`: builds and pushes image to GHCR (`ghcr.io/<owner>/<repo>`)

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
