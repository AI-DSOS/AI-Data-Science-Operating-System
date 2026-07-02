---
title: Prompt — Slow SQL Query
purpose: Diagnose and improve a slow query.
---

## Prompt
```
This query is slow: {paste query + rough table sizes}. What's likely
causing it, and how would you fix it without violating
docs/engineering-standards/sql.md?
```

## Use When
A query exceeds an acceptable latency for its use case.
