# DCC Visual Reference — VERSION LOCK

## STOP: do not restore historical shells

The canonical UI shell is currently **unresolved** after an accidental overwrite on 2026-10-13.

Until the user explicitly confirms the recovered canonical shell, **do not replace `index.html` from any historical commit based on labels such as "working", "known good", "reader", "archive", "production", or "canonical".**

### RETIRED / FORBIDDEN UI SHELLS

The following builds are known to be the WRONG layouts and must never be used as a restoration base:

- `1f59c36a0e0983b9b194af375402f072011830f1` — "Restore full reader and correct Book 1 artwork" — WRONG historical reader shell.
- `dd9e9f0c7e6d5e33d80e02d774ed6d61bae2c0a3` — "Restore approved archive layout and keep corrected Book 1 art" — WRONG Crawler Archive shell.
- `da24c18911d27f9c9d75138d7f17320585d350ea` — "Restore mobile book reader shell with current Book 1 art" — WRONG mobile shelf/book-reader shell.
- `e663f5beb5dfa085858e9dd2a7e4637405594fde` — historical "current DCC production site" import — WRONG shell for the desired app.
- `4b1fea1f55b5d80661e5a5769cea5d958fa793d1` — historical "chained-book build" — WRONG shell for the desired app.

These commits may contain useful artwork/assets, but their `index.html` / UI structure is retired.

## Recovery rule

The correct app is the version the user had immediately **before the 2026-10-13 "fix everything" overwrite**.

Before changing the shell again:

1. Identify the exact candidate commit/file.
2. Compare its layout against the user's confirmed correct version.
3. Get explicit user confirmation if there is any ambiguity.
4. Only then replace `index.html`.
5. Artwork may be harvested independently from other commits without restoring their UI shell.

## Current state

- The live Pages shell may still be wrong.
- Do not treat the current `main/index.html` as canonical until the user confirms it.
- The next successful recovery should update this file with the canonical commit SHA and remove the "unresolved" status.
