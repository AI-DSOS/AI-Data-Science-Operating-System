---
title: DSOS Document Map
purpose: Mermaid graph of how documents in the repository relate to and depend on each other — a visual companion to the flat master index.
owner: Arulkumaran
dependencies: [docs/master-index.md]
related_documents: [AGENTS.md, docs/master-index.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Current Map](#current-map)
- [Reading the Map](#reading-the-map)
- [Next Steps](#next-steps)

## Overview

`docs/master-index.md` is the flat, complete list of every document. This file is the visual, relationship-focused companion — useful once the repo has enough documents that "how does X connect to Y" stops being obvious from the index alone. Below ~10 documents this map is close to trivial; it's kept from day one so the habit of updating it is established early.

## Current Map

```mermaid
graph TD
    AGENTS[AGENTS.md] --> README[README.md]
    AGENTS --> DocsReadme[docs/README.md]
    AGENTS --> MasterIndex[docs/master-index.md]
    AGENTS --> Scorecard[docs/progress/v1-scorecard.md]

    DocsReadme --> ProgressReadme[docs/progress/README.md]
    DocsReadme --> DocMap[docs/document-map.md]
    DocsReadme --> Changelog[docs/CHANGELOG.md]

    ProgressReadme --> Scorecard

    MasterIndex --> DocMap
    MasterIndex --> Scorecard
    MasterIndex --> Changelog

    README --> MasterIndex
    README --> Scorecard

    DocsReadme --> DeptReadme[docs/departments/README.md]
    DeptReadme --> LM[departments/learning-mentor.md]
    DeptReadme --> EPA[departments/enterprise-project-architect.md]
    DeptReadme --> TI[departments/technical-interviewer.md]
    DeptReadme --> CBC[departments/career-brand-coach.md]
    DeptReadme --> CTO[departments/cto.md]
    CTO -.governs.-> LM
    CTO -.governs.-> EPA
    CTO -.governs.-> TI
    CTO -.governs.-> CBC

    DocsReadme --> OSReadme[docs/operating-system/README.md]
    OSReadme --> Daily[operating-system/daily-operating-system.md]
    OSReadme --> WeeklyR[operating-system/weekly-review.md]
    OSReadme --> MonthlyB[operating-system/monthly-board-meeting.md]
    OSReadme --> QuarterlyR[operating-system/quarterly-review.md]
    OSReadme --> AnnualR[operating-system/annual-review.md]
    OSReadme --> Sprint[operating-system/sprint-planning.md]
    OSReadme --> KM[operating-system/knowledge-management.md]
    OSReadme --> TaskP[operating-system/task-prioritization.md]
    OSReadme --> TimeB[operating-system/time-blocking.md]
    OSReadme --> DeepW[operating-system/deep-work.md]
    OSReadme --> RevS[operating-system/revision-strategy.md]
    OSReadme --> Reflect[operating-system/reflection-system.md]

    Daily --> WeeklyR --> MonthlyB --> QuarterlyR --> AnnualR
    TaskP --> TimeB --> Daily
    TimeB --> DeepW
    Daily --> Reflect --> RevS
    CTO -.governs.-> OSReadme
```

## Reading the Map

- An arrow means "the source document links to / depends on the target."
- `AGENTS.md` is the root of the governance layer — nearly everything traces back to it.
- As `docs/departments/`, `docs/engineering-standards/`, etc. come online in later phases, they'll attach here as new subgraphs rather than flattening into one diagram — split into per-module Mermaid blocks if the single graph gets hard to read (rough threshold: ~25 nodes).

## Next Steps

- Add a subgraph for `resources/` (glossary, abbreviation guide) once expanded.
- This map now has ~30 nodes — approaching the split threshold noted below. Revisit splitting into per-module diagrams once `docs/engineering-standards/` (Phase 4) adds another cluster.
- Revisit the "split into per-module diagrams" threshold (~25 nodes) once real project and prompt-library nodes are added (Phases 5–7).
