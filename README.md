# Project Designer

**Version:** 0.1.0

Project Designer turns a software idea, assignment, or project brief into a clear plan for people and AI coding agents. It is an **Agent Skill**: it plans and writes instructions; it does not build the application or write its code.

## What it produces

When asked to create a full project plan, the skill produces three coordinated documents:

1. `project-brief.md` — a detailed, human-readable project statement.
2. `human-system-design.md` — user workflows, architecture, technology choices, data design, and requirement traceability.
3. `ai-build-instructions.md` — ordered, actionable instructions for a coding agent, including boundaries and completion checks.

It can plan web, mobile, desktop, API, data/AI, game, IoT, automation, modernization, research, and mixed software projects. It labels assumptions and open questions, and keeps optional features distinct from required scope.

## Repository structure

```text
project-designer/
├── SKILL.md
├── README.md
└── References/
    ├── INDEX.md
    ├── Project-Brief-Examples/
    └── supporting planning guides
```

`SKILL.md` is the entry point. It links to the supporting guides and examples in `References/`; keep that folder and its relative paths alongside the skill when installing or sharing it. The sample briefs are synthetic format examples, not requirements for a real project.

## Use the skill

### In an AI tool that supports Agent Skills

1. Clone or download this repository.
2. Place the `project-designer` skill folder in the tool's documented skills directory. The folder must contain `SKILL.md` and `References/`.
3. Restart or refresh the AI tool if needed.
4. Invoke `project-designer` explicitly, or describe a planning task that matches its purpose.

Skill directories and invocation syntax vary by tool. For example, Antigravity uses `.agents/skills/` for workspace skills and a user-level skills directory for global skills; Codex has its own skills directories. Follow the current setup instructions for your chosen tool.

### In an AI tool without Agent Skills support

Upload `SKILL.md` and the complete `References/` folder with your request. Ask the AI to read `SKILL.md`, follow its instructions, and consult the linked references. If the tool cannot access multiple files, provide the relevant reference files along with `SKILL.md`.

## Example test prompt

```text
Use Project Designer to plan a campus equipment lending system. Produce the project brief, human system design, and AI build instructions. Label assumptions, separate optional features, and do not write code or build the application.
```

## References

See [References/INDEX.md](References/INDEX.md) for the guide and example index.
