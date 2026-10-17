# Security and privacy planning

Scale security detail to the project's exposure, data, user impact, and deployment context. This is planning guidance, not a security audit or legal opinion.

## Baseline questions

Identify assets, user and service identities, trust boundaries, entry points, external dependencies, sensitive data, abuse cases, and likely impact. For meaningful risk, include a lightweight threat model: assets, actors, threats, mitigations, residual risks, and owner.

Consider applicable needs for:
- Authentication, authorization, role/tenant boundaries, and least privilege.
- Input validation, output encoding, secrets, cryptography, dependency and supply-chain hygiene.
- Secure configuration, logging, monitoring, incident handling, backups, and recovery.
- Data minimization, purpose, consent, retention, deletion, export, and third-party processors.
- Abuse prevention, rate limiting, fraud, content moderation, and audit trails where relevant.
- Device identity, firmware updates, physical safety, and secure provisioning for IoT/embedded systems.
- Model/prompt/tool boundaries and data leakage for AI systems.

Do not invent a compliance regime. Ask for deployment jurisdictions and sector when they materially affect requirements. Browse current government/regulator and primary standards sources for applicable law or regulation, and identify expert review where needed. Do not say “compliant” without a defined scope and assessment.

## Security source use

Use current OWASP guidance for application-specific risks and verification where relevant, and NIST SSDF for secure development process context. These are starting points, not exhaustive guarantees. Select the correct standard and version for the project; do not copy large checklists into every plan.