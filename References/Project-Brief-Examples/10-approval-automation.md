# Sample Brief 10 — Invoice Approval Automation

> Illustrative sample input for planning practice. This is not a real assignment, contract, or fixed technology mandate.

## Problem Statement

A small organization routes invoices through email and loses track of approvals. Build a workflow that records an invoice, routes it to the right approver, and preserves an audit history.

## Roles
- Requester: submits invoice details and supporting documents.
- Approver: approves, rejects, or requests changes within assigned authority.
- Finance operator: reconciles approved invoices and closes the workflow.
- Administrator: configures routing rules and access.

## Core requirements
- Create a workflow case with supplier, amount, invoice date, due date, and attachment reference.
- Route cases based on explicit configurable approval rules.
- Require a reason for rejection or return for changes.
- Prevent duplicate submissions using a defined identifier or review step.
- Send reminders and show overdue approvals.
- Preserve immutable history of state changes, actor, timestamp, and reason.
- Provide manual recovery for failed notifications or integrations.

## Data concepts
InvoiceCase, Supplier, ApprovalRule, ApprovalStep, Decision, AttachmentRef, NotificationAttempt, AuditEvent.

## Constraints to resolve
Confirm accounting-system integrations, amount limits, separation-of-duties rules, retention, document storage, and whether the automation may trigger payment. Keep payment execution out of scope until explicitly authorized.

## Optional ideas
OCR extraction, accounting export, dashboard, mobile approval.

## Acceptance and delivery
Demonstrate happy path, rejection, change request, duplicate, overdue case, and notification failure. Include auditability, permission checks, and a clear manual fallback.

You are required to build the application described below and demonstrate the role-based workflows.

## Frameworks to Be Used

These are the illustrative technology constraints for this sample brief:
- Flask for workflow logic.
- Jinja2, HTML, CSS, and Bootstrap for the interface.
- SQLite database created programmatically.
- Mock notifications only; do not send real invoices or trigger payments.

## Notes

Confirm accounting-system integrations, amount limits, separation-of-duties rules, retention, document storage, and whether the automation may trigger payment. Keep payment execution out of scope until explicitly authorized.
- Demonstrate the core workflows in a reproducible local or documented test environment.
- Create or initialize required data through application code or versioned scripts; do not depend on manual database editing.

## Roles & Functionalities

### Admin
- Can configure approver groups, amount thresholds, routing order, and role assignments.
- Can view cases and audit events across the organization.

### Requester
- Can submit invoice details and supporting documents.
- Can view their own case status and respond to a request for correction.
- Cannot approve their own invoice where separation of duties applies.

### Approver
- Can see cases assigned to them and review relevant invoice information.
- Can approve, reject, or request changes; rejection/change requests require a reason.
- Cannot alter invoice details after decision without creating a traceable revision.

### Finance Operator
- Can view approved cases, record reconciliation, and close the workflow.
- Cannot trigger a payment in this sample application.

## Key Terminologies and Attributes

- Invoice Case: supplier, invoice number, amount, currency, dates, status.
- Approval Rule: amount range, department, required role/sequence.
- Approval Step: case ID, approver, decision, reason, timestamp.
- Attachment: case ID, safe storage key, type, uploader.
- Notification Attempt: case ID, channel, outcome, retries.
- Audit Event: actor, action, target, old/new status, timestamp.

The listed tables and attributes are starting points. Add fields or related tables only when required by a workflow, and document important relationships and integrity rules.

## Similar Apps

- SAP Concur and Ramp are workflow inspiration only.

## Application Wireframe

A wireframe may be supplied separately to illustrate application flow and navigation. Exact UI replication is not mandatory unless the actual project statement says so. Maintain the intended functionality and navigation while designing an appropriate interface for the target platform.

## Core Features

1. Create a workflow case with supplier, amount, invoice date, due date, and attachment reference.
2. Route cases based on explicit configurable approval rules.
3. Require a reason for rejection or return for changes.
4. Prevent duplicate submissions using a defined identifier or review step.
5. Send reminders and show overdue approvals.
6. Preserve immutable history of state changes, actor, timestamp, and reason.
7. Provide manual recovery for failed notifications or integrations.

## Recommended and/or Optional Functionalities

- OCR extraction, accounting export, dashboard, mobile approval.
- Additional feature relevant to the stated user problem, provided all core features are complete.

## Evaluation and Submission

The sample project report should include: student/team details; the problem statement and approach; AI/LLM usage declaration; frameworks and libraries; ER/data-flow diagram where applicable; API endpoints/contracts where applicable; and a link to the demo video.


Submit the source code and required documentation in the format requested by the actual course or client. For this illustrative assignment format, package the project as a single ZIP and include setup instructions. The presenter should be able to explain the submitted code and demonstrate the required workflows.

## Possible Folder Structure

```text
app/routes/ pages and workflow actions.
app/workflow/ state transitions and approval rules.
app/data/ schema and migrations.
app/notifications/ mock delivery and retry tracking.
uploads/ safe local storage, excluded from source control.
tests/ permissions, duplicate detection, and transitions.
```

## Video Presentation Guidelines

1. Short introduction (up to 30 seconds).
2. Explain the problem and approach (about 30 seconds).
3. Demonstrate the core features (about 90 seconds).
4. Mention additional features (about 30 seconds).

Keep the full video within the actual course/client limit. The original example brief suggests a 5–10 minute limit. Provide a link accessible to the reviewer and ensure the project can also be demonstrated live where required.

> This sample is modeled on the structure of the supplied Trekking Management project statement. Technology choices and requirements here are illustrative, not external or binding requirements.