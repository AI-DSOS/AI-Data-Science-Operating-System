---
title: Career System — GitHub Strategy
purpose: The strategic approach behind GitHub presence, distinct from templates/github-strategy-template.md's fill-in structure.
owner: Arulkumaran
dependencies: [docs/career-system/README.md]
related_documents: [templates/github-strategy-template.md, docs/engineering-standards/documentation.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Pinned Repos Strategy](#pinned-repos-strategy)
- [README Standard](#readme-standard)
- [Contribution Consistency](#contribution-consistency)
- [What GitHub Signals to a Reviewer](#what-github-signals-to-a-reviewer)
- [Checklist](#checklist)
- [References](#references)
- [Next Steps](#next-steps)

## Overview

GitHub is where a technical reviewer actually checks claims made on a resume or LinkedIn — it needs to hold up to real scrutiny, not just look active.

## Pinned Repos Strategy

Pin the strongest 3–4 repos, prioritizing: (1) the `nhecf` regulatory reporting package (real, tested, production-quality), (2) whichever flagship project (Data Quality Monitoring or Defect Classification) is furthest along, (3) the multi-agent QA orchestrator, and (4) this DSOS repository itself, since it demonstrates systems thinking and documentation discipline that most portfolios lack entirely.

## README Standard

Every pinned repo's README must pass the check in `templates/github-strategy-template.md`: business problem clear in the first 3 lines, a results section with honest metrics, and run instructions that have actually been tested to work.

## Contribution Consistency

Commit cadence matters less than commit *substance* — a repo with occasional, meaningful commits reads better than one with padded daily commits. Don't game the contribution graph; let real work set the pace.

## What GitHub Signals to a Reviewer

A technical reviewer looks for: does the code match the claims, are there tests, is the README honest about limitations, does the commit history tell a coherent story. This is exactly what `docs/engineering-standards/` is designed to make true by default, not something to fake after the fact.

## Checklist

- [ ] Pinned repos are the strongest 3-4, not just the most recent
- [ ] Every pinned README passes the quality check
- [ ] No padded/gamed commit history
- [ ] Code matches claims made elsewhere (resume, LinkedIn)

## References

- `templates/github-strategy-template.md`
- `docs/engineering-standards/documentation.md`

## Next Steps

- Once Projects 21 and 22 are migrated into `projects/`, evaluate whether they should be split into standalone pinned repos or stay within the DSOS monorepo structure.
