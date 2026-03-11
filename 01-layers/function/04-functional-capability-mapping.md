---
doc-type: law
authority: constitutional
status: layer-law
owner: Architecture Council
created: 2026-01-17
last-reviewed: 2026-01-17
next-review: 2026-04-17
version: 1.0
mapped-capabilities: [C01-C15]
runtime-surfaces: [capability-registry, syscall-router]
enforcement-layer: kernel
---

# 04-Functional Capability Mapping

**Saafree OS Constitutional Capability Registry to Functional Domain Mapping**
**Constitutional Authority:** Supreme Governance Layer
**Effective Date:** January 17, 2026

## Constitutional Authority Statement

**This document establishes the authoritative mapping between constitutional capabilities (C01-C15) and functional domain responsibilities. All domain implementations must align with these constitutional capability mappings.**

**No domain may implement capabilities outside its constitutionally assigned mappings.**

## Capability to Domain Mapping

| Capability ID | Capability Name                    | Primary Domain    | Runtime Surface |
| ------------- | ---------------------------------- | ----------------- | --------------- |
| C01           | Agent Lifecycle Management         | Agent Domain      | syscall         |
| C02           | Agent Orchestration                | OS Domain         | syscall         |
| C03           | Workflow Execution Engine          | OS Domain         | kernel          |
| C04           | Policy & Governance Enforcement    | OS Domain         | kernel          |
| C05           | Syscall Routing & Isolation        | OS Domain         | kernel          |
| C06           | Model Selection & Routing          | Agent Domain      | syscall         |
| C07           | Platform Integration Gateway       | OS Domain         | syscall         |
| C08           | Permission & Capability Control    | Compliance Domain | kernel          |
| C09           | State & Context Management         | OS Domain         | kernel          |
| C10           | Audit, Logging & Traceability      | Compliance Domain | kernel          |
| C11           | Rollback & Recovery Handling       | OS Domain         | kernel          |
| C12           | Extension & Custom Hook System     | OS Domain         | runtime         |
| C13           | Multi-Tenant Isolation             | OS Domain         | kernel          |
| C14           | Resource Quota & Throttling        | OS Domain         | kernel          |
| C15           | Versioning & Compatibility Control | OS Domain         | kernel          |

## Domain Capability Ownership

### OS Domain Capabilities (Supreme Authority)

- C01-C07, C09, C11-C15: Complete runtime control and orchestration
- C08, C10: Shared governance enforcement with Compliance Domain

### Business Domain Capabilities

- None (semantic sovereignty over business processes)

### Agent Domain Capabilities

- None (OS-mediated agent lifecycle and orchestration)

### Data Domain Capabilities

- None (OS-mediated data governance and analytics)

### Compliance Domain Capabilities

- C04: Shared governance enforcement
- C08, C10: Security and audit capabilities

---

**Owner:** Architecture Council
**Authority:** Constitutional Capability Registry
**Reference:** 03-capability-registry.md, 05-domain-governance.md

**This document establishes the authoritative capability-to-domain mapping. All implementations must align with these constitutional mappings.**

#### Principle 3: Runtime Enforcement Unity

All capabilities enforce through unified runtime surfaces.

```
ENFORCEMENT UNITY:
├── All capabilities route through OS kernel
├── Syscall interface provides unified access
