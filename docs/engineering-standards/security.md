---
title: Engineering Standard — Security
purpose: Baseline security practices for DSOS project code, weighted toward the investment banking / FinTech domain context (KYC/AML, sensitive financial data).
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, docs/engineering-standards/sql.md, docs/engineering-standards/logging.md, docs/engineering-standards/docker.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Table of Contents

- [Overview](#overview)
- [Standard](#standard)
- [Examples](#examples)
- [Checklist](#checklist)
- [References](#references)
- [Next Steps](#next-steps)

## Overview

Portfolio projects targeting investment banking and FinTech roles are judged partly on whether the candidate thinks about security by default, not as an afterthought — this standard makes that visible in every project rather than assuming it.

## Standard

- **Secrets management:** no secrets (API keys, DB credentials, model registry tokens) in code or version control, ever — environment variables or a secrets manager only. `.env` files are gitignored, with a `.env.example` committed instead.
- **Input validation:** every external input (API request, uploaded file, query parameter) is validated before use — this is also enforced structurally via FastAPI's Pydantic schemas (`fastapi.md`) and SQL parameterization (`sql.md`).
- **Dependency scanning:** run a vulnerability scan (`pip-audit` or equivalent) as part of CI for any production-grade project.
- **Least privilege:** database users, service accounts, and container users (per `docker.md`) all run with the minimum permissions needed — no service connects as a database admin when it only needs read access to one table.
- **PII/financial data handling:** any project touching data resembling customer, transaction, or KYC/AML-adjacent information treats it as sensitive by default — anonymized/synthetic data used for portfolio projects unless there's a specific, documented reason and consent for real data.
- **No security-through-obscurity claims:** if a project's README discusses security, it describes actual controls (auth, validation, least privilege), not "we didn't publish the endpoint."

## Examples

```python
# .env.example (committed)
DATABASE_URL=postgresql://user:password@localhost:5432/dbname
MODEL_REGISTRY_TOKEN=your-token-here

# .env (gitignored, real values)
```

## Checklist

- [ ] No secrets in code or version control; `.env.example` committed, `.env` gitignored
- [ ] All external input validated (schema-enforced where possible)
- [ ] Dependency vulnerability scan in CI
- [ ] Least-privilege access for DB users, service accounts, container users
- [ ] Sensitive-data-resembling fields use synthetic/anonymized data by default

## References

- `docs/engineering-standards/sql.md` — parameterized queries
- `docs/engineering-standards/fastapi.md` — Pydantic validation
- `docs/engineering-standards/docker.md` — non-root containers
- `resources/glossary.md` — KYC/AML definition

## Next Steps

- Add `.env.example` and CI vulnerability-scan step to the project scaffold template in `templates/` (Phase 5).
