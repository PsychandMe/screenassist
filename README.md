# ScreenAssist

Free, private, in-browser **title/abstract screening for systematic reviews**, with a
learning ranker, a stopping heuristic and a built-in random-effects meta-analysis.

**By Joshua Bellot · [Psych & Me](https://substack.com/@psychandme)**

## What it does

- **Learns as you decide** — every include/exclude decision re-trains an on-device
  ranker (TF-IDF + supervised re-weighting) that reorders the queue so probably-relevant
  studies surface first. No server, no model upload — the learning happens in your tab.
- **Stopping heuristic** — screen until *N* consecutive irrelevant records (configurable)
  and the tool tells you the well has likely run dry.
- **Transparent by design** — include/exclude keywords are highlighted green/red in each
  record, so the ranking is never a black box.
- **Import** RIS, CSV (title, abstract, authors, year, doi, journal) with duplicate
  detection; optionally fetch missing abstracts from OpenAlex (the tool's only optional
  network call — records otherwise never leave your device).
- **Meta-analysis** — random-effects model built in, with export, for after the screening.

## Run it

Single-page app, no build step. Serve the `screenassist/` folder (e.g.
`python3 -m http.server`) and open `index.html`, or just host the folder anywhere static.

## Deploy to GitHub Pages

1. Create a public repo (e.g. `screenassist`) and upload this folder's contents.
2. Settings → Pages → Deploy from branch → `main` / `(root)`.
3. Live at `https://<username>.github.io/screenassist/`.

## Licence & reuse

Free to use, share and adapt for research and teaching. Attribution appreciated.
