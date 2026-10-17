# Output contract

Generate a coordinated human blueprint and AI build plan. Use Markdown unless the user asks for another format. For a small project, keep both in one response with clear sections; for a large project, propose separate files and create them when requested or when the environment supports useful deliverables.

## Human blueprint

Include the sections relevant to the project:
1. **Project summary** — problem, goal, intended users, and scope.
2. **Requirements and assumptions** — required, optional, assumed, and unresolved items.
3. **User workflows** — role-by-role flows, including important alternate or failure paths.
4. **System design** — major components, responsibilities, boundaries, and how requests/data move between them. A compact Mermaid diagram is useful when it clarifies the design.
5. **Technology stack** — technology, role in the system, reason for selection, and constraint satisfied. Distinguish mandated choices from recommendations.
6. **Data design** — entities, key fields, relationships, and important integrity rules. Include an ER diagram when useful.
7. **Project structure** — proposed folders/files and each one's responsibility.
8. **Requirement traceability** — requirement → workflow/component/data → completion check.
9. **Delivery checklist** — reports, demos, deployment, or submission items in the source brief.

Avoid padding sections that do not apply. Explain tradeoffs plainly and keep scope proportional.

## AI build plan

Write as direct instructions to a coding agent. Include:
- **Goal and boundaries:** what to build and what is out of scope.
- **Source of truth:** supplied brief, user choices, and how to treat optional suggestions.
- **Non-negotiable constraints:** exact technologies, prohibited approaches, environment, and submission restrictions.
- **Architecture and file responsibilities:** consistent with the human blueprint.
- **Ordered phases:** setup, data model, core workflows, role-specific behavior, interface, and polish as appropriate.
- **Per-task completion checks:** observable behavior or artifacts, not vague quality claims.
- **Validation expectations:** suitable checks implied by the brief; do not claim they have passed until run.
- **Uncertainty handling:** when to ask, when to record assumptions, and how to avoid inventing requirements.
- **Final report:** summarize files/behavior changed, checks actually run and results, assumptions, and remaining work.

The AI plan must not authorize unrelated external actions, deployment, publication, destructive changes, or scope expansion. Such actions need separate user authorization where applicable.

## Consistency review

Before presenting, verify:
- Every mandatory source requirement appears in the plan and traceability map.
- Optional ideas remain visibly optional.
- Roles, workflows, data, architecture, and folder structure agree across both deliverables.
- The AI build plan can be followed without relying on hidden context.
- Assumptions, unresolved issues, and unsupported claims are labeled.