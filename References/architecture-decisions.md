# Architecture decision guide

Choose architecture from requirements and constraints. A named architecture is a set of tradeoffs, not a quality badge.

## Gather design drivers

Record the top business and technical drivers: scope and deadline, expected scale, team expertise, change frequency, availability and recovery needs, latency, consistency, privacy/security, offline behavior, deployment environment, cost, and mandated technologies. Mark measurable targets only when the source gives them or the user agrees to them.

## Select the least complex viable shape

Compare options that fit the drivers: single deployable application, modular monolith, client-server, layered/n-tier, event-driven, queue-worker, data pipeline, serverless, microservices, edge/hybrid, or a relevant domain-specific structure. Do not present every pattern as an equal candidate. Start with the simplest viable option and add distributed components only for a concrete need such as independent scaling, deployment, ownership, fault isolation, or hardware boundaries.

For each serious option, summarize:
- Why it fits the drivers.
- Main operational and development cost.
- Data ownership and communication pattern.
- Failure modes and recovery behavior.
- What future evidence would justify evolving the design.

Avoid microservices for fashion. Account for network failure, observability, deployment, consistency, retries, duplicate messages, and local development when recommending distributed services.

## Define boundaries

Describe responsibilities and allowed dependencies for UI/client, business logic/domain, persistence/data access, external services, background processing, and infrastructure as relevant. Identify system boundary, actors, trust boundaries, and external dependencies. Keep the proposed folder/module structure consistent with those responsibilities.

## Diagrams

Use only diagrams that clarify decisions. Prefer a simple context diagram and container/component view for most software systems. Add sequence, data-flow, deployment, state-machine, or ER diagrams when they answer a specific question. Use Mermaid when supported; label systems, actors, interfaces, and important trust boundaries. Avoid decorative diagrams and excessive levels of detail.

## Decision record

For consequential choices, record: decision, status (mandated/selected/proposed), context, alternatives considered, rationale, tradeoffs, assumptions, and source/date for changeable facts. Keep low-impact choices lightweight.

## Cloud and infrastructure

For cloud-hosted systems, compare relevant provider-neutral needs first: reliability, security, operations, performance, cost, sustainability, portability, and vendor constraints. Map to a named provider only if user constraints or research justify it. Do not assume a cloud deployment is needed; local-only, on-prem, self-hosted, edge, and offline deployments are valid options.