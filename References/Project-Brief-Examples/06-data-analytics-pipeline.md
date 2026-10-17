# Sample Brief 06 — Campus Energy Analytics

> Illustrative sample input for planning practice. This is not a real assignment, contract, or fixed technology mandate.

## Problem Statement

Facilities teams receive meter readings from multiple buildings but lack a consistent view of energy use and data quality. Build a data pipeline and dashboard for comparing usage and identifying anomalies.

You are required to build the application described below and demonstrate the role-based workflows.

## Frameworks to Be Used

These are the illustrative technology constraints for this sample brief:
- Python for ingestion and transformations.
- Pandas for tabular validation and aggregation.
- SQLite for local sample storage.
- Flask and Bootstrap for the dashboard.

## Notes

Confirm data owners, volume, timezone, expected freshness, historical depth, privacy classification, and refresh schedule. Select batch or streaming only after confirming the latency need.
- Demonstrate the core workflows in a reproducible local or documented test environment.
- Create or initialize required data through application code or versioned scripts; do not depend on manual database editing.

## Roles & Functionalities

### Admin
- Can add or deactivate buildings and meters and assign analysts to allowed buildings.
- Can view ingestion runs, data-quality issues, and dashboard totals across the installation.

### Facilities Analyst
- Can view readings for permitted buildings and filter by date, meter, and period.
- Can compare periods, inspect freshness, and export filtered results.
- Cannot modify source readings or resolve ingestion errors unless given operator access.

### Data Operator
- Can upload a source file, inspect row-level validation errors, and rerun a corrected import.
- Can review duplicate detection and reconcile source row counts with accepted readings.
- Cannot silently convert missing readings into zero usage.

## Key Terminologies and Attributes

- Building: ID, name, location, area.
- Meter: ID, building ID, identifier, unit, status.
- Reading: meter ID, timestamp, value, unit, source row ID.
- Ingestion Run: source, start/end time, result, row counts.
- Validation Issue: run ID, row reference, issue and resolution status.
- User/Access Grant: user ID, role, permitted buildings.

The listed tables and attributes are starting points. Add fields or related tables only when required by a workflow, and document important relationships and integrity rules.

## Similar Apps

- Energy Star Portfolio Manager and campus energy dashboards are reporting references only.

## Application Wireframe

A wireframe may be supplied separately to illustrate application flow and navigation. Exact UI replication is not mandatory unless the actual project statement says so. Maintain the intended functionality and navigation while designing an appropriate interface for the target platform.

## Core Features

1. Import timestamped readings from agreed source formats.
2. Validate required fields, units, timestamps, and duplicates; quarantine invalid rows with reasons.
3. Normalize readings and retain source lineage.
4. Present daily/weekly usage by building with filters and downloadable results.
5. Show freshness and data-quality indicators so users can judge missing or delayed data.
6. Support replay of corrected source data without silently double-counting.

## Recommended and/or Optional Functionalities

- Forecasting, anomaly detection, emissions estimates, scheduled reports.
- Additional feature relevant to the stated user problem, provided all core features are complete.

## Evaluation and Submission

The sample project report should include: student/team details; the problem statement and approach; AI/LLM usage declaration; frameworks and libraries; ER/data-flow diagram where applicable; API endpoints/contracts where applicable; and a link to the demo video.


Submit the source code and required documentation in the format requested by the actual course or client. For this illustrative assignment format, package the project as a single ZIP and include setup instructions. The presenter should be able to explain the submitted code and demonstrate the required workflows.

## Possible Folder Structure

```text
pipeline/ import, validation, and transformations.
app/ dashboard routes and templates.
data/sample/ input CSV and expected outputs.
database/ schema and seed scripts.
tests/ invalid rows, aggregation, duplicate handling.
docs/ data dictionary and source format.
```

## Video Presentation Guidelines

1. Short introduction (up to 30 seconds).
2. Explain the problem and approach (about 30 seconds).
3. Demonstrate the core features (about 90 seconds).
4. Mention additional features (about 30 seconds).

Keep the full video within the actual course/client limit. The original example brief suggests a 5–10 minute limit. Provide a link accessible to the reviewer and ensure the project can also be demonstrated live where required.

> This sample is modeled on the structure of the supplied Trekking Management project statement. Technology choices and requirements here are illustrative, not external or binding requirements.