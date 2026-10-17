# Quality and validation planning

Translate requirements into checks that can demonstrate behavior. Avoid asserting that anything passed before it is run.

## Acceptance criteria

For each important requirement, define an observable result and relevant boundary conditions. Prefer “Given/When/Then” or a concise example when it removes ambiguity. Cover permissions, validation, empty states, errors, cancellation, duplicate requests, and recovery when relevant.

## Verification layers

Choose only useful checks for the project:
- Static analysis, formatting, types, and dependency checks.
- Unit tests for rules and calculations.
- Integration tests for persistence, APIs, queues, and external boundaries.
- End-to-end tests for critical user journeys.
- Contract tests for APIs/events and compatibility.
- Performance, load, resilience, security, accessibility, usability, device, or domain-specific validation when required by risk or source requirements.
- Manual review/demo for user-visible or difficult-to-automate behavior.

Use a risk-based test pyramid; don't prescribe a fixed test count or technology without reason. Include test data strategy and environment only when relevant.

## Non-functional requirements

Ask which measurable targets matter: response time, throughput, capacity, uptime, recovery time/objective, data freshness, accessibility level, supported devices/browsers, and budget. Do not make up numbers. If unknown, state what should be decided and propose a lightweight measurement plan.

## Completion

A task is complete when its listed behavior is implemented, relevant checks are run and their results recorded, and the affected documentation is updated. Separate “planned check” from “check executed.” Record failures, skipped checks, and limitations plainly.