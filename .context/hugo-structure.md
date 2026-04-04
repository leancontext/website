---
last-reviewed: 2026-04-04
---
# Hugo Structure

## Content Pages

```
content/
├── _index.md          → / (landing page, uses layouts/index.html)
├── thesis/index.md    → /thesis/ (the full thesis)
├── standard/index.md  → /standard/ (the lean context standard)
└── prompting/index.md → /prompting/ (reusable adoption prompts)
```

## Layouts

```
layouts/
├── _default/
│   ├── baseof.html    → base template (head, nav, body wrapper)
│   └── single.html    → template for content pages (thesis, standard, prompting)
├── index.html         → homepage/landing page template
├── partials/
│   └── nav.html       → site navigation
└── 404.html           → 404 page
```

## Key Decisions

- The landing page (_index.md) uses its own layout (layouts/index.html) with a different structure than content pages.
- Content pages use layouts/_default/single.html which renders the thesis-body class.
- All URLs use Hugo's relURL function so the site works at any path (github.io/repo/ or custom domain root).
- relativeURLs = true in hugo.toml.
- CSS lives in static/css/style.css, referenced via relURL in baseof.html.
- No Hugo themes. All layouts are custom and in the repo.
