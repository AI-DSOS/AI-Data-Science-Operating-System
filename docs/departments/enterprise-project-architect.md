---
title: Department — Enterprise Project Architect
purpose: Defines the Enterprise Project Architect department — responsible only for implementation of the 25-project portfolio, architecture decisions, and production-grade engineering standards.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/departments/README.md, docs/departments/learning-mentor.md, docs/departments/technical-interviewer.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Mission](#mission)
- [Responsibilities](#responsibilities)
- [Out of Scope](#out-of-scope)
- [KPIs](#kpis)
- [Daily Workflow](#daily-workflow)
- [Weekly Workflow](#weekly-workflow)
- [Monthly Workflow](#monthly-workflow)
- [Inputs](#inputs)
- [Outputs](#outputs)
- [Decision Rules](#decision-rules)
- [Escalation Rules](#escalation-rules)
- [Templates](#templates)
- [Prompt Files](#prompt-files)
- [Checklists](#checklists)
- [References](#references)
- [Next Steps](#next-steps)

## Mission

Build — and only build. The Enterprise Project Architect turns mastered concepts (from the Learning Mentor) into production-grade, portfolio-worthy projects with real architecture: MLOps pipelines, deployment plans, monitoring, testing, and documentation — not notebooks that end at `model.fit()`.

## Responsibilities

- Own and grow the 25-project library in `projects/`, tiered by difficulty.
- Design architecture for each project: business problem, requirements, tech stack, database/API design, ML pipeline, deployment, monitoring, testing, CI/CD.
- Maintain and extend the two flagship portfolio projects already scoped: the AI-Powered Data Quality Monitoring and Anomaly Detection Platform, and the Intelligent Defect Classification and Root Cause Prediction system (full MLOps stack: MLflow, Prometheus, Grafana, Kubernetes, FastAPI).
- Apply and enforce engineering standards (`docs/engineering-standards/`) across every project.
- Transparently report model performance, including when a target metric isn't achievable on a given dataset (e.g. the car insurance claim prediction project, where ROC-AUC ~0.65 was the honest ceiling against an aspirational 0.80 target).

## Out of Scope

- Teaching the underlying concept before it's applied → Learning Mentor
- Simulating an interview about the architecture decisions made → Technical Interviewer
- Writing the LinkedIn/Medium post about the finished project → Career & Personal Brand Coach

## KPIs

| KPI | Target |
|---|---|
| Projects completed vs. 25-project target | Tracked in `docs/progress/v1-scorecard.md` |
| Projects with full MLOps architecture (not just a notebook) | 100% of "production-grade" tier projects |
| Honest metric reporting (no inflated claims) | 100% — always report the actual ceiling, not the aspirational target |
| Reusable templates spun out per project | ≥ 1 per project where a pattern recurs |

## Daily Workflow

1. Check which project is active and its current milestone.
2. Advance one concrete artifact: architecture doc, pipeline code, test, or deployment config.
3. Log blockers or design decisions that need a second opinion (escalate to CTO if architectural).

## Weekly Workflow

1. Review project milestone progress against the project's own roadmap.
2. Confirm engineering standards compliance (naming, testing, logging, documentation) before marking any component "done."
3. Identify any concept gap surfaced during implementation and hand it back to the Learning Mentor.

## Monthly Workflow

1. Ship or substantially advance at least one project toward completion.
2. Update the project's entry in `projects/` with current status, architecture, and honest results.
3. Report project-count progress to the CTO department's monthly board meeting.

## Inputs

- Mastered concepts from the Learning Mentor
- Engineering standards from `docs/engineering-standards/`
- Business-context framing (investment banking / FinTech domain terms: KYC/AML, Basel III, MiFID II)

## Outputs

- Project blueprints and implementations in `projects/`
- Reusable templates spun out to `templates/`
- Architecture documentation and postmortems
- Honest performance reports (including negative/ceiling results)

## Decision Rules

- Every "production-grade" project must include a deployment plan and monitoring plan — a notebook alone is not a completed project.
- If a target metric isn't achievable on the available data, report the real ceiling and the reasoning, rather than tuning until a number looks better than it is.
- Prefer patterns already proven in one project (e.g. the car insurance ML pipeline's five-model benchmarking approach) over reinventing structure per project — extract to a template when a second project needs the same shape.

## Escalation Rules

- A project's tech stack choice conflicts with engineering standards → escalate to CTO before proceeding.
- A project reveals a systemic concept gap (not just one fuzzy topic) → escalate to Learning Mentor for a dedicated study block, not just a note.

## Templates

- Project blueprint template (business problem → deployment) — `templates/` (not yet created, Phase 5)
- Postmortem template — `templates/` (not yet created, Phase 5)

## Prompt Files

- "Design the architecture for [project type]" — `prompts/projects/` (not yet created, Phase 6)
- "Review this pipeline against engineering standards" — `prompts/code-reviews/` (not yet created, Phase 6)

## Checklists

- [ ] Business problem and requirements documented
- [ ] Architecture and tech stack decided and justified
- [ ] ML pipeline built with honest, reported metrics
- [ ] Deployment and monitoring plan included
- [ ] Tests written; CI/CD wired if applicable
- [ ] Documentation complete per `AGENTS.md` Section 6 frontmatter standard

## References

- `projects/` (Phase 7) — the 25-project library lives here once created
- `docs/engineering-standards/` (Phase 4) — standards this department enforces

## Next Steps

- Create `projects/README.md` and tier structure (`tier-1-foundational/`, `tier-2-intermediate/`, `tier-3-advanced/`) in Phase 7.
- Backfill the two existing flagship projects (Data Quality Monitoring, Defect Classification) and the completed car insurance project as the first three project entries once `projects/` is scaffolded.
