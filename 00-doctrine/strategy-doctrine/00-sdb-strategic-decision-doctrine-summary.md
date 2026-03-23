# Strategy Doctrine — Strategic Decision Brain (SDB)

**doc-type:** doctrine-summary  
**status:** active  
**owner:** Architecture & Platform Council  
**category:** EEOS (Enterprise Evolution Operating System) — **organizational runtime (Model A)**  
**last-reviewed:** 2026-03-20  
**scope:** Enterprise / multi-tenant strategic decisioning — **not** personal assistant or consumer product patterns.

---

## Purpose

This document is the **doctrine entry** for the **Strategic Intelligence plane** of Saafree OS: the **Strategy Decision Brain (SDB)**. SDB decides **how** the enterprise should execute work; it does **not** execute business operations (that is Execution Fabric / BEU).

SDB operates **inside** the governance constitutional field. See `docs/00-doctrine/eeos-category/03-governance-constitutional-field-principle.md`.

---

## Canonical definitions

- **SDB:** OS-level strategic decision system: Intent → analysis → Strategic Decision Graph (SDG) candidates → human ratification (War Room) → governance validation plan → execution directive.  
- **SDG:** Time-bound strategic artifact; trace chain documented in authoritative spec.

**Authoritative technical spec:** `docs/03-infrastructure/architecture-sdb/01-sdb-spec.md`  
**Signal → decision flow:** `docs/03-infrastructure/architecture-sdb/07-signal-to-decision-flow.md`  
**SDP / IRP (development methodology):** `.cursor/skills/strategic-decision-preparation/SKILL.md`

---

## Runtime alignment (codebase — verify on G2/AWS)

| Surface | Location (repo) |
|---------|-----------------|
| Strategy kernel (HTTP activation, IFG + `buildStrategy`) | `lib/os/kernel/strategy-kernel.ts` |
| Strategy build pipeline | `lib/sdb/strategy/*`, `lib/sdb/intent/*` |
| Public API (intents) | `app/api/os/strategy/intents/`, `app/api/os/strategy/intent/[id]/` |
| Constitutional DB artifacts | `migrations/constitutional/20260316-100000-strategic-decision-graphs.sql`, `20260316-105000-intent-records-sdg-id-selected.sql`, `20260316-110000-governance-validation-results.sql`, `20260316-130000-sdg-outcomes.sql` |

**Truth rule:** If this summary conflicts with **migrations + runtime behavior** on G2, **runtime wins**; update this file.

---

## Relationship to Model B (infrastructure)

Per `docs/03-infrastructure/architecture/01-unified-saafree-architecture-model.md`, SDB computation runs on the **Control Plane** (orchestration, policy, registries). Doctrine here describes **organizational behavior**; deployment topology remains Model B.

---

## Downstream documentation

- **Logical law:** `docs/01-layers/logic/05-strategy-logic-framework.md`  
- **Domain stub:** `docs/02-domains/domain-of-logic/strategy/01-spec/00-strategy-spec-guide/00-strategy-spec-guide.md`

---

## Explicit non-goals (DNA)

- No positioning of Saafree as a **personal** “AI second brain” or consumer growth OS.  
- No conflation of **constitutional amendment** (core-articles / Article 7 narrative) with **SDG lifecycle** — different mechanisms; CEP doctrine addresses operational evolution separately.
