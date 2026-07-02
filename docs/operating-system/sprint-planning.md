---
title: Sprint Planning
purpose: How a DSOS "module" (per AGENTS.md) or a bootcamp phase gets planned into concrete, time-boxed work before it starts.
owner: Arulkumaran
dependencies: [AGENTS.md, docs/departments/cto.md, docs/departments/enterprise-project-architect.md]
related_documents: [docs/operating-system/README.md, docs/operating-system/task-prioritization.md, docs/operating-system/time-blocking.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [What Counts as a Sprint Here](#what-counts-as-a-sprint-here)
- [Planning Steps](#planning-steps)
- [Inputs](#inputs)
- [Outputs](#outputs)
- [Decision Rules](#decision-rules)
- [Checklist](#checklist)
- [References](#references)
- [Next Steps](#next-steps)

## Overview

DSOS doesn't run two-week sprints in the classic engineering-team sense — the available time (weekday evenings, Sundays) is the real constraint, not story points. "Sprint Planning" here means: before starting a module (per `AGENTS.md` Section 5) or a bootcamp phase, define what "done" looks like and how many evening/Sunday sessions it will realistically take.

## What Counts as a Sprint Here

- One DSOS repository module (e.g. "Phase 4: Engineering Standards")
- One bootcamp phase (per the 62-day, six-phase plan)
- One portfolio project milestone (e.g. "ship the MLOps monitoring layer for the Data Quality Platform")

## Planning Steps

1. **Define done:** what specific files/artifacts/scores mark this sprint complete (not vague — "Phase 4 done" means every named engineering standard doc exists and passes the quality gates).
2. **Estimate sessions:** how many evening sessions + Sunday blocks this realistically takes, based on similar past work (e.g. Phase 1 took roughly 2 modules; Phase 2 took 1).
3. **Check for conflicts:** does this sprint compete with an active bootcamp phase or Vaagai commitment for the same time blocks? Resolve via `time-blocking.md` before starting, not mid-sprint.
4. **Assign to the daily/weekly cadence:** slot the sessions into the coming week(s) via `docs/operating-system/daily-operating-system.md`.

## Inputs

- The current roadmap phase (`AGENTS.md` Section 10) or bootcamp phase
- Time availability from `time-blocking.md`
- Prior sprint actuals (how long similar work actually took)

## Outputs

- A short sprint definition: scope, done-criteria, session estimate
- Updated weekly time allocation

## Decision Rules

- Never start a module without a done-criteria — "work on Phase 4 for a while" is not a sprint, it's drift.
- If a sprint's session estimate exceeds the time available before the next Weekly Review, break it into two sprints rather than letting it run open-ended.
- Bootcamp-phase sprints always get first claim on weekday evenings; DSOS-module and project sprints compete for remaining evening time and Sunday blocks.

## Checklist

- [ ] Done-criteria defined concretely, not vaguely
- [ ] Session estimate made based on past actuals where available
- [ ] Time-block conflicts checked and resolved before starting
- [ ] Sessions slotted into the daily/weekly cadence

## References

- `AGENTS.md` Section 5 (module discipline) and Section 10 (roadmap phases)
- `docs/operating-system/time-blocking.md`

## Next Steps

- Create a sprint definition template in `templates/` (Phase 5).
