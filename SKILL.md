---
name: project-designer
description: Turn a product idea into a human-readable project blueprint and a separate, actionable build plan for an AI coding agent.
---

# Project designer

Turn the user's idea or source material into a complete, reviewable project specification. The human-facing brief must follow the detailed section structure in the sample briefs. Also produce a separate, operational AI build plan. A vague idea should become a useful draft with labeled assumptions, not a thin list of generic suggestions.

## Read the references

Always read:
- [Source handling](References/source-handling.md) to distinguish source requirements, recommendations, assumptions, and unresolved questions.
- [Output contract](References/output-contract.md) for deliverable content and consistency checks.
- [Sample project briefs](References/Project-Brief-Examples/README.md) to follow the expected assignment-style structure and level of specificity. Read one or two examples closest to the project's type; examples are synthetic format references, never requirements for the current project.

Classify the project and load only the supporting guides that apply:
- [Project type router](References/project-types.md) for type classification and cross-cutting concerns.
- [Architecture decisions](References/architecture-decisions.md) for system design and diagrams.
- [Technology selection](References/technology-selection.md) when choosing or comparing a stack.
- [Workflows and UX](References/workflows-and-ux.md) for roles, journeys, interfaces, and accessibility.
- [Data and AI](References/data-and-ai.md) for data pipelines, machine learning, or generative AI.
- [Security and privacy](References/security-and-privacy.md) for identity, sensitive data, external access, or meaningful risk.
- [Quality and validation](References/quality-and-validation.md) for acceptance criteria and verification.
- [Delivery and operations](References/delivery-and-operations.md) for hosting, deployment, devices, offline use, releases, or operation.
- [AI agent plan](References/ai-agent-plan.md) when writing instructions for a coding agent.
- [Primary source map](References/primary-source-map.md) for current official standards and platform documentation.

## Inputs and source review

The user may provide a short idea, assignment, product brief, existing codebase, links, screenshots, wireframes, technology mandates, or example deliverables. Inspect every accessible source. If a source is inaccessible, say so and continue from the material that is available.

If the user gives only an idea, generate a complete first draft. Ask focused questions only when a missing answer materially changes scope, architecture, safety, or cost. Otherwise make a conservative assumption, label it, and keep the design easy to revise.

For an existing assignment or client brief, preserve its requirements and wording where precision matters. Do not replace the user's source with a synthetic example. Mark each major item as **Required**, **Optional**, **Recommendation**, **Assumption**, or **Open question**.

## Workflow

1. Identify the project goal, users, environment, project stage, and deliverables.
2. Classify the project; read the matching type and technical references. Research official, current sources for changing stack versions, platform rules, prices, laws, standards, and provider capabilities.
3. Extract roles, permissions, workflows, core and optional features, data concepts, constraints, integrations, and evaluation/submission requirements.
4. Resolve conflicts using the source priority rules. Do not silently omit a requirement or turn an optional idea into a mandatory feature.
5. Design the user workflows, architecture, data model, stack, and project structure as one coherent proposal. Map every major requirement to components and a way to verify it.
6. Produce the human-facing project brief and the separate AI build pack below. Match the level of detail and section order in the sample briefs.
7. Review the result against the source. Check that requirements, roles, workflows, data, architecture, folder structure, and acceptance criteria agree across deliverables.

## Human-facing project brief format

For software project briefs, use these headings in this order. Include every applicable section. If the user wants a shorter format, shorten the content while preserving the requirements.

1. **Project title**
2. **Problem Statement** — context, current pain, intended outcome, and a direct statement of what must be built.
3. **Frameworks to Be Used / Technology Stack** — separate mandatory choices from recommendations. Give a short reason for recommendations. If the stack is undecided, propose a fit-for-purpose stack and explain key tradeoffs.
4. **Notes and Constraints** — local/demo needs, database creation, platforms, prohibited approaches, budget, hosting, privacy, or other real constraints.
5. **Roles & Functionalities** — one subheading per role and concrete capabilities beneath it. Specify permissions, approval states, and data boundaries where relevant.
6. **Key Terminologies and Attributes** — define core entities and useful fields; include relationships and integrity rules. Mark the list as extensible when the source permits changes.
7. **Similar Apps / Inspiration** — provide relevant linked products only when useful. Explain that they guide patterns, not mandatory replication, unless the user says otherwise.
8. **Application Wireframe / UX Guidance** — describe provided wireframes and what is mandatory versus illustrative. Include navigation/screen flows if a wireframe is absent and that would help.
9. **Core Features** — numbered, specific, testable requirements. Group by authentication, role, and cross-cutting behavior when appropriate. Include important edge cases such as invalid access, empty data, overbooking, retry, offline sync, or failure recovery only when relevant.
10. **Recommended and/or Optional Functionalities** — clearly separate optional extensions from required scope.
11. **Evaluation and Submission** — include only source-provided requirements. If the source does not specify them and an assignment-style deliverable needs them, label proposed report/demo criteria as suggestions requiring confirmation. Do not invent a course rubric.
12. **Possible Project Folder Structure** — give a realistic tree or module list with each responsibility; align it with the architecture and stack.
13. **Video / Demo Guidelines** — preserve source requirements. If absent, provide a clearly labeled suggested demo outline only when useful.
14. **Assumptions, Open Questions, and References** — include unresolved decisions and citations/links for current facts or supplied source material.

Use plain language and the specificity of the provided examples. Avoid generic filler. Define state transitions, who can perform them, what data changes, and what visible result confirms success.

## System design and human workflow deliverable

Include a separate `human-system-design.md` (or equivalent section if the user wants one document) with:
- role-by-role user workflows, including important error and alternate paths;
- system context and component responsibilities;
- data flow and external integrations;
- architecture choice with rationale and tradeoffs;
- database entities and relationships, preferably an ER diagram when useful;
- API/event contracts when relevant;
- requirement traceability: requirement → role/workflow → component/data → acceptance check;
- deployment and operational needs when the project requires them.

Choose only diagrams that clarify the design. Keep the architecture proportional to project size and team capacity.

## AI build pack

Create a separate `ai-build-instructions.md` that speaks directly to a coding agent. It must be specific enough to implement from without guessing. Include:
- goal, scope, non-goals, and source of truth;
- mandatory stack, constraints, role permissions, and security boundaries;
- expected file/module structure and responsibilities;
- ordered implementation phases with concrete tasks;
- completion checks for each phase, tied to observable behavior;
- validation and checks the agent should run, while distinguishing planned checks from executed results;
- how to handle missing requirements, conflicts, existing repository conventions, and generated data;
- final report requirements: files/areas changed, behavior delivered, checks and results, assumptions, and remaining work.

Do not authorize unrelated changes, paid services, publication, production deployment, destructive actions, or external messages. Those actions need separate authorization when execution is requested. The AI build plan must not claim that work or tests are already complete.

## Deliverables

When creating files, produce these minimum outputs in the user's requested location:
- `project-brief.md` — detailed human-facing project statement in the example format;
- `human-system-design.md` — workflows, architecture, data design, stack rationale, and traceability;
- `ai-build-instructions.md` — coding-agent implementation contract.

Add supporting diagrams, API contracts, or decision records only when they materially help. If the user asks for an inline answer, use the same structure directly in the response.

## Guardrails

- User instructions outrank this skill; the user's source brief outranks generic recommendations and synthetic examples.
- Never invent roles, integrations, deadlines, regulatory compliance, performance targets, or acceptance rules. Label proposals and assumptions.
- Do not default to microservices, cloud, paid APIs, AI features, or a specific database without a project reason.
- Browse and cite authoritative current sources for unstable technical or regulatory claims. State uncertainty when a source does not settle the question.
- For regulated, safety-critical, health, finance, children’s, or other high-impact systems, identify the jurisdiction and domain, research applicable authoritative guidance, and flag expert review needs. Do not claim a generic plan is a compliance certification.
- Keep the human brief understandable to a student, client, or product owner. Keep AI instructions explicit about boundaries, sequence, and observable completion.