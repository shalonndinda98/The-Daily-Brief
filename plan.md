# The Daily Brief — Implementation Plan

## Product outcome

Deliver a simple, modern, responsive news website titled **The Daily Brief** with the tagline **Stay informed Stay ahead**, focused on Kenya, Africa, and international coverage. The experience includes the requested editorial sections, breaking news, top stories, latest news, most-read content, search, images, article detail pages, related stories, social sharing, follow links, and optional dark mode.

## Architecture and serving

Use a framework-free static frontend: semantic HTML in `index.html`, styles in `styles.css`, and browser behavior in `script.js`. This is a static-first experience with editorial sample data embedded in JavaScript. Static delivery is the best fit for SEO, fast first paint, and the requested HTML/CSS/JS constraint. No backend, database, login, or external data API is required for this initial version; the blueprint explicitly left Live News Data unselected.

The local development server will be a small Node-free Python HTTP server on port 3000. The managed deployment build will copy the repository root to `dist/`, where `dist/index.html` is the static entry point. Versioned assets can be cached for a long lifetime; HTML remains revalidated by the host. No API routes are declared.

## Project structure

- `index.html` — crawler-visible homepage shell with meaningful editorial content, SEO metadata, navigation, sections, and article detail region.
- `styles.css` — responsive editorial design system, dark theme tokens, layout, cards, and interaction states.
- `script.js` — article data, category filters, live search, article detail routing via `?article=`, related stories, share buttons, dark-mode persistence, and menu interactions.
- `assets/hero-nairobi.jpg` — custom lead image.
- `assets/logo.svg`, `assets/logo.png` — project-specific logo and favicon.
- `manus-routes.json` — current source route manifest for `/` and `/?article=:slug`.
- `sitemap.xml`, `robots.txt` — public search-discovery documents.
- `app.config.ts` — managed project logo metadata.

## UX and responsive behavior

- Desktop: masthead, horizontal category nav, breaking strip, two-column lead grid, latest feed plus most-read rail.
- Tablet: collapse supporting grid to two columns and keep nav scrollable.
- Mobile: compact masthead with menu toggle, single-column editorial flow, stacked story cards, and an accessible dark-mode toggle.
- Search filters stories by title, excerpt, category, and location; empty results show a clear recovery message.
- Article mode updates the page title, metadata, hero image, reading time, related stories, and share actions without requiring a separate build step.

## SEO and accessibility

Keep the homepage content-bearing in initial HTML, include descriptive title/description, Open Graph/Twitter metadata, semantic headings, alt text, visible focus styles, keyboard-accessible controls, `aria-live` for search results, and explicit links. Use canonical/sitemap values only with the configured preview/public origin; do not guess an internal origin in source.

## Verification

Validate with static source inspection, JavaScript syntax checking (`node --check`), a local HTTP readiness check, a JSON contract check for `/manus-routes.json`, and curl checks for the homepage, sitemap, robots, and asset responses. Inspect the responsive CSS and the article/search/theme state logic directly. No browser screenshot pass is required unless a concrete rendered defect is observed.
