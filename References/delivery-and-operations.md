# Delivery and operations

Decide how the product is built, installed, deployed, observed, updated, and recovered based on the actual environment. Local-only coursework, self-hosted services, cloud workloads, mobile stores, desktop installers, embedded firmware, and internal automation have different delivery needs.

## Plan only applicable concerns

- Environments, configuration, secrets, build and release steps.
- CI/CD, artifact provenance, dependency updates, and rollback.
- Hosting or distribution target, network boundaries, regions, and cost limits.
- Database migrations, backup/restore, retention, and disaster recovery.
- Logs, metrics, traces, alerts, health checks, and ownership.
- Availability, scaling, queue/job recovery, rate limits, and maintenance windows.
- Mobile/desktop/firmware signing, app store or update channel, staged rollout, compatibility, and rollback.
- Offline mode, synchronization, conflict resolution, and safe local storage.
- Runbooks, support, incident response, and end-of-life/data export.

State who operates the system and what they need to know. Distinguish developer setup from production operations. Keep deployment plans reversible where possible; external publication or production changes require explicit user authorization at execution time.

Browse current official provider/platform docs for specific deployment products, limits, supported versions, pricing, security behavior, and store policies. Do not hardcode changeable provider facts in this reference.