# Template upgrade notes

This site is based on the [Academic Pages](https://github.com/academicpages/academicpages.github.io)
template. The notes below record the last template refresh and the local customisations that must be
kept when updating again.

## Last refresh

- **Upstream version:** `academicpages/academicpages.github.io@7b95833` (master, 2026-10-18)
- **Refreshed on:** 2026-10-21
- **Rollback point:** git branch/tag `backup/pre-upgrade-2026-10-21` / `pre-upgrade-2026-10-21`

### What was brought in from upstream

- Theme system reworked: separate light/dark palettes plus the `air`, `sunrise`, `mint`, `dirt` and
  `contrast` themes (`_sass/theme/`), a light/dark toggle in the masthead, and a no-flash theme
  bootstrap in `_includes/head/custom.html`.
- New layouts/includes: selected nav highlighting, better publication/talk metadata (`Published in …`),
  `bibtexurl` support, improved SEO/Open Graph/Twitter meta tags (`_includes/seo.html`), sitemap link in
  the footer, new social share buttons (Bluesky, Mastodon), MathJax 4, Mermaid and Plotly support.
- Bundled JS rebuilt from the new `assets/js/_main.js` (theme toggle, lazy Plotly/Mermaid), dropping
  jQuery Smooth Scroll, FitVids and Magnific Popup.
- Font Awesome updated to 6.7.2 (new icons such as `fa-bluesky`), with matching webfonts.
- Template-only pages refreshed: `_pages/markdown.md` (documents Mermaid/Plotly), `_pages/terms.md`,
  `_pages/archive-layout-with-content.md`, and `README.md`.

### Deliberately *not* taken from upstream

| Upstream change | Why it was skipped |
| --- | --- |
| `Gemfile` switching to Jekyll 4.4 + `kramdown`, dropping `github-pages` | This site is deployed by GitHub Pages' classic build, which runs **Jekyll 3.10.0 + Ruby Sass 3.7.4**. Keeping `github-pages` makes local builds match production. |
| GitHub Actions deploy workflow (`.github/workflows/jekyll.yml`) | Would switch the repo's Pages source from the classic build to Actions. Do that only as a deliberate migration. |
| Dart Sass syntax (`@use 'sass:math'`, `math.div()`) in `_sass/_themes.scss`, `_sass/vendor/breakpoint`, `_sass/vendor/susy` | Ruby Sass 3.7.4 cannot parse it. Those vendor files were kept at their working versions; only the site-level Sass files follow the new layout. |
| `append` filter inside `assets/css/main.scss` theme imports | Jekyll 3.10's SCSS pipeline does not evaluate that filter chain inside an `@import` list, so the theme files are referenced literally (`theme/default_light`, `theme/default_dark`). |
| `author_profile: true` in `_config.yml` defaults | The site intentionally shows the sidebar only on About/Publications/CV/Teaching-style pages. |
| Removed `patents` publication category | `_publications/NIEE_Patent.md` uses it. |
| Dockerfile rewrite, `.gitignore` changes | Not needed for this deployment, and `Gemfile.lock` is intentionally tracked here. |

## Local customisations to preserve on future upgrades

1. **`_config.yml`** — personal identity, URLs, `timezone`, `patents` category, analytics.
2. **`_includes/analytics.html`** — Cloudflare Web Analytics beacon (local addition), plus the
   provider switch (currently `google-analytics-4` with the existing `G-…` measurement ID).
3. **`_includes/footer.html`** — copyright left / visitor tracker right layout, plus the sitemap link.
4. **`_includes/head/custom.html`** — no-flash dark theme bootstrap, favicons, Academicons, Font
   Awesome, MathJax. The bootstrap deliberately defaults to **dark** and does not follow the OS
   preference, keeping the site's long-standing appearance.
5. **`assets/css/custom.css`** — footer positioning for the taller custom footer, and
   `overflow-wrap` so long inline code/URLs don't widen mobile pages.
6. **`assets/js/_main.js` / `assets/js/main.min.js`** — `determineComputedTheme()` returns `"dark"`
   instead of the OS preference when no stored choice exists.
7. **`images/`** — `og-image.png` (1200×630 social card), `favicon*.png`, `apple-touch-icon-180x180.png`,
   updated `manifest.json` / `browserconfig.xml`.
8. **`_data/navigation.yml`** — Talks, Portfolio, Blog Posts and Guide are intentionally commented out.

## Building / previewing locally

GitHub Pages uses Jekyll 3.10.0, so the repo keeps the `github-pages` gem:

```bash
bundle install
bundle exec jekyll serve -l -H localhost
```

A `bundle exec jekyll build` of the upgraded site succeeds with this toolchain. Building with
Jekyll 4.x also works (the hard-coded theme imports are version independent), but it reports Dart
Sass `@import`/division deprecation warnings because the template still targets Ruby Sass.
