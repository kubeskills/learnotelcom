# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

learnOTel.com: a single-page static site linking to OpenTelemetry learning resources. Deployed on Netlify with no build command; the publish directory is the repo root, so every file in the repo is served as-is. There is no package manager, test suite, or linter config.

## Commands

```bash
python3 -m http.server 8000   # local preview at http://localhost:8000
```

Netlify `_redirects` rules are **not** applied by `http.server`; verify them on a Netlify deploy preview (or `netlify dev`).

## Architecture

- `index.html` is fully self-contained: all CSS is in one inline `<style>` block, with brand colors as CSS custom properties in `:root` (`--otel-blue`, `--otel-orange`, ...). Don't split out a stylesheet or add a build step or framework; the README documents "no build step" as a deliberate property.
- Resource cards are hand-written `<li>` entries in `ul.links` (link + `<span>` description). Adding a resource means adding an `<li>` **and** updating the "Resources featured" list in `README.md`; the two are maintained by hand and must stay in sync.
- Images (`opentelemetry-horizontal-color.png`, `kubeskills-horizontal-logo.png`) sit in the repo root and are referenced by relative path. Keep the explicit `width`/`height` attributes on `<img>` tags (they prevent layout shift).
- `_redirects` holds Netlify redirect rules, one per line (`/from  destination  status`). Currently only `/demo-arch` → the OpenTelemetry demo architecture docs.
- When adding or renaming files, update the "Structure" table in `README.md` (recent history shows this is done as a separate `docs(readme)` commit after each new file).

## Conventions

- Commit style is conventional commits with scope, e.g. `feat(site): ...`, `docs(readme): ...`.
- Commit directly to `main` in this repo; do not create `feature/` branches or PRs unless asked. This overrides the global `feature/<change-name>` branch convention. Never force-push.
- `index.html` is formatted prettier-style (2-space indent, `<a>` text wrapped as `>Text</a\n>` when long); keep new markup consistent with that.
- The site is not affiliated with the OpenTelemetry project; keep the trademark disclaimer in `README.md` if editing branding.
