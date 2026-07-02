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

The map now spans four modules (Foundation, Departments, Operating System, Engineering Standards) and exceeded the ~25-node single-graph threshold — split into per-module diagrams below, per the rule stated in "Reading the Map."

### Foundation

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
```

### Departments

```mermaid
graph TD
    DeptReadme[departments/README.md] --> LM[departments/learning-mentor.md]
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

### Operating System

```mermaid
graph TD
    OSReadme[operating-system/README.md] --> Daily[daily-operating-system.md]
    OSReadme --> WeeklyR[weekly-review.md]
    OSReadme --> MonthlyB[monthly-board-meeting.md]
    OSReadme --> QuarterlyR[quarterly-review.md]
    OSReadme --> AnnualR[annual-review.md]
    OSReadme --> Sprint[sprint-planning.md]
    OSReadme --> KM[knowledge-management.md]
    OSReadme --> TaskP[task-prioritization.md]
    OSReadme --> TimeB[time-blocking.md]
    OSReadme --> DeepW[deep-work.md]
    OSReadme --> RevS[revision-strategy.md]
    OSReadme --> Reflect[reflection-system.md]

    Daily --> WeeklyR --> MonthlyB --> QuarterlyR --> AnnualR
    TaskP --> TimeB --> Daily
    TimeB --> DeepW
    Daily --> Reflect --> RevS
```

*(The CTO department governs this whole module — see the cross-module link below.)*

### Engineering Standards

```mermaid
graph TD
    ESReadme[engineering-standards/README.md] --> Python[python.md]
    ESReadme --> SQL[sql.md]
    ESReadme --> Jupyter[jupyter.md]
    ESReadme --> FastAPI[fastapi.md]
    ESReadme --> Docker[docker.md]
    ESReadme --> ML[machine-learning.md]
    ESReadme --> MLOps[mlops.md]
    ESReadme --> GitGH[git-github-workflow.md]
    ESReadme --> Testing[testing.md]
    ESReadme --> Logging[logging.md]
    ESReadme --> Docs[documentation.md]
    ESReadme --> Naming[naming-conventions.md]
    ESReadme --> Folder[folder-structure.md]
    ESReadme --> Security[security.md]
    ESReadme --> Perf[performance-and-scalability.md]

    ML --> MLOps
    MLOps --> Docker --> FastAPI
    MLOps --> Logging
    Python --> Testing
    Python --> Naming
    Jupyter --> Python
    Folder --> Jupyter
    Folder --> Docker
    Security --> SQL
    Security --> FastAPI
    Security --> Docker
    Perf --> MLOps
    Perf --> Docker
```

### Cross-Module Links

```mermaid
graph LR
    CTO[departments/cto.md] -.governs.-> OS[operating-system/README.md]
    EPA[departments/enterprise-project-architect.md] -.enforces.-> ES[engineering-standards/README.md]
    LM2[departments/learning-mentor.md] -.depends on.-> LSystem[learning-system/ - not yet created]
```

## Reading the Map

- An arrow means "the source document links to / depends on the target."
- `AGENTS.md` is the root of the governance layer — nearly everything traces back to it, even where not drawn explicitly in every subgraph.
- Diagrams are split per module now that the repo exceeds ~25 nodes total. Each new module (Templates, Prompt Library, Project Library, Career System) gets its own diagram below rather than growing an existing one past readability.

## Next Steps

- Add a subgraph for `resources/` (glossary, abbreviation guide) once expanded.

- Add a diagram for `docs/learning-system/`, `docs/career-system/` once those are created (deferred — not part of the original 10-phase roadmap's explicit folder list, revisit if department docs' forward-references to them turn into real content).
- Add diagrams for Templates, Prompt Library, and Project Library as Phases 5–7 complete.
=======
- This map now has ~30 nodes — approaching the split threshold noted below. Revisit splitting into per-module diagrams once `docs/engineering-standards/` (Phase 4) adds another cluster.
- Revisit the "split into per-module diagrams" threshold (~25 nodes) once real project and prompt-library nodes are added (Phases 5–7).
