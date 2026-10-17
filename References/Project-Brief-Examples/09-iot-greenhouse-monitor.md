# Sample Brief 09 — Greenhouse Monitoring System

> Illustrative sample input for planning practice. This is not a real assignment, contract, or fixed technology mandate.

## Problem Statement

A greenhouse operator needs to monitor temperature and soil moisture across several beds and receive warnings when readings leave configured ranges. Build a sensor-to-dashboard system with optional local alerts.

You are required to build the application described below and demonstrate the role-based workflows.

## Frameworks to Be Used

These are the illustrative technology constraints for this sample brief:
- ESP32 with MicroPython, or a documented simulator, for sensor readings.
- Flask dashboard and SQLite for the local demonstration server.
- HTTP or MQTT may be selected and must be documented.
- No actuator control is included in the core sample.

## Notes

Confirm hardware, power/network availability, environmental ratings, safety impact, update ownership, data retention, and whether any actuator can change physical conditions. Research device-specific and jurisdictional requirements before implementation.
- Demonstrate the core workflows in a reproducible local or documented test environment.
- Create or initialize required data through application code or versioned scripts; do not depend on manual database editing.

## Roles & Functionalities

### Admin
- Can register devices, assign them to greenhouse beds, create user accounts, and configure alert permissions.
- Can review device status and audit device registration changes.

### Grower
- Can view current and historical readings for assigned beds.
- Can set permitted warning thresholds and acknowledge an alert.
- Can see when a sensor is stale or offline and distinguish that from a normal reading.

### Installer
- Can provision a device identity, pair it with a bed, and confirm data reception.
- Can check connection and sensor health without seeing unrelated greenhouse data.

### Operator
- Can inspect ingestion failures and supported firmware/software version.
- Can reset or replace a device through the documented process; actuator control is outside core scope.

## Key Terminologies and Attributes

- Greenhouse: ID, name, location, owner.
- Bed: greenhouse ID, label, crop notes.
- Device: bed ID, device identity, status, last contact.
- Reading: device ID, metric, value, unit, captured time, quality.
- Threshold: metric, minimum/maximum, active period.
- Alert: triggering value, status, acknowledgement time.

The listed tables and attributes are starting points. Add fields or related tables only when required by a workflow, and document important relationships and integrity rules.

## Similar Apps

- ThingsBoard dashboards and greenhouse monitoring platforms are dashboard references only.

## Application Wireframe

A wireframe may be supplied separately to illustrate application flow and navigation. Exact UI replication is not mandatory unless the actual project statement says so. Maintain the intended functionality and navigation while designing an appropriate interface for the target platform.

## Core Features

1. Register each sensor to a greenhouse and bed; reject unknown device identities.
2. Capture readings with device ID, timestamp, unit, and quality/status.
3. Show latest readings, history, and stale/offline sensor state.
4. Allow authorized users to configure thresholds and alert channels.
5. Buffer readings during temporary connectivity loss and sync safely later.
6. Provide update, reset, and recovery processes appropriate to the selected hardware.

## Recommended and/or Optional Functionalities

- Irrigation control, weather integration, predictive alerts, solar power.
- Additional feature relevant to the stated user problem, provided all core features are complete.

## Evaluation and Submission

The sample project report should include: student/team details; the problem statement and approach; AI/LLM usage declaration; frameworks and libraries; ER/data-flow diagram where applicable; API endpoints/contracts where applicable; and a link to the demo video.


Submit the source code and required documentation in the format requested by the actual course or client. For this illustrative assignment format, package the project as a single ZIP and include setup instructions. The presenter should be able to explain the submitted code and demonstrate the required workflows.

## Possible Folder Structure

```text
device/ firmware or simulator.
server/ ingestion API and device authentication.
dashboard/ Flask pages and charts.
database/ schema and seed data.
tests/ validation, stale detection, and duplicate sync.
docs/ wiring, setup, and hardware assumptions.
```

## Video Presentation Guidelines

1. Short introduction (up to 30 seconds).
2. Explain the problem and approach (about 30 seconds).
3. Demonstrate the core features (about 90 seconds).
4. Mention additional features (about 30 seconds).

Keep the full video within the actual course/client limit. The original example brief suggests a 5–10 minute limit. Provide a link accessible to the reviewer and ensure the project can also be demonstrated live where required.

> This sample is modeled on the structure of the supplied Trekking Management project statement. Technology choices and requirements here are illustrative, not external or binding requirements.