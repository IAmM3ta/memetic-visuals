# Changelog — Memetic Visuals

All notable changes to this site. Dates are ET.

## 2026-11-25 — v1.1.0 Visionary Stills Vol. 1 (draft, unmerged)

### Changed
- Replaced the Loops Vol. 1 "Buy link coming soon" placeholder with a buy button
  for Visionary Stills Vol. 1, pointing at the placeholder Gumroad slug
  `https://ledgerwright.gumroad.com/l/memetic-visuals-pack`. Update the href
  (and the JSON-LD `offers.url`) if that slug changes when the product is created.
- Replaced the loop gallery and preview reel with web-size previews of the
  eighteen Drive stills. Hero, cover and Open Graph card now use a crop of
  Flow State. Product copy, license, 404 nav, sitemap lastmod and README
  match the stills pack.
- JSON-LD Product is now Visionary Stills Vol. 1 at $14, with `availability`
  set to PreOrder until the Gumroad listing is live.

### Notes
- Pages still deploys only from `main`. This change is intended to land
  through a pull request and should not be merged until the Gumroad product
  exists, or the public button will 404.
- Full-resolution masters are not in this repo.


## 2026-11-23 — v1.0.1 CI fix

### Fixed
- Pages deploys failed intermittently with 'No artifacts named "github-pages" were found' even though the artifact was uploaded: deploy-pages queried it about one second after upload, in the same job, before it was indexed. The workflow now uses separate build and deploy jobs (GitHub's reference layout) plus one retry after 30 seconds. Action versions unchanged (upload-pages-artifact@v5 + deploy-pages@v5 are a matched pair); concurrency was not cancelling runs (`cancel-in-progress: false`).

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
