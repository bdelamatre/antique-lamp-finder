# antique-lamp-finder

Repository for the **Antique Electric Lamp Acquisition** routine, which runs weekly on a
schedule. Two artifacts live here:

- `LAMP-GUIDE.md` — persistent expertise. **Amend, never rewrite.** Read first every run.
- `LAMP-CATALOG.md` — buy candidates. **Rebuilt every run** from live-verified data.

## Standing instructions

### The routine spec is not the whole spec — read `LAMP-GUIDE.md` §0 first
The routine prompt lives in the scheduler and cannot be edited from inside a run. Owner-approved
amendments to it are recorded in **`LAMP-GUIDE.md` §0 "Active overrides"** and **supersede the
routine text they name**. Currently in force:

- **OV-1 (2026-07-27)** — replaces the §1 size gate. Single lamp **14–28"** high, shade
  **8–18"**; pair **12–28"** each, shade **6–18"** each; 20" shade cap retained. The original
  18"/10" floors excluded boudoir and desk lamps, which is the affordable Tier A supply and
  the historically correct form for a dresser.

### Catalogs go in the repo, never to hosted artifacts
Per the repository owner (2026-07-27): the HTML catalog view is **committed to this repository**
as `LAMP-CATALOG.html`. Do not publish it as a hosted artifact. It must stay a self-contained
single file so it renders straight from the repo.

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
