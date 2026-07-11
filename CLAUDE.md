# CLAUDE.md — jazz-presentations

## What this is

Static HTML presentation archive deployed to **GitHub Pages** at `jazzpujols34.github.io/jazz-presentations/`. No build step. No backend. Each deck is a self-contained HTML file under `decks/`.

## Workflow

- New deck: drop a `.html` file into `decks/` and link it from `index.html`
- Use the `/frontend-slides` skill for new decks (13 style presets) or write standalone HTML
- Default font: **Google Sans** (per Jazz's preference) — fallback to Poppins / system stack
- No emojis in deck content; use SVG icons

## Deploy

`git push` to main → GitHub Pages publishes automatically. No CI needed.

## What's already here

- `index.html` — landing page listing all decks
- `decks/` — individual deck HTML files
- Favicon set + `site.webmanifest` for PWA-ish behavior

## Don't

- Don't add a build pipeline
- Don't add backend / API calls — kept dependency-free for portability
- Don't commit large media (>1 MB) — link to external CDN instead
