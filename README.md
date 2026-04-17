# SourceInc

Workspace for the SourceAbility site **rebrand / redesign** (exported from Stitch).

## CSS / Tailwind (build pipeline)

- **Source:** `assets/css/tailwind.css` (Tailwind layers + site base styles).
- **Built file:** `assets/css/main.css` (commit this so static hosts work without Node; rebuild after HTML/class changes).
- **Theme tokens:** `tailwind.config.js` at the project root.

```bash
npm install          # once
npm run watch:css    # dev: rebuild main.css on save
npm run build:css    # production minified bundle
```

Add new HTML paths under `content` in `tailwind.config.js` when you introduce subfolders (e.g. `./pages/**/*.html`).

## Next steps

1. Add or edit HTML at the repo root (or under `pages/` after updating `tailwind.config.js` `content`), then run `npm run build:css`.
2. Open `index.html` via a local server (e.g. `npx serve .` from this folder).
3. Push to Git; CI can run `npm ci && npm run build:css` before deploy if you prefer not to commit `main.css`.

## Relationship to `sourceability-website`

The existing `sourceability-website` project stays as-is. This repo is the fresh redesign track until you choose to merge or replace.
