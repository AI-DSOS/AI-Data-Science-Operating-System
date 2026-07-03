---
title: Project 16 — NLP-Based Contract Clause Extraction
purpose: Extract and classify key clauses (e.g. termination, liability, indemnification) from financial contracts.
owner: Arulkumaran
dependencies: [docs/engineering-standards/machine-learning.md]
related_documents: []
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started

## Business Problem
Extract and classify key clauses from legal/financial contracts to speed up legal review — relevant to the QFR/fund-report document work already done outside this repo.

## Planned Architecture
Named entity recognition + clause classification pipeline; OCR pre-processing for scanned contracts, echoing the CAP Partners fund report OCR architecture.

## Planned Tech Stack
Python, spaCy or Hugging Face Transformers for NER, pdfplumber/camelot for extraction (reusing patterns from the existing `nhecf` PDF comparison package).

## Target Metric
Clause-level extraction precision/recall against a manually labeled sample.

## Next Steps
Consider reusing OCR/extraction components from the existing `nhecf` PDF comparison framework rather than rebuilding from scratch.
