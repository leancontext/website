---
last-reviewed: 2026-04-04
---
# Deployment

## GitHub Pages

- The site deploys via GitHub Actions on push to main.
- Workflow file: .github/workflows/hugo.yml
- Pages source: GitHub Actions (not "Deploy from a branch").
- Hugo version: 0.139.0 (extended).

## Custom Domain

When leancontext.dev is ready:
1. Add static/CNAME file containing: leancontext.dev
2. Set custom domain in repo Settings → Pages
3. DNS records on registrar (Name.com):
   - A @ → 185.199.108.153, .109, .110, .111
   - CNAME www → jjahns.github.io
4. Enable "Enforce HTTPS" once SSL cert provisions.

## URL Structure

- All URLs use Hugo's relURL function.
- relativeURLs = true in hugo.toml.
- The site works at any base path without configuration changes.
- Do not hardcode absolute URLs in templates or content.
