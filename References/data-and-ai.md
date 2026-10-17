# Data and AI systems

Use this guide for databases, analytics, machine learning, generative AI, retrieval, recommendation, or data-powered product features.

## Data design

Identify sources and ownership, entities/events, schema and identifiers, relationships, validation, consistency needs, access controls, classification, retention/deletion, backups, lineage, quality checks, migration, and recovery. Specify freshness and volume targets only when known. Separate source-of-truth data from derived data and cache.

For pipelines, describe ingestion, transformation, storage, serving, scheduling/streaming, retries, deduplication, observability, replay/backfill, and data-quality failure handling. Do not select a database or warehouse before understanding access patterns and constraints.

## Decide whether AI is needed

State the user problem and why rules, search, or conventional software is insufficient or less suitable. Keep an AI feature out of the plan when there is no clear benefit or feasible evaluation. Identify model tasks, input/output boundaries, source data, inference location, latency/cost constraints, and provider/model dependencies.

## ML and generative AI lifecycle

Where relevant, specify:
- Data rights, consent, provenance, privacy, and representative evaluation data.
- Baseline and measurable task-specific quality criteria.
- Offline/online evaluation, edge cases, regressions, and human review.
- Confidence/uncertainty behavior, fallback, escalation, and user disclosure.
- Prompt injection, unsafe output, data exfiltration, and tool permission boundaries for LLM systems.
- Monitoring for drift, quality, latency, spend, abuse, and incidents.
- Versioning, rollback, retraining/update policy, and model/vendor change management.

Never assume model outputs are factual or deterministic. Do not expose secrets or unrestricted tools to a model. High-impact decisions require domain-specific safeguards, meaningful human oversight, and current authoritative risk guidance.