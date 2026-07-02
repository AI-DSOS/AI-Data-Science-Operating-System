---
title: Template — Dockerfile (FastAPI Service)
purpose: Baseline Dockerfile for a served FastAPI project, per docs/engineering-standards/docker.md.
related_documents: [docs/engineering-standards/docker.md, docs/engineering-standards/fastapi.md]
---

# Dockerfile Template — FastAPI Service

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
