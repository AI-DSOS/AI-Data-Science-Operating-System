---
title: Engineering Standard — Naming Conventions (Code-Level)
purpose: Naming conventions for code identifiers, files, and project artifacts — distinct from repository-file naming, which is governed by AGENTS.md Section 8.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, docs/engineering-standards/python.md, docs/engineering-standards/sql.md]
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

`AGENTS.md` Section 8 governs how files are named across the DSOS repository (`kebab-case.md`, project folder patterns, etc.). This document governs naming *inside* code and project artifacts — variables, functions, classes, database objects, model versions.

## Standard

- **Python:** `snake_case` for variables/functions/modules, `PascalCase` for classes, `UPPER_SNAKE_CASE` for constants. No single-letter variable names except conventional loop counters (`i`, `j`) or well-known math notation (`x`, `y` in a clearly mathematical context).
- **SQL:** covered in `sql.md` — `snake_case`, plural table names.
- **Model artifacts:** `<project_slug>_<model_type>_v<version>` (e.g. `fraud_detection_xgboost_v3`), registered under that name in the MLflow model registry.
- **Environment variables:** `UPPER_SNAKE_CASE`, prefixed by project (e.g. `FRAUDDETECT_DB_URL`) to avoid collisions when multiple project services run on the same host.
- **Booleans:** prefixed `is_`, `has_`, `should_` (`is_flagged_fraud`, not `flagged_fraud`) — makes intent unambiguous at the call site.
- **No abbreviations that aren't domain-standard:** `roc_auc` is fine (domain-standard), `calc_amt` is not (write `calculate_amount`).

## Examples

```python
MAX_RETRY_ATTEMPTS = 3

class FraudRiskScorer:
    def __init__(self, model_version: str) -> None:
        self.model_version = model_version

    def is_high_risk(self, transaction_amount: float) -> bool:
        return transaction_amount > self._risk_threshold
```

## Checklist

- [ ] Python identifiers follow `snake_case`/`PascalCase`/`UPPER_SNAKE_CASE` correctly
- [ ] Model artifacts named `<project_slug>_<model_type>_v<version>`
- [ ] Environment variables prefixed by project
- [ ] Booleans prefixed `is_`/`has_`/`should_`
- [ ] No non-standard abbreviations

## References

- `AGENTS.md` Section 8 — repository-file naming (a different scope)
- `docs/engineering-standards/sql.md` — SQL-specific naming rules

## Next Steps

- None currently.
