---
title: templates/ — Reusable Templates
purpose: Index of the 50 reusable Markdown templates DSOS ships with, organized by the system each supports.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/master-index.md, docs/engineering-standards/README.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Project Blueprint Templates (15)](#project-blueprint-templates-15)
- [Learning System Templates (5)](#learning-system-templates-5)
- [Interview / Assessment Templates (4)](#interview--assessment-templates-4)
- [Career System Templates (8)](#career-system-templates-8)
- [Operating System / Review Templates (5)](#operating-system--review-templates-5)
- [Engineering / Code Templates (8)](#engineering--code-templates-8)
- [Governance Templates (5)](#governance-templates-5)
- [How to Use a Template](#how-to-use-a-template)
- [Next Steps](#next-steps)

## Overview

These 50 files satisfy the v1.0 "reusable templates" target. Each is compact by design — meant to be copied into a working document and filled in, not read as documentation. Every template still declares `title`, `purpose`, and `related_documents` per `AGENTS.md` Section 6, with other frontmatter fields compressed since templates are copied repeatedly.

## Project Blueprint Templates (15)

Match the "every project must include" list from the original DSOS scope: `business-problem-template.md`, `requirements-template.md`, `architecture-template.md`, `tech-stack-template.md`, `database-design-template.md`, `api-design-template.md`, `ml-pipeline-template.md`, `deployment-template.md`, `monitoring-template.md`, `testing-plan-template.md`, `cicd-template.md`, `project-readme-template.md`, `production-checklist-template.md`, `postmortem-template.md`, `project-folder-structure-template.md`.

## Learning System Templates (5)

`learning-journal-entry-template.md`, `mastery-rubric-template.md`, `concept-map-template.md`, `weekly-learning-plan-template.md`, `revision-quiz-template.md`.

## Interview / Assessment Templates (4)

`mock-interview-session-template.md`, `readiness-scoring-rubric-template.md`, `assessment-rubric-template.md`, `interview-question-template.md`.

## Career System Templates (8)

Match the original CAREER SYSTEM list: `resume-template.md`, `linkedin-post-template.md`, `github-strategy-template.md`, `portfolio-strategy-template.md`, `networking-plan-template.md`, `conference-preparation-template.md`, `technical-writing-guide-template.md`, `case-study-template.md`.

## Operating System / Review Templates (5)

`weekly-review-template.md`, `monthly-board-meeting-template.md`, `quarterly-review-template.md`, `annual-review-template.md`, `sprint-definition-template.md`.

## Engineering / Code Templates (8)

`pyproject-toml-template.md`, `dockerfile-fastapi-template.md`, `dockerfile-ml-training-template.md`, `fastapi-service-scaffold-template.md`, `adr-template.md`, `model-evaluation-report-template.md`, `code-review-checklist-template.md`, `ci-workflow-template.md`.

## Governance Templates (5)

`pr-description-template.md`, `issue-template.md`, `changelog-entry-template.md`, `glossary-entry-template.md`, `onboarding-template.md`.

## How to Use a Template

Copy the file into its real destination (e.g. a project blueprint template into `projects/<tier>/<NN>-slug/docs/`), fill in the bracketed placeholders, and delete the template's own frontmatter `related_documents` line if the copy needs its own (real) related-documents list instead.

## Next Steps

- Wire each project blueprint template into the first real project once `projects/` is scaffolded (Phase 7).
- Revisit whether 50 is still the right number once real usage surfaces gaps or redundant templates — raise at Quarterly Review.
