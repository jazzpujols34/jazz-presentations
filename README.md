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
| 001 | [PodSight](https://jazzpujols34.github.io/jazz-presentations/podsight.html) | AI-powered podcast summarization pipeline |

## Project structure

```
jazz-presentations/
  index.html          # Gallery landing page
  decks/              # HTML slide decks
    podsight.html
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
