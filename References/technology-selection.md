# Technology selection

Recommend a stack that can actually be implemented within the user's constraints, team skills, timeline, operating environment, and maintenance capacity.

## Decision process

1. Extract mandated technologies, prohibited technologies, compatibility requirements, and existing dependencies.
2. Identify the capabilities the project needs: UI, server, persistence, API, queue, search, analytics, model inference, device support, build/package, hosting, and observability as applicable.
3. Shortlist only plausible options. Compare fit, maturity, learning curve, ecosystem, maintainability, accessibility/security support, performance, total cost, hosting availability, licensing, portability, and lock-in.
4. Browse primary vendor/project documentation for current support status, versions, limits, license, pricing, and compatibility when those facts could change. Prefer official docs and standards; date time-sensitive findings.
5. Recommend one coherent default and explain why. Include a credible alternative only when the tradeoff is meaningful.
6. Avoid unnecessary dependencies and speculative scale. State what would cause reconsideration.

## Output format

| Concern | Choice | Status | Why it fits | Tradeoff / caveat |
|---|---|---|---|---|

Use **Mandated**, **Recommended**, or **Existing** in Status. Do not describe a recommendation as a requirement. Avoid claiming a technology is “best” without naming the criteria.

## Version and provider facts

Don't hardcode current versions, pricing, free tiers, quotas, support windows, or service availability in this reference. Verify the exact target environment and current official source when making a project-specific recommendation. If not verified, label the value unknown and avoid precision.