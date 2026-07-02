---
title: Engineering Standard — Folder Structure (Project-Level)
purpose: The standard folder layout every project in projects/ follows — distinct from the repository-level structure governed by AGENTS.md Section 3.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, docs/engineering-standards/python.md, docs/engineering-standards/jupyter.md, docs/engineering-standards/docker.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Standard](#standard)
- [Examples](#examples)
- [Checklist](#checklist)
- [References](#references)
- [Next Steps](#next-steps)

## Overview

`AGENTS.md` Section 3 lays out the DSOS repository's own top-level structure. This document lays out the structure *inside each project* under `projects/<tier>/<NN>-project-slug/`, so all 25 projects are navigable the same way regardless of who (or which agent) built them.

## Standard

```
<NN>-project-slug/
├── README.md               # business problem, architecture, run/test/deploy (docs.md standard)
├── pyproject.toml
├── docs/
│   └── adr/                 # architecture decision records
├── notebooks/                # EDA, benchmarking (jupyter.md standard)
├── src/
│   └── <project_slug>/
│       ├── training/
│       ├── serving/
│       └── monitoring/
├── tests/
├── k8s/                       # if deployed
├── Dockerfile
└── .dockerignore
```

- Every project has this shape at minimum; a project too simple to need `k8s/` or `monitoring/` omits those folders rather than leaving them empty.
- No project-specific deviation from this layout without a documented reason in that project's README.

## Examples

See the layout above — it's intentionally the same shape as the examples already given in `jupyter.md`, `docker.md`, and `mlops.md`, so this document is the single place that shows the full picture assembled together.

## Checklist

- [ ] Project matches the standard layout, or deviation is documented
- [ ] Empty/unneeded folders omitted rather than left as placeholders
- [ ] `README.md` present at project root per `documentation.md`

## References

- `AGENTS.md` Section 3 — repository-level structure (different scope)
- `docs/engineering-standards/jupyter.md`, `docker.md`, `mlops.md` — the standards this layout accommodates

## Next Steps

- Scaffold this structure as a copyable template in `templates/` (Phase 5) so every new project in Phase 7 starts from it directly.
