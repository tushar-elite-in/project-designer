# Sample Brief 02 — Local Services Marketplace

> Illustrative sample input for planning practice. This is not a real assignment, contract, or fixed technology mandate.

## Problem Statement

Residents need a simple way to discover local service providers and request appointments. Providers need a way to publish availability and manage incoming requests.

You are required to build the application described below and demonstrate the role-based workflows.

## Frameworks to Be Used

These are the illustrative technology constraints for this sample brief:
- Flask back-end.
- Jinja2 templates, HTML, CSS, and Bootstrap front-end.
- SQLite database created programmatically.
- Backend validation is required for booking and availability rules.

## Notes

Decide whether the first release handles payments or only appointment requests. Define timezone behavior, cancellation rules, location precision, and whether providers are verified. Stack and hosting are open choices.
- Demonstrate the core workflows in a reproducible local or documented test environment.
- Create or initialize required data through application code or versioned scripts; do not depend on manual database editing.

## Roles & Functionalities

### Admin
- Can view provider applications, users, listings, bookings, and reports.
- Can approve or reject provider profiles and suspend a listing or account.
- Can search records and review moderation history.

### Provider
- Can register and sign in; an unapproved provider is not publicly listed.
- Can create and update a profile, services, prices, durations, and available slots.
- Can confirm, reject, reschedule, or cancel a booking request with a reason where appropriate.
- Can view customers and booking history only for their own services.

### Customer
- Can register, sign in, edit their profile, and search approved providers.
- Can filter by service category, location, and available time.
- Can create a booking request, review its status, and cancel within the stated policy.
- Can post one review after an eligible booking is completed and report an issue.

## Key Terminologies and Attributes

- User: ID, name, email, role, status.
- Provider Profile: user ID, business name, location, approval status.
- Service: provider ID, title, category, duration, price, status.
- Availability Slot: provider ID, start/end time, status.
- Booking: customer ID, service ID, slot ID, booking status, created date.
- Review/Report: booking or user ID, rating/reason, status, timestamp.

The listed tables and attributes are starting points. Add fields or related tables only when required by a workflow, and document important relationships and integrity rules.

## Similar Apps

- Airbnb Experiences, Thumbtack, and TaskRabbit are discovery/booking references only.

## Application Wireframe

A wireframe may be supplied separately to illustrate application flow and navigation. Exact UI replication is not mandatory unless the actual project statement says so. Maintain the intended functionality and navigation while designing an appropriate interface for the target platform.

## Core Features

1. Search and filter providers by service type, location, and availability.
2. Show provider profiles, services, prices, and available time slots.
3. Create, confirm, reschedule, and cancel appointment requests.
4. Prevent conflicting confirmed bookings for the same provider and time.
5. Keep both parties informed of booking status.
6. Allow reviews only after a completed appointment; support reporting and moderation.

## Recommended and/or Optional Functionalities

- Online payments, map view, waitlists, coupons, multilingual listings.
- Additional feature relevant to the stated user problem, provided all core features are complete.

## Evaluation and Submission

The sample project report should include: student/team details; the problem statement and approach; AI/LLM usage declaration; frameworks and libraries; ER/data-flow diagram where applicable; API endpoints/contracts where applicable; and a link to the demo video.


Submit the source code and required documentation in the format requested by the actual course or client. For this illustrative assignment format, package the project as a single ZIP and include setup instructions. The presenter should be able to explain the submitted code and demonstrate the required workflows.

## Possible Folder Structure

```text
app/routes/ customer, provider, and admin pages.
app/models/ users, services, slots, and bookings.
app/services/ booking rules and notifications.
templates/ and static/ Bootstrap interface.
migrations/ and tests/.
```

## Video Presentation Guidelines

1. Short introduction (up to 30 seconds).
2. Explain the problem and approach (about 30 seconds).
3. Demonstrate the core features (about 90 seconds).
4. Mention additional features (about 30 seconds).

Keep the full video within the actual course/client limit. The original example brief suggests a 5–10 minute limit. Provide a link accessible to the reviewer and ensure the project can also be demonstrated live where required.

> This sample is modeled on the structure of the supplied Trekking Management project statement. Technology choices and requirements here are illustrative, not external or binding requirements.