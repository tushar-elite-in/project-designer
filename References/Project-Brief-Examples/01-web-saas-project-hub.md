# Sample Brief 01 — Web SaaS Project Hub

> Illustrative sample input for planning practice. This is not a real assignment, contract, or fixed technology mandate.

## Problem Statement

Small teams coordinate projects across chat messages and spreadsheets. Build a browser-based project hub that helps a team organize work, see progress, and catch overdue tasks.

You are required to build the application described below and demonstrate the role-based workflows.

## Frameworks to Be Used

These are the illustrative technology constraints for this sample brief:
- Flask for application back-end.
- Jinja2, HTML, CSS, and Bootstrap for the front-end.
- SQLite database created through application code; no manual database editing.
- Core workflows must work without JavaScript.

## Notes

The stack listed above is mandatory for this illustrative brief. A real project should replace it with the exact technologies mandated by its source statement. Support common desktop and mobile browser sizes. Do not assume multi-region scale, billing, or enterprise compliance unless requested.
- Demonstrate the core workflows in a reproducible local or documented test environment.
- Create or initialize required data through application code or versioned scripts; do not depend on manual database editing.

## Roles & Functionalities

### Admin
- Is the pre-existing superuser; no public admin registration is allowed.
- Can view and search all users, workspaces, projects, and tasks.
- Can suspend accounts and inspect workspace activity when support is required.

### Workspace Owner / Project Manager
- Can create a workspace and invite, approve, remove, or change the role of members.
- Can create, edit, archive, and search projects in an authorized workspace.
- Can create tasks, assign members, set priority and due date, and review completion status.
- Can view project progress, overdue work, and the activity history.

### Member
- Can view projects in workspaces where they are an active member.
- Can view assigned tasks, update allowed statuses, add comments, and edit their own profile.
- Cannot invite members or change workspace settings unless explicitly granted that permission.

## Key Terminologies and Attributes

- User: ID, name, email, password hash, role, status.
- Workspace: ID, name, owner ID, creation date.
- Membership: workspace ID, user ID, role, invitation status.
- Project: ID, workspace ID, title, dates, status.
- Task: project ID, assignee ID, priority, status, due date.
- Comment/Activity Event: actor, target, body/event type, timestamp.

The listed tables and attributes are starting points. Add fields or related tables only when required by a workflow, and document important relationships and integrity rules.

## Similar Apps

- Trello, Asana, and Basecamp are workflow references only; exact UI replication is not required.

## Application Wireframe

A wireframe may be supplied separately to illustrate application flow and navigation. Exact UI replication is not mandatory unless the actual project statement says so. Maintain the intended functionality and navigation while designing an appropriate interface for the target platform.

## Core Features

1. Sign up, sign in, sign out, and recover access.
2. Create workspaces and projects; invite or remove members.
3. Create, assign, edit, filter, and complete tasks with status, due date, priority, and description.
4. Show project progress and tasks due soon or overdue.
5. Enforce workspace membership and role permissions on every operation.
6. Keep a useful activity history for project changes.

## Recommended and/or Optional Functionalities

- File attachments, notifications, calendar view, recurring tasks, export, paid plans.
- Additional feature relevant to the stated user problem, provided all core features are complete.

## Evaluation and Submission

The sample project report should include: student/team details; the problem statement and approach; AI/LLM usage declaration; frameworks and libraries; ER/data-flow diagram where applicable; API endpoints/contracts where applicable; and a link to the demo video.


Submit the source code and required documentation in the format requested by the actual course or client. For this illustrative assignment format, package the project as a single ZIP and include setup instructions. The presenter should be able to explain the submitted code and demonstrate the required workflows.

## Possible Folder Structure

```text
app/ routes, templates, models, services, and static files.
instance/ local database and private configuration.
migrations/ schema changes.
tests/ authentication, workspace boundaries, and task workflows.
run.py and requirements.txt.
```

## Video Presentation Guidelines

1. Short introduction (up to 30 seconds).
2. Explain the problem and approach (about 30 seconds).
3. Demonstrate the core features (about 90 seconds).
4. Mention additional features (about 30 seconds).

Keep the full video within the actual course/client limit. The original example brief suggests a 5–10 minute limit. Provide a link accessible to the reviewer and ensure the project can also be demonstrated live where required.

> This sample is modeled on the structure of the supplied Trekking Management project statement. Technology choices and requirements here are illustrative, not external or binding requirements.