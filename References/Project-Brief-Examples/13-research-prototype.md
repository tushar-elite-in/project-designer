# Sample Brief 13 — Research Prototype and Evaluation

> Illustrative sample input for planning practice. This is not a real assignment, contract, or fixed technology mandate.

## Problem Statement

A research team wants to test whether a new interaction concept helps participants complete a defined task. Build a prototype and an evaluation plan that can answer the research question without collecting unnecessary personal data.

## Stakeholders and participants
- Research lead: defines question, protocol, and success measures.
- Prototype developer: implements only the needed interaction.
- Participant: completes study tasks and provides feedback.
- Data steward: controls access, retention, and deletion of study records.

## Core requirements
- State research question, hypotheses, assumptions, and what evidence would change the decision.
- Implement the smallest prototype capable of testing the hypothesis.
- Define participant tasks, consent language, inclusion/exclusion criteria, and data fields with the responsible research team.
- Separate identifiable contact data from study responses where feasible.
- Record protocol deviations and prototype version for each session.
- Analyze results using a method appropriate to sample and study design; report limitations.

## Data concepts
Study, ProtocolVersion, ParticipantCode, Session, Task, Observation, Response, ConsentRecord, PrototypeBuild.

## Constraints to resolve
Confirm ethics review requirements, participant population, jurisdiction, recruitment, accessibility, data retention, and whether the study is formative or intended to support a stronger causal claim. Do not claim statistical significance or generalizability without suitable design and analysis.

## Optional ideas
Remote sessions, analytics instrumentation, follow-up interviews.

## Acceptance and delivery
Provide a runnable prototype, study protocol, data-handling plan, analysis approach, findings with limitations, and a recommendation for the next experiment.

You are required to build the application described below and demonstrate the role-based workflows.

## Frameworks to Be Used

These are the illustrative technology constraints for this sample brief:
- Flask and server-rendered HTML for a small interactive prototype.
- SQLite for pseudonymous study events and consent status.
- Use synthetic sample data for the demo.
- Do not recruit participants or collect real research data without the responsible review/approval.

## Notes

Confirm ethics review requirements, participant population, jurisdiction, recruitment, accessibility, data retention, and whether the study is formative or intended to support a stronger causal claim. Do not claim statistical significance or generalizability without suitable design and analysis.
- Demonstrate the core workflows in a reproducible local or documented test environment.
- Create or initialize required data through application code or versioned scripts; do not depend on manual database editing.

## Roles & Functionalities

### Research Lead
- Defines the question, hypotheses, task protocol, measures, and analysis plan.
- Approves the fields collected and the data retention period with the responsible institution.

### Prototype Developer
- Implements only the interaction needed to answer the research question.
- Maintains a prototype version and can reset a session between participants.

### Participant
- Sees study information and consent choices before a session begins.
- Completes the defined tasks and may stop or withdraw according to the approved protocol.

### Data Steward
- Controls access to study records, export, deletion, and retention.
- Keeps identity/contact data separate from pseudonymous responses when feasible.

## Key Terminologies and Attributes

- Study: research question, protocol version, status.
- Participant Code: pseudonymous ID, eligibility, consent state.
- Session: participant code, prototype version, start/end time.
- Task: prompt, expected outcome, completion measure.
- Observation/Response: session, task, response, timestamp.
- Deletion Record: data scope, request date, completion date.

The listed tables and attributes are starting points. Add fields or related tables only when required by a workflow, and document important relationships and integrity rules.

## Similar Apps

- Usability-testing prototypes and HCI study examples are method references only; follow the applicable institutional review process.

## Application Wireframe

A wireframe may be supplied separately to illustrate application flow and navigation. Exact UI replication is not mandatory unless the actual project statement says so. Maintain the intended functionality and navigation while designing an appropriate interface for the target platform.

## Core Features

1. State research question, hypotheses, assumptions, and what evidence would change the decision.
2. Implement the smallest prototype capable of testing the hypothesis.
3. Define participant tasks, consent language, inclusion/exclusion criteria, and data fields with the responsible research team.
4. Separate identifiable contact data from study responses where feasible.
5. Record protocol deviations and prototype version for each session.
6. Analyze results using a method appropriate to sample and study design; report limitations.

## Recommended and/or Optional Functionalities

- Remote sessions, analytics instrumentation, follow-up interviews.
- Additional feature relevant to the stated user problem, provided all core features are complete.

## Evaluation and Submission

The sample project report should include: student/team details; the problem statement and approach; AI/LLM usage declaration; frameworks and libraries; ER/data-flow diagram where applicable; API endpoints/contracts where applicable; and a link to the demo video.


Submit the source code and required documentation in the format requested by the actual course or client. For this illustrative assignment format, package the project as a single ZIP and include setup instructions. The presenter should be able to explain the submitted code and demonstrate the required workflows.

## Possible Folder Structure

```text
app/ prototype pages and session flow.
study/ protocol, task definitions, and consent text.
data/ synthetic fixtures only.
analysis/ reproducible scripts or notebooks.
tests/ consent gate, data minimization, deletion.
docs/ study limitations and setup.
```

## Video Presentation Guidelines

1. Short introduction (up to 30 seconds).
2. Explain the problem and approach (about 30 seconds).
3. Demonstrate the core features (about 90 seconds).
4. Mention additional features (about 30 seconds).

Keep the full video within the actual course/client limit. The original example brief suggests a 5–10 minute limit. Provide a link accessible to the reviewer and ensure the project can also be demonstrated live where required.

> This sample is modeled on the structure of the supplied Trekking Management project statement. Technology choices and requirements here are illustrative, not external or binding requirements.