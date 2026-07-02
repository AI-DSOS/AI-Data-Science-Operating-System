---
title: Engineering Standard — FastAPI
purpose: Conventions for FastAPI services used to serve models or expose project APIs (e.g. the Data Quality Monitoring platform).
owner: Arulkumaran
dependencies: [AGENTS.md]
related_documents: [docs/engineering-standards/README.md, docs/engineering-standards/python.md, docs/engineering-standards/logging.md, docs/engineering-standards/security.md]
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

FastAPI is the standard framework for serving models and exposing APIs across DSOS projects — already named as part of the MLOps stack for the Data Quality Monitoring and Defect Classification platforms.

## Standard

- **Structure:** `main.py` for app creation only; routes in `routers/`, business logic in `services/`, data models in `schemas/` (Pydantic) — routes should not contain business logic directly.
- **Validation:** every request/response uses a Pydantic schema — no raw `dict` payloads in production endpoints.
- **Versioning:** API routes are versioned from the start (`/api/v1/...`), even for a single-consumer internal service.
- **Health checks:** every service exposes `/health` (liveness) at minimum; `/ready` if it has external dependencies (DB, model registry).
- **Errors:** use FastAPI's `HTTPException` with meaningful status codes and messages; never leak stack traces in production responses.

## Examples

```python
from fastapi import APIRouter, HTTPException
from .schemas import PredictionRequest, PredictionResponse

router = APIRouter(prefix="/api/v1/predictions", tags=["predictions"])

@router.post("/", response_model=PredictionResponse)
async def predict(request: PredictionRequest) -> PredictionResponse:
    try:
        result = run_inference(request)
    except ModelNotLoadedError:
        raise HTTPException(status_code=503, detail="Model not ready")
    return result
```

## Checklist

- [ ] Routes separated from business logic
- [ ] Pydantic schemas on every request/response
- [ ] Routes versioned (`/api/v1/...`)
- [ ] `/health` (and `/ready` if applicable) implemented
- [ ] No stack traces leaked in error responses

## References

- `docs/engineering-standards/logging.md` — request/error logging expectations
- `docs/engineering-standards/security.md` — auth and input validation

## Next Steps

- Add a FastAPI service scaffold template to `templates/` (Phase 5).
