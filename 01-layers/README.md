---
doc-type: guide
authority: informational
status: active
owner: Architecture Council
created: 2026-01-16
last-reviewed: 2026-01-17
next-review: 2026-04-17
version: 3.0
mapped-capabilities: []
runtime-surfaces: []
enforcement-layer: documentation
---

# Core Platform Documentation

---

## 🎯 Overview

This directory contains documentation for the **Core Platform** of Saafree OS, organized by **authority hierarchy**:

### 📋 Authority Hierarchy & Legal Logic

#### **Legal Logic Flow:**
**🏛️ Constitution → ⚖️ Layer Laws → 📋 Domain Specs**

1. **🏛️ Constitutional Layer** - **Supreme Constitution** (doc-type: constitution, authority: supreme-law)
   - Supreme authority, foundational laws, immutable governance framework
   - Cannot be modified without Chủ tịch approval
   - **Defines WHAT must be done** (constitutional principles, capabilities, domains)

2. **⚖️ Layer Laws** - **Constitutional Implementation** (doc-type: law, authority: constitutional)
   - **Functional Layer**: Domain ownership and sovereignty boundaries (WHO owns WHAT)
   - **Logical Layer**: Conceptual behavior patterns and orchestration logic (HOW behavior works)
   - **Physical Layer**: Infrastructure implementation and deployment patterns (HOW deployment works)
   - Must comply with constitutional principles
   - **Defines HOW to implement within constitutional boundaries**

3. **📋 Domain Specs** - **Domain-Specific Implementation** (doc-type: spec, authority: constitutional)
   - Technical specifications and runtime contracts for each domain
   - Must comply with both constitution and layer laws
   - **Defines HOW each domain implements its constitutional role**

### 🎯 Layer Purpose

- **Constitution**: Defines what must be done (supreme authority)
- **Layer Laws**: Specify how to implement within constitutional boundaries

### 📊 Authority Metadata Hierarchy

| Authority Level             | doc-type     | authority      | status             | Modification Rights                             |
| --------------------------- | ------------ | -------------- | ------------------ | ----------------------------------------------- |
| **🏛️ Supreme Constitution** | constitution | supreme-law    | constitutional-law | Chủ tịch approval only                          |
| **📋 Layer Laws**           | law          | constitutional | layer-law          | Architecture Council (constitutional compliant) |

### ⚖️ Legal Analogy

- **Constitution** = Hiến Pháp Việt Nam (supreme, immutable)
- **Layer Laws** = Bộ Luật (tuân thủ hiến pháp, có thể sửa đổi theo quy trình)

---

## 🔒 Security Layer (Chuyên biệt – Không map xuống 14 domain)

**Vai trò:** Layer Security được giữ với **mục đích chuyên biệt**, không mapping trực tiếp xuống 14 domain để tránh trùng lặp với luồng dọc (Constitution 08 → Function/Logic/Physical → domain).

**Tác dụng:**

1. **Công thức hóa và tham chiếu:** Nơi chứa **bản formulation chính thức** của Security Constitution (S1–S8) dưới dạng layer laws (01–08 trong `01-layers/security/`) và mapping từ Hiến pháp (`00-constitution-to-security-layer-mapping.md`). Domain nhận yêu cầu security **qua layer cha** (Function/Logic/Physical), không qua mapping riêng Security Layer → domain.
2. **Khả năng security chuyên biệt (tương lai):** Chủ sở hữu các công cụ/tính năng security **cross-cutting**: lớp bảo vệ vòng ngoài (runtime monitoring, anomaly detection, kill-switch), quét và bảo vệ **plugin của đối tác** trên marketplace, supply-chain và integrity (S8). Tương tự “bộ chuyên trách” trong mô hình chính phủ.

**Chi tiết:** Xem `01-layers/security/README.md`.

---

## 🏗️ Five-Domain Architecture

Saafree OS is designed with a **Five-Domain Architecture** where Constitution governs all functional layers:

### **Domain Roles & Authority Levels**

#### **🏛️ OS Domain (Supreme Runtime Authority - First Among Equals)**
- **Constitutional Role**: Complete runtime control, syscall supremacy, platform abstraction
- **Authority Level**: Supreme runtime authority under constitutional delegation
- **Capabilities**: 11 capabilities (C03, C04, C05, C07, C09, C11, C12, C13, C14, C15)
- **Position**: **Runtime enforcer** - First among equals but equal sovereign with other domains

#### **💼 Business Domain (Process Sovereignty)**
- **Constitutional Role**: Business process semantics, value flow, business logic control
- **Capabilities**: 3 capabilities (C03, C04, C10)

#### **🤖 Agent Domain (Lifecycle Control)**
- **Constitutional Role**: AI agent lifecycle management under OS governance
- **Capabilities**: 3 capabilities (C01, C02, C06)
- **Restrictions**: No independent authority, mandatory OS syscall routing

#### **📊 Data Domain (Analytics Sovereignty)**
- **Constitutional Role**: Data governance, analytics control, storage strategy
- **Capabilities**: 1 capability (C10)

#### **🔒 Compliance Domain (Authority Constraints)**
- **Constitutional Role**: Security enforcement, regulatory compliance, audit trails
- **Capabilities**: 3 capabilities (C04, C08, C10)

### **Domain Structure Standards**

All functional domains follow the **01-domain-foundation/** pattern:

```
docs/02-domains/domain-of-function/{domain}/01-spec/
├── 01-{domain}-foundation/     ← Domain charter & constitutional role
├── 02-architecture-decisions/  ← Why decisions made
├── 03-architecture/           ← Technical architecture
├── 04-runtime-contracts/      ← Runtime specifications
├── 05-implementation-standards/ ← Implementation guidelines
├── 06-implementation-patterns/ ← Reference implementations
└── 07-domain-integration/     ← Domain boundaries & integration
```

### **OS Layer (11 Services - Production Ready)**

The OS Layer provides governance, runtime enforcement, and platform abstraction:

- **AMS** (Audit Management Service) - Compliance audit trails & reporting
- **AOS** (Agent Orchestration Service) - AI agent lifecycle management & orchestration
- **DPS** (Data Persistence Service) - Data storage, backup & recovery
- **GES** (Governance Enforcement Service) - Runtime policy enforcement
- **IHS** (Integration Hub Service) - External system integration
- **PAS** (Platform Abstraction Service) - Platform driver management (Largest - 18 files)
- **PMS** (Process Management Service) - Business process orchestration (15 files)
- **RMS** (Resource Management Service) - Resource allocation & quotas
- **SCS** (Scheduling Coordination Service) - Task scheduling & coordination
- **UMS** (User Management Service) - User lifecycle & permissions
- **WOS** (Workflow Orchestration Service) - Complex workflow orchestration

**Total:** 80 source files + 8 shared libraries

### Business Layer (57+ Microservices after Transformation)

The Business Layer consists of:

- **Platform Services** - 28 platforms (Facebook, Zalo, TikTok, YouTube, etc.)
- **Business Domain Services** - 12+ services (AI, Analytics, Collaboration, E-commerce, Media, etc.)
- **Infrastructure Services** - 6+ services (Authentication, API Keys, Notifications, Webhooks, Billing, Monitoring)

---

## 📂 Directory Structure

```
02-domains/domain-of-function/
├── constitution/                  ← Constitutional Law & Supreme Authority
│   ├── README.md                      ← Constitutional authority documentation
│   ├── 01-os-philosophy.md            ← AI Agent era philosophy and OS evolution
│   ├── 02-constitutional-principles.md ← Process Supremacy, Rule=Law, etc.
│   ├── 03-governance-model.md         ← Authority hierarchy and enforcement
│   ├── 04-capability-registry.md      ← Official capability registry
│   └── 05-layer-governance.md         ← Multi-layer governance model
│
├── domain-of-function/agent/                       ← Agent Layer Documentation (Migrating)
│   ├── README.md                      ← Agent layer overview and migration status
│   ├── agent-chat/                    ← AI agent chat systems
│   ├── agent-dual-role/               ← Dual-role agent capabilities
│   ├── agent-learning-training/       ← Agent learning & training systems
│   ├── agent-tools/                   ← Agent tool ecosystem
│   ├── agent-v5/                      ← Agent v5 architecture
│   ├── agent-voice/                   ← Voice agent systems
│   ├── 01-spec/                       ← Future: Agent specifications
│   ├── 02-ship/                       ← Future: Implementation & deployment
│   └── 03-live/                       ← Future: Production operations
│
├── domain-of-function/data/                        ← Data Layer Documentation (Migrating)
│   ├── README.md                      ← Data layer overview and migration status
│   ├── ai-models/                     ← AI model management systems
│   ├── analytics-engine/              ← Analytics processing engine
│   ├── analytics/                     ← Analytics capabilities & intelligence
│   ├── platform-analytics/            ← Platform-specific analytics
│   ├── storage/                       ← Data storage & persistence
│   ├── search/                        ← Search & indexing (migrated)
│   ├── services/                      ← Shared data services (migrated)
│   ├── 01-spec/                       ← Future: Data specifications
│   ├── 02-ship/                       ← Future: Implementation & deployment
│   └── 03-live/                       ← Future: Production operations
│
├── domain-of-function/compliance/                  ← Compliance Layer Documentation (Migrating)
│   ├── README.md                      ← Compliance layer overview and migration status
│   ├── ai-compliance/                 ← AI compliance requirements
│   ├── auth/                          ← Authentication & authorization systems
│   ├── crypto/                        ← Cryptographic standards & security
│   ├── legal-policies/                ← Legal compliance & regulatory frameworks
│   ├── 01-spec/                       ← Future: Compliance specifications
│   ├── 02-ship/                       ← Future: Implementation & deployment
│   └── 03-live/                       ← Future: Production operations
│
├── domain-of-function/os/                          ← OS Layer Documentation
│   ├── 01-spec/                       ← Specifications & Design (Normative Truth)
│   │   ├── 01-os-canon/              ← Core OS canonical specifications
│   │   ├── 02-core/                  ← Core system components
│   │   ├── 03-specifications/        ← Technical specifications
│   │   ├── 04-custom-features/       ← Custom feature specifications
│   │   ├── 05-api-routes-standards/  ← API routing standards
│   │   ├── 06-adrs/                  ← Architecture Decision Records
│   │   └── 07-reference-architectures/ ← Reference implementations
│   ├── 02-ship/                       ← Implementation & Deployment (Transitional Truth)
│   │   ├── 05-infrastructure-setup/  ← Infrastructure setup
│   │   └── 06-flow-forensic/         ← Flow analysis and debugging
│   ├── 03-live/                       ← Production Operations (Operational Truth)
│   ├── scripts/                       ← OS layer scripts and utilities
│   ├── ANALYSIS-AND-PROPOSAL.md      ← OS transformation analysis
│   ├── SYSTEM-IMPROVEMENT-PROPOSAL.md ← System improvement recommendations
│   └── README.md                      ← Legacy OS transformation documentation
│
└── domain-of-function/business/                    ← Business Layer Documentation
    ├── 01-spec/                       ← Business Specifications (Normative Truth)
    │   ├── 09-operations/            ← Operational specifications
    │   └── 10-compliance/            ← Compliance requirements
    │   ├── ai-dashboard/             ← AI dashboard implementations
    │   ├── ai-code-generation/       ← AI code generation features
    │   └── generate-content-hybrid/  ← Content generation systems
    ├── business-processes/           ← Business process definitions & workflows
    ├── platforms/                    ← Platform integrations & payment systems
    ├── user-experience/              ← User interface & experience features
    ├── 02-ship/                      ← Implementation & Integration (Transitional Truth)
    ├── 03-live/                      ← Production Business Operations (Operational Truth)
    └── README.md                     ← Business layer documentation
```

---

## 📋 Documentation Status

### OS Layer (`domain-of-function/os/`)

- ⚠️ **Status:** STRUCTURALLY ORGANIZED
- **Note:** Đã di chuyển vào cấu trúc Spec-Ship-Live chuẩn, nhưng cần tiếp tục tinh chỉnh nội dung
- **Current State:** 3 thư mục spec-ship-live đã được tổ chức trực tiếp trong domain-of-function/os/
- **Next Step:** Tiếp tục biên tập và tinh chỉnh nội dung theo governance standards

### Business Layer (`domain-of-function/business/`)

- ✅ **Status:** FULLY INTEGRATED & ORGANIZED
- **Note:** Đã merge content từ 02-domains/ và tổ chức theo layer structure
- **Current State:** Business processes, platforms, UX features đã được integrate
- **Next Step:** Organize content theo spec-ship-live pattern

---

## 🔗 Related Documentation

- **Architecture Overview:** `docs/00-restructuring/01-analysis.md`
- **Proposed Structure:** `docs/00-restructuring/02-proposed-structure.md`
- **Execution Plan:** `docs/00-restructuring/03-execution-plan.md`
- **Business Domains:** Integrated into `domain-of-function/business/` (completed)
- **Data Infrastructure:** Reorganized 2026-02-01 - see `domain-of-function/data/infrastructure-services-MIGRATION.md`
- **Technical Infrastructure:** `docs/03-infrastructure/`
- **Development Standards:** `docs/04-standards/`

---

## 🎯 Navigation Guide

### For Constitutional Layer Documentation:

1. Start with `constitution/README.md` for supreme authority and constitutional law
2. Read `constitution/01-os-philosophy.md` for AI Agent era philosophy
3. Review `constitution/02-constitutional-principles.md` for core principles
4. Check `constitution/04-capability-registry.md` for official capabilities

### For Agent Layer Documentation:

1. Start with `domain-of-function/agent/README.md` for AI agent capabilities overview
2. Review `domain-of-function/agent/agent-chat/` for chat and communication systems
3. Check `domain-of-function/agent/agent-learning-training/` for training systems
4. Explore `domain-of-function/agent/agent-v5/` for next-generation architecture

### For Data Layer Documentation:

1. Start with `domain-of-function/data/README.md` for data management overview
2. Review `domain-of-function/data/ai-models/` for AI model management systems
3. Check `domain-of-function/data/analytics-engine/` for analytics processing
4. Explore `domain-of-function/data/storage/` for data persistence infrastructure

### For Compliance Layer Documentation:

1. Start with `domain-of-function/compliance/README.md` for security and compliance overview
2. Review `domain-of-function/compliance/auth/` for authentication and authorization systems
3. Check `domain-of-function/compliance/legal-policies/` for legal compliance frameworks
4. Explore `domain-of-function/compliance/crypto/` for cryptographic standards

### For OS Layer Documentation:

1. Start with `domain-of-function/os/01-spec/` for OS specifications and canonical definitions
2. Check `domain-of-function/os/02-ship/` for implementation progress and deployment status
3. Refer to `domain-of-function/os/03-live/` for production operations and monitoring

### For Business Layer Documentation:

1. Start with `domain-of-function/business/01-spec/` for business requirements and domain specifications
2. Review `domain-of-function/business/01-spec/ai-dashboard/` for AI dashboards and user interfaces
3. Check `domain-of-function/business/01-spec/ai-code-generation/` for AI code generation features
4. Explore `domain-of-function/business/02-ship/` for implementation status and integration progress
5. Refer to `domain-of-function/business/03-live/` for business operations and optimization

---

## ⚠️ Important Notes

1. **Truth Hierarchy:** Spec (Normative Truth) → Ship (Transitional Truth) → Live (Operational Truth)
   - Live **KHÔNG ĐƯỢC** override Spec
   - Ship **KHÔNG BAO GIỜ** trở thành Spec
   - Mọi sai lệch Live vs Spec → ghi RFC

2. **Pattern Spec-Ship-Live:** Áp dụng cho các thư mục có đầy đủ 3 giai đoạn: thiết kế, thi công, và vận hành production

3. **Documentation Standards:** Tuân thủ standards từ `docs/99-docs-governance/`

4. **Structural Changes:** Đã di chuyển nội dung từ sub-folders ra trực tiếp trong domain-of-function/os/ và domain-of-function/business/ để có cấu trúc spec-ship-live chuẩn
5. **Domain Integration:** Đã merge 02-domains/ content vào các functional layers (business-layer, data-layer)
6. **Layer Consolidation:** Tất cả business domains, data infrastructure, và platform integrations đã được consolidate theo layer architecture

---

**Maintained by:** Architecture & Platform Council
**Last Updated:** 2026-01-16
