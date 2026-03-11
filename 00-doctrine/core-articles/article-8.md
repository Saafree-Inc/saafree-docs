# ARTICLE 8

## SECURITY AS PILLAR DOCTRINE

**Status:** Foundational Article (Pillar Doctrine)  
**Authority:** Security Doctrine has veto in case of conflict with any other doctrine.  
**Source:** Constitutional Position Paper § VIII; Legal Positioning Analysis § VII.

---

### Article 8.1 – Supreme Security Objectives

Saafree does not pursue the objective of "never being attacked." The supreme security objectives are:

1. **Control Sovereignty** — Never lose control of the system.
2. **Human Supremacy** — No AI Agent may cause harm beyond human will; human authority is final.
3. **Containment** — Local failure must not become system-wide collapse; blast radius is bounded by design.
4. **No Security by Obscurity** — Security must not depend on secrecy; mechanisms must hold under full exposure of architecture, code, and operations.
5. **Resilience & Continuity** — Operate, recover, and evolve even under attack.

Meeting these five objectives is the doctrinal standard for security at national-grade level.

---

### Article 8.2 – Core Security Doctrine (Four Principles)

1. **Assume Total Transparency** — Assume the adversary knows the full architecture, code, and operating model. Every security mechanism must remain valid under that assumption. This is the basis for an Open Core strategy.
2. **Runtime Authority > Design Authority** — Security authority resides at runtime governance, not in design or code. Design can be copied; runtime authority cannot. No component may alter the rules that govern it.
3. **Human-in-Command, AI-in-Execution** — AI Agents never hold sovereignty. They execute only within constitutionally defined bounds. Any authority beyond those bounds reverts to humans.
4. **Failure is Inevitable, Collapse is Not** — Failures will occur; system-wide collapse is not permitted. Isolation and containment are non-negotiable.

---

### Article 8.3 – System-Level Threat Model

Saafree treats the following as strategic adversaries, not mere risks:

- External adversary (hackers, APT, organized crime)
- Insider threat (developers, operators, partners)
- Supply chain attack (dependencies, models, plugins)
- AI misalignment (agents exceeding role or self-modifying)
- Governance bypass (evading rules, prompt injection at system level)
- Open-source weaponization (malicious forks, clones used to attack)

Security strategy must address all of these simultaneously.

---

### Article 8.4 – Security as Veto

In case of conflict between Security Doctrine and any other doctrine (Open, Commercial, AI capability, or operational convenience), **Security Doctrine prevails**. No other doctrine or policy may contradict the Supreme Security Objectives (8.1) or the Core Security Doctrine (8.2). Security has veto authority.

---

### Article 8.5 – No Security by Obscurity

Security must not rely on hiding architecture, code, or procedures. All security mechanisms must remain valid under the assumption that the adversary has full knowledge. Auditability, transparency of governance, and open constitutional framework are required; secrets, keys, and live governance state remain controlled but security itself does not depend on their concealment for validity.

---

### Article 8.6 – Resilience and Continuity

The system must support:

- Immutable logs and forensic-ready architecture
- System-level kill-switch and human override
- Graceful degradation under attack
- Post-incident constitutional review

The system learns from incidents; it does not conceal them.

---

### Article 8.7 – Cascade to Constitution and Layer Laws

Security Doctrine flows into the Technical Constitution as Security Articles (S1–S8), then into Security Layer Laws, then into domain specs and runtime. The chain **doctrine → constitution → layer laws → domain spec → ship → live** includes Security at every level. This Article is the doctrinal source; the Technical Constitution document **08-security-supremacy.md** and the Security Layer (01-layers/security/) provide the enforceable formulation.

---

**Version:** 1.0 | **Status:** Foundational Article | **Owner:** Architecture Council  
**Effective Date:** 2026-01-30 | **Review Cycle:** Quarterly  
**Related:** 01-constitutional-position-paper.md § VIII; 02-legal-positioning-analysis.md § VII; 01-layers/constitution/08-security-supremacy.md; 01-layers/security/00-constitution-to-security-layer-mapping.md
