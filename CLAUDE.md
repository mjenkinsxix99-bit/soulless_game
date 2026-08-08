# Project Rules

## Git

- NEVER push or merge to `master` without explicit instruction from the user in the current conversation. Always wait to be told before touching master.
- ALWAYS create a new branch at the start of each session before making any changes.
- ALWAYS open a pull request to GitHub after pushing a branch, without waiting to be asked.

## Changelog

- Do NOT write changelog entries (or bump the version for them) until the user explicitly says to.

## Stage Background

- The left panel was removed. There is now a SINGLE shared realm background,
  `#realm-bg-img-left`, hosted on `#main` and spanning the whole stage.
- Its transform is locked at `translateX(-1px) translateY(-76px)` with
  `scale` driven by `REALM_BG_LEFT_SCALE` (all realms `1.15`). This value was rebaked
  (2026, with explicit user confirmation) from the previous locked `translateY(-400px)`
  to fit the approved 1920×1080 full-screen HUD layout.
- The former middle image (`#realm-bg-img`) is retired and kept hidden; do not revive it.
- NEVER change the locked transform value for any reason.
- NEVER change the anchor points (`top:0; left:0; transform-origin:top left`) on the
  background image.
- On mobile only, `#realm-bg-img-left` keeps its pre-existing portrait override
  (`translateX(0px) translateY(-315px) scale(0.80)`); that is separate from the locked
  desktop value above.
- If the user requests something that would alter the background position or anchor,
  WARN them before making any change and get explicit confirmation.
