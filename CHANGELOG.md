# Changelog — Memetic Visuals

All notable changes to this site. Dates are ET.

## 2026-11-23 — v1.0.0 launch

- First public version at https://iamm3ta.github.io/memetic-visuals/ (github.io; no custom domain yet).
- Shared Memetic Media template: header, network footer cross-linking all six sites, shared `css/site.css`.
- Full SEO set: title, description, canonical, OG/Twitter with 1200x630 `assets/og.jpg`, JSON-LD, sitemap.xml, robots.txt, favicons, alt text.
- GitHub Actions Pages workflow with a no-CNAME guard and an SEO smoke check.

### Verified (live, 2026-11-23 ET)
- Lighthouse 12.8.2 (mobile, headless Chrome) on https://iamm3ta.github.io/memetic-visuals/: Performance 100 · Accessibility 100 · Best Practices 100 · SEO 100.
- Pages settings: HTTPS enforced (`https_enforced: true`), no CNAME.

### Fixed
- Pages workflow: grant `actions: read` so deploy-pages@v5 can find the uploaded artifact (first deploy failed without it).
