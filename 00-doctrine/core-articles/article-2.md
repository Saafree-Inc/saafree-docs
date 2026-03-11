# ARTICLE 2

## AUTHORITY LEVELS & RISK CLASSIFICATION

**Status:** Foundational Governance Article

---

### Article 2.1 – Principle of Graduated Authority

All delegated authority within the Saafree system shall be structured into explicit authority levels.

No AI Agent shall operate under undefined or implicit authority.

---

### Article 2.2 – Authority Levels

Saafree recognizes, at minimum, the following authority levels:

1. **Level 0 – Observational**

   * Read-only access
   * No execution capability

2. **Level 1 – Assistive Execution**

   * Executes predefined actions
   * Requires prior human approval

3. **Level 2 – Conditional Autonomy**

   * Executes within bounded conditions
   * Subject to runtime monitoring

4. **Level 3 – Limited Autonomous Operation**

   * Executes without prior approval
   * Restricted to low-risk, reversible actions

5. **Level 4 – High-Impact Delegated Authority**

   * Executes actions with significant impact
   * Requires enhanced safeguards and oversight

No authority level beyond those explicitly defined may be assumed.

---

### Article 2.3 – Risk Classification Principle

Every AI Agent action shall be classified according to risk prior to execution.

Risk classification shall consider:

* Potential harm to legally protected interests
* Irreversibility of outcomes
* Scale and propagation effects
* Degree of uncertainty

---

### Article 2.4 – Risk Categories

Saafree defines the following risk categories:

* **Low Risk:** Reversible, minimal impact actions
* **Medium Risk:** Bounded impact, partial reversibility
* **High Risk:** Significant or irreversible impact
* **Critical Risk:** Threats to safety, rights, or systemic stability

---

### Article 2.5 – Authority–Risk Alignment

An AI Agent may execute an action only if:

* Its authority level is equal to or greater than the classified risk level

Mismatches shall result in automatic denial or escalation.

---

### Article 2.6 – Dynamic Risk Reassessment

Risk classification shall be continuously reassessed at runtime.

If risk escalates beyond authorized thresholds, execution shall be:

* Suspended, or
* Escalated to human authority

---

### Article 2.7 – Prohibition of Risk Obfuscation

AI Agents shall not:

* Conceal risk
* Fragment actions to evade thresholds
* Reframe objectives to downgrade classification

Such behavior shall trigger immediate suspension.

---

---

**Implementation References:**
- **Technical Constitution**: `docs/01-layers/constitution/02-constitutional-principles.md` - Principles 4-7: Explicit Authority, Business Observability, etc.
- **Capability Registry**: `docs/01-layers/constitution/03-capability-registry.md` - C01-C15 capability definitions
- **Governance Model**: `docs/01-layers/constitution/04-governance-model.md` - Authority hierarchy and risk-based classification

**End of Article 2**
