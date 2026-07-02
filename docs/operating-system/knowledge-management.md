---
title: Knowledge Management (Process)
purpose: The process rules for keeping DSOS's knowledge artifacts (master index, document map, glossary, changelog) accurate over time — the "how we keep this honest" layer, as opposed to the artifacts themselves.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/operating-system/README.md, docs/master-index.md, docs/document-map.md, resources/glossary.md, docs/CHANGELOG.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [The Artifacts This Process Governs](#the-artifacts-this-process-governs)
- [When Each Artifact Gets Updated](#when-each-artifact-gets-updated)
- [Decay Prevention](#decay-prevention)
- [Decision Rules](#decision-rules)
- [Checklist](#checklist)
- [References](#references)
- [Next Steps](#next-steps)

## Overview

`docs/master-index.md`, `docs/document-map.md`, `resources/glossary.md`, and `docs/CHANGELOG.md` are only useful if they're accurate. This document is the process — not the artifact — for keeping them that way. A knowledge base that's 80% accurate is often worse than no knowledge base, because it's trusted at 100%.

## The Artifacts This Process Governs

| Artifact | Risk if it decays |
|---|---|
| `docs/master-index.md` | Duplicate documents get written because the existing one wasn't found |
| `docs/document-map.md` | Relationships between documents become invisible; orphans go unnoticed |
| `resources/glossary.md` | Terms get redefined inconsistently across documents |
| `docs/CHANGELOG.md` | No audit trail of why the repo looks the way it does |

## When Each Artifact Gets Updated

- **Master index:** same change that adds/moves/deletes any document (per `AGENTS.md` Section 5, rule 6, and `docs/master-index.md`'s own "How to Use" section).
- **Document map:** same module that introduces a new cluster of related documents (e.g. a new department, a new project). Trivial single-document additions can wait for the next map review rather than triggering a Mermaid edit every time.
- **Glossary:** same module that first uses a term more than once.
- **Changelog:** end of every module, one entry, per `AGENTS.md` Section 5.

## Decay Prevention

- The Weekly Review doesn't check these artifacts (too frequent for the drift rate). The **Monthly Board Meeting's scorecard reconciliation** is the backstop — if index/map/glossary drift is caught there, it's fixed immediately, not queued.
- Any agent starting a new module does a quick master-index search before writing — this is the cheapest decay-prevention step and is mandatory per `AGENTS.md` Section 5, rule 3.

## Decision Rules

- If updating an artifact would take longer than the module itself, that's a signal the artifact's structure needs to change (e.g. splitting the glossary, restructuring the map into subgraphs) — raise at the next Monthly Board Meeting rather than skipping the update.
- Never batch multiple modules' worth of index/changelog updates into one catch-up edit — this defeats the purpose of per-module tracking and makes the changelog's dates meaningless.

## Checklist

- [ ] Master index updated in the same change as any document add/move/delete
- [ ] Glossary checked/updated for any term used more than once
- [ ] Changelog entry added at module end
- [ ] Document map updated if a new cluster of related documents was introduced

## References

- `docs/master-index.md`, `docs/document-map.md`, `resources/glossary.md`, `docs/CHANGELOG.md` — the artifacts this process governs
- `AGENTS.md` Section 9 (Knowledge Management requirements)

## Next Steps

- Revisit the glossary-split threshold (~30 entries) and document-map subgraph threshold (~25 nodes) at the first Quarterly Review, once real usage data exists.
