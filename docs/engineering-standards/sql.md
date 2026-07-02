---
title: Engineering Standard — SQL
purpose: Baseline SQL conventions for queries, schema design, and migrations used across DSOS projects.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, docs/engineering-standards/naming-conventions.md]
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

SQL shows up in DSOS projects for feature stores, data quality checks, and application backends (e.g. the fraud/anomaly detection projects). Consistency here matters especially given the investment banking domain context, where query correctness has real audit implications.

## Standard

- **Keywords:** uppercase (`SELECT`, `FROM`, `WHERE`) — improves scanability against lowercase identifiers.
- **Naming:** `snake_case` for tables and columns; tables are plural nouns (`transactions`, not `transaction`); no reserved-word column names.
- **Formatting:** one clause per line for anything beyond a trivial single-table query; explicit `JOIN ... ON` (never implicit comma joins).
- **Migrations:** every schema change is a versioned migration file, never a manual `ALTER TABLE` run ad hoc against a live database.
- **Queries in application code:** parameterized always — no string-concatenated SQL, ever (this is also a Security standard, see `security.md`).

## Examples

```sql
SELECT
    t.transaction_id,
    t.amount,
    c.customer_name
FROM transactions AS t
JOIN customers AS c
    ON t.customer_id = c.customer_id
WHERE t.transaction_date >= '2026-01-01'
    AND t.flagged_fraud = TRUE;
```

## Checklist

- [ ] Uppercase keywords, `snake_case` identifiers
- [ ] Explicit `JOIN ... ON`, no comma joins
- [ ] Schema changes go through versioned migrations
- [ ] Application queries are parameterized, not string-concatenated

## References

- `docs/engineering-standards/security.md` — parameterized queries as an injection-prevention control
- `docs/engineering-standards/naming-conventions.md`

## Next Steps

- Pick a migration tool standard (e.g. Alembic for Python projects) once the first project needing schema migrations starts (Phase 7).
