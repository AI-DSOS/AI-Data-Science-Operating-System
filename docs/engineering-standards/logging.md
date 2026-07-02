---
title: Engineering Standard — Logging
purpose: Structured logging conventions for DSOS project code, so production issues are debuggable and monitoring dashboards have real signal to work with.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, docs/engineering-standards/mlops.md, docs/engineering-standards/fastapi.md]
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

Logging is what makes the Prometheus/Grafana monitoring layer (per `mlops.md`) actually useful — dashboards are only as good as the structured data feeding them.

## Standard

- **Structured logging:** JSON-formatted logs (via Python's `logging` + a JSON formatter, or `structlog`) — not free-text `print()` statements, ever, in production code.
- **Levels used correctly:** `DEBUG` for development detail, `INFO` for normal operational events (request received, model loaded), `WARNING` for recoverable issues (fallback used, retry triggered), `ERROR` for failures needing attention, `CRITICAL` reserved for failures that stop the service.
- **No secrets in logs:** never log API keys, tokens, PII, or full request/response bodies containing sensitive financial or customer data (directly relevant given the KYC/AML-adjacent domain context).
- **Correlation IDs:** every request gets a trace/correlation ID, logged on every related log line, so a single request's full path can be reconstructed from logs alone.
- **Log destination:** stdout/stderr in containers (12-factor style) — let the orchestration layer (Kubernetes, Docker) handle collection, don't write to local files inside a container.

## Examples

```python
import structlog

logger = structlog.get_logger()

logger.info("prediction_requested", correlation_id=request_id, model_version="1.2.0")
try:
    result = run_inference(payload)
except ModelNotLoadedError:
    logger.error("model_not_loaded", correlation_id=request_id)
    raise
```

## Checklist

- [ ] Structured (JSON) logging used, not `print()`
- [ ] Log levels used correctly
- [ ] No secrets or sensitive data in logs
- [ ] Correlation ID present and threaded through related log lines
- [ ] Logs go to stdout/stderr in containers

## References

- `docs/engineering-standards/mlops.md` — where these logs feed monitoring
- `docs/engineering-standards/security.md` — the no-secrets-in-logs rule as a security control

## Next Steps

- None currently.
