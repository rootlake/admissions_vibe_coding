# Vibe Coding for Admissions

Slides, live demos, and copy-paste prompts for the **GBS AI in Admissions Workshop** (June 1, 2026).

**Live site:** [rootlake.github.io/admissions_vibe_coding](https://rootlake.github.io/admissions_vibe_coding/)

**Takeaways (mobile):** [takeaways.html](https://rootlake.github.io/admissions_vibe_coding/takeaways.html) — QR on final slide links here.

## What's here

| Path | Description |
|------|-------------|
| [`index.html`](index.html) | reveal.js talk deck |
| [`demos/funnel.html`](demos/funnel.html) | Admissions pipeline dashboard (aggregates only) |
| [`demos/lost-to.html`](demos/lost-to.html) | Competitive intel dashboard |
| [`LIVE-PROMPTS.md`](LIVE-PROMPTS.md) | Sanitized JSON + Canvas / Cursor prompts |
| [`prompts/`](prompts/) | Same prompts as plain `.txt` / `.json` for copy-paste |
| [`PRESENTER-NOTES.md`](PRESENTER-NOTES.md) | Presenter cheat sheet |
| [`RUNNING.md`](RUNNING.md) | Local server & shortcuts |

Demo dashboards load **pre-computed aggregates** from `demos/data/*.js` — no row-level student data.

## Run locally

```bash
npx serve .
```

Open `http://localhost:3000`

## GitHub Pages

This repo is configured for GitHub Pages from the **`main`** branch, root `/`.

After push: **Settings → Pages → Build from branch → main → /** 

Site URL: `https://rootlake.github.io/admissions_vibe_coding/`

## License

MIT — see [LICENSE](LICENSE).
