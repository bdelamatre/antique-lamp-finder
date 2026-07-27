# Routine: Antique Electric Lamp Acquisition

**Version 1.2** — revised from run 1 (2026-07-27). Supersedes v1.1.
**Cadence:** Weekly. Auction catalogs post 2–4 weeks ahead.

---

## 0. Settings

| Setting | Value |
|---|---|
| Working budget, all-in landed | **$2,000** |
| Stretch ceiling, signed exceptional piece | **$5,500** |
| Absolute walk-away | **$6,500** |
| "Excellent value" threshold | Landed ≤ **65%** of low comp (= value score ≥ 1.54) |
| "Act now" threshold | Landed ≤ **45%** of low comp (= value score ≥ 2.2) |
| Shipping | Local pickup strongly preferred; ship only if the seller professionally packs glass |
| Geographic priority | New England, then NY, then national |
| Placement | **Bedroom, on the maple dresser** — see size gate, §1 |
| Max restoration | Rewiring and replaced socket/cord: fine. Replaced glass: disqualifying above Tier C. |

---

## 1. Scope

### Size gate — **revised in v1.2**

|  | Overall height | Shade diameter |
|---|---|---|
| **Single lamp** | **14–28"** | **8–18"** |
| **Pair**, each lamp | **12–28"** | **6–18"** |

- Shade over **20"** is disqualifying in all cases.
- Below the floor reads as an accessory; above 28" overpowers a dresser.
- Viewed at close range and against warm honey maple — favor amber, gold, caramel, green, and
  copper palettes. Cold blue-white and stark black-and-white read wrong on this piece.
- **Flag matching pairs.** Boudoir and small table lamps were often sold in pairs, and a
  dresser takes a pair well. **A pair at the working budget beats a single at the stretch
  ceiling.**

> **v1.1 → v1.2.** The old gate (18–28" high, 10–18" shade) excluded boudoir and desk lamps
> entirely — they run 11–16" with 6–10" shades. That is both the affordable Tier A supply and
> the form historically built for a dresser, so the gate was working against the brief. Two
> independent floors were doing the exclusion; both were lowered. **When a gate eliminates
> everything, suspect the gate.**

### Tiers

| Tier | Category | Weight | Notes |
|---|---|---|---|
| **A** | Tiffany Studios, Handel, Pairpoint (puffy & reverse-painted), Duffner & Kimberly, Bigelow & Kennard, Gorham | **High — in reach at the stretch ceiling** | Handel and Pairpoint table lamps regularly land in the $2.5–6k band. Smaller forms — desk, damascene, boudoir — are the realistic entry, and are now inside the size gate. |
| **B** | Moe Bridges, Jefferson, Miller, Bradley & Hubbard, Wilkinson, Chicago Mosaic, Suess, quality unsigned leaded | **High — best price-to-quality** | Where the working budget buys an excellent lamp outright |
| **C** | Arts & Crafts metal + mica: Dirk van Erp, Roycroft, Heintz, Old Mission Kopper Kraft, quality unsigned hammered copper | High | Copper and mica against maple is the strongest material match in the list |
| **D** | French / Continental Art Nouveau: Daum Nancy, Gallé, Muller Frères, Schneider, Loetz-shaded, Austrian/WMF | **Highest — strongest taste match** | Established collecting lane. Watch for marriages **and for the reproduction problem in §7.** |
| **E** | Art Deco: figural spelter & bronze, molded glass, chrome/Bakelite | Low | Only if exceptional or an outright steal |

### Out of scope
- Shade-only, base-only, parts lots, project lamps
- "Tiffany style," "Tiffany-inspired," Dale Tiffany, Meyda, Quoizel, Warehouse of Tiffany, all
  modern repro lines
- **Modern makers trading on the vernacular** — Mica Lamp Company and similar. Founded
  1970s–80s; the name reads period, the goods are not.
- Kerosene/oil converted to electric, unless a documented period factory conversion priced as such
- Anything post-1945
- Shade confirmed replaced with modern glass
- Floor and bridge lamps
- Anything outside the size gate

---

## 2. Artifacts

All four live in the repository and are **committed and pushed every run** (§10).

### `LAMP-GUIDE.md` — persistent expertise
Read first every run. **Amend, never rewrite.** Contents:
- **§0 Active overrides** — owner-approved amendments to this spec. This routine prompt lives
  in the scheduler and cannot be edited from inside a run, so approved changes are recorded
  there and **supersede the routine text they name.** Fold them into `ROUTINE.md` when convenient.
- **Makers & marks** — signature locations, mark forms, cloth labels, variants
- **Authenticity red flags** (§7)
- **Channel directory** — with a **fetchability** rating (§3) and a quality rating
- **Search strings** — exact queries and negative keywords, so runs are reproducible
- **Comp library** — realized prices by maker/form/size, with date and source
- **Lessons learned** · **Changelog**, version bumped every run

### `LAMP-CATALOG.md` — buy candidates, source of record
Rebuilt every run from live-verified data. Schema in §9.

### `LAMP-CATALOG.html` — the published view
The same catalog as a self-contained page, **committed to the repo** (not published as a
hosted artifact). This is the preferred way to read a run. Rebuild it whenever the markdown
changes; keep the two consistent.

### `README.md` — settings and current status
Keep the settings table and the Status section current.

**Live/sold split:** the no-ended-listings rule governs the Buy Candidates table only. Sold
data is valuation evidence and belongs in the guide's comp library and the catalog's comp
column, always labeled SOLD with a date. Never in the candidates table.

---

## 3. Run protocol

**Reordered in v1.2** by actual yield. Budget ~25–35 tool calls. Never skip steps 1, 2, or 7.

**1. Prune.** Re-verify every existing catalog row (§4). Delete anything sold, ended,
withdrawn, or out of stock. Move realized prices into the comp library. Prune runs before new
searching, so a truncated run still leaves a clean catalog.

**2. Comps first.** *(New in v1.2 — promoted from a sub-step of valuation.)* Nothing can be
published without a low comp to divide by, so establish comps **before** searching for new
inventory. Sources in order: LiveAuctioneers price-guide and price-result pages, Worthpoint,
published house results, Invaluable archives. **eBay sold search is login-walled — do not
spend calls on it.** If a run ends with no comps, it ends with no candidates, regardless of
what it found.

**3. Fixed-price sweep.** eBay first — it produced 100% of run 1's verifiable candidates.
Auction and BIN; sort by ending soonest and by newly listed. Then Etsy, Ruby Lane, EBTH,
ShopGoodwill. 1stDibs and Chairish for comp calibration only.

**4. Local sweep.** Facebook Marketplace and Craigslist for Portland/Portsmouth/Boston;
EstateSales.net for upcoming New England sales. Best value per dollar and no shipping risk.

**5. Regional auction sweep.** Upcoming sales, next 30 days. Treat as **watchlist-building**,
not candidate-building — catalogs for the next 30 days are usually unposted.
- Maine: Thomaston Place, Bruce Gamage Jr., Kaja Veilleux
- Massachusetts: Fontaine's (Pittsfield), Eldred's, Bonhams Skinner
- RI/CT/NY: Bruneau & Co., Copake, Cottone
- National, watch regardless of distance: Woody Auction, Morphy, Jeffrey S. Evans, Rago

**6. Aggregator sweep.** LiveAuctioneers, Invaluable, HiBid, Bidsquare, AuctionZip, Proxibid.
Upcoming only. Record sale start date and lot close time.

**7. Verify, score, publish** (§4, §5, §9). Rebuild both the markdown and the HTML.

**8. Learn one thing.** Add exactly one substantive guide entry — a maker profile, a mark
detail, a fake-identification technique, a channel rating.

**9. Commit, merge, push** (§10).

---

## 4. Verification

- **No listing enters the catalog from a search snippet.** Fetch the listing URL and read the
  live page.
- Every row records `Verified live: YYYY-MM-DD HH:MM ET`.
- Unfetchable page — paywall, login, timeout, JS-only, 403 — **does not publish.**
- **Record fetchability in the channel directory.** *(New in v1.2.)* A channel that cannot be
  fetched yields zero candidates no matter how good its inventory, so this is a first-class
  property of a channel, not an incidental failure. Known blocked as of run 1: Fontaine's
  (403), eBay sold search (login), `live.thomastonauction.com` (403).
- **When sources disagree about whether a sale exists, say so and resolve by phone rather than
  picking one.** *(New in v1.2.)*
- Auction lots: status is `Upcoming — opens [date]` or `Bidding open — closes [date/time ET]`.
  Already hammered is out.
- Fixed-price: confirm active and in stock.

---

## 5. Valuation

```
Landed = Hammer
       + Buyer's premium (20–28% — read the actual terms)
       + Online platform fee (LiveAuctioneers/Invaluable typically 3–5% on top)
       + Card surcharge (0–4%)
       + Sales tax where applicable
       + Packing & shipping (art glass $100–400; leaded shades more)
       + Insurance
       + Rewiring allowance ($60–150) if needed
```

Fees routinely add 50–70% to hammer. A $500 hammer shipped cross-country lands near $850; the
same lamp picked up locally lands near $625.

**Comps.** Minimum three realized sales, same maker and comparable form/size/condition, within
3 years. Fewer than three → mark `Comps: thin` and widen the range rather than inventing
precision. **A pre-sale estimate is not a comp** — it is a house's marketing position, not a
realized sale. *(Clarified in v1.2.)*

**Value score = low comp ÷ landed cost**

| Score | Band |
|---|---|
| ≥ 2.2 | **ACT NOW** — top of catalog |
| 1.54 – 2.2 | Strong candidate — meets the excellent-value threshold |
| 1.15 – 1.54 | Watch |
| < 1.15 | Do not publish |

Show the arithmetic, not just the verdict.

---

## 6. Completeness gate

All must pass to publish:

- [ ] Shade and base both present, shade plausibly original to the base (§7)
- [ ] No cracked, missing, or replaced glass segments; no significant chips
- [ ] Socket, switch, and cord present — condition irrelevant, rewiring is expected
- [ ] Shade support present: harp, heat cap, spider, or shade ring as the form requires
- [ ] Finial present, or absence noted and priced in
- [ ] Base uncracked, not heavily dented; original unpolished patina preferred
- [ ] Within the §1 size gate

If photos are insufficient to judge, generate a condition report request (§9) rather than
discarding — bad photos are where value hides.

---

## 7. Authenticity

**Marriages** — a period shade wed to an unrelated period base. The most common trap. Tells:
proportions wrong for the form, fitter that required shimming, mismatched patina or metal
color, mounting hardware inconsistent with the shade type, "attributed" or "matched" in the
description. **A title that names the base's maker but not the shade's is conceding a
marriage.** *(New in v1.2.)*

**Reverse-painted shades** (Handel, Pairpoint, Moe Bridges, Jefferson) are painted on the
**interior**. Exterior decoration is a repro tell. Handel signs the lower rim and often carries
a cloth label. Pairpoint puffies are molded, not blown-and-painted. Note that Handel's
chipped-ice and "Teroca" *textured* exteriors are period-correct and are not the same thing as
exterior painting — the decoration still lives inside.

**Leaded shades** — original came shows aged, oxidized solder joints; repro solder is bright
and uniform. Original glass has striations, variation, occasional bubbles. Perfectly uniform
glass in a "period" shade is a repro.

**Signatures** — learn where each maker actually signed: Tiffany Studios on the base underside
and shade inner rim tag; Dirk van Erp's windmill; Roycroft's orb-and-cross. A signature in the
wrong place or wrong form is worse than none — it means someone was trying.
**For Muller Frères specifically, a plausible signature is not evidence:** since the 1980s,
glass has been produced copying the correct 1919 signature style with different graphism.
Demand a raking-light photograph of the signature. *(New in v1.2.)*

**Metal** — spelter is light, gray at chips, worth a fraction of bronze. Check weight for size
and color at wear points.

**Shipping economics that contradict the asking price.** *(New in v1.2.)* A four-figure art
glass lamp offered with $17 economy shipping is incoherent — nobody insures and professionally
packs real cameo glass at that price. The shipping line is a claim about what the seller
believes the object is worth. When it contradicts the ask, believe the shipping line.

**Keyword pollution** — "style," "in the manner of," "after," "inspired by" are repro markers.
Negative-keyword them in every saved search.

**Restoration** — reputable houses disclose. Silence in a condition report is a question, not a
green light.

---

## 8. Bid discipline

- Compute the max bid before the sale, write it in the catalog, do not recompute during bidding.
- Prefer absentee/proxy bids at the ceiling over live participation.
- Register to bid 48+ hours ahead; approval isn't instant everywhere.
- Assume as-is, final, no returns. The condition report is the only protection — request it early.
- **No purchase is a valid run outcome.** So is a run that publishes nothing, provided it says
  clearly *why*.

---

## 9. Catalog schema

Sort: ACT NOW first, then soonest deadline. Thumbnail per row.

| Field | Content |
|---|---|
| Image | Thumbnail from listing. In the HTML view, a drawn silhouette indicating form is acceptable and should be labeled as such — never present a drawing as a photograph of the lot. |
| Lamp | Maker (or attributed/unsigned), form, date, **overall height and shade diameter** |
| Tier | A–E |
| Channel | House or platform + location |
| Status | `Upcoming — opens [date]` / `Bidding open — closes [date/time ET]` / `Fixed price — in stock` |
| Ask | Current bid or asking price; house estimate if published |
| Est. landed | Full §5 arithmetic, shown |
| Comp range | Low–high from ≥3 realized sales, each dated and sourced, labeled SOLD |
| Value score | Ratio + band |
| Condition | Pass/fail against §6, concerns named |
| Auth notes | What was checked, what couldn't be, confidence |
| Max bid | Ceiling computed backward from the value threshold |
| Link | Direct URL |
| Verified live | Timestamp |
| Action needed | e.g. "Request condition report — no underside photo" / "Register to bid by [date]" |

Below the table:
- **Reinstated / in scope but unscoreable** — in scope, blocked on something nameable
- **Watchlist** — auctions with catalogs not yet posted, plus the date to check back
- **Rejected this run** — item + one-line reason

---

## 10. Git

Development happens on the run's designated `claude/*` branch, then:

```
git checkout main
git merge --ff-only claude/<run-branch>
git push -u origin main
git push -u origin claude/<run-branch>
```

**Always merge to `main`** — never leave a run's output stranded on a feature branch. Do not
open a pull request unless explicitly asked. The run container is ephemeral: nothing survives
unless committed and pushed.

---

## 11. Escalation

Lead the response in plain language, before the catalog, with the exact deadline, if a run finds:
- value score ≥ 2.2, or
- an auction closing within 72 hours, or
- a fixed-price listing below 45% of low comp, or
- **a defect in this spec that is suppressing results** *(new in v1.2 — this is how the size
  gate problem surfaced)*, or
- **the routine could not run** — access denied, credentials missing, a channel newly blocked.

Notify by push when any of the above fires. A run that finds nothing and has nothing to fix
should stay quiet.

---

## 12. Self-improvement

Each run, append to Lessons learned:
- Which channels produced publishable candidates and which produced nothing → reorder §3
- **Which channels could not be fetched at all** → §4, and consider whether access is worth
  solving before adding new channels
- Realized prices for anything watched → comp library
- Any estimate off by >30% → why
- Any authenticity call now made differently

After ~6 runs, review whether the §1 tier weighting matches what's actually appearing.

---

## Changelog

- **v1.2 — 2026-07-27** — Revised from run 1. **Size gate lowered** (single 14–28"/8–18", pair
  12–28"/6–18") after the old floors excluded the affordable Tier A supply. **§3 reordered by
  yield** — comps promoted to step 2, fixed-price ahead of auction houses, auction sweeps
  demoted to watchlist-building. **Fetchability made a first-class channel property** (§4).
  Three authenticity tells added (§7): shipping-cost incoherence, the Muller Frères signature
  graphism problem, marriage-by-title. Modern-vernacular makers added to out-of-scope.
  Estimates explicitly excluded from comps (§5). Git and escalation sections added (§10, §11).
  Artifacts now include an HTML view committed to the repo (§2).
- **v1.1** — Settings filled. Size gate added for dresser placement. Tier A reweighted for the
  $5,500 stretch ceiling. Meta-commentary removed.
- **v1.0** — Initial spec.
