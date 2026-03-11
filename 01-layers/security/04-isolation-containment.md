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

# Security Layer Law 04 – Isolation & Containment

**Scope:** Failure isolation; blast radius per execution/tenant (Blueprint 12.1); no global cascade.

**Reference:** Constitution `08-security-supremacy.md` (S4); Constitution VIII (Platform Failure Containment); `00-security-constitution.md`; `00-constitution-to-security-layer-mapping.md`.

---

## Principles

1. Local failure must not become system collapse; blast radius limited by execution/tenant.
2. Control / Execution / Connector plane boundaries are explicit; connector = code only, no wrapper service (Iron Laws).
3. WASM sandbox and worker contracts limit attack surface.

---

## Execution Fabric Alignment

- **Control Plane:** Isolated from Execution/Connector failure modes.
- **Execution Plane:** Worker failure does not cascade to Control; tenant isolation.
- **Connector Plane:** Code-only; no lateral movement by default.

---

## Security Constitution Mapping

| Article | Application |
|---------|-------------|
| S4 (Containment First) | Failure isolation; blast radius control |

**Security Governance Domain:** Isolation & Containment (4/8).
