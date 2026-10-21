# Computing Infrastructure for Clinical AI

### ▶ [View the slides](https://rudolphpienaar.github.io/NSDF2026/) — https://rudolphpienaar.github.io/NSDF2026/

Slides for Rudolph Pienaar's talk at the **NSDF Summit on Federated Autonomous Science**,
Monday 19 October 2026, Discovery Partners Institute, Chicago. Session: *Science Domains and
Trustworthy Autonomy* (10:30–12:00), 10-minute slot.

The argument in one line: the clinical AI that delivers value is small, predictive and local —
and hospitals can neither *run* it (they were never built to compute) nor *approve* it (governance
was written for LLMs). The fix is infrastructure, and governance that can tell the difference.

## Presenting

The deck is a hub-and-spoke "nexus": an outline (slide 4) from which sections are chosen live.

| Key | Action |
|---|---|
| `1`–`8`, or Up/Down + Enter, or click | open a section from the outline |
| Right / Left | next / previous (reveals bullets one at a time) |
| Backspace (or Esc) | back to the outline from anywhere in a section |
| `f` | toggle the deck's own fullscreen |

Running off the end of a section also returns to the outline; visited sections are dimmed (per
browser tab). In browser fullscreen, use **Backspace** — browsers keep Esc for leaving
fullscreen.

## Building locally

The deck is written in [slidedown](https://github.com/FNNDSC/slidedown) (`talk.sd`, `terminal`
theme) and compiles to static HTML in `talk/`.

```bash
# with a slidedown checkout at ~/src/slidedown
uv run --project ~/src/slidedown slidedown . talk --inputFile talk.sd --theme terminal
cd talk && python3 -m http.server 8000      # then open http://localhost:8000
```

Or with pip: `pip install -e path/to/slidedown`, then run `slidedown` as above. The deck needs
slidedown `main` at or after the FNNDSC/slidedown#2 merge (deck CSS overrides the theme, console
highlighting, nexus return keys).

## Deployment

`.github/workflows/pages.yml` builds the deck on every push to `master` and deploys `talk/` to
GitHub Pages. slidedown is pinned to a specific commit so an upstream change can't break the
deck unannounced — bump the pin deliberately. The runner is pinned to `ubuntu-24.04`.

## Layout

| Path | What |
|---|---|
| `talk.sd` | the deck source |
| `docs/notes.adoc` | working notes: the argument section by section, evidence, open questions |
| `docs/refs.bib` | every source behind a figure on a slide (BibTeX, with provenance notes) |
| `notes/run-of-show.md` | timing, slide map, presenting notes |
| `.github/workflows/pages.yml` | build and deploy |

## Sources

Every number on a slide carries a source line; full references are in
[`docs/refs.bib`](docs/refs.bib). Journal entries were checked against PubMed; trade and vendor
surveys are marked as such.

## License

[MIT](LICENSE) © 2026 Rudolph Pienaar
