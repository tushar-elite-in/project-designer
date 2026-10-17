# Sample Brief 03 — Mobile Field Service App

> Illustrative sample input for planning practice. This is not a real assignment, contract, or fixed technology mandate.

## Problem Statement

Field technicians receive job details by phone and report completion later, causing missed updates and duplicate paperwork. Build a mobile app for job assignments and field reports.

You are required to build the application described below and demonstrate the role-based workflows.

## Frameworks to Be Used

These are the illustrative technology constraints for this sample brief:
- Android app using Kotlin and Jetpack Compose.
- Room for local persistence and WorkManager for deferred synchronization.
- Flask API with SQLite for a local demonstration server.
- All core job actions must be demonstrable on an emulator or supported device.

## Notes

Select target mobile platforms, supported OS versions, offline depth, data retention, and device permission requirements. Verify current platform APIs and store requirements before choosing implementation details.
- Demonstrate the core workflows in a reproducible local or documented test environment.
- Create or initialize required data through application code or versioned scripts; do not depend on manual database editing.

## Roles & Functionalities

### Admin
- Can create staff accounts, assign roles, and deactivate accounts.
- Can manage service categories and search all jobs and reports.

### Dispatcher
- Can create a job with customer, location, instructions, priority, and appointment window.
- Can assign or reassign a technician and view the status of all jobs.
- Can review blocked jobs and contact the assigned technician through the approved workflow.

### Technician
- Can sign in and view only assigned jobs.
- Can accept a job and update its lifecycle status with a timestamp.
- Can add notes and optional attachments, save a draft offline, and submit it after sync.
- Can see whether an update is saved, pending, failed, or needs conflict resolution.

### Customer
- Can view appointment and completion updates for their own job, if customer access is included.

## Key Terminologies and Attributes

- User: ID, name, email, role, status.
- Technician: user ID, skills, availability.
- Job: customer, address, instructions, scheduled window, priority, status.
- Assignment: job ID, technician ID, assignment time.
- Field Report: job ID, author, notes, attachment reference, sync state.
- Status Event: job ID, old/new status, actor, timestamp.

The listed tables and attributes are starting points. Add fields or related tables only when required by a workflow, and document important relationships and integrity rules.

## Similar Apps

- Jobber and Salesforce Field Service are workflow references only.

## Application Wireframe

A wireframe may be supplied separately to illustrate application flow and navigation. Exact UI replication is not mandatory unless the actual project statement says so. Maintain the intended functionality and navigation while designing an appropriate interface for the target platform.

## Core Features

1. Sign in securely and show each technician only their assigned jobs.
2. Display job address, instructions, scheduled time, and contact details.
3. Support status changes: assigned, accepted, en route, in progress, blocked, completed.
4. Capture notes and optional photos; record timestamps and author.
5. Preserve a draft during temporary network loss and sync it when connectivity returns.
6. Show sync conflicts or failures clearly; do not silently lose reports.

## Recommended and/or Optional Functionalities

- Route optimization, barcode scan, signatures, inventory usage, push notifications.
- Additional feature relevant to the stated user problem, provided all core features are complete.

## Evaluation and Submission

The sample project report should include: student/team details; the problem statement and approach; AI/LLM usage declaration; frameworks and libraries; ER/data-flow diagram where applicable; API endpoints/contracts where applicable; and a link to the demo video.


Submit the source code and required documentation in the format requested by the actual course or client. For this illustrative assignment format, package the project as a single ZIP and include setup instructions. The presenter should be able to explain the submitted code and demonstrate the required workflows.

## Possible Folder Structure

```text
androidApp/ Compose screens and navigation.
data/ Room database, API client, repositories, sync.
server/ Flask API, models, and routes.
tests/ offline sync and role access.
docs/ emulator setup and demo steps.
```

## Video Presentation Guidelines

1. Short introduction (up to 30 seconds).
2. Explain the problem and approach (about 30 seconds).
3. Demonstrate the core features (about 90 seconds).
4. Mention additional features (about 30 seconds).

Keep the full video within the actual course/client limit. The original example brief suggests a 5–10 minute limit. Provide a link accessible to the reviewer and ensure the project can also be demonstrated live where required.

> This sample is modeled on the structure of the supplied Trekking Management project statement. Technology choices and requirements here are illustrative, not external or binding requirements.