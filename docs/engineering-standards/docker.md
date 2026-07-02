---
title: Engineering Standard — Docker
purpose: Conventions for containerizing DSOS projects for deployment, matching the Kubernetes-based MLOps architecture already scoped for flagship projects.
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, docs/engineering-standards/mlops.md, docs/engineering-standards/security.md]
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

Docker is the packaging standard for any project deployed beyond a local script — every "production-grade" project in the 25-project target should have a working container, since Kubernetes deployment is already part of the flagship projects' scoped MLOps architecture.

## Standard

- **Base images:** official slim images (e.g. `python:3.12-slim`) — no unpinned `latest` tags in anything meant to run more than once.
- **Multi-stage builds:** separate build stage (installs deps, compiles if needed) from runtime stage, to keep final images small.
- **Non-root user:** containers run as a non-root user by default — never `root` in a production image.
- **`.dockerignore`:** always present, excludes `.git`, `notebooks/`, test fixtures, and anything not needed at runtime.
- **One process per container:** no supervisord-style multi-process containers unless there's a specific, documented reason.

## Examples

```dockerfile
FROM python:3.12-slim AS builder
WORKDIR /app
COPY pyproject.toml uv.lock ./
RUN pip install uv && uv sync --frozen --no-dev

FROM python:3.12-slim
WORKDIR /app
COPY --from=builder /app/.venv /app/.venv
COPY src/ ./src/
RUN useradd --create-home appuser
USER appuser
ENV PATH="/app/.venv/bin:$PATH"
CMD ["uvicorn", "src.main:app", "--host", "0.0.0.0", "--port", "8000"]
```

## Checklist

- [ ] Base image pinned, slim variant
- [ ] Multi-stage build used
- [ ] Runs as non-root
- [ ] `.dockerignore` present and correct
- [ ] Single process per container (or exception documented)

## References

- `docs/engineering-standards/mlops.md` — how containers fit into the broader deployment pipeline
- `docs/engineering-standards/security.md`

## Next Steps

- Add a Dockerfile template (FastAPI service variant, ML training-job variant) to `templates/` (Phase 5).
