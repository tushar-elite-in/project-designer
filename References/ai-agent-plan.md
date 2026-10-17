# AI coding agent plan

Write implementation directions as a compact working contract for the coding agent. These instructions should carry enough project context to guide work without repeating the full human explanation.

## Include

1. **Mission and scope:** user outcome, required deliverables, out-of-scope items.
2. **Source of truth:** exact brief and which user decisions override defaults; label required versus optional.
3. **Constraints:** mandated stack, prohibited approaches, supported environments, privacy/security limits, and assignment rules.
4. **Current-state inspection:** inspect existing files and conventions before changing an existing project; preserve unrelated work.
5. **Architecture:** module responsibilities, interfaces, data model, authorization boundaries, and important decisions.
6. **Ordered milestones:** small, dependency-aware implementation tasks, each with expected files/behavior and observable completion criteria.
7. **Verification:** checks relevant to the task, how to report executed versus unexecuted checks, and what failures mean.
8. **Uncertainty:** ask only when an ambiguity blocks safe or correct work; otherwise record conservative assumptions and avoid invented requirements.
9. **Finish report:** summarize outcomes, files or areas changed, checks/results, known gaps, and decisions needed.

## Instruction quality

Use direct imperative language for actual requirements. Keep rationale brief but include it where it prevents a wrong choice. Name the artifact, behavior, boundary, or measurable condition. Link project-specific references and say when to consult them. Avoid vague adjectives (“robust,” “clean,” “production-ready”) unless translated into verifiable criteria.

Do not instruct the agent to deploy, publish, incur paid costs, contact people, alter unrelated systems, expose credentials, or make destructive changes unless separately authorized. Never tell it to claim a check passed without evidence.

Make the plan adaptable: if the agent finds a source conflict, unexpected existing architecture, or missing critical requirement, it should stop that dependent change, report the evidence, and ask the user.