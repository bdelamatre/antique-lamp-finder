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
| **`LAMP-CATALOG.html`** | Buy candidates. **Rebuilt every run** from live-verified data. Source of record. |
| **`LAMP-CATALOG.html`** | The catalog as a published page — the preferred way to read a run. |
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

**Run 1 — 27 July 2026.** 14 sources swept, 6 reachable, 44 lots surfaced, 6 verified live.

**One scored buy candidate:** a Pairpoint puffy boudoir lamp, Lot 0116 at Americana Auctions in
Rehoboth, MA, closing **8 August, 11:00 AM EDT**. 14.5" tall with an 8.5" shade, base stamped
*Pairpoint C3064*, shade perfect, local pickup available.

**Max bid $228.** Realized comps for the form run $645–$1,512 and the house takes a 28%
premium, so landed cost is roughly hammer × 1.40 + $100. At the current $300 bid it scores 1.24
(watch); at its own low estimate of $650 it scores 0.64, which is a bad buy. The estimate is
above what these actually fetch. Register by 6 August if you want the option.

**The comp blocker is solved.** Toomey & Co. and Rago publish realized prices openly with
dates — they are now the standing comp sources, and comp gathering leads each run.
