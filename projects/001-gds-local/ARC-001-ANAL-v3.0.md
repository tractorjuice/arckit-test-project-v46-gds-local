# Architecture Governance Analysis Report: GDS Local

> **Template Status**: Beta | **Version**: 3.0 | **Command**: `/arckit.analyze`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-ANAL-v3.0 |
| **Document Type** | Governance Analysis Report |
| **Project** | GDS Local (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 3.0 |
| **Created Date** | 2026-03-01 |
| **Last Modified** | 2026-03-01 |
| **Review Cycle** | Monthly |
| **Next Review Date** | 2026-03-31 |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | GDS Local Programme Team, Architecture Team, GDS Director General, MHCLG Digital, LGA |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-28 | ArcKit AI | Initial creation from `/arckit:analyze` command | PENDING | PENDING |
| 2.0 | 2026-02-28 | ArcKit AI | Refreshed analysis with updated artifact context | PENDING | PENDING |
| 3.0 | 2026-03-01 | ArcKit AI | Comprehensive analysis across 11 artifacts including Service Assessment, Diagram, and Plan | PENDING | PENDING |

---

## Executive Summary

**Overall Status**: ⚠️ Issues Found

**Key Metrics**:

- Total Requirements: 46 (6 BR, 10 FR, 20 NFR, 5 INT, 5 DR)
- Requirements Coverage (Context Diagram): 100% at Level 1; 0% at HLD/DLD detail
- Critical Issues: 3
- High Priority Issues: 6
- Medium Priority Issues: 8
- Low Priority Issues: 3

**Recommendation**: RESOLVE CRITICAL ISSUES FIRST — The project has exceptionally strong governance foundations (stakeholder analysis, risk register, business case, requirements) but is missing three critical compliance artifacts (DPIA, Secure by Design assessment, and formal Architecture Decision Records) that must be produced before entering Alpha. No design documents (HLD/DLD) exist yet, which is expected at this stage but limits traceability validation.

---

## Findings Summary

| ID | Category | Severity | Location(s) | Summary | Recommendation |
|----|----------|----------|-------------|---------|----------------|
| C1 | UK Gov Compliance | CRITICAL | Missing artifact | No DPIA despite cross-service citizen data sharing with special category data | Run `/arckit:dpia` before Alpha |
| C2 | UK Gov Compliance | CRITICAL | Missing artifact | No Secure by Design assessment despite PII processing across organisational boundaries | Run `/arckit:secure` before Alpha |
| C3 | Governance | CRITICAL | Missing artifact | No formal Architecture Decision Records — 4 decisions exist informally in DIAG only | Run `/arckit:adr` for each decision |
| H1 | UK Gov Compliance | HIGH | Missing artifact | No TCoP assessment despite UK Government project requiring spend controls | Run `/arckit:tcop` |
| H2 | Data Model | HIGH | Missing artifact | No data model despite 5 DR-xxx requirements — GDPR data mapping incomplete | Run `/arckit:data-model` |
| H3 | Traceability | HIGH | Missing artifact | No formal traceability matrix — traceability scattered across artifacts | Run `/arckit:traceability` |
| H4 | Risk Management | HIGH | ARC-001-RISK-v1.0 | 7 risks exceed programme risk appetite without formal escalation/acceptance record | Obtain formal acceptance from Programme Board |
| H5 | Traceability | HIGH | ARC-001-REQ-v1.0 Appendix C | Only 16/46 requirements (35%) have direct traceability to stakeholder goals | Extend traceability table to cover NFR, INT, DR |
| H6 | Design Coverage | HIGH | Missing artifact | No HLD or DLD — design coverage cannot be validated beyond context diagram | Produce HLD during Alpha phase |
| M1 | Document Control | MEDIUM | All artifacts | All document owners show `[OWNER_NAME_AND_ROLE]` placeholder | Assign document owners |
| M2 | Document Control | MEDIUM | All artifacts | All 11 documents in DRAFT status with PENDING approvals — no formal review cycle completed | Establish approval workflow |
| M3 | UK Gov Compliance | MEDIUM | Missing artifact | No formal threat model documented (SVCASS Point 9 gap) | Produce threat model during Alpha |
| M4 | UK Gov Compliance | MEDIUM | ARC-001-SVCASS-v1.0 | No explicit open source code strategy — repository, licensing, publication approach undefined | Document open source strategy |
| M5 | Requirements Quality | MEDIUM | ARC-001-REQ-v1.0 | No explicit DR-xxx requirements for citizen consent records or citizen data subject access request handling | Add DR-006 and DR-007 for consent and SAR data |
| M6 | Architecture | MEDIUM | Missing artifact | No Wardley Map — strategic positioning decisions lack formal evolutionary analysis | Run `/arckit:wardley` |
| M7 | Consistency | MEDIUM | ARC-001-REQ-v1.0:L112 | BR-001 references both P13 and P16 as "Reuse Government Platforms" — duplicate or miscoded principle | Verify principle numbering |
| M8 | Service Assessment | MEDIUM | ARC-001-SVCASS-v1.0 | 9 of 14 Service Standard points rated Amber — significant evidence gaps for Alpha assessment | Address critical SVCASS recommendations |
| L1 | Consistency | LOW | ARC-001-REQ-v1.0 | MoSCoW priorities use "MUST_HAVE" / "SHOULD_HAVE" format while requirement text uses RFC 2119 "MUST" / "SHOULD" — minor style inconsistency | Standardise to one convention |
| L2 | Consistency | LOW | ARC-001-REQ-v1.0 vs ARC-001-RISK-v1.0 | Risk IDs differ between REQ (R-1 to R-5 summary) and RISK register (R-001 to R-020 detailed) — cosmetic but confusing | Align to R-xxx format consistently |
| L3 | Documentation | LOW | ARC-001-DIAG-001-v1.0 | Cloud provider listed as "TBC" — acceptable at this stage but decision needed before Alpha | Confirm cloud provider during research phase |

---

## Requirements Analysis

### Requirements Inventory

| Category | Prefix | Count | MUST | SHOULD | MAY |
|----------|--------|-------|------|--------|-----|
| Business Requirements | BR-xxx | 6 | 6 | 0 | 0 |
| Functional Requirements | FR-xxx | 10 | 8 | 2 | 0 |
| Non-Functional: Performance | NFR-P-xxx | 2 | 2 | 0 | 0 |
| Non-Functional: Availability | NFR-A-xxx | 3 | 3 | 0 | 0 |
| Non-Functional: Scalability | NFR-S-xxx | 1 | 1 | 0 | 0 |
| Non-Functional: Security | NFR-SEC-xxx | 5 | 5 | 0 | 0 |
| Non-Functional: Compliance | NFR-C-xxx | 4 | 4 | 0 | 0 |
| Non-Functional: Usability | NFR-U-xxx | 2 | 1 | 1 | 0 |
| Non-Functional: Maintainability | NFR-M-xxx | 3 | 2 | 1 | 0 |
| Integration Requirements | INT-xxx | 5 | 2 | 3 | 0 |
| Data Requirements | DR-xxx | 5 | — | — | — |
| **Total** | | **46** | **34** | **7** | **0** |

**Priority Distribution Assessment**: Reasonable. 74% MUST_HAVE, 15% SHOULD_HAVE, 11% unclassified (DR-xxx). The requirements are well-prioritised with clear MoSCoW categorisation.

### Requirements Quality Assessment

**Strengths**:
- All functional requirements have structured acceptance criteria with Given/When/Then format
- Clear use cases (UC-1 to UC-3) with actors, preconditions, main flow, alternative flows, and exception flows
- 5 well-defined user personas with roles, goals, and pain points
- 4 requirement conflicts formally documented with trade-off analysis and resolution strategies
- Measurable success criteria with specific numeric targets (50 councils, £50M, 99.9% availability)

**Issues**:
- 5 assumptions (A-1 to A-5) need validation plans — A-5 (DSIT funding) noted as "At Risk" in dependencies table
- No DR-xxx requirements for citizen consent records (needed for FR-010) or data subject access request handling (needed for NFR-C-001)
- DR-xxx requirements lack explicit priority classification (no MoSCoW)

### Requirements Coverage Matrix (System Context Diagram)

| Requirement Category | Total | Covered in DIAG | Partially Covered | Not Covered |
|---------------------|-------|-----------------|-------------------|-------------|
| BR-xxx | 6 | 6 (100%) | 0 | 0 |
| FR-xxx | 10 | 10 (100%) | 0 | 0 |
| INT-xxx | 5 | 5 (100%) | 0 | 0 |
| NFR-xxx | 20 | 0 | 20 (noted) | 0 |
| DR-xxx | 5 | 0 | 5 (noted) | 0 |
| **Total** | **46** | **21 (46%)** | **25 (54%)** | **0** |

> **Note**: The System Context Diagram (C4 Level 1) explicitly maps all 21 BR, FR, and INT requirements. NFR and DR requirements are referenced in the diagram's non-functional and data flow sections but cannot be fully validated without a C4 Container Diagram (Level 2), HLD, and DLD. This is expected at the current project stage.

---

## Architecture Principles Compliance

| # | Principle | Requirements | Design Coverage | Status |
|---|-----------|-------------|-----------------|--------|
| P1 | User-Centred Design | BR-004, NFR-U-001 | DIAG personas, SVCASS Points 1-5 | ✅ COMPLIANT |
| P2 | Simplicity / Scalability | NFR-P-002, NFR-S-001 | DIAG scalability section | ✅ COMPLIANT |
| P3 | Resilience and Fault Tolerance | NFR-A-001 to A-003 | DIAG availability section | ✅ COMPLIANT |
| P4 | Interoperability / Open Standards | BR-001, INT-001 to INT-005 | DIAG Decision 4: open standards only | ✅ COMPLIANT |
| P5 | Security by Design | NFR-SEC-001 to SEC-005 | DIAG security architecture | ⚠️ PARTIAL — no formal SbD assessment |
| P6 | Accessibility by Default | NFR-C-002 | DIAG WCAG 2.2 AA mandate | ✅ COMPLIANT |
| P7 | Observability | NFR-M-001 | DIAG monitoring section | ✅ COMPLIANT |
| P8 | Central-Local Collaboration | BR-004, BR-006 | DIAG Decision 3: voluntary pathfinder | ✅ COMPLIANT |
| P9 | Cross-Service Data Sharing | BR-002, FR-004 | DIAG Decision 2: governed sharing | ✅ COMPLIANT |
| P10 | Federated Identity | FR-001, INT-001 | DIAG Decision 1: OneLogin extension | ✅ COMPLIANT |
| P11 | Data Sovereignty | NFR-C-001, TC-4 | DIAG UK sovereign data centres | ✅ COMPLIANT |
| P13 | Reuse Government Platforms | BR-001, INT-001 to INT-004 | DIAG reuses OneLogin, Notify, Pay | ✅ COMPLIANT |
| P14 | Loose Coupling | NFR-A-003, NFR-M-002 | DIAG circuit breaker, API versioning | ✅ COMPLIANT |
| P23 | Open Source by Default | NFR-M-003 | DIAG open source noted | ⚠️ PARTIAL — no open source strategy |
| P24 | GDS Service Standard | BR-005, NFR-C-003 | SVCASS: 5G/9A/0R | ⚠️ PARTIAL — assessment gaps |
| P25 | Spend Controls and VfM | BR-003 | SOBC BCR 2.8:1 | ✅ COMPLIANT |

**Critical Principle Violations**: 0
**Partial Compliance**: 3 (P5 Security by Design, P23 Open Source, P24 GDS Service Standard)

---

## Stakeholder Traceability Analysis

**Stakeholder Analysis Exists**: ✅ Yes (ARC-001-STKE-v1.0)

**Stakeholder-Requirements Coverage**:

- Requirements with direct goal traceability (BR + FR): 16/46 (35%) — all 6 BR and all 10 FR have explicit "Relates To" goal references
- Orphan requirements (no stakeholder justification): 30 (NFR, INT, DR) — these are supporting requirements that inherit traceability through their parent BR/FR
- Requirement conflicts documented and resolved: ✅ Yes — 4 conflicts (C-1 to C-4) with formal trade-off analysis

**RACI Governance Alignment**:

| Artifact | Role | Aligned with RACI? | Issues |
|----------|------|-------------------|--------|
| Risk Register | Risk Owners | ✅ Yes | All 20 risk owners from stakeholder RACI matrix |
| SOBC | Benefits Owners | ✅ Yes | All 6 benefits mapped to goal owners |
| Requirements | Stakeholder mapping | ⚠️ Partial | 16/46 formally traced; remaining 30 inherit through BR/FR chain |
| Data Model | Data Owners | ❌ No data model exists | Missing artifact — no data governance assignments |
| Service Assessment | Assessment roles | ✅ Yes | SVCASS references all relevant stakeholder groups |

**Critical Issues**:
- 30 NFR/INT/DR requirements lack direct stakeholder goal traceability — the chain exists (e.g., NFR-SEC-002 supports BR-002 which supports G-2) but is not formally documented for all requirements
- No data model means data governance roles from RACI are not applied to specific data entities

---

## Risk Management Analysis

**Risk Register Exists**: ✅ Yes (ARC-001-RISK-v1.0)

**Risk Profile Summary**:

| Risk Level | Inherent | Residual |
|------------|----------|----------|
| Critical (20-25) | 0 | 0 |
| High (13-19) | 8 | 0 |
| Medium (6-12) | 12 | 18 |
| Low (1-5) | 0 | 2 |
| **Total Score** | **248** | **160** |

**Overall Risk Reduction**: 35% from controls — all 8 High risks reduced to Medium

**Risks Exceeding Programme Appetite**:

| Risk ID | Title | Category | Residual | Appetite | Excess | Required Action |
|---------|-------|----------|----------|----------|--------|-----------------|
| R-001 | Insufficient local authority adoption | STRATEGIC | 12 | 9 | +3 | Formal Programme Board acceptance |
| R-002 | Ministerial direction or MoG change | STRATEGIC | 10 | 9 | +1 | GDS DG formal acceptance |
| R-004 | GDS platform team capacity | OPERATIONAL | 9 | 8 | +1 | GDS DG formal acceptance |
| R-008 | Programme funding not sustained | FINANCIAL | 10 | 8 | +2 | GDS DG / DSIT Finance acceptance |
| R-011 | Data sharing privacy breach | COMPLIANCE | 10 | 6 | +4 | MHCLG Digital Director escalation |
| R-012 | UK GDPR non-compliance | COMPLIANCE | 8 | 6 | +2 | MHCLG Digital Director escalation |
| R-015 | Parliamentary scrutiny | REPUTATIONAL | 9 | 8 | +1 | GDS DG formal acceptance |

**Risk-Requirements Alignment**: ✅ Strong
- R-001 (adoption) mitigated by BR-006 (voluntary model), FR-002 (onboarding portal)
- R-011 (data breach) mitigated by NFR-C-001 (GDPR), NFR-SEC-004 (audit logging), FR-005 (governance dashboard)
- R-013 (accessibility) mitigated by NFR-C-002 (WCAG 2.2 AA)
- All top 10 risks have requirements coverage

**Risk-SOBC Alignment**: ✅ Strong
- Top 10 risks reflected in SOBC Management Case Part E ✅
- Financial risks (R-008, R-009, R-010) reflected in Financial Case ✅
- Strategic risks (R-001, R-002) reflected in Strategic Case "Why Now?" ✅
- Risk appetite analysis included in Risk Register ✅

**Risk Governance**:
- Risk owners from stakeholder RACI: ✅ Yes (all 20 owners traceable to STKE)
- Risk appetite defined per category: ✅ Yes
- Monthly review cadence established: ✅ Yes (recommended before pathfinder onboarding)
- 7 risks require formal escalation/acceptance — **no evidence of formal acceptance yet** (Finding H4)

---

## Business Case Analysis

**SOBC Exists**: ✅ Yes (ARC-001-SOBC-v1.0)

**Benefits Traceability**:

| Benefit ID | Description | Stakeholder Goal | Requirements | Measurable? | Status |
|------------|-------------|------------------|--------------|-------------|--------|
| B-001 | Council procurement savings (£50M) | G-4 (LGA) | BR-003, FR-007 | ✅ Yes | ✅ Complete |
| B-002 | Technology cost avoidance (£13M) | G-1, G-3 | BR-001, FR-001 to FR-003 | ✅ Yes | ✅ Complete |
| B-003 | Citizen outcome improvement (£4M) | G-2 (O-2) | BR-002, FR-004 | ✅ Yes | ✅ Complete |
| B-004 | Citizen time savings (£6.5M) | G-1 (O-1) | BR-001, FR-001 | ✅ Yes | ✅ Complete |
| B-005 | Council IT staff productivity (£5.5M) | G-3 (O-3) | BR-001 | ✅ Yes | ✅ Complete |
| B-006 | Compliance cost reduction (£1.7M) | G-5 | BR-005, NFR-C-003 | ✅ Yes | ✅ Complete |

**Benefits Coverage**:

- Total benefits: 6
- Benefits traced to stakeholder goals: 100%
- Benefits supported by requirements: 100%
- Benefits measurable and verifiable: 100%

**Option Analysis Quality**:
- Do Nothing baseline included: ✅ Yes (Option 0)
- Options analyzed: 4 (Do Nothing, Minimal, Balanced, Comprehensive)
- Recommended option: Option 2 (Balanced) — BCR 2.8:1
- Sensitivity analysis: ✅ Comprehensive (5 scenarios including optimism bias)
- Optimism bias applied: ✅ 40% uplift per Green Book — BCR still 2.0:1

**SOBC-Requirements Alignment**:
- Strategic Case drivers reflected in requirements: ✅ Yes — all 7 primary drivers mapped
- Economic Case benefits achievable with requirements: ✅ Yes — all benefits traced to requirements
- Financial Case budget adequate: ✅ Yes — sensitivity shows positive BCR at +30% cost
- Management Case delivery plan realistic: ✅ Yes — phased approach aligns with PLAN

**Business Case Score**: Excellent — no material issues

---

## Data Model Analysis

**Data Model Exists**: ❌ No (RECOMMENDED — Finding H2)

**Data Requirements in Scope**: 5 DR-xxx requirements (DR-001 to DR-005)

| DR ID | Description | Classification | Retention | Entity Mapping | Status |
|-------|-------------|---------------|-----------|----------------|--------|
| DR-001 | Council registration data | OFFICIAL | Active + 2 years | ❌ No entity model | ⚠️ Unmapped |
| DR-002 | Identity federation data | OFFICIAL-SENSITIVE | 90 days / 7 years | ❌ No entity model | ⚠️ Unmapped |
| DR-003 | Data sharing audit logs | OFFICIAL-SENSITIVE | 7 years (tamper-evident) | ❌ No entity model | ⚠️ Unmapped |
| DR-004 | Data sharing agreements | OFFICIAL | Active + 7 years | ❌ No entity model | ⚠️ Unmapped |
| DR-005 | Community engagement data | OFFICIAL | Active; anonymised | ❌ No entity model | ⚠️ Unmapped |

**Missing Data Requirements**:
- No DR-xxx for citizen consent records (needed by FR-010: Citizen Consent Management)
- No DR-xxx for data subject access request (SAR) handling (needed by NFR-C-001 data subject rights)
- No DR-xxx for incident/breach notification records (needed by NFR-C-001 breach notification requirement)

**Data Governance**:
- Data owners not assigned to specific entities: ❌ (no data model)
- PII identification: ⚠️ Partial — PII handling documented in DIAG data flow section but not in formal entity model
- GDPR compliance mapping: ⚠️ Partial — lawful basis referenced in DIAG but not mapped per entity

**Recommendation**: Run `/arckit:data-model` to create formal entity model with GDPR compliance, data governance matrix, and CRUD access patterns.

---

## Design Quality Analysis

### HLD Analysis

**HLD Exists**: ❌ No

> **Context**: No High-Level Design document exists. This is expected at the current project stage (pre-Alpha). The System Context Diagram (ARC-001-DIAG-001-v1.0) provides C4 Level 1 architecture with component inventory, technology choices, security architecture, and deployment architecture — functioning as a lightweight architectural overview. A formal HLD should be produced during Alpha (PLAN: weeks 13-32).

### DLD Analysis

**DLD Exists**: ❌ No

> **Context**: Expected. DLD is produced during Beta (PLAN: weeks 33-68).

### System Context Diagram Quality

**Diagram Exists**: ✅ Yes (ARC-001-DIAG-001-v1.0)

| Aspect | Status | Assessment |
|--------|--------|------------|
| Requirements Coverage | 46% explicit (21/46), 100% referenced | All BR, FR, INT mapped; NFR/DR noted |
| Principles Alignment | ✅ Strong | TCoP points mapped, technology choices aligned |
| Security Architecture | ✅ Strong | 5 security zones, 7 security controls, zero-trust, encryption |
| Integration Design | ✅ Strong | 6 external systems mapped with protocols, SLAs, and error handling |
| 4 Architecture Decisions | ✅ Documented | Decisions 1-4 with context, rationale, consequences |
| Component Evolution | ✅ Strong | Wardley evolution stages estimated; BUILD/BUY/USE alignment verified |

---

## UK Government Compliance Analysis

### GDS Service Standard (14 Points)

**Assessment Document**: ARC-001-SVCASS-v1.0

| Point | Requirement | Status | Key Gap |
|-------|-------------|--------|---------|
| 1 | Understand users and their needs | 🟡 Amber | No primary user research; no prototype testing |
| 2 | Solve a whole problem for users | 🟢 Green | Strong end-to-end problem definition |
| 3 | Joined up experience across channels | 🟡 Amber | No explicit channel strategy; no assisted digital plan |
| 4 | Make the service simple to use | 🟡 Amber | No prototype usability testing evidence |
| 5 | Make sure everyone can use the service | 🟡 Amber | No assistive technology testing plan |
| 6 | Have a multidisciplinary team | 🟢 Green | Team structure defined in PLAN and SOBC |
| 7 | Use agile ways of working | 🟢 Green | Scrum within GDS Agile Delivery framework |
| 8 | Iterate and improve frequently | 🟡 Amber | No iteration evidence yet (pre-Alpha) |
| 9 | Create a secure service | 🟡 Amber | **No SbD assessment, no DPIA, no threat model** |
| 10 | Define what success looks like | 🟢 Green | Comprehensive KPIs in REQ and PLAN |
| 11 | Choose the right tools and technology | 🟡 Amber | Technology choices sound but cloud provider TBC |
| 12 | Make new source code open | 🟡 Amber | **No open source strategy documented** |
| 13 | Use and contribute to open standards | 🟢 Green | OIDC, SAML, REST, OAuth 2.0 mandated |
| 14 | Operate a reliable service | 🟡 Amber | SLAs defined but no operational runbooks |

**Service Standard Summary**: 5 Green, 9 Amber, 0 Red

### Technology Code of Practice

**TCoP Assessment Exists**: ❌ No formal assessment document

**Informal TCoP Evidence** (from DIAG and REQ):

| TCoP Point | Evidence Found | Formal Assessment |
|------------|---------------|-------------------|
| 1. Define user needs | STKE, REQ, RSCH | ❌ Not assessed |
| 2. Make things accessible | NFR-C-002 (WCAG 2.2 AA) | ❌ Not assessed |
| 3. Be open and use open source | NFR-M-003 | ❌ Not assessed |
| 4. Make use of open standards | DIAG Decision 4, NFR-M-002 | ❌ Not assessed |
| 5. Use cloud first | DIAG (cloud-hosted, TC-4) | ❌ Not assessed |
| 6. Make things secure | NFR-SEC-001 to 005 | ❌ Not assessed |
| 7. Make privacy integral | NFR-C-001 (UK GDPR) | ❌ Not assessed |
| 8. Share, reuse and collaborate | BR-001 (GDS platforms), FR-003 | ❌ Not assessed |
| 9. Integrate and adapt technology | INT-001 to INT-005 | ❌ Not assessed |
| 10. Make better use of data | BR-002, FR-004 | ❌ Not assessed |
| 11. Define your purchasing strategy | SOBC Part C (Commercial Case) | ❌ Not assessed |
| 12. Meet the Service Standard | BR-005, SVCASS | ❌ Not assessed |
| 13. Spend controls | SOBC Part D (Financial Case) | ❌ Not assessed |

**Recommendation**: Run `/arckit:tcop` to produce formal TCoP assessment with evidence mapping and RAG ratings.

### Secure by Design

**SbD Assessment Exists**: ❌ No (Finding C2)

**Security Evidence in Existing Artifacts**:
- DIAG: 5 security zones, 7 security controls, zero-trust architecture, encryption standards
- REQ: 5 NFR-SEC requirements covering zero-trust, tenant isolation, encryption, audit logging, vulnerability management
- RISK: R-011 (data breach), R-012 (GDPR non-compliance) with mitigations

**Missing**:
- Formal threat model (STRIDE or equivalent)
- NCSC Secure by Design principles assessment
- Cyber Essentials Plus compliance plan
- Penetration testing plan

**Recommendation**: Run `/arckit:secure` before Alpha to produce formal SbD assessment.

### DPIA

**DPIA Exists**: ❌ No (Finding C1)

**Why This Is Critical**:
- FR-004 processes citizen data across organisational boundaries (housing, health, social care)
- Special category data (health, social care status) is involved
- Multiple data controllers (10+ councils) create complex controllership
- UK GDPR Article 35 mandates DPIA for high-risk processing
- SVCASS Point 9 identifies this as the most critical assessment gap

**Recommendation**: Run `/arckit:dpia` before any data sharing pilot engagement.

### AI Playbook / ATRS

**AI Risk Level**: N/A — GDS Local Platform does not include AI/ML components in current scope (confirmed in DIAG).

---

## Traceability Analysis

**Traceability Matrix**: ❌ Does not exist (Finding H3)

**Forward Traceability** (Requirements → Design):

| Chain | Coverage | Evidence |
|-------|----------|---------|
| Requirements → Context Diagram | 100% | DIAG requirements traceability table (21 explicit + 25 noted) |
| Requirements → HLD | 0% | No HLD exists |
| Requirements → DLD | 0% | No DLD exists |
| Requirements → Tests | 0% | No test plan exists |
| Requirements → Stakeholder Goals | 35% direct | 16/46 requirements formally traced in REQ Appendix C |
| Requirements → Principles | ~70% | Most requirements cite principle alignment |

**Backward Traceability** (Design → Requirements):

| Chain | Coverage | Evidence |
|-------|----------|---------|
| DIAG → Requirements | 100% | All DIAG components map to requirements |
| DIAG → Principles | ✅ | TCoP point mapping and principle alignment in DIAG |

**Gap Summary**:
- 0 requirements with zero design acknowledgement (all referenced in DIAG)
- 30 requirements without direct stakeholder goal traceability (inherit through BR/FR chain)
- No formal traceability matrix — traceability exists but is scattered across artifacts
- No HLD/DLD means detailed design validation is impossible

---

## Consistency Across Artifacts

### Terminology Consistency

| Term | REQ | STKE | RISK | SOBC | DIAG | Status |
|------|-----|------|------|------|------|--------|
| GDS Local | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ Consistent |
| Stakeholder IDs (SD-1 to SD-11) | ✅ | ✅ | ✅ | ✅ | — | ✅ Consistent |
| Goal IDs (G-1 to G-6) | ✅ | ✅ | ✅ | ✅ | — | ✅ Consistent |
| Risk IDs (R-001 to R-020) | ⚠️ R-1 to R-5 | — | ✅ | ✅ | — | ⚠️ Minor inconsistency (Finding L2) |
| MoSCoW format | MUST_HAVE | — | — | — | — | ✅ Consistent within REQ |
| Priority RFC 2119 | MUST/SHOULD | — | — | — | — | ⚠️ Mixed with MoSCoW (Finding L1) |

### Technology Stack Consistency

| Technology | REQ | DIAG | PLAN | SOBC | Status |
|------------|-----|------|------|------|--------|
| OIDC / SAML 2.0 | ✅ | ✅ | ✅ | ✅ | ✅ Consistent |
| REST APIs | ✅ | ✅ | ✅ | ✅ | ✅ Consistent |
| TLS 1.3 / AES-256 | ✅ | ✅ | — | — | ✅ Consistent |
| GOV.UK Design System | ✅ | ✅ | — | — | ✅ Consistent |
| Cloud provider | TBC | TBC | TBC | AWS (mentioned) | ⚠️ SOBC references "AWS UK" but DIAG says TBC |

### Budget Consistency

| Source | Programme Cost | Operational | Total TCO |
|--------|---------------|-------------|-----------|
| REQ | £18-29M | £2.5-3.5M/yr | — |
| SOBC | £29.6M (high), £24M (mid) | £3.3M/yr (steady-state) | £38.2M (3-yr) |
| PLAN | £24M programme | £8.6M operational | £38.2M (3-yr) |

**Assessment**: Budget figures are consistent within ROM ranges. REQ gives the broadest range (±40%); SOBC and PLAN converge on £24M midpoint / £38.2M TCO. Minor discrepancy: SOBC references "Platform hosting (AWS UK)" specifically while DIAG states cloud provider is TBC.

---

## Security & Compliance Summary

### Security Posture

- Security requirements defined: ✅ Yes (5 NFR-SEC requirements)
- Threat model documented: ❌ No (Finding M3)
- Security architecture in DIAG: ✅ Yes (5 zones, 7 controls, zero-trust)
- Secure by Design assessment: ❌ No (Finding C2)
- Security testing plan: ⚠️ Partial (PLAN references SAST/DAST/pentest but no formal plan)

**Security Coverage**: 65% — strong requirements and architecture, missing formal assessments

### Compliance Posture

- UK GDPR requirements identified: ✅ Yes (NFR-C-001)
- DPIA completed: ❌ No (Finding C1)
- WCAG 2.2 AA planned: ✅ Yes (NFR-C-002)
- GDS Service Standard: ⚠️ 5G/9A/0R (SVCASS)
- NCSC engagement planned: ✅ Yes (in requirements and PLAN)
- Audit readiness: ⚠️ Partial — NAO-ready benefits tracking planned but no formal audit framework

**Compliance Coverage**: 55% — requirements comprehensive but formal assessments missing

---

## Recommendations

### Critical Actions (MUST resolve before Alpha)

1. **[C1] Complete Data Protection Impact Assessment**: Cross-service citizen data sharing with special category data (health, social care) mandates DPIA under UK GDPR Article 35. This is the single most important compliance gap.
   - Run: `/arckit:dpia`
   - Owner: MHCLG Digital Director / DPO
   - Timeline: 3-4 weeks

2. **[C2] Complete Secure by Design Assessment**: Processing citizen PII across organisational boundaries requires formal SbD assessment with threat model, NCSC guidance mapping, and Cyber Essentials Plus baseline.
   - Run: `/arckit:secure`
   - Owner: Security Architect
   - Timeline: 2-3 weeks

3. **[C3] Create formal Architecture Decision Records**: 4 architecture decisions exist informally in the System Context Diagram. These need formal ADR treatment for governance audit trail, especially Decision 2 (data sharing approach) which has significant compliance implications.
   - Run: `/arckit:adr` (4 times, one per decision)
   - Owner: Programme Architect
   - Timeline: 1-2 weeks

### High Priority Actions (SHOULD resolve before Alpha assessment)

4. **[H1] Complete TCoP Assessment**: UK Government projects require formal TCoP assessment for spend controls approval. Evidence exists across artifacts but is not consolidated.
   - Run: `/arckit:tcop`
   - Timeline: 2 weeks

5. **[H2] Create Data Model**: 5 DR-xxx requirements lack entity mapping. GDPR compliance requires formal data governance with PII identification, lawful basis per entity, and data owner assignments.
   - Run: `/arckit:data-model`
   - Timeline: 2-3 weeks

6. **[H3] Generate Traceability Matrix**: Traceability exists across artifacts but is not consolidated into a formal matrix for audit purposes.
   - Run: `/arckit:traceability`
   - Timeline: 1 week

7. **[H4] Obtain formal risk appetite escalation**: 7 risks exceed programme risk appetite. Programme Board must formally accept these risks or approve additional mitigation.
   - Owner: GDS Director General (SRO)
   - Timeline: Next Programme Board meeting

8. **[H5] Extend requirements traceability**: Only 16/46 requirements have direct goal traceability in Appendix C. Extend to show chain for NFR, INT, and DR requirements.
   - Owner: Programme Director
   - Timeline: 1 week

### Medium Priority Actions (Address during Alpha)

9. **[M1-M2] Assign document owners and establish approval workflow**: All 11 documents show placeholder owners and PENDING approvals. Assign named owners and schedule review cycle.
10. **[M3] Produce formal threat model**: STRIDE or equivalent during Alpha architecture sprints.
11. **[M4] Document open source strategy**: Repository location, licensing (MIT/Apache/OGL), publication criteria.
12. **[M5] Add missing data requirements**: DR-006 (citizen consent records), DR-007 (data subject access requests).
13. **[M6] Create Wardley Map**: Strategic positioning analysis for build/buy decisions.
14. **[M7] Verify principle numbering**: BR-001 references P13 and P16 both as "Reuse Government Platforms".
15. **[M8] Address SVCASS Amber ratings**: Prioritise Points 1, 4, 9, 12 evidence gaps.

### Low Priority Actions (Address when convenient)

16. **[L1] Standardise priority format**: Choose either MoSCoW (MUST_HAVE) or RFC 2119 (MUST) consistently.
17. **[L2] Align risk ID format**: Use R-xxx consistently across all documents.
18. **[L3] Confirm cloud provider**: Resolve "TBC" before Alpha procurement decisions.

---

## Metrics Dashboard

### Requirement Quality
- Total Requirements: 46
- Ambiguous Requirements: 0 (all have measurable criteria)
- Duplicate Requirements: 0
- Untestable Requirements: 0 (all have acceptance criteria)
- Missing Data Requirements: 3 (consent, SAR, breach records)
- **Quality Score**: 85%

### Architecture Alignment
- Principles Compliant: 13/16 assessed
- Principles Partially Compliant: 3 (P5, P23, P24)
- Principle Violations: 0
- **Alignment Score**: 81%

### Traceability
- Requirements with design coverage (L1): 46/46 (100%)
- Requirements with detailed design coverage: 0/46 (0%) — no HLD/DLD
- Requirements with stakeholder goal trace: 16/46 (35%) direct
- Formal traceability matrix exists: ❌ No
- **Traceability Score**: 55%

### Stakeholder Traceability
- Requirements traced to stakeholder goals: 35% (direct), ~100% (via chain)
- Orphan requirements: 0 (all traceable via BR/FR chain)
- Conflicts resolved: 4/4 (100%)
- RACI governance alignment: 90%
- **Stakeholder Score**: 78%

### Risk Management
- High/Very High inherent risks mitigated: 8/8 (100%)
- Risk owners from RACI: 20/20 (100%)
- Risks reflected in SOBC: 10/10 top risks (100%)
- Risks exceeding appetite with formal acceptance: 0/7 (0%)
- **Risk Management Score**: 82%

### Business Case
- Benefits traced to stakeholder goals: 6/6 (100%)
- Benefits supported by requirements: 6/6 (100%)
- Benefits measurable: 6/6 (100%)
- Budget adequacy: ✅ Adequate (BCR 2.0:1 even with 40% optimism bias)
- **Business Case Score**: 95%

### UK Government Compliance
- GDS Service Standard: 5/14 Green (36% Green, 64% Amber)
- TCoP Assessment: ❌ Not produced
- Secure by Design Assessment: ❌ Not produced
- DPIA: ❌ Not produced
- **UK Gov Compliance Score**: 40%

### Overall Governance Health

| Domain | Weight | Score | Weighted |
|--------|--------|-------|----------|
| Requirement Quality | 15% | 85% | 12.8 |
| Architecture Alignment | 15% | 81% | 12.2 |
| Traceability | 10% | 55% | 5.5 |
| Stakeholder Traceability | 10% | 78% | 7.8 |
| Risk Management | 15% | 82% | 12.3 |
| Business Case | 15% | 95% | 14.3 |
| UK Gov Compliance | 20% | 40% | 8.0 |
| **Total** | **100%** | | **72.9** |

**Overall Score**: 73/100
**Grade**: C (70-79%) — Adequate governance; address critical and high-priority issues before Alpha

**Grade Thresholds**:
- A (90-100%): Excellent governance, ready to proceed
- B (80-89%): Good governance, minor issues
- C (70-79%): Adequate governance, address high-priority issues
- D (60-69%): Poor governance, major rework needed
- F ( < 60%): Insufficient governance, do not proceed

---

## Next Steps

### Immediate Actions

1. **CRITICAL issues exist**: ⚠️ **RESOLVE BEFORE ALPHA** — 3 critical issues (DPIA, SbD assessment, ADRs) must be completed before the programme enters its formal Alpha phase (planned for weeks 13-32, starting June 2026).

2. **HIGH issues**: Address within the next 4-6 weeks — TCoP, data model, traceability matrix, and risk appetite escalation.

3. **If critical issues are resolved**: Governance score would improve to approximately 82% (Grade B), enabling confident progression to Alpha.

### Suggested Commands

**Critical (Run immediately)**:
- `/arckit:dpia` — Data Protection Impact Assessment for cross-service data sharing
- `/arckit:secure` — UK Government Secure by Design assessment
- `/arckit:adr` — Formal Architecture Decision Records (4 decisions)

**High Priority (Run within 4-6 weeks)**:
- `/arckit:tcop` — Technology Code of Practice assessment
- `/arckit:data-model` — Data model with ERD, GDPR compliance, data governance
- `/arckit:traceability` — Formal requirements traceability matrix

**Medium Priority (Run during Alpha)**:
- `/arckit:wardley` — Strategic Wardley Map for build/buy validation
- `/arckit:hld-review` — Review HLD when produced during Alpha
- `/arckit:principles-compliance` — Formal principles compliance scorecard

### Re-run Analysis

After addressing critical and high-priority findings:
```
/arckit:analyze
```

Expected improvement: Score rising from 73% (Grade C) to 82-88% (Grade B) after producing DPIA, SbD, ADRs, TCoP, data model, and traceability matrix.

---

## Detailed Findings

### Critical Issues

#### C1: No DPIA Despite Cross-Service Citizen Data Sharing

**Severity**: 🔴 CRITICAL
**Category**: UK Gov Compliance
**Location**: Missing artifact — no ARC-001-DPIA-*.md exists

**Description**:
The GDS Local programme processes citizen personal data across organisational boundaries, including special category data (health status, social care involvement). FR-004 enables housing officers to query health and social care data about specific citizens. UK GDPR Article 35 mandates a Data Protection Impact Assessment before any processing that is "likely to result in a high risk to the rights and freedoms of natural persons." Cross-organisational profiling of vulnerable citizens unambiguously requires DPIA.

**Impact**:
- ICO cannot endorse the data sharing framework without a DPIA
- Regulatory sandbox engagement (planned Q2 2026) will be blocked
- If data sharing proceeds without DPIA, ICO enforcement action possible
- Goal G-2 (data sharing framework) is dependent on DPIA completion

**Recommendation**:
1. Run `/arckit:dpia` to generate DPIA covering all 3 pilot data sharing use cases
2. Submit DPIA to DPO for review before ICO regulatory sandbox engagement
3. ICO endorsement of DPIA is a prerequisite for data sharing framework approval

**Evidence**:
- ARC-001-REQ-v1.0 FR-004: Cross-service data sharing with purpose limitation
- ARC-001-SVCASS-v1.0 Point 9: "No DPIA despite processing citizen PII across services"
- ARC-001-DIAG-001-v1.0: PII Handling table confirms special category data processing

---

#### C2: No Secure by Design Assessment

**Severity**: 🔴 CRITICAL
**Category**: UK Gov Compliance
**Location**: Missing artifact — no ARC-001-SECD-*.md exists

**Description**:
GDS Local processes citizen PII across organisational boundaries with authentication, data sharing, and consent management components. NCSC Secure by Design principles require a formal security assessment for any government service handling personal data. The Service Assessment (SVCASS Point 9) identifies this as a critical gap — "No Secure by Design (SECD) assessment or DPIA despite cross-service citizen data sharing."

**Impact**:
- GDS Service Standard Point 9 ("Create a secure service") cannot achieve Green rating
- Alpha assessment likely to flag security assurance as insufficient
- NCSC engagement at design gate requires formal SbD assessment as input
- No threat model means security controls may miss attack vectors

**Recommendation**:
1. Run `/arckit:secure` to generate formal SbD assessment
2. Include STRIDE threat model for data sharing and identity federation components
3. Map NCSC Cyber Assessment Framework controls to NFR-SEC requirements

**Evidence**:
- ARC-001-SVCASS-v1.0 Point 9: Rated Amber with SbD as critical gap
- ARC-001-REQ-v1.0: 5 NFR-SEC requirements exist but no formal assessment
- ARC-001-PLAN-v1.0: Security threat model planned for Alpha weeks 22-24

---

#### C3: No Formal Architecture Decision Records

**Severity**: 🔴 CRITICAL
**Category**: Governance
**Location**: `projects/001-gds-local/decisions/` — directory is empty

**Description**:
Four significant architecture decisions are documented informally in ARC-001-DIAG-001-v1.0 (Decisions 1-4: platform extension, governed data sharing, voluntary adoption, open standards integration). These decisions have major compliance, commercial, and operational implications but are not captured as formal Architecture Decision Records with status, alternatives considered, and approval chain. For governance audit, the NAO and Programme Board need formal, versioned decision records.

**Impact**:
- Architecture decisions lack formal approval chain — who approved these decisions?
- No evidence of alternatives considered for Decision 2 (data sharing approach) — auditors may question due diligence
- Decisions cannot be superseded or amended without formal ADR lifecycle
- Governance audit trail incomplete

**Recommendation**:
1. Run `/arckit:adr` four times to create ADR-001 through ADR-004
2. Include alternatives considered, decision rationale, and consequences
3. Present ADRs to Programme Board for formal approval

**Evidence**:
- ARC-001-DIAG-001-v1.0: Decisions 1-4 documented informally
- `decisions/` directory is empty — no formal ADRs exist

---

### High Priority Issues

#### H1: No TCoP Assessment Document

**Severity**: 🟠 HIGH
**Category**: UK Gov Compliance
**Location**: Missing artifact

**Description**: UK Government projects above spend control thresholds require formal TCoP assessment. Evidence for all 13 points exists across REQ, DIAG, and SOBC artifacts but is not consolidated into a formal assessment document with RAG ratings. Cabinet Office spend controls may require this document.

**Recommendation**: Run `/arckit:tcop` — evidence already exists; assessment consolidates it with formal ratings.

---

#### H2: No Data Model Despite DR-xxx Requirements

**Severity**: 🟠 HIGH
**Category**: Data Model
**Location**: Missing artifact

**Description**: 5 DR-xxx requirements define data needs but no entity-relationship model, data governance matrix, or CRUD access patterns exist. GDPR compliance requires formal PII mapping with lawful basis per data processing activity.

**Recommendation**: Run `/arckit:data-model` with inputs from REQ (DR-001 to DR-005) and DIAG (data flow section).

---

#### H3: No Formal Traceability Matrix

**Severity**: 🟠 HIGH
**Category**: Traceability
**Location**: Missing artifact

**Description**: Requirements traceability exists in fragments: DIAG has a requirements coverage table, REQ Appendix C has a stakeholder goal mapping, and individual requirements have "Relates To" fields. No single consolidated traceability matrix exists for audit.

**Recommendation**: Run `/arckit:traceability` to generate forward and backward traceability matrix.

---

#### H4: 7 Risks Exceed Programme Risk Appetite Without Formal Acceptance

**Severity**: 🟠 HIGH
**Category**: Risk Management
**Location**: ARC-001-RISK-v1.0

**Description**: 7 of 20 risks exceed programme risk appetite. The risk register documents this and identifies escalation paths, but there is no evidence that the Programme Board or GDS Director General has formally accepted these risks. Risk appetite exceedance requires documented acceptance or additional mitigation.

**Recommendation**: Present risk appetite analysis to Programme Board; obtain formal acceptance with conditions (e.g., monthly review, additional mitigations for R-011 and R-012 compliance risks).

---

#### H5: Incomplete Requirements-to-Goals Traceability

**Severity**: 🟠 HIGH
**Category**: Traceability
**Location**: ARC-001-REQ-v1.0 Appendix C

**Description**: The formal traceability table in Appendix C maps only 12 of 46 requirements to stakeholder goals. While all 16 BR+FR requirements have goal references in their body text, 30 NFR/INT/DR requirements lack direct traceability. These supporting requirements are traceable through the BR/FR chain but the indirect traceability is not documented.

**Recommendation**: Extend Appendix C to include chain traceability for all 46 requirements (e.g., NFR-SEC-002 → supports BR-002 → serves G-2).

---

#### H6: No HLD or DLD

**Severity**: 🟠 HIGH
**Category**: Design Coverage
**Location**: Missing artifacts

**Description**: No High-Level Design or Detailed Design documents exist. The System Context Diagram provides strong C4 Level 1 coverage but cannot validate NFR implementation, database schema, component interaction, or security implementation at detail. This is expected at pre-Alpha stage but means design coverage cannot be scored.

**Recommendation**: Produce HLD during Alpha (planned in PLAN weeks 13-32). Run `/arckit:hld-review` after production.

---

### Medium Priority Issues

#### M1-M2: Document Control Gaps

**Severity**: 🟡 MEDIUM
**Location**: All 11 artifacts

All documents show `[OWNER_NAME_AND_ROLE]` placeholder for document owner. All documents are in DRAFT status with PENDING review and approval. No artifact has completed a formal review cycle. While acceptable for a pre-Alpha programme, formal approval should begin as the programme mobilises.

---

#### M5: Missing Data Requirements for Consent and SAR

**Severity**: 🟡 MEDIUM
**Location**: ARC-001-REQ-v1.0

FR-010 (Citizen Consent Management) requires consent record storage, but no DR-xxx defines this data entity. NFR-C-001 requires data subject rights (access, erasure, portability) but no DR-xxx defines SAR handling data. Add DR-006 (citizen consent records) and DR-007 (data subject access requests).

---

#### M8: Service Assessment Amber Ratings

**Severity**: 🟡 MEDIUM
**Location**: ARC-001-SVCASS-v1.0

9 of 14 Service Standard points are rated Amber. The most critical gaps (Points 1, 4, 9, 12) relate to: primary user research not yet conducted, no prototype testing, no SbD assessment, and no open source strategy. These are expected pre-Alpha but must be addressed during Alpha to achieve Green ratings before booking the Alpha assessment.

---

### Low Priority Issues

#### L1: Priority Format Inconsistency

**Severity**: 🟢 LOW
**Location**: ARC-001-REQ-v1.0

Requirements use MoSCoW format (`MUST_HAVE`, `SHOULD_HAVE`) in requirement headers but RFC 2119 keywords (`MUST`, `SHOULD`) in requirement text. Both are valid but using both in the same document may cause confusion. Recommend standardising.

---

#### L2: Risk ID Format Inconsistency

**Severity**: 🟢 LOW
**Location**: ARC-001-REQ-v1.0 Dependencies/Risks section

The REQ document's Dependencies and Risks section uses abbreviated IDs (R-1 to R-5) while the formal risk register uses R-001 to R-020. This is cosmetic but could confuse cross-referencing.

---

#### L3: Cloud Provider TBC

**Severity**: 🟢 LOW
**Location**: ARC-001-DIAG-001-v1.0

Cloud provider is listed as "TBC" across DIAG and REQ. SOBC Part C references "AWS UK" in the hosting cost line. Decision should be made during Alpha research/procurement phase. Consider running `/arckit:aws-research` or `/arckit:gcp-research`.

---

## Appendix A: Artifacts Analyzed

| Artifact | Location | Created | Status |
|----------|----------|---------|--------|
| Architecture Principles v1.1 | `projects/000-global/ARC-000-PRIN-v1.1.md` | 2026-02-16 | ✅ Analyzed |
| Stakeholder Analysis v1.0 | `projects/001-gds-local/ARC-001-STKE-v1.0.md` | 2026-02-16 | ✅ Analyzed |
| Requirements v1.0 | `projects/001-gds-local/ARC-001-REQ-v1.0.md` | 2026-02-16 | ✅ Analyzed |
| Risk Register v1.0 | `projects/001-gds-local/ARC-001-RISK-v1.0.md` | 2026-02-17 | ✅ Analyzed |
| SOBC v1.0 | `projects/001-gds-local/ARC-001-SOBC-v1.0.md` | 2026-02-17 | ✅ Analyzed |
| Project Plan v1.0 | `projects/001-gds-local/ARC-001-PLAN-v1.0.md` | 2026-02-17 | ✅ Analyzed |
| Research v2.0 | `projects/001-gds-local/ARC-001-RSCH-v2.0.md` | 2026-02-17 | ✅ Referenced |
| System Context Diagram v1.0 | `projects/001-gds-local/diagrams/ARC-001-DIAG-001-v1.0.md` | 2026-02-26 | ✅ Analyzed |
| Service Assessment v1.0 | `projects/001-gds-local/ARC-001-SVCASS-v1.0.md` | 2026-02-28 | ✅ Analyzed |
| Data Model | — | — | ❌ Not Found |
| HLD / DLD | — | — | ❌ Not Found |
| TCoP Assessment | — | — | ❌ Not Found |
| Secure by Design | — | — | ❌ Not Found |
| DPIA | — | — | ❌ Not Found |
| Traceability Matrix | — | — | ❌ Not Found |
| ADRs | — | — | ❌ Not Found |

---

## Appendix B: Analysis Methodology

**Analysis Date**: 2026-03-01
**Analyzed By**: ArcKit `/arckit.analyze` command

**Checks Performed**:

- Requirements completeness and quality (46 requirements across 5 categories)
- Architecture principles compliance (16 principles assessed)
- Stakeholder traceability (11 drivers, 6 goals, 4 conflicts)
- Risk coverage and mitigation (20 risks, 7 exceeding appetite)
- Business case alignment (6 benefits, 4 options, sensitivity analysis)
- Data model consistency (5 DR-xxx requirements, no entity model)
- UK Government compliance (GDS Service Standard, TCoP, SbD, DPIA)
- Design quality (System Context Diagram at C4 Level 1)
- Consistency across 9 analyzed artifacts (terminology, technology, budget)
- Security and compliance coverage (NFR-SEC, NFR-C, NCSC, ICO)

**Severity Classification**:

- 🔴 **CRITICAL**: Blocks Alpha progression or regulatory compliance; must resolve immediately
- 🟠 **HIGH**: Significant governance gap; resolve before major milestones
- 🟡 **MEDIUM**: Should be addressed; can proceed with caution
- 🟢 **LOW**: Minor issues; address when convenient

**Detection Rules Applied**:

- 15 duplication checks across requirement categories
- 12 ambiguity patterns (vague adjectives, missing measurable criteria, placeholders)
- 16 principle validation checks against 25 principles
- 46 requirements traceability checks (forward and backward)
- 20 risk coverage checks (mitigation in requirements and design)
- 6 benefit traceability checks (goals, requirements, measurability)
- 13 TCoP evidence checks
- 14 Service Standard point assessments
- 11 artifact consistency checks (terminology, technology, budget)

---

**Generated by**: ArcKit `/arckit:analyze` command
**Generated on**: 2026-03-01 GMT
**ArcKit Version**: 2.22.3
**Project**: GDS Local (Project 001)
**AI Model**: claude-opus-4-6
**Generation Context**: Comprehensive analysis across 9 primary artifacts (PRIN v1.1, STKE v1.0, REQ v1.0, RISK v1.0, SOBC v1.0, PLAN v1.0, DIAG-001 v1.0, SVCASS v1.0, RSCH v2.0) plus gap analysis for 6 missing artifacts (DPIA, SECD, TCoP, DATA, TRAC, ADRs).
