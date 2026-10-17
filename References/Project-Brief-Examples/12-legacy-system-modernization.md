# Sample Brief 12 — Legacy Library System Modernization

> Illustrative sample input for planning practice. This is not a real assignment, contract, or fixed technology mandate.

## Problem Statement

A community library relies on an aging circulation application that is difficult to maintain. Plan a phased replacement that preserves member records, catalog data, and checkout history while staff continue daily operations.

You are required to build the application described below and demonstrate the role-based workflows.

## Frameworks to Be Used

These are the illustrative technology constraints for this sample brief:
- Flask for a local replacement prototype.
- Jinja2, HTML, CSS, and Bootstrap for staff/member pages.
- SQLite initialized through versioned migrations.
- A repeatable import script for the sample legacy CSV format.

## Notes

Discover the actual source system and its APIs/export formats, downtime limits, privacy obligations, integrations, training needs, and budget. Do not assume a big-bang replacement or a specific cloud vendor.
- Demonstrate the core workflows in a reproducible local or documented test environment.
- Create or initialize required data through application code or versioned scripts; do not depend on manual database editing.

## Roles & Functionalities

### Admin
- Can manage staff access, run or review migration batches, and perform backups.
- Can inspect reconciliation results and approve a cutover only after required checks.

### Librarian
- Can search catalog items and copies and manage members, loans, returns, renewals, and holds.
- Can review loan history and resolve a circulation exception with a recorded reason.

### Member
- Can search the public catalog and view only their own current loans and holds.
- Can request or cancel a hold where allowed.

### Migration Operator
- Can preview a source import, inspect invalid/duplicate rows, rerun a corrected batch, and compare record counts.
- Cannot discard an unresolved record without recording its disposition.

## Key Terminologies and Attributes

- Member: ID, name, contact details, status.
- Catalog Item: title, author, ISBN, subject, year.
- Copy: catalog item ID, barcode, location, availability.
- Loan: copy ID, member ID, checkout/due/return dates, status.
- Hold: member ID, catalog item ID, queue position, status.
- Migration Batch: source file, imported/rejected counts, reconciliation result.

The listed tables and attributes are starting points. Add fields or related tables only when required by a workflow, and document important relationships and integrity rules.

## Similar Apps

- Koha and Evergreen are library workflow references only.

## Application Wireframe

A wireframe may be supplied separately to illustrate application flow and navigation. Exact UI replication is not mandatory unless the actual project statement says so. Maintain the intended functionality and navigation while designing an appropriate interface for the target platform.

## Core Features

1. Inventory existing workflows, interfaces, data formats, and operational dependencies before changing the system.
2. Support catalog search, member lookup, checkout, return, renewal, and hold management.
3. Preserve audit history and define how malformed or duplicate records are handled.
4. Provide a repeatable migration with counts, reconciliation, and error reports.
5. Support a staged rollout or coexistence period with a rollback path.
6. Define data export and backup/restore procedures.

## Recommended and/or Optional Functionalities

- Self-checkout, RFID, public API, recommendation features.
- Additional feature relevant to the stated user problem, provided all core features are complete.

## Evaluation and Submission

The sample project report should include: student/team details; the problem statement and approach; AI/LLM usage declaration; frameworks and libraries; ER/data-flow diagram where applicable; API endpoints/contracts where applicable; and a link to the demo video.


Submit the source code and required documentation in the format requested by the actual course or client. For this illustrative assignment format, package the project as a single ZIP and include setup instructions. The presenter should be able to explain the submitted code and demonstrate the required workflows.

## Possible Folder Structure

```text
app/ catalog, circulation, and member modules.
migrations/ versioned schema changes.
imports/ mapping and validation scripts.
tests/ circulation rules and data reconciliation.
docs/ system inventory, cutover, rollback, and user guide.
```

## Video Presentation Guidelines

1. Short introduction (up to 30 seconds).
2. Explain the problem and approach (about 30 seconds).
3. Demonstrate the core features (about 90 seconds).
4. Mention additional features (about 30 seconds).

Keep the full video within the actual course/client limit. The original example brief suggests a 5–10 minute limit. Provide a link accessible to the reviewer and ensure the project can also be demonstrated live where required.

> This sample is modeled on the structure of the supplied Trekking Management project statement. Technology choices and requirements here are illustrative, not external or binding requirements.