# antique-lamp-finder

Repository for the **Antique Electric Lamp Acquisition** routine, which runs weekly on a
schedule. Two artifacts live here:

- `LAMP-GUIDE.html` — persistent expertise. **Amend, never rewrite.** Read first every run.
- `LAMP-CATALOG.html` — buy candidates. **Rebuilt every run** from live-verified data.

## Standing instructions

### The routine spec is not the whole spec — read `LAMP-GUIDE.html` §0 first
The routine prompt lives in the scheduler and cannot be edited from inside a run. Owner-approved
amendments to it are recorded in **`LAMP-GUIDE.html` §0 "Active overrides"** and **supersede the
routine text they name**. Currently in force:

- **OV-1 (2026-07-27)** — replaces the §1 size gate. Single lamp **14–28"** high, shade
  **8–18"**; pair **12–28"** each, shade **6–18"** each; 20" shade cap retained. The original
  18"/10" floors excluded boudoir and desk lamps, which is the affordable Tier A supply and
  the historically correct form for a dresser.

### HTML only — the markdown artifacts are retired
Per the repository owner (2026-07-27): both `LAMP-CATALOG.html` and `LAMP-GUIDE.html` are
**high-fidelity HTML, committed to this repository**. The `.md` versions were deleted and must
not be recreated. Do not publish either as a hosted artifact. Each must stay a self-contained
single file so it renders straight from the repo.

### Every listing carries its link
Per the repository owner (2026-07-27): rejected lots and watchlist entries get direct URLs too,
not just buy candidates — a rejection should be checkable, not taken on trust. The catalog also
opens with a **count by source**, so the breadth of the sweep is visible up front.

### Sweep the whole internet, not just the easy channel
Per the repository owner (2026-07-27): run 1 leaned almost entirely on eBay because it fetched
reliably. That is a failure, not a shortcut. Work the aggregators (LiveAuctioneers reaches
dozens of houses in one query), the auction houses direct, the comp publishers (Toomey, Rago),
and the fixed-price and local channels. Record every source attempted — including the ones that
blocked — with counts.

### Always merge to `main` at the end of a run
Per the repository owner (2026-07-27): work is developed on the run's designated
`claude/*` branch, then **merged into `main` and pushed** as part of the same run. Do not
leave a run's output stranded on a feature branch, and do not open a pull request for it
unless explicitly asked — merge directly.

The owner refers to this branch as "master"; the actual default branch is **`main`**.

Sequence at end of run:
```
git checkout main
git merge --ff-only claude/<run-branch>    # falls back to a normal merge if diverged
git push -u origin main
git push -u origin claude/<run-branch>     # keep the run branch too
```

## Environment notes

- **Commit signing is broken in the run container.** `commit.gpgsign=true` with
  `gpg.format=ssh`, but `/home/claude/.ssh/commit_signing_key.pub` is provisioned as a
  0-byte file, so commits push as *Unverified*. `--reset-author` does not fix this; the
  key itself is empty. Cosmetic only — do not burn run budget on it.
- The run container is **ephemeral**. Nothing survives unless committed and pushed.
