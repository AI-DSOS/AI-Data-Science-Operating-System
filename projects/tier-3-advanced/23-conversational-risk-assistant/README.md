---
title: Project 23 — Conversational AI Risk Assistant
purpose: A RAG-based conversational assistant for querying risk/compliance information, echoing FutureTecSolutions' ConversAI and RiskGuard AI product concepts.
owner: Arulkumaran
dependencies: [docs/engineering-standards/fastapi.md]
related_documents: []
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started; conceptually related to existing FutureTecSolutions product pages (ConversAI, RiskGuard AI)

## Business Problem
Let risk/compliance analysts query internal policy and risk documents conversationally instead of manual document search.

## Planned Architecture
RAG (retrieval-augmented generation) pipeline: document ingestion + embedding, vector search, LLM-based answer synthesis with citations, served via FastAPI.

## Domain Context
Directly extends the FutureTecSolutions product concepts already designed (ConversAI, RiskGuard AI) into a working portfolio demonstration.

## Planned Tech Stack
Python, FastAPI, a vector store (e.g. Chroma/pgvector), an embedding model, Claude API for synthesis.

## Target Metric
Answer relevance/groundedness against a labeled Q&A set — explicitly checked for hallucination, given the compliance-sensitive use case.

## Next Steps
Define a realistic policy-document corpus to ingest (synthetic if real ones aren't available).
