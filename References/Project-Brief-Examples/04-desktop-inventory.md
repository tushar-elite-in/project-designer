# Sample Brief 04 — Desktop Inventory Manager

> Illustrative sample input for planning practice. This is not a real assignment, contract, or fixed technology mandate.

## Problem Statement

A small repair shop tracks parts in paper notebooks and cannot reliably tell which items are low or where stock moved. Build a desktop inventory application for use at the counter and stockroom.

You are required to build the application described below and demonstrate the role-based workflows.

## Frameworks to Be Used

These are the illustrative technology constraints for this sample brief:
- Python with Tkinter for the desktop interface.
- SQLite database initialized by application code.
- CSV import/export using supported Python libraries.
- The core workflow must work offline on one supported computer.

## Notes

Choose target operating systems, local-only versus shared multi-device data, backup destination, and packaging/update approach. Do not assume a cloud account or network connection is available.
- Demonstrate the core workflows in a reproducible local or documented test environment.
- Create or initialize required data through application code or versioned scripts; do not depend on manual database editing.

## Roles & Functionalities

### Admin / Owner
- Can create staff accounts, item categories, and stock locations.
- Can set reorder thresholds and review all item and movement history.
- Can run a backup and restore the database after an explicit confirmation.

### Clerk
- Can search items and view on-hand quantities by location.
- Can record received stock and stock used or sold, with a reason and quantity.
- Can import an approved CSV and review invalid rows before accepting the import.
- Cannot erase or silently overwrite historical stock movements.

### Auditor
- Can view and filter stock movement history and export reports.
- Cannot change item quantities or edit historical movements.

## Key Terminologies and Attributes

- User: ID, name, role, account status.
- Item: SKU, name, category, unit, reorder threshold.
- Location: ID, name, description.
- Stock Balance: item ID, location ID, quantity.
- Stock Movement: item ID, quantity change, reason, actor, timestamp.
- Import Batch: file name, row counts, validation errors, date.

The listed tables and attributes are starting points. Add fields or related tables only when required by a workflow, and document important relationships and integrity rules.

## Similar Apps

- Sortly and inFlow Inventory are inventory workflow references only.

## Application Wireframe

A wireframe may be supplied separately to illustrate application flow and navigation. Exact UI replication is not mandatory unless the actual project statement says so. Maintain the intended functionality and navigation while designing an appropriate interface for the target platform.

## Core Features

1. Maintain item name, SKU, unit, location, current quantity, and reorder threshold.
2. Record every increase/decrease as a dated movement with a reason and actor.
3. Search and filter items; flag low stock.
4. Import a provided CSV and export selected inventory or movement history.
5. Require a reason for manual adjustments and preserve an audit trail.
6. Provide a backup/restore plan and clear behavior for file errors.

## Recommended and/or Optional Functionalities

- Barcode scanning, purchase orders, label printing, supplier price history.
- Additional feature relevant to the stated user problem, provided all core features are complete.

## Evaluation and Submission

The sample project report should include: student/team details; the problem statement and approach; AI/LLM usage declaration; frameworks and libraries; ER/data-flow diagram where applicable; API endpoints/contracts where applicable; and a link to the demo video.


Submit the source code and required documentation in the format requested by the actual course or client. For this illustrative assignment format, package the project as a single ZIP and include setup instructions. The presenter should be able to explain the submitted code and demonstrate the required workflows.

## Possible Folder Structure

```text
src/ui/ screens and dialogs.
src/services/ stock rules and validation.
src/data/ schema and database access.
data/ generated database, excluded from source control.
tests/ stock arithmetic, imports, export, and backup.
```

## Video Presentation Guidelines

1. Short introduction (up to 30 seconds).
2. Explain the problem and approach (about 30 seconds).
3. Demonstrate the core features (about 90 seconds).
4. Mention additional features (about 30 seconds).

Keep the full video within the actual course/client limit. The original example brief suggests a 5–10 minute limit. Provide a link accessible to the reviewer and ensure the project can also be demonstrated live where required.

> This sample is modeled on the structure of the supplied Trekking Management project statement. Technology choices and requirements here are illustrative, not external or binding requirements.