---
title: Engineering Standard — Documentation (Code-Level)
purpose: Documentation expectations inside project code and project repos — distinct from the repository-level Markdown documentation standard in AGENTS.md Section 6.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, docs/engineering-standards/python.md]
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

`AGENTS.md` Section 6 governs Markdown documents in the DSOS repository itself (department specs, operating-system docs, etc.). This standard governs documentation *inside project code* — docstrings, project READMEs, architecture decision records — a different scope with different conventions.

## Standard

- **Docstrings:** required on every public function/class in production code (Google-style, per `python.md`). Not required on private helpers unless the logic is non-obvious.
- **Project README:** every project in `projects/` has its own README covering: business problem, architecture summary, how to run it locally, how to run tests, deployment notes. This is separate from and more detailed than its one-line entry in `docs/master-index.md` / the project library index.
- **Architecture Decision Records (ADRs):** any non-obvious architecture choice (why this database, why this model family, why this deployment pattern) gets a short ADR — a few paragraphs, not a full document — stored in the project's `docs/adr/` folder.
- **Comments:** explain *why*, not *what* — code should be readable enough that *what* is obvious; comments earn their place by explaining a non-obvious reason.
- **No stale documentation:** if a docstring or README section no longer matches the code, fixing it is part of the same change that changed the code — not a follow-up ticket.

## Examples

```markdown
# ADR 003: Use Isolation Forest for anomaly detection baseline

## Context
Need an unsupervised baseline for the Data Quality Monitoring platform before
labeled anomaly data exists.

## Decision
Isolation Forest, over One-Class SVM or Autoencoder, for interpretability and
training speed on the initial dataset size (~500K rows).

## Consequences
Revisit once labeled data exists — a supervised model will likely outperform
this baseline, but it establishes a monitoring floor immediately.
```

## Checklist

- [ ] Public functions/classes have docstrings
- [ ] Project README covers problem, architecture, run/test/deploy instructions
- [ ] Non-obvious architecture decisions have an ADR
- [ ] Comments explain why, not what
- [ ] Documentation updated in the same change as the code it describes

## References

- `AGENTS.md` Section 6 — the repository-level Markdown standard this document complements
- `docs/engineering-standards/python.md` — docstring format

## Next Steps

- Add a project README template and ADR template to `templates/` (Phase 5).
