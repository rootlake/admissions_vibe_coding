# Running the Talk

## Start local server

```bash
cd /Users/jlake/Documents/code/GBS_admissions_slides
npx serve .
```

Open the URL shown (usually `http://localhost:3000`).

## Direct links

| What | URL |
|------|-----|
| Slide deck | `http://localhost:3000/` |
| Funnel demo | `http://localhost:3000/demos/funnel.html` |
| Lost-to demo | `http://localhost:3000/demos/lost-to.html` |

## Present shortcuts (reveal.js)

| Key | Action |
|-----|--------|
| → / ↓ | Next slide |
| ← / ↑ | Previous slide |
| `s` | Speaker notes |
| `f` | Fullscreen |
| `o` | Overview grid |
| `Esc` | Exit overview / fullscreen |

## Export to PDF

Open `http://localhost:3000/?print-pdf` then browser Print → Save as PDF.

## Pre-talk checklist

- [ ] `npx serve .` running
- [ ] Funnel + lost-to open in backup tabs
- [ ] `LIVE-PROMPTS.md` — JSON + Tier 1 prompt copied into three AI tools
- [ ] STYLE preset snippets ready for color swaps
- [ ] Cursor open on project (`demos/` tree visible)
- [ ] Test grade slider, gender toggle, print buttons
- [ ] Read `PRESENTER-NOTES.md` once

## Offline fallback

Demos work from `file://` if CDN scripts cached. Deck needs network for reveal.js CDN on first load.

## Project layout

```
data-source/          ← raw files, NEVER served at runtime
demos/data/*.js       ← aggregates only
demos/funnel.html     ← slide 4 embed
demos/lost-to.html    ← slide 8 embed
index.html            ← reveal.js deck
LIVE-PROMPTS.md       ← copy-paste prompts
PRESENTER-NOTES.md    ← your private cheat sheet
```
