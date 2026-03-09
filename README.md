# Jazz — Presentations

A curated archive of slide presentations by Jazz Lien, hosted on GitHub Pages.

**Live site:** [jazzpujols34.github.io/jazz-presentations](https://jazzpujols34.github.io/jazz-presentations/)

## What's here

This site collects visual presentations for projects, talks, and product demos. Each presentation is a self-contained HTML slide deck — no frameworks, no dependencies, just open and browse.

Visitors can:
- Browse all presentations from the gallery landing page
- Search/filter by title or tag
- Click any card to view the full slide deck

## Presentations

| # | Title | Description |
|---|-------|-------------|
| 001 | [PodSight](https://jazzpujols34.github.io/jazz-presentations/decks/podsight.html) | AI-powered podcast summarization pipeline |
| 002 | [拾光 Glimmer](https://jazzpujols34.github.io/jazz-presentations/decks/glimmer.html) | AI memorial video generation platform |
| 003 | [Jazz Gallery](https://jazzpujols34.github.io/jazz-presentations/decks/jazz-gallery.html) | AI artwork gallery with auth and admin |
| 004 | [Articulate](https://jazzpujols34.github.io/jazz-presentations/decks/articulate.html) | Etymology-based vocabulary learning app |
| 005 | [GCP Landing Zone](https://jazzpujols34.github.io/jazz-presentations/decks/gcp-landing-zone.html) | Production-grade Terraform infrastructure |
| 006 | [Portfolio Manager](https://jazzpujols34.github.io/jazz-presentations/decks/portfolio-manager.html) | Investment portfolio tracker & audit engine |
| 007 | [Claude Code Workflow](https://jazzpujols34.github.io/jazz-presentations/decks/claude-code-workflow.html) | AI-assisted development system (open source) |

## Project structure

```
jazz-presentations/
  index.html          # Gallery landing page
  decks/              # HTML slide decks
    podsight.html
    glimmer.html
    jazz-gallery.html
    articulate.html
    gcp-landing-zone.html
    portfolio-manager.html
    claude-code-workflow.html
  thumbnails/         # Card preview images
    podsight.png
  README.md
```

## Adding a new presentation

1. Drop the `.html` slide deck into `decks/`
2. Add a screenshot to `thumbnails/` — name it to match the HTML file (e.g. `my-talk.png`)
3. Add a card to `index.html` (template in the HTML comments)
4. Update the table above
5. Push to `main` — GitHub Pages deploys automatically

## Thumbnail guidelines

- **Format:** PNG or WebP
- **Size:** ~1200x630px (2:1 ratio works well for the card grid)
- Keep file sizes under 200KB for fast page loads
