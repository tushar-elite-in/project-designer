# Sample Brief 05 — Reservations API

> Illustrative sample input for planning practice. This is not a real assignment, contract, or fixed technology mandate.

## Problem Statement

Several client applications need a consistent way to search availability and create reservations. Build an API that exposes reservation operations to authorized clients.

## Client and actor types
- Customer-facing client: searches and manages its user's reservations.
- Partner client: accesses approved endpoints using scoped credentials.
- Operator: inspects health, configuration, and operational events.

## Core requirements
- Publish a versioned API contract for availability, reservation creation, lookup, cancellation, and health.
- Validate inputs and return consistent success and error formats.
- Prevent duplicate reservations when a client retries the same request.
- Enforce authorization and partner-specific rate limits.
- Track reservation state transitions and timestamps.
- Support webhook delivery for selected state changes with retry and signature verification, if webhooks are in scope.

## Data concepts
Client, Credential, Resource, AvailabilitySlot, Reservation, IdempotencyKey, WebhookSubscription, DeliveryAttempt.

## Constraints to resolve
Define peak load, consistency needs, data retention, authentication model, webhook guarantees, and service-level targets. Use the current OpenAPI specification if an OpenAPI contract is selected.

## Optional ideas
Bulk reservation endpoints, sandbox mode, SDKs, partner self-service portal.

## Acceptance and delivery
Provide a machine-readable contract, representative request/response examples, auth and retry behavior, versioning policy, and automated checks for critical API behavior.

You are required to build the application described below and demonstrate the role-based workflows.

## Frameworks to Be Used

These are the illustrative technology constraints for this sample brief:
- FastAPI for the HTTP API.
- Pydantic schemas for request/response validation.
- SQLite for the local demo; isolate persistence behind a data-access layer.
- Document endpoints using the generated OpenAPI description.

## Notes

Define peak load, consistency needs, data retention, authentication model, webhook guarantees, and service-level targets. Use the current OpenAPI specification if an OpenAPI contract is selected.
- Demonstrate the core workflows in a reproducible local or documented test environment.
- Create or initialize required data through application code or versioned scripts; do not depend on manual database editing.

## Roles & Functionalities

### Admin
- Can create partner clients, assign API scopes, set limits, rotate/revoke credentials, and review usage.
- Can inspect reservation records and webhook delivery failures.

### Partner Client
- Can authenticate with its assigned credential and use only granted endpoints/scopes.
- Can search resources and availability within its permitted area.
- Can create a reservation, retrieve its own reservation, and cancel when allowed.
- Can retry a create request safely using the same idempotency key.

### Operator
- Can inspect health/readiness status and retry eligible webhook deliveries.
- Cannot read secret credential values or alter customer reservation data without an authorized role.

## Key Terminologies and Attributes

- Client: ID, name, scopes, status, rate limit.
- Credential: client ID, key hash, expiry/revocation dates.
- Resource: ID, name, location, capacity, status.
- Availability Slot: resource ID, start/end time, remaining capacity.
- Reservation: client/customer, slot, status, idempotency key, timestamps.
- Webhook Attempt: subscription ID, event ID, attempt status, response code.

The listed tables and attributes are starting points. Add fields or related tables only when required by a workflow, and document important relationships and integrity rules.

## Similar Apps

- OpenTable and Ticketmaster developer APIs are contract-design references only.

## Application Wireframe

A wireframe may be supplied separately to illustrate application flow and navigation. Exact UI replication is not mandatory unless the actual project statement says so. Maintain the intended functionality and navigation while designing an appropriate interface for the target platform.

## Core Features

1. Publish a versioned API contract for availability, reservation creation, lookup, cancellation, and health.
2. Validate inputs and return consistent success and error formats.
3. Prevent duplicate reservations when a client retries the same request.
4. Enforce authorization and partner-specific rate limits.
5. Track reservation state transitions and timestamps.
6. Support webhook delivery for selected state changes with retry and signature verification, if webhooks are in scope.

## Recommended and/or Optional Functionalities

- Bulk reservation endpoints, sandbox mode, SDKs, partner self-service portal.
- Additional feature relevant to the stated user problem, provided all core features are complete.

## Evaluation and Submission

The sample project report should include: student/team details; the problem statement and approach; AI/LLM usage declaration; frameworks and libraries; ER/data-flow diagram where applicable; API endpoints/contracts where applicable; and a link to the demo video.


Submit the source code and required documentation in the format requested by the actual course or client. For this illustrative assignment format, package the project as a single ZIP and include setup instructions. The presenter should be able to explain the submitted code and demonstrate the required workflows.

## Possible Folder Structure

```text
app/api/ routes and request/response schemas.
app/domain/ reservation rules.
app/data/ persistence and migrations.
app/security/ authentication, scopes, and rate limits.
tests/ contract, retry, and permission behavior.
openapi/ exported API contract and examples.
```

## Video Presentation Guidelines

1. Short introduction (up to 30 seconds).
2. Explain the problem and approach (about 30 seconds).
3. Demonstrate the core features (about 90 seconds).
4. Mention additional features (about 30 seconds).

Keep the full video within the actual course/client limit. The original example brief suggests a 5–10 minute limit. Provide a link accessible to the reviewer and ensure the project can also be demonstrated live where required.

> This sample is modeled on the structure of the supplied Trekking Management project statement. Technology choices and requirements here are illustrative, not external or binding requirements.