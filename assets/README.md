---
title: assets/ — Diagrams and Exported Artifacts
purpose: Home for binary/exported assets that don't belong inline in Markdown — exported diagram images, screenshots, and other non-text artifacts referenced by documentation.
owner: Arulkumaran
dependencies: []
related_documents: [docs/master-index.md, docs/document-map.md]
version: 1.0.0
last_updated: 2026-07-03
---

## Table of Contents

- [Overview](#overview)
- [Why This Folder Is Empty](#why-this-folder-is-empty)
- [What Belongs Here vs. Inline Mermaid](#what-belongs-here-vs-inline-mermaid)
- [Naming Convention](#naming-convention)
- [Next Steps](#next-steps)

## Overview

`assets/` exists for binary and exported files — PNG/SVG exports, screenshots, presentation-ready diagram exports — that shouldn't live inline in a Markdown file's source.

## Why This Folder Is Empty

Every diagram in DSOS so far (department interaction maps, the document map, project dependency graphs) is a Mermaid code block living directly inside its Markdown file — this is deliberate, since Mermaid renders natively in both GitHub and the MkDocs site (`docs/documentation-site.md`) without needing a separate exported image, and keeps the diagram's source next to the document it illustrates rather than in a disconnected binary file. As a result, nothing has needed `assets/` yet. This folder is scaffolded and ready, not populated with placeholder content that doesn't exist.

## What Belongs Here vs. Inline Mermaid

| Use inline Mermaid (in the `.md` file itself) | Use `assets/` |
|---|---|
| Any diagram whose source should stay next to its document | A screenshot of a real UI, dashboard, or external tool |
| Anything that benefits from being version-controlled as readable text | A diagram too complex for Mermaid's layout engine to render well |
| The default choice for any new diagram in this repo | Presentation-ready exports needed outside the repo (e.g. for a resume, LinkedIn post, or slide deck) |

## Naming Convention

- `assets/diagrams/<topic>-<description>.svg` or `.png`
- `assets/screenshots/<project-slug>-<description>.png`
- `assets/exports/<purpose>-<description>.<ext>` (e.g. a portfolio-strategy diagram exported for a LinkedIn post)

Subfolders are created on first real use, matching the pattern established in `journal/README.md`.

## Next Steps

- The first realistic candidate for this folder: a dashboard screenshot from one of the MLOps flagship projects (Projects 18–19), once their monitoring dashboards exist and are worth screenshotting for a case study or LinkedIn post.
