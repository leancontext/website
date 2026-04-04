---
last-reviewed: 2026-04-04
---
# Deployment

## GitHub Pages

- Source: Deploy from branch → main → / (root)
- No build step. No GitHub Actions. Plain HTML served directly.

## Custom Domain

When leancontext.dev is ready:
1. Add a CNAME file to the repo root containing: leancontext.dev
2. Set custom domain in repo Settings → Pages
3. DNS records on registrar (Name.com):
   - A @ → 185.199.108.153, .109, .110, .111
   - CNAME www → jjahns.github.io
4. Enable "Enforce HTTPS" once SSL cert provisions.

## URL Structure

All links are relative. No absolute URLs anywhere. The site works at any base path without configuration changes.
