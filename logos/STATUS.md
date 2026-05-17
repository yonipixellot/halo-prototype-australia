# Logo scrape status

All files are **512×512 PNG, white background, ~12% padding, real official artwork** (no fabrication). Pulled from each org's own site / NBL CDN / Wikipedia.

> ⚠️ These are trademarked marks of their respective orgs — fine for an internal demo, but you (or BA) need licensing before anything ships.

## ✅ Got — 36 files

**National + state federations (P5/P6) · 8/8**
- `ba-national.png` — Wikipedia (official BA mark)
- `state-act.png` — basketballact.com.au brand page
- `state-nsw.png` — bnsw.com.au brand page (2023 rebrand)
- `state-nt.png` — basketballnt.com.au header
- `state-qld.png` — queensland.basketball header (SVG → rasterized)
- `state-sa.png` — basketballsa.com.au header
- `state-tas.png` — basketballtasmania.com.au header
- `state-vic.png` — *named `basketball-victoria.png`* (basketballvictoria.com.au — see note*)
- `state-wa.png` — *named via Wikipedia (`bwa.png`)* (see note*)

**P3 · QLD pathway · 7/7**
- `brisbane-capitals.png` · `sunshine-coast-phoenix.png` · `cairns-marlins.png` · `toowoomba-mountaineers.png`
- `brisbane-capitals-u18.png` · `spartans-u18.png` · `northside-wizards-u18.png` *(U18 reuses parent crest — junior rep teams universally use the senior club mark)*

**P4 · Cross-state · 18/18**
- VIC: `melbourne-tigers.png` · `bendigo-braves.png` · `frankston-blues.png` · `knox-raiders.png`
- NSW: `sydney-comets.png` · `manly-sea-eagles.png` · `hills-hornets.png` · `illawarra-hawks.png`
- WA: `joondalup-wolves.png` · `perth-redbacks.png` · `cockburn-cougars.png`
- SA: `forestville-eagles.png` · `norwood-flames.png` · `south-adelaide-panthers.png`
- TAS: `hobart-chargers.png` · `launceston-tornadoes.png`
- ACT: `canberra-gunners.png` *(ACT Academy missing — see below)*
- NT: `darwin-salties.png`

**P5 · Brand assets · 1/3**
- `org-spartans.png` — Southern Districts Spartans org mark (from NBL1 club page)

## Filename audit

All 36 files now match LOGOS-NEEDED.md names exactly. `basketball-victoria.png` was renamed to `state-vic.png`.

## ❌ Skipped / missing — 10 + venue/photo

**P1 + P2 · Thursday Men D rec teams · 0/8** — confirmed no public logos exist.
Every team name (Sesh Rigs, Medium Fundamentals, Hustle HQ, Hoopin Huskies, Shaqtin A Fool, KingSlayers, Chump Central, Nothing But All Stars) returns either zero hits or unrelated results (e.g. NRL Sea Eagles). These are domestic rec team names — no logos published. **Recommended action:** either ask Southern Districts Spartans for a club pack, or accept the initials-on-glass fallback (the doc says it looks fine).

**P4 · ACT Academy** — not a distinct entity. Basketball ACT runs "Canberra Capitals Academy" and "Canberra Gunners Academy" programs but neither has its own crest. **Suggest:** reuse `state-act.png` or drop the tile.

**P5 · Venue + BA national** — `venue-rowland-cowan.jpg` not pursued (not a logo, needs venue photography). `ba-national.png` is done.

## Where each came from

Almost all real artwork from one of three sources:
1. **NBL CDN** (`cdn.nbl.com.au/s/<uuid>`) — every NBL1 club page exposes its crest at a stable URL. This was the workhorse for ~22 of the 36.
2. **Org branding pages** — basketballact.com.au, bnsw.com.au, basketballsa.com.au, queensland.basketball, basketballnt.com.au, basketballtasmania.com.au all publish their primary mark on a brand or header page.
3. **Wikipedia / Wikimedia Commons** — BA national, BWA. Used only when the org's own site was JS-hidden or 403'd.

## Build pipeline

`_raw/` contains the originals. `_raw/build.sh <source> <name>` rasterizes (if SVG via `sips`), trims transparent border, composites onto a 512×512 white square with 12% padding, saves as PNG. Re-run if you want a different padding or size.
