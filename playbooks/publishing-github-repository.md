---
title: Playbook — Publishing a GitHub Repository
purpose: The exact steps to follow before pinning or sharing a project's GitHub repository.
owner: Arulkumaran
dependencies: [docs/career-system/github-strategy.md]
related_documents: [playbooks/README.md, docs/engineering-standards/documentation.md]
version: 1.0.0
last_updated: 2026-07-03
---

## When to Use
A project is ready to be pinned, shared with a recruiter, or linked from the resume/LinkedIn.

## Steps

1. Run the README quality check from `templates/github-strategy-template.md` — business problem in first 3 lines, honest results section, tested run instructions.
2. Actually run the README's setup instructions from a clean checkout — don't assume they work.
3. Confirm no secrets or credentials are anywhere in the commit history (`docs/engineering-standards/security.md`) — check history, not just the current state.
4. Confirm the license file exists and is appropriate.
5. Confirm tests pass in CI, not just locally.
6. Write or update the repo description (GitHub's short one-liner, separate from the README).
7. Add topics/tags for discoverability if relevant.
8. Only then: pin it, and update `docs/career-system/portfolio-strategy.md`'s anchor-projects list if this becomes one of the 2-3 anchors.

## Common Pitfalls

- Pinning a repo whose README setup instructions don't actually work — this is the fastest way to lose credibility with a technical reviewer.
- Secrets in old commits even if removed from the current file — history matters.

## Checklist

- [ ] README passes the quality check
- [ ] Setup instructions tested from a clean checkout
- [ ] No secrets anywhere in history
- [ ] License present
- [ ] CI passing
- [ ] Repo description written

## References

- `docs/career-system/github-strategy.md`
- `docs/engineering-standards/security.md`, `documentation.md`
