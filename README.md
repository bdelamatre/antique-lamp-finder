# antique-lamp-finder

A weekly scheduled routine that hunts for an antique electric lamp — c.&thinsp;1900–1945,
signed where possible — to stand on a maple dresser in the bedroom. It sweeps auction houses,
aggregators, fixed-price marketplaces and local listings, verifies every candidate on its live
page, prices the true landed cost, and scores it against realized comparable sales.

Nothing is ever bought automatically. The routine produces a scored buy list and a maximum bid;
every purchase decision stays with the owner.

---

## Files

| File | What it is |
|---|---|
| **`ROUTINE.md`** | The routine instruction. The authoritative spec — v1.2, revised from run 1. |
| **`LAMP-GUIDE.html`** | Persistent expertise. **Amend, never rewrite.** Read first every run. Maker marks, authenticity red flags, channel ratings, search strings, comp library, lessons. |
| **`LAMP-CATALOG.html`** | Buy candidates. **Rebuilt every run** from live-verified data. Source of record, and the preferred way to read a run. |
| **`CLAUDE.md`** | Operating notes for the agent: standing instructions, environment quirks. |

The routine prompt itself lives in the scheduler and cannot be edited from inside a run.
Owner-approved amendments are recorded in **`LAMP-GUIDE.html` §0 "Active overrides"** and
supersede the routine text they name. `ROUTINE.md` folds those overrides in.

---

## Settings

| Setting | Value |
|---|---|
| Working budget, all-in landed | **$2,000** |
| Stretch ceiling, signed exceptional piece | **$5,500** |
| Absolute walk-away | **$6,500** |
| "Excellent value" threshold | Landed &le; **65%** of low comp (value score &ge; 1.54) |
| "Act now" threshold | Landed &le; **45%** of low comp (value score &ge; 2.2) |
| Shipping | Local pickup strongly preferred; ship only if the seller professionally packs glass |
| Geographic priority | New England &rarr; NY &rarr; national |
| Placement | Bedroom, on the maple dresser |
| Max restoration | Rewiring and replaced socket/cord fine. Replaced glass disqualifying above Tier C. |
| Cadence | Weekly. Auction catalogs post 2–4 weeks ahead. |

### Size gate — amended 2026-07-27 (OV-1)

|  | Overall height | Shade diameter |
|---|---|---|
| **Single lamp** | **14–28"** | **8–18"** |
| **Pair**, each lamp | **12–28"** | **6–18"** |

Shade over 20" is disqualifying in all cases. A pair at the working budget beats a single at
the stretch ceiling.

Viewed at close range against warm honey maple, so amber, gold, caramel, green and copper
palettes are favored; cold blue-white and stark black-and-white read wrong on the piece.

> **Why these numbers changed.** The original gate was 18–28" high with a 10–18" shade. Run 1
> established that this excluded boudoir and desk lamps entirely — they measure 11–16" with
> 6–10" shades — which is both the affordable Tier A supply and the form historically built for
> a dresser. Two independent floors were doing the exclusion, so both were lowered; moving
> height alone would have had no effect.

### Tiers

| Tier | Category | Weight |
|---|---|---|
| **A** | Tiffany Studios, Handel, Pairpoint, Duffner & Kimberly, Bigelow & Kennard, Gorham | High — in reach at the stretch ceiling |
| **B** | Moe Bridges, Jefferson, Miller, Bradley & Hubbard, Wilkinson, Chicago Mosaic, Suess, quality unsigned leaded | High — best price-to-quality |
| **C** | Arts & Crafts metal + mica: Dirk van Erp, Roycroft, Heintz, Old Mission Kopper Kraft, quality unsigned hammered copper | High |
| **D** | French / Continental Art Nouveau: Daum Nancy, Gallé, Muller Frères, Schneider, Loetz-shaded, Austrian/WMF | **Highest — strongest taste match** |
| **E** | Art Deco: figural spelter & bronze, molded glass, chrome/Bakelite | Low — only if exceptional |

### Out of scope

Shade-only, base-only, parts lots, project lamps · "Tiffany style", Dale Tiffany, Meyda,
Quoizel, all modern repro lines · kerosene converted to electric, unless a documented period
factory conversion priced as such · anything post-1945 · shades confirmed replaced with modern
glass · floor and bridge lamps · anything outside the size gate.

---

## Status

**Run 2 — 2 August 2026.** 12 sources swept, 5 reachable, 72 lots surfaced, 6 re-verified live.

**No buy candidate this run**, and two things need attention before the next one.

**1 — Stand down on the Americana Pairpoint.** Lot 0116 closes **8 August, 11:00 AM EDT**, and the
next weekly run fires after the hammer, so this is the last run that can speak to it. The bid sat
unmoved at $300 all week against a computed ceiling of **$228** — it is already $72 above the price
at which it was ever worth buying. Registering by 6 August only buys the option to place a losing
bid. Everything else about the lot checks out; the number does not.

**2 — The comp blocker came back.** Toomey & Co. and Rago, the two houses run 1 identified as
solving it, both now return **403 at the domain level** — they fetched normally six days earlier.
Under §5 nothing can be scored without a low comp, so three otherwise in-scope lots are stuck
unscoreable. A partial workaround is in the guide: their realized prices are still readable through
the search index, which recovered five dated Handel comps this run, though it cannot be steered to a
specific lot and found nothing for Pairpoint or Moe Bridges.

Also this run: a Handel reverse-painted lamp closing inside 72 hours was checked and declined
(unsupported attribution, boilerplate condition line, Caution-rated house, scores 1.40). **Red flag
14** added — the same lot listed at two houses with estimates matching to the dollar, which
disqualified 11 of 37 aggregator results at a glance. Local sweep run for the first time: Craigslist
and EstateSales.net are both effectively unusable by fetch.
