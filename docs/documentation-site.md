---
title: About This Site
purpose: Explain how the DSOS documentation site is built, what's in the nav vs. not, and the one manual step needed to make it live.
owner: Arulkumaran
dependencies: [mkdocs.yml, .github/workflows/deploy-docs.yml]
related_documents: [docs/master-index.md, docs/progress/v1-scorecard.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [How It Builds](#how-it-builds)
- [Why the Site Is Scoped to docs/ Only](#why-the-site-is-scoped-to-docs-only)
- [What "Tested" Means Here](#what-tested-means-here)
=======
- [The Phase 1 Bug This Phase Fixed](#the-phase-1-bug-this-phase-fixed)
=======
configuration (tested))
- [Nav Curation Policy](#nav-curation-policy)
- [The One Manual Step Left](#the-one-manual-step-left)
- [Local Preview](#local-preview)
- [Next Steps](#next-steps)

## Overview

DSOS is published as a static documentation site via [MkDocs](https://www.mkdocs.org/) with the Material theme, built and deployed automatically by `.github/workflows/deploy-docs.yml` on every push to `main`. **The site is scoped to `docs/` only** — templates, trackers, prompts, and projects are browsed on GitHub directly. This page explains why, and every claim in it has been verified with a real local build, not assumed.
=======
DSOS is published as a static documentation site via [MkDocs](https://www.mkdocs.org/) with the Material theme, built and deployed automatically by `.github/workflows/deploy-docs.yml` on every push to `main`.
=======
configuration (tested))

## How It Builds

1. GitHub Actions checks out the repo and installs `mkdocs`, `mkdocs-material`, and `pymdown-extensions`.
2. `mkdocs build --strict` builds the site from `mkdocs.yml`'s configuration.
3. `mkdocs gh-deploy --force` pushes the built site to the `gh-pages` branch, which GitHub Pages serves.

## Why the Site Is Scoped to docs/ Only

This repo's real content spans multiple top-level folders by deliberate design (`docs/`, `templates/`, `trackers/`, `prompts/`, `projects/`, `resources/`, plus root `README.md` and `AGENTS.md`) — that structure was set in Phase 1 and is referenced by hundreds of cross-links throughout the repo.

The first attempt at this phase tried to set `docs_dir: .` (repo root) so the site could include everything. **This was wrong, and testing caught it immediately:** MkDocs refuses to build with `docs_dir` set to the same directory as `mkdocs.yml` itself — it errors outright ("docs_dir should not be the parent directory of the config file"). A follow-up attempt reached for a plugin that looked like it solved this (`mkdocs-same-dir`); that turned out to be an unrelated package for a different tool entirely, not a real MkDocs plugin, and was caught the same way — by actually running the build rather than trusting the package name.

The real fix: `docs_dir: docs` (MkDocs' actual default, used explicitly). This means:
- **Fully on the site:** everything already in `docs/` — Departments, Operating System, Engineering Standards, Career System, Progress, Master Index, Document Map, Changelog.
- **GitHub only, not on the site:** `AGENTS.md`, root `README.md`, `templates/`, `trackers/`, `prompts/`, `projects/`, `resources/`. Linked clearly from `docs/README.md` (the site homepage) with direct GitHub URLs.

This was a real tradeoff, not a limitation to hide: restructuring the repo so *everything* lived under `docs/` would mean rewriting path references across the majority of the repo's 258 files and abandoning the top-level folder structure the whole repo was designed around from Phase 1 onward. Scoping the site to `docs/` was the smaller, honest tradeoff.

## What "Tested" Means Here

Every claim in this document was checked by actually running `pip install mkdocs mkdocs-material pymdown-extensions` and `mkdocs build --strict` locally against the real repo content, not inferred from reading the config. The build was iterated three times before it passed cleanly:
1. `docs_dir: .` → hard config error (caught, reverted)
2. `docs_dir: .` + a plugin that turned out to be for an unrelated tool → same config error persisted (caught, plugin removed)
3. `docs_dir: docs` + `README.md`/`index.md` conflict resolved + link validation corrected + two broken TOC anchors fixed → **clean build, exit code 0, zero warnings, 51 pages**

## Nav Curation Policy

Within `docs/`, the nav gives full detail to every document — the folder is small enough (49 files) that an exhaustive nav is genuinely useful, unlike the flat 50/14/104-file collections outside it.

## The One Manual Step Left

GitHub Actions can build and push to `gh-pages`, but **someone with repo admin access must enable GitHub Pages once**, pointing it at the `gh-pages` branch (or the "Deploy from GitHub Actions" source type). This repository was pushed to `github.com/AI-DSOS/AI-Data-Science-Operating-System` between Phases 1 and 2 — Pages deployment status as of this phase has **not been confirmed** (see `docs/progress/v1-scorecard.md`). Check under the repo's **Settings → Pages**.
=======
## The Phase 1 Bug This Phase Fixed
=======

This repo's real content spans multiple top-level folders by deliberate design (`docs/`, `templates/`, `trackers/`, `prompts/`, `projects/`, `resources/`, plus root `README.md` and `AGENTS.md`) — that structure was set in Phase 1 and is referenced by hundreds of cross-links throughout the repo.

The first attempt at this phase tried to set `docs_dir: .` (repo root) so the site could include everything. **This was wrong, and testing caught it immediately:** MkDocs refuses to build with `docs_dir` set to the same directory as `mkdocs.yml` itself — it errors outright ("docs_dir should not be the parent directory of the config file"). A follow-up attempt reached for a plugin that looked like it solved this (`mkdocs-same-dir`); that turned out to be an unrelated package for a different tool entirely, not a real MkDocs plugin, and was caught the same way — by actually running the build rather than trusting the package name.

The real fix: `docs_dir: docs` (MkDocs' actual default, used explicitly). This means:
- **Fully on the site:** everything already in `docs/` — Departments, Operating System, Engineering Standards, Career System, Progress, Master Index, Document Map, Changelog.
- **GitHub only, not on the site:** `AGENTS.md`, root `README.md`, `templates/`, `trackers/`, `prompts/`, `projects/`, `resources/`. Linked clearly from `docs/README.md` (the site homepage) with direct GitHub URLs.

This was a real tradeoff, not a limitation to hide: restructuring the repo so *everything* lived under `docs/` would mean rewriting path references across the majority of the repo's 258 files and abandoning the top-level folder structure the whole repo was designed around from Phase 1 onward. Scoping the site to `docs/` was the smaller, honest tradeoff.

## What "Tested" Means Here

Every claim in this document was checked by actually running `pip install mkdocs mkdocs-material pymdown-extensions` and `mkdocs build --strict` locally against the real repo content, not inferred from reading the config. The build was iterated three times before it passed cleanly:
1. `docs_dir: .` → hard config error (caught, reverted)
2. `docs_dir: .` + a plugin that turned out to be for an unrelated tool → same config error persisted (caught, plugin removed)
3. `docs_dir: docs` + `README.md`/`index.md` conflict resolved + link validation corrected + two broken TOC anchors fixed → **clean build, exit code 0, zero warnings, 51 pages**

## Nav Curation Policy

Within `docs/`, the nav gives full detail to every document — the folder is small enough (49 files) that an exhaustive nav is genuinely useful, unlike the flat 50/14/104-file collections outside it.

## The One Manual Step Left

GitHub Actions can build and push to `gh-pages`, but **someone with repo admin access must enable GitHub Pages once**, pointing it at the `gh-pages` branch (or the "Deploy from GitHub Actions" source type). This repository was pushed to `github.com/AI-DSOS/AI-Data-Science-Operating-System` between Phases 1 and 2 — Pages deployment status as of this phase has **not been confirmed** (see `docs/progress/v1-scorecard.md`). Check under the repo's **Settings → Pages**.

## Local Preview

```bash
pip install mkdocs mkdocs-material pymdown-extensions
mkdocs serve
```

Then open `http://127.0.0.1:8000`.

## Next Steps

- Confirm GitHub Pages is enabled and the site is actually live — the last open item before the "Documentation site: Deployed" v1.0 target can be marked 100%.
- If the `docs/`-only scope ever feels too limiting, the real fix would be migrating `templates/`, `trackers/`, `prompts/`, and `projects/` under `docs/` as subfolders — a deliberate, larger restructuring decision to make at a Quarterly Review, not a quick config change.
=======
- Revisit the nav curation policy once real usage shows whether search alone is sufficient for templates/trackers/prompts, or whether a few high-traffic files deserve promotion into the nav.

=======
