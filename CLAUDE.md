# antique-lamp-finder

Repository for the **Antique Electric Lamp Acquisition** routine, which runs weekly on a
schedule. Two artifacts live here:

- `LAMP-GUIDE.md` — persistent expertise. **Amend, never rewrite.** Read first every run.
- `LAMP-CATALOG.md` — buy candidates. **Rebuilt every run** from live-verified data.

## Standing instructions

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
