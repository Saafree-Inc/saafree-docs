# Evolution Doctrine — Controlled Evolution Protocol (CEP)

**doc-type:** doctrine-summary  
**status:** active  
**owner:** Architecture & Platform Council  
**category:** EEOS (Enterprise Evolution Operating System) — **organizational runtime (Model A)**  
**last-reviewed:** 2026-03-20  
**scope:** Enterprise-controlled capability evolution — **not** ad-hoc model tuning for consumer apps.

---

## Purpose

This document is the **doctrine entry** for the **Evolution plane** of Saafree OS: the **Controlled Evolution Protocol (CEP)**. CEP turns **governance-accepted execution outcomes** into **qualified learning signals** and **capability lineage** that feed back into strategic cognition — under constitutional gates.

**Distinction (mandatory):**

| Mechanism | Scope |
|-----------|--------|
| **Article 7 — Constitutional amendment** (`core-articles/article-7.md`) | Evolution of **constitutional doctrine / technical constitution** process |
| **CEP** | **Operational** evolution of strategic capability, epochs, signals, proposals — per `controlled-evolution-protocol/` |

Do not use “evolution” interchangeably without specifying which layer.

---

## Canonical status (as documented in repo)

CEP Phase 1–2.3 are **sealed / operationally documented** per `docs/03-infrastructure/controlled-evolution-protocol/README.md` and binding docs referenced there (e.g. `24-evolution-constitutional-protocol-v1.0.md`).

**Authoritative architecture:** `docs/03-infrastructure/controlled-evolution-protocol/00-unified-evolution-framework-architecture.md`  
**Operations / audit:** `28-cep-operations-manual.md`, `29-cep-audit-monitoring-guide.md` (under same directory)

---

## Runtime alignment (codebase — verify on G2/AWS)

| Surface | Location (repo) |
|---------|-----------------|
| Evolution kernel (Evolution Plane activation, analytics / proposals) | `lib/os/kernel/evolution-kernel.ts` |
| Epoch / CEP DB foundation | Migrations under `migrations/` as referenced in CEP README (e.g. epoch state, constitutional CEP tables — **verify current G2 schema** against latest migration manifest) |
| SDG outcomes bridge (execution → learning input) | `migrations/constitutional/20260316-130000-sdg-outcomes.sql` (comment in migration: source for CEP strategic learning) |

**Truth rule:** If this summary conflicts with **deployed DB + observability on G2**, **runtime wins**; update this file.

---

## Relationship to Model B (infrastructure)

Per `docs/03-infrastructure/architecture/01-unified-saafree-architecture-model.md`, evolution computation is anchored on the **Control Plane** with observability from execution. Doctrine here describes **organizational evolution behavior**; scaling and plane placement remain Model B.

---

## Downstream documentation

- **Logical law:** `docs/01-layers/logic/06-evolution-logic-framework.md`  
- **Domain stub:** `docs/02-domains/domain-of-logic/evolution/01-spec/00-evolution-spec-guide/00-evolution-spec-guide.md`

---

## Explicit non-goals (DNA)

- No **real-time autonomous strategy rewrite** narrative — CEP is **controlled** signal pipeline, not strategy replacement (per CEP README).  
- No **personal OS** or consumer “self-improvement” framing; evolution is **enterprise capability** under governance.
