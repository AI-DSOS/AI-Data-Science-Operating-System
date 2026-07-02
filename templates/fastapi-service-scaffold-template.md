---
title: Template — FastAPI Service Scaffold
purpose: Starting file layout and boilerplate for a FastAPI service, per docs/engineering-standards/fastapi.md.
related_documents: [docs/engineering-standards/fastapi.md]
---

# FastAPI Service Scaffold

```
src/project_slug/
├── main.py          # app = FastAPI() only
├── routers/
│   └── predictions.py
├── services/
│   └── inference.py
└── schemas/
    └── prediction.py
```

```python
# main.py
from fastapi import FastAPI
from .routers import predictions

app = FastAPI(title="Project Name")
app.include_router(predictions.router)

@app.get("/health")
async def health():
    return {"status": "ok"}
```
