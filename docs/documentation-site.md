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
- [The Phase 1 Bug This Phase Fixed](#the-phase-1-bug-this-phase-fixed)
- [Nav Curation Policy](#nav-curation-policy)
- [The One Manual Step Left](#the-one-manual-step-left)
- [Local Preview](#local-preview)
- [Next Steps](#next-steps)

## Overview

DSOS is published as a static documentation site via [MkDocs](https://www.mkdocs.org/) with the Material theme, built and deployed automatically by `.github/workflows/deploy-docs.yml` on every push to `main`.

## How It Builds

1. GitHub Actions checks out the repo and installs `mkdocs`, `mkdocs-material`, and `pymdown-extensions`.
2. `mkdocs build --strict` builds the site from `mkdocs.yml`'s configuration.
3. `mkdocs gh-deploy --force` pushes the built site to the `gh-pages` branch, which GitHub Pages serves.

## The Phase 1 Bug This Phase Fixed

The original `mkdocs.yml` (Phase 1) never set `docs_dir`. MkDocs defaults `docs_dir` to a folder literally named `docs/` — but this repo's real content spans multiple top-level folders (`docs/`, `templates/`, `trackers/`, `prompts/`, `projects/`, `resources/`, plus root-level `README.md` and `AGENTS.md`). With the default, nav entries like `README.md` and `AGENTS.md` would have pointed at files outside `docs_dir` and failed to build. Phase 9 set `docs_dir: .` (repo root) to fix this — flagged here explicitly rather than silently, since it sat unnoticed for 8 phases.

## Nav Curation Policy

With 250+ Markdown files, the site's left-hand navigation is a **curated table of contents, not an exhaustive file list** — the same judgment call `docs/document-map.md` already made for diagramming:

- **Full nav detail:** Departments, Operating System, Engineering Standards, Career System — these are read-in-order documentation, so every document gets its own nav entry.
- **One nav entry per collection:** Templates (50 files), Trackers (14 files), Prompts (104 files) — each links only to its `README.md` index, which lists every file with a description. A nav entry per file would be noise for collections this size and this flat.
- **One nav entry per tier:** Projects — 3 tier entries plus the overview, not 25 individual project entries. `projects/README.md`'s full table is the real index.

Files not in the nav are **still built and still searchable** via the site's built-in search — they're reachable, just not in the sidebar.

## The One Manual Step Left

GitHub Actions can build and push to `gh-pages`, but **someone with repo admin access must enable GitHub Pages once**, pointing it at the `gh-pages` branch (or, if using the newer "Deploy from GitHub Actions" source type, at the Actions workflow itself). This repository was pushed to `github.com/AI-DSOS/AI-Data-Science-Operating-System` between Phases 1 and 2 — Pages deployment status as of this phase has **not been confirmed** (see `docs/progress/v1-scorecard.md`). Check under the repo's **Settings → Pages**.

## Local Preview

```bash
pip install mkdocs mkdocs-material pymdown-extensions
mkdocs serve
```

Then open `http://127.0.0.1:8000`.

## Next Steps

- Confirm GitHub Pages is enabled and the site is actually live — the last open item before the "Documentation site: Deployed" v1.0 target can be marked 100%.
- Revisit the nav curation policy once real usage shows whether search alone is sufficient for templates/trackers/prompts, or whether a few high-traffic files deserve promotion into the nav.
