---
doc-type: law
authority: constitutional
status: layer-law
owner: Architecture Council
created: 2026-01-30
last-reviewed: 2026-01-30
next-review: 2026-04-30
version: 1.0
---

# Security Layer Law 01 – Identity & Authentication

**Scope:** Agent and human identity management; integration with Control Plane auth.

**Reference:** Constitution `08-security-supremacy.md` (S1, S3, S5, S7); `00-security-constitution.md`; `00-constitution-to-security-layer-mapping.md`.

---

## Principles

1. Every job (connector/agent/workflow) must carry **tenant_id** and identity (user/agent) validated by the Control Plane before dispatch.
2. Human identity: operators and Chairman have explicit delegation paths; audit trail records who performed each action.
3. Agent identity: agent_id in job payload; capability_scope and tenant tier (04 Free/Vip/Pro/Max) apply.

---

## Execution Fabric Alignment

- **Control Plane:** Kong JWT plugin; Auth & Tenant service; Temporal namespace/queue by tenant when required.
- **Job payload:** tenant_id, (agent_id | user_id), idempotency_key; no dispatch without valid identity.
- **Audit:** execution_fabric_results records tenant_id, job_id; compliance hooks for identity events.

---

## Security Constitution Mapping

| Article | Application |
|---------|-------------|
| S1 (Human Sovereignty) | Human identity supreme; agent identity subordinate |
| S3 (Total Transparency) | Identity events audited; no obscurity |
| S5 (Audit Everything) | Identity in audit trail |
| S7 (Human Intervention) | Human identity in escalation path |

**Security Governance Domain:** Identity & Authentication (1/8).
