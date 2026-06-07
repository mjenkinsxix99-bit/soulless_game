# Project Rules

## Git

- NEVER push or merge to `master` without explicit instruction from the user in the current conversation. Always wait to be told before touching master.
- ALWAYS create a new branch at the start of each session before making any changes.
- ALWAYS open a pull request to GitHub after pushing a branch, without waiting to be asked.

## Left Panel Background

- The left panel background transform is permanently locked at `translateX(0px) translateY(-400px)` with `scale` driven by `REALM_BG_LEFT_SCALE` (all realms `1.15`).
- The middle panel background transform is permanently locked at `translateX(-370px) translateY(-400px)` with `scale` driven by `REALM_BG_SCALE` (all realms `1.15`).
- NEVER change these transform values for any reason.
- NEVER change the anchor points (`top:0; left:0; transform-origin:top left`) on either background image.
- If the user requests something that would alter either background position or anchor, WARN them before making any change and get explicit confirmation.
