---
title: Project 14 — Document Classification for KYC Onboarding
purpose: Classify uploaded documents (passport, utility bill, bank statement) during KYC onboarding.
owner: Arulkumaran
dependencies: [docs/engineering-standards/machine-learning.md]
related_documents: [resources/glossary.md]
version: 0.1.0
last_updated: 2026-07-02
---

## Status: **Blueprint only** — not started

## Business Problem
Automatically classify documents uploaded during customer KYC onboarding to route them to the correct verification step.

## Planned Architecture
Image/text hybrid classifier — OCR extraction + text classification, or a vision transformer for document-type classification.

## Domain Context
Direct KYC/AML onboarding relevance.

## Planned Tech Stack
Python, OCR (pytesseract or similar), Hugging Face Transformers.

## Target Metric
Classification accuracy per document type, plus OCR extraction quality spot-check.

## Next Steps
Source or simulate a labeled document dataset.
