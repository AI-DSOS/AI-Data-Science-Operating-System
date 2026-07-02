---
title: Template — Dockerfile (ML Training Job)
purpose: Baseline Dockerfile for a batch training job, per docs/engineering-standards/docker.md.
related_documents: [docs/engineering-standards/docker.md, docs/engineering-standards/mlops.md]
---

# Dockerfile Template — ML Training Job

```dockerfile
FROM python:3.12-slim
WORKDIR /app
COPY pyproject.toml uv.lock ./
RUN pip install uv && uv sync --frozen --no-dev
COPY src/ ./src/
RUN useradd --create-home appuser
USER appuser
ENV PATH="/app/.venv/bin:$PATH"
ENTRYPOINT ["python", "-m", "src.training.train"]
```
