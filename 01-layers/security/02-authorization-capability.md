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

# Security Layer Law 02 – Authorization & Capability

**Scope:** Permission and capability control; worker/connector capability limits.

**Reference:** Constitution `08-security-supremacy.md` (S2, S6); `00-security-constitution.md`; `00-constitution-to-security-layer-mapping.md`.

---

## Principles

1. No agent or component has unlimited authority; capability limits by tenant tier (04 Free/Vip/Pro/Max) and capability_scope in job payload.
2. Control Plane enforces quota, scope, and timeout before publishing job (NATS).
3. Human escalation and Chairman override required for decisions exceeding thresholds (S7).

---

## Execution Fabric Alignment

- **Control Plane:** Policy checks before job publish; capability_scope and tenant tier validation.
- **Execution Plane:** Worker contracts enforce capability boundaries; no execution beyond granted scope.
- **Audit:** Capability grants and overrides in audit trail.

---

## Security Constitution Mapping

| Article | Application |
|---------|-------------|
| S2 (Runtime Supremacy) | Runtime enforces capability boundaries over design |
| S6 (No Absolute Power) | Capability limits; quota; human override |

**Security Governance Domain:** Authorization & Capability (2/8).
