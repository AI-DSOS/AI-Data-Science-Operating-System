---
title: Playbook — Debugging Production Issues
purpose: The exact steps to follow when a deployed project misbehaves.
owner: Arulkumaran
dependencies: [docs/engineering-standards/logging.md]
related_documents: [playbooks/README.md, prompts/debugging/root-cause-first.md]
version: 1.0.0
last_updated: 2026-07-03
---

## When to Use
A deployed project (per `docs/engineering-standards/mlops.md`) throws errors, degrades in performance, or produces suspect output.

## Steps

1. Check the monitoring dashboard first (`docs/engineering-standards/mlops.md`'s minimum dashboard: latency, volume, error rate) — don't start reading code before checking whether the metrics tell the story already.
2. Pull the relevant structured logs, using the correlation ID if the issue traces to a specific request (per `docs/engineering-standards/logging.md`).
3. Use `prompts/debugging/root-cause-first.md` — get the actual cause explained before any fix is proposed.
4. Reproduce locally if at all possible before patching in place.
5. Write a regression test that fails against the bug, before writing the fix (per `docs/engineering-standards/testing.md`).
6. Fix the minimal cause, not a broader refactor — file a separate follow-up if a bigger issue is uncovered.
7. Deploy the fix per the project's `templates/deployment-template.md` rollback plan being ready, not assumed.
8. Write a postmortem using `templates/postmortem-template.md` if the issue reached production impact, not just a caught bug.

## Common Pitfalls

- Patching the symptom (e.g. adding a try/except) without understanding why it happened.
- Skipping the regression test because the fix "obviously" works.

## Checklist

- [ ] Monitoring checked before code
- [ ] Root cause understood, not guessed
- [ ] Reproduced locally
- [ ] Regression test written before the fix
- [ ] Postmortem written if production-impacting

## References

- `docs/engineering-standards/logging.md`, `mlops.md`, `testing.md`
