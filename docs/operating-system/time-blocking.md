---
title: Time Blocking
purpose: The concrete weekly time-block map — which evenings and Sunday segments are allocated to what, by default, before Task Prioritization exceptions are applied.
owner: Arulkumaran
dependencies: [AGENTS.md, docs/operating-system/task-prioritization.md]
related_documents: [docs/operating-system/README.md, docs/operating-system/daily-operating-system.md, docs/operating-system/deep-work.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Default Weekly Map](#default-weekly-map)
- [Block Definitions](#block-definitions)
- [Decision Rules](#decision-rules)
- [Checklist](#checklist)
- [References](#references)
- [Next Steps](#next-steps)

## Overview

`task-prioritization.md` decides *what* wins when time is scarce. This document defines the *default* weekly map before any scarcity or exception is applied — the baseline schedule to deviate from, not reinvent each week.

## Default Weekly Map

| Day | Block | Default allocation |
|---|---|---|
| Mon–Fri (daytime) | Work | Synechron QA automation (not DSOS) |
| Mon, Wed, Fri (evening) | Study | Bootcamp session (Learning Mentor) |
| Tue, Thu (evening) | Build | Portfolio project work (Enterprise Project Architect) or content (Career & Personal Brand Coach), alternating weekly |
| Sunday AM | Deep Dive 1 | Hardest bootcamp topic of the week |
| Sunday midday | Deep Dive 2 | Portfolio project implementation |
| Sunday PM (early) | Light session | Mock interview or content, whichever is due |
| Sunday PM (reserve) | Vaagai / buffer | Vaagai business development, or catch-up if the week slipped |

## Block Definitions

- **Study block:** single-topic, evening-length (~60–90 min), matches the bootcamp's existing "3 x 30-minute weekday slots" pattern where applicable.
- **Build block:** implementation or content work, evening-length, lower cognitive load than a Deep Dive.
- **Deep Dive block:** 2+ contiguous hours, reserved for work that doesn't survive interruption — see `deep-work.md`.
- **Reserve block:** the only block allowed to flex toward Vaagai, and only after the week's catch-up need (if any) is satisfied.

## Decision Rules

- The reserve block goes to catch-up first, Vaagai second — never the reverse, per `task-prioritization.md`'s default order.
- Don't reallocate a Study block to Build without checking the phase tracker first (per `docs/departments/learning-mentor.md`) — a fast week doesn't mean bootcamp time is free to give away.
- If the Tue/Thu alternation between project work and content work isn't happening in practice, surface it at the next Weekly Review rather than letting one silently win by default.

## Checklist

- [ ] Weekly map followed, or deviations logged as exceptions
- [ ] Sunday reserve block allocation checked against catch-up status before Vaagai
- [ ] Tue/Thu alternation (project vs. content) actually alternating

## References

- `docs/operating-system/task-prioritization.md` — the priority order this map defaults to
- `docs/operating-system/deep-work.md` — what makes Sunday blocks different from evening blocks

## Next Steps

- Once real weeks of data exist, revisit whether 2 evening Study blocks (Mon/Wed/Fri = 3) is the right ratio against Build blocks — check at the first Quarterly Review.
