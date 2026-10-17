# Computing Infrastructure for Clinical AI — run of show

NSDF Summit on Federated Autonomous Science — Mon 19 Oct 2026, Discovery
Partners Institute, 200 S Wacker, Chicago (4th floor).

Session: *Science Domains and Trustworthy Autonomy*, 10:30–12:00, moderator
Mike Papka (Argonne/UIC). **10-minute talk**, then a 20-minute cross-domain
discussion shared with Hart, Alter, Bremer, Nikolich, Xu, Kirby.

Deck: `talk.sd` → build in `talk/`. Terminal theme, styling carried over from
`RedHat2026_Hackathon/deep_dive.sd`.

## Build and serve

```bash
uv run --project ~/src/slidedown slidedown . talk --inputFile talk.sd --theme terminal
cd talk && python3 -m http.server 8000
```

## Shape (so far)

| Slide | What |
|---|---|
| 1 | Boot — title, venue |
| 2 | Whoami — roles, then credentials. 7 reveals |
| 3 | Whatido — ChRIS, HARBOR, the hospital/cloud boundary |
| 4 | Outline — the nexus hub. Press 1–8, arrows + Enter, or click |
| 5–22 | Sections 1–6, three slides each: the point, the evidence, a closing slide |
| 23–29 | Section 7, The AI Bubble: facts, the premise, earned vs lost, the subsidy, the gap, if it pops, local models |
| 30 | Section 8, Conclusions |

Advancing off the end of a section returns to the hub; Backspace (or Esc)
returns from anywhere. In fullscreen use Backspace -- the browser keeps Esc
for exiting fullscreen. `f` toggles the deck's own fullscreen.
Visited sections dim on the hub (per browser tab — a fresh tab starts clean).
To reset after a practice run: open the deck in a **new tab** (or close and reopen the
tab). Reloading the same tab keeps the history — it lives in that tab's `sessionStorage`
(`slidedown:visited:<path>`), by design so a mid-talk reload doesn't lose your place.

## Opening

The moderator will likely introduce you, so slide 2 can go faster than at the
hackathon — thirty seconds. Slide 3 is the pivot into the argument: land the
prompt line and move on.
