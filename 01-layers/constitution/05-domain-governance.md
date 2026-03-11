---
doc-type: constitution
authority: supreme-law
status: constitutional-law
owner: Architecture Council
created: 2026-01-17
last-reviewed: 2026-01-17
next-review: 2026-04-17
version: 1.0
mapped-capabilities: [C04, C08]
runtime-surfaces: [domain-orchestrator, boundary-checker, governance-engine]
enforcement-layer: constitutional
---

# 00-DOMAIN-GOVERNANCE

## Purpose

This document defines the **authoritative governance model for domains, processes, and agents in the Saafree system**. It establishes a single, non-negotiable framework for how functional domains are governed, how business processes are orchestrated, and how AI agents are managed.

The objective is to eliminate conceptual ambiguity between layers and domains, prevent governance drift, and ensure that scaling the system (technically and organizationally) does not introduce structural contradictions.

---

## Constitutional Authority

The **constitution/** directory represents the **supreme normative truth** of the Saafree system.

All domains, processes, agents, specifications, architectures, implementations, and runtime behaviors are **subordinate** to the Constitution.

No domain — including the OS domain — has the authority to override, reinterpret, or bypass constitutional definitions.

---

## Domain Governance Framework

Saafree operates with **functional domains as governance units** and **layer dimensions as analytical tools**. Confusion between governance units (domains) and analytical tools (layers) is explicitly disallowed.

**Governance Units (What we govern):**

- Functional Domains (OS, Business, Agent, Data, Compliance)
- Business Processes (sovereign objects)
- AI Agents (managed processes)

**Analytical Tools (How we analyze):**

- Layer Dimensions (Constitutional, Functional, Logical, Physical)
- These are tools for architecture analysis, not governance boundaries

### 1. Constitutional Layer

**Definition:**

- The global governance layer for the entire Saafree system
- Defines meaning, authority, rights, responsibilities, and enforcement boundaries

**Characteristics:**

- Exists exactly once
- Is system-wide
- Does not execute runtime logic
- Does not describe implementation details

**Examples:**

- Capability Registry
- Governance Authority Model
- Runtime Enforcement Principles

---

### 2. Functional Domains (Governance Units)

**Definition:**
Functional domains represent **governance units with constitutional sovereignty**. Each domain owns specific responsibilities and operates with full autonomy within constitutional boundaries.

**Governance Responsibilities:**

- **OS Domain**: Supreme authority over all runtime operations, syscall routing, platform integration
- **Business Domain**: Sovereign ownership of business processes and workflows
- **Agent Domain**: Complete lifecycle management of AI agents and orchestration
- **Data Domain**: Data sovereignty and analytics governance
- **Compliance Domain**: Regulatory compliance and audit enforcement

**Sovereignty Rules:**

- Each domain has **constitutional sovereignty** over its defined responsibilities
- Domains are **peers with equal authority** - no domain hierarchy exists
- **Cross-domain operations** require explicit constitutional authorization
- Domain boundaries are **enforced at runtime** through OS governance

---

### BEU and Domain

**BEU (Business Execution Unit):** unit of execution for a business intent (Intent → Outcome); **always ephemeral**; answers *"what outcome is this execution trying to achieve?"*

- BEU **must be created, evolved, and terminated by the OS**. Any long-lived structure belongs to Domain or Infrastructure, never to BEU.
- **A BEU that becomes persistent ceases to be an execution unit and is architecturally invalid.**

**Domain:** space of functional capability; long-lived; answers *"what kinds of work can be done here?"*

**Relationship:** BEU does not sit "above" Domain in a hierarchy; BEU comes **before** Domain in design thinking. BEU creates demand for execution; Domain supplies capability; OS sits in between. Order: **Doctrine → Institutions → BEU → Domain → Code** (design order; at runtime, domains run continuously, BEUs spawn and terminate).

**Key statement:** BEU does not replace Domain. BEU uses Domain. Domain does not decide work; BEU decides work.

*Reference:* `docs/00-doctrine/execution-doctrine/01-ses-and-execution-centric-doctrine.md`, `docs/03-infrastructure/architecture-ses-beu/01-ses-positioning-and-doctrine.md`.

---

### 3. Logical Layers (Analytical Tools)

**Definition:**
Logical layers are **analytical tools** for understanding conceptual behavior patterns. They help analyze how domains interact and behave, but do not define governance boundaries or authority.

**Analytical Purpose:**

- **Process Logic Layer**: How business processes are orchestrated across domains
- **Execution Logic Layer**: How agents execute tasks within governance boundaries
- **Governance Logic Layer**: How constitutional rules are enforced across domains
- **Platform Logic Layer**: How external platforms are abstracted for domain use

**Governance Clarification:**

- Logical layers **do not own authority** - they analyze domain interactions
- Logical layers **span multiple domains** as needed for analysis
- Logical layers are **tools for understanding**, not units of governance
- **Domain sovereignty takes precedence** over logical layer boundaries

---

### 4. Physical Layers (Implementation Tools)

**Definition:**
Physical layers are **implementation tools** describing how governance requirements are deployed. They ensure domains can operate with required infrastructure while maintaining sovereignty.

**Implementation Purpose:**

- **Microservices**: Domain deployment units with isolation boundaries
- **Infrastructure**: Runtime environment supporting domain operations
- **Networking**: Communication channels respecting domain sovereignty
- **Storage**: Data persistence supporting domain requirements

**Governance Clarification:**

- Physical layers **must support domain sovereignty** - never override it
- Physical topology **cannot redefine** domain governance semantics
- Physical implementation **serves domains** - domains do not serve physical layers
- **Domain requirements drive** physical implementation choices

---

## Specification Governance Model

### The Meaning of `01-spec/`

`01-spec/` represents **Normative Truth**, not documentation and not current state.

A spec defines:

- The intended architecture
- The desired constraints
- The target operating model

Specs are **mandatory**.

Live systems may temporarily deviate, but deviations must be:

- Explicit
- Tracked
- Governed via RFC or exception mechanisms

---

## Spec Alignment Rules

### Global Rule

All `01-spec/` directories across the system **must align with the Constitution**.

### Alignment Flow

```
constitution/
      ↓
<function>/01-spec/
      ↓
<subsystem or feature>/01-spec/
```

### Prohibited Patterns

- A functional-layer spec contradicting constitutional definitions
- A live system redefining spec semantics
- An implementation-driven rewrite of spec intent

---

## OS Domain Clarification

The OS domain is:

- A functional domain
- A governance and execution substrate

The OS domain is **not**:

- The Constitution
- The owner of business semantics
- The source of ultimate authority

The OS enforces rules; it does not create them.

---

## Business Domain Clarification

The Business domain:

- Owns business semantics
- Defines business processes and value flows

The Business layer:

- Is governed by the Constitution
- Is executed and enforced by the OS
- Does not override OS enforcement rules

---

## Non-Negotiable Principles

1. Constitution precedes architecture
2. Specification precedes implementation
3. Governance precedes execution
4. Runtime never redefines truth
5. Scale without clarity is forbidden

---

## Final Authority Statement

Any ambiguity regarding layer ownership, authority, or responsibility must be resolved by **defaulting upward to the Constitution**.

If clarification is not possible, the system must pause, not proceed.

This document is binding.

---

## APPENDIX: Canonical Vocabulary & Glossary

### Constitutional Vocabulary Authority

This appendix establishes the **canonical vocabulary** for Saafree OS constitutional concepts. All documentation, specifications, and communications must use these terms with their constitutional meanings.

**Constitutional Authority:** No alternative definitions permitted. No exceptions.

### Core Constitutional Terms

#### Governance Units vs Analytical Tools

| Term                  | Constitutional Definition                                                                    | Prohibited Alternative Usage                             |
| --------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| **Functional Domain** | Governance unit with constitutional sovereignty (OS, Business, Agent, Data, Compliance)      | "Architecture layer", "Service layer", "Component layer" |
| **Business Process**  | Sovereign governance object defining automation scope                                        | "Workflow", "Task", "Job", "Use case"                    |
| **AI Agent**          | Managed process under OS governance (not autonomous entity)                                  | "AI", "Assistant", "Bot", "Worker", "Service"            |
| **Layer Dimensions**  | Analytical tools for architecture understanding (Constitutional/Functional/Logical/Physical) | Governance units, authority boundaries                   |

**Analytical Tools (Not Governance Units):**
| Term | Constitutional Definition | Prohibited Alternative Usage |
|------|---------------------------|------------------------------|
| **Logical Layer** | Analytical tool for conceptual behavior patterns | "Abstract layer", "Conceptual layer", "Design layer", governance boundary |
| **Physical Layer** | Analytical tool for implementation patterns | "Runtime layer", "Deployment layer", "Infrastructure layer", governance unit |

#### Authority & Governance

| Term            | Constitutional Definition                                | Prohibited Alternative Usage                           |
| --------------- | -------------------------------------------------------- | ------------------------------------------------------ |
| **Authority**   | Constitutional power to make decisions and enforce rules | "Permission", "Access", "Control", "Ownership"         |
| **Governance**  | Runtime enforcement of constitutional principles         | "Management", "Oversight", "Policy", "Rules"           |
| **Sovereignty** | Constitutional supremacy over specific domain            | "Ownership", "Control", "Authority", "Responsibility"  |
| **Enforcement** | Runtime application of governance rules                  | "Validation", "Checking", "Verification", "Compliance" |

#### Process & Execution

| Term                 | Constitutional Definition                                          | Prohibited Alternative Usage                          |
| -------------------- | ------------------------------------------------------------------ | ----------------------------------------------------- |
| **Business Process** | Sovereign object (goals + semantics) without execution authority   | "Workflow", "Task", "Job", "Operation", "Use case"    |
| **Execution**        | OS-controlled runtime behavior (scheduling, resources, governance) | "Running", "Processing", "Handling", "Performing"     |
| **Runtime**          | OS-managed execution environment with governance enforcement       | "System", "Platform", "Environment", "Infrastructure" |
| **Capability**       | Enforceable runtime power mapped to syscall surfaces               | "Feature", "Function", "Ability", "Skill", "Tool"     |

#### Agent & AI

| Term                    | Constitutional Definition                                   | Prohibited Alternative Usage                              |
| ----------------------- | ----------------------------------------------------------- | --------------------------------------------------------- |
| **Agent**               | Managed process under OS governance (not autonomous entity) | "AI", "Assistant", "Bot", "Worker", "Service"             |
| **Agent Lifecycle**     | OS-controlled process lifecycle (spawn, monitor, terminate) | "Agent management", "AI lifecycle", "Process management"  |
| **Capability Matching** | OS-mediated assignment of tasks to agent processes          | "Agent selection", "Task assignment", "Work distribution" |
| **Orchestration**       | OS-controlled coordination of agent processes               | "Management", "Coordination", "Scheduling", "Workflow"    |

#### Platform & Integration

| Term                     | Constitutional Definition                          | Prohibited Alternative Usage                          |
| ------------------------ | -------------------------------------------------- | ----------------------------------------------------- |
| **Platform**             | External device abstracted through OS drivers      | "API", "Service", "System", "Provider", "Vendor"      |
| **Platform Abstraction** | OS device driver layer isolating business logic    | "Integration", "Connector", "Adapter", "Gateway"      |
| **Device Driver**        | OS-managed interface to external platforms         | "API client", "SDK", "Library", "Wrapper"             |
| **Syscall**              | OS kernel interface for agent-platform interaction | "API call", "Function call", "Method call", "Request" |

#### Compliance & Security

| Term                           | Constitutional Definition                          | Prohibited Alternative Usage                                   |
| ------------------------------ | -------------------------------------------------- | -------------------------------------------------------------- |
| **Compliance Layer**           | Authority constraint layer protecting constitution | "Security layer", "Auth layer", "Compliance service"           |
| **Authority Constraint**       | Runtime enforcement of constitutional boundaries   | "Security control", "Access control", "Policy enforcement"     |
| **Governance Boundary**        | Constitutional separation of authority domains     | "Security boundary", "Trust boundary", "Isolation boundary"    |
| **Constitutional Enforcement** | Runtime protection of supreme law                  | "Compliance checking", "Policy validation", "Rule enforcement" |

### Constitutional Authority Statement

This vocabulary supersedes all prior terminology and definitions. It represents the **linguistic foundation** of Saafree OS constitutional governance.

**No exceptions. No alternatives. No compromises.**

**Implementation Rules:** Domain terminology usage and enforcement patterns are defined in layer laws and domain specifications.

**Domain Specification References:**
- **OS Domain Charter:** `docs/02-domains/domain-of-function/os/01-spec/01-os-foundation/01-os-domain-charter.md`
- **Business Domain Charter:** `docs/02-domains/domain-of-function/business/01-spec/01-business-foundation/01-business-domain-charter.md`
- **Agent Domain Charter:** `docs/02-domains/domain-of-function/agent/01-spec/01-agent-foundation/01-agent-domain-charter.md`
- **Data Domain Charter:** `docs/02-domains/domain-of-function/data/01-spec/01-data-foundation/01-data-domain-charter.md`
- **Compliance Domain Charter:** `docs/02-domains/domain-of-function/compliance/01-spec/01-compliance-foundation/01-compliance-domain-charter.md`

---

**Version:** 1.1 | **Status:** CONSTITUTIONAL LAW | **Owner:** Chủ tịch
**Effective Date:** January 17, 2026 | **Authority:** Supreme
**Last Constitutional Review:** January 17, 2026
