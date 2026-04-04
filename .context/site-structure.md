---
last-reviewed: 2026-04-04
---
# Site Structure

## Plain HTML — No Build Step

This is a static HTML site served directly from the main branch via GitHub Pages. There is no build step, no static site generator, no framework.

## File Layout

```
/index.html              → landing page
/thesis/index.html       → the thesis
/standard/index.html     → the standard
/prompting/index.html    → prompting guide
/css/style.css           → shared stylesheet
```

## Relative Paths

All links use relative paths. From the root: `thesis/`, `standard/`, `prompting/`, `css/style.css`. From subpages: `../`, `../thesis/`, `../standard/`, `../prompting/`, `../css/style.css`.

No absolute paths. No build-time URL resolution. Everything just works at any deployment path.

## GitHub Pages

- Source: Deploy from branch → main → / (root)
- No GitHub Actions workflow needed.
- Custom domain: add CNAME file to root when ready.
