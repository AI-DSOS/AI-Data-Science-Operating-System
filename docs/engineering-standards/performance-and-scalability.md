---
title: Engineering Standard — Performance & Scalability
purpose: Baseline expectations for how DSOS projects handle load and scale, covered together since scalability is largely performance considered at a larger input size.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, docs/engineering-standards/mlops.md, docs/engineering-standards/docker.md]
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

Performance and Scalability are named separately in the original DSOS scope but are treated together here: scalability is what happens to performance characteristics as load or data size grows, so the same document covers both rather than artificially separating them.

## Standard

- **Measure before optimizing:** no performance work without a baseline measurement first (profiling, load testing) — optimizing a guess wastes time and often optimizes the wrong thing.
- **Data pipeline scaling:** pipelines built against realistic data volume assumptions stated explicitly in the project README (e.g. "designed for up to 1M rows in-memory; beyond that, requires a chunked/streaming approach") — don't silently assume infinite scale or silently cap it without saying so.
- **API performance:** FastAPI services report p50/p95/p99 latency in their monitoring dashboard (`mlops.md`); a documented target (e.g. "p95 < 200ms for single predictions") is set per project, not left implicit.
- **Horizontal scaling readiness:** stateless service design by default (no in-memory session state) so a service can scale horizontally in Kubernetes without code changes — statefulness, if needed, is explicit and documented.
- **Batch vs. real-time:** the project explicitly states whether it's designed for batch scoring, real-time inference, or both — this decision drives most of the architecture and shouldn't be left ambiguous.

## Examples

```markdown
## Performance Targets (from project README)
- Single prediction: p95 latency < 200ms
- Batch scoring: 100K rows in under 5 minutes
- Designed for: real-time inference primary, nightly batch reconciliation secondary
```

## Checklist

- [ ] Baseline measurement taken before any optimization work
- [ ] Data volume assumptions stated explicitly in the project README
- [ ] Latency targets documented and measured in monitoring
- [ ] Services designed stateless unless statefulness is explicit and justified
- [ ] Batch vs. real-time design decision stated explicitly

## References

- `docs/engineering-standards/mlops.md` — where latency/throughput get monitored
- `docs/engineering-standards/docker.md` — the container layer this scales at

## Next Steps

- None currently — revisit once the first Phase 7 project has real load data to check these targets against.
