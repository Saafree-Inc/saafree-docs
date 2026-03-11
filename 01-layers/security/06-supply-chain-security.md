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

# Security Layer Law 06 – Supply Chain Security

**Scope:** Third-party code validation; connector S3 integrity; marketplace tool scanning.

**Reference:** Constitution `08-security-supremacy.md` (S8); Constitution VI (Multi-Platform Isolation); Blueprint 7.2.2 (Marketplace Legal); `00-security-constitution.md`; `00-constitution-to-security-layer-mapping.md`.

---

## Principles

1. Connector = code only (S3); metadata connector.yaml; no deployment of connector as separate microservice (Iron Laws).
2. Third-party code (WASM tools) must pass security validation and sandbox; scanning before publish.
3. Marketplace Legal & Compliance (Blueprint 7.2.2): takedown 24h, compliance hook.

---

## Execution Fabric Alignment

- **Connector Plane:** S3 code integrity; version and metadata governance; no connector wrapper service.
- **Marketplace Plane:** WASM tool validation; scanning; takedown and compliance hooks.

---

## Security Constitution Mapping

| Article | Application |
|---------|-------------|
| S8 (Supply Chain Security) | Third-party code validation; connector/marketplace security |

**Security Governance Domain:** Supply Chain Security (6/8).
