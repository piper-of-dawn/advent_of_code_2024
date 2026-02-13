# Making Software MkDocs Theme Clone

This repository contains a custom MkDocs theme structured to mimic the aesthetics of [makingsoftware.com](https://www.makingsoftware.com).

## Structure

- `mkdocs.yml`: MkDocs configuration using a custom theme directory.
- `makingsoftware_theme/`: Theme package with MkDocs-compatible files:
  - `mkdocs_theme.yml`
  - `base.html`, `main.html`, `404.html`
  - `partials/` for shared header/footer templates
  - `assets/stylesheets/` and `assets/javascripts/` for static resources
- `docs/`: Example pages, including fake blog posts under `docs/blog/`.
- `.github/workflows/deploy-gh-pages.yml`: GitHub Actions workflow to build and deploy to GitHub Pages.

## Run locally

```bash
pip install mkdocs
mkdocs serve
```

Then open `http://127.0.0.1:8000`.

## GitHub Pages deployment

1. Push to the `main` branch.
2. In GitHub repository settings, enable **Pages** and set **Build and deployment** to **GitHub Actions** (this must be enabled once, or GitHub will return a 404 during deployment).
3. The `Deploy MkDocs to GitHub Pages` workflow will run `actions/configure-pages`, build the site, upload the `site/` artifact, and publish it.
