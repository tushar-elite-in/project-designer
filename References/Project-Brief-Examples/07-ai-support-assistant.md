# Sample Brief 07 — AI Support Knowledge Assistant

> Illustrative sample input for planning practice. This is not a real assignment, contract, or fixed technology mandate.

## Problem Statement

Support agents search a growing set of approved help articles while responding to customer questions. Build an assistant that finds relevant material and drafts a response with citations for an agent to review.

You are required to build the application described below and demonstrate the role-based workflows.

## Frameworks to Be Used

These are the illustrative technology constraints for this sample brief:
- Python Flask or FastAPI for the application service.
- A relational database for accounts, document metadata, and audit records.
- Use a model-provider adapter and deterministic mock mode for local demos.
- Select a real model/provider only after confirming current cost, privacy, and access constraints.

## Notes

The application framework and local mock mode listed above are mandatory for this illustrative brief. Model/provider, processing region, retention, source access, quality thresholds, cost ceiling, and permission to use an external model remain decisions to resolve before implementation.
- Demonstrate the core workflows in a reproducible local or documented test environment.
- Create or initialize required data through application code or versioned scripts; do not depend on manual database editing.

## Roles & Functionalities

### Admin
- Can manage user access, knowledge source access groups, retention configuration, and provider settings.
- Can inspect system health and aggregate usage/evaluation metrics without unnecessarily exposing sensitive queries.

### Knowledge Editor
- Can add, revise, approve, and retire articles.
- Can assign access groups and preview the indexed text and citations.
- Can review indexing failures and ensure retired versions are no longer retrieved.

### Support Agent
- Can ask a question using only knowledge sources they are permitted to access.
- Can inspect citations, edit a draft, request another draft, or escalate when evidence is weak.
- Must explicitly approve any customer-facing response; the system does not send autonomously.

### Evaluator
- Can run the curated evaluation set, record expected/observed behavior, and compare model or retrieval versions.

## Key Terminologies and Attributes

- Article: ID, title, source, access group, status.
- Article Version: article ID, content hash, revision date.
- Retrieved Passage: version ID, passage, access decision.
- Query/Draft: actor, model version, output, timestamp.
- Citation: draft ID, article version, passage location.
- Evaluation Case/Feedback: expected behavior, result, reviewer notes.

The listed tables and attributes are starting points. Add fields or related tables only when required by a workflow, and document important relationships and integrity rules.

## Similar Apps

- Intercom Fin and Zendesk AI are workflow references only; their capabilities and policies are not requirements.

## Application Wireframe

A wireframe may be supplied separately to illustrate application flow and navigation. Exact UI replication is not mandatory unless the actual project statement says so. Maintain the intended functionality and navigation while designing an appropriate interface for the target platform.

## Core Features

1. Search only approved, access-controlled knowledge sources.
2. Return a draft answer with citations that link to retrieved source passages.
3. Clearly say when evidence is insufficient; offer escalation instead of fabricating a policy.
4. Require human review before any customer-facing send action.
5. Keep sensitive customer data out of model prompts unless explicitly approved and protected.
6. Record feedback and allow evaluation of groundedness, helpfulness, latency, and cost.
7. Treat retrieved documents as untrusted content; they cannot override system policy or grant tool permissions.

## Recommended and/or Optional Functionalities

- Multilingual answers, suggested article updates, agent productivity analytics.
- Additional feature relevant to the stated user problem, provided all core features are complete.

## Evaluation and Submission

The sample project report should include: student/team details; the problem statement and approach; AI/LLM usage declaration; frameworks and libraries; ER/data-flow diagram where applicable; API endpoints/contracts where applicable; and a link to the demo video.


Submit the source code and required documentation in the format requested by the actual course or client. For this illustrative assignment format, package the project as a single ZIP and include setup instructions. The presenter should be able to explain the submitted code and demonstrate the required workflows.

## Possible Folder Structure

```text
app/ UI, API, and permissions.
retrieval/ loading, indexing, and source filtering.
providers/ model adapters and mock provider.
evals/ cases and scoring.
security/ access controls and logging policy.
docs/ data flow and limitations.
```

## Video Presentation Guidelines

1. Short introduction (up to 30 seconds).
2. Explain the problem and approach (about 30 seconds).
3. Demonstrate the core features (about 90 seconds).
4. Mention additional features (about 30 seconds).

Keep the full video within the actual course/client limit. The original example brief suggests a 5–10 minute limit. Provide a link accessible to the reviewer and ensure the project can also be demonstrated live where required.

> This sample is modeled on the structure of the supplied Trekking Management project statement. Technology choices and requirements here are illustrative, not external or binding requirements.