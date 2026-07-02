---
title: Engineering Standard — Git, GitHub & Code Review Workflow
purpose: Covers Git, GitHub, branch strategy, commit messages, and code review together as one connected workflow, for both project code and DSOS repository changes.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, AGENTS.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Branch Strategy](#branch-strategy)
- [Commit Messages](#commit-messages)
- [Code Review](#code-review)
- [GitHub Conventions](#github-conventions)
- [Checklist](#checklist)
- [References](#references)
- [Next Steps](#next-steps)

## Overview

Git, GitHub, branch strategy, commit messages, and code review are named separately in the original DSOS scope but function as one workflow in practice — this document covers all five together rather than splitting an artificial line between them.

## Branch Strategy

- **Trunk-based, lightweight:** `main` is always deployable/mergeable. Short-lived feature branches (`module/<slug>` for DSOS repo work per `AGENTS.md` Section 11, `feature/<slug>` or `fix/<slug>` for project code).
- **No long-lived parallel branches** — branches live days, not weeks. If a branch is stale beyond ~2 weeks, either merge it or delete it; don't let it silently rot.
- **Protected `main`:** for any project repo with more than one contributor (including AI-agent-assisted solo work where review discipline still matters), require at least a self-review checklist pass before merging.

## Commit Messages

- Format: `<scope>: <what changed>` — mirrors `AGENTS.md` Section 11's repo-level convention (`templates: add 5 project-tracker variants`), applied the same way inside project repos (`api: add rate limiting to prediction endpoint`).
- Imperative mood ("add," "fix," "refactor" — not "added," "fixes").
- Body (optional, for non-trivial changes): why, not just what — the diff already shows what.

## Code Review

- Even solo work gets a review pass — either a genuine second look after a break, or an explicit AI-agent review pass against the relevant engineering standard before merging.
- Review checks: does it meet the standard for its category (Python, SQL, etc.), is it tested, is it documented, does it introduce any of the anti-patterns named in `security.md`.
- Review comments are specific — point to the line and the standard being violated, not a vague "clean this up."

## GitHub Conventions

- Repository README present and current (per `AGENTS.md` Section 6-style structure, adapted for a project rather than the whole DSOS repo).
- Issues used for anything taking more than one sitting to resolve — even solo, this creates a paper trail.
- PRs (even self-merged) include a short description of what changed and why, mirroring the module-report discipline in `AGENTS.md` Section 5.

## Checklist

- [ ] Feature branch used, not direct commits to `main` for non-trivial changes
- [ ] Commit messages follow `<scope>: <what changed>` format, imperative mood
- [ ] A review pass happened (self or AI-agent) before merge
- [ ] PR/commit description explains why, not just what

## References

- `AGENTS.md` Section 11 — the repo-level commit/branch convention this standard extends to project code
- `docs/engineering-standards/security.md` — anti-patterns checked during review

## Next Steps

- Add a PR template to project repos once the first Phase 7 project is scaffolded, mirroring `.github/PULL_REQUEST_TEMPLATE.md` (still open at the DSOS repo level too, see `.github/README.md`).
