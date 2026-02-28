# Architecture Governance Analysis Report: GDS Local

> **Template Status**: Beta | **Version**: 2.20.1 | **Command**: `/arckit.analyze`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-ANAL-v2.0 |
| **Document Type** | Governance Analysis Report |
| **Project** | GDS Local (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 2.0 |
| **Created Date** | 2026-02-28 |
| **Last Modified** | 2026-02-28 |
| **Review Cycle** | On-Demand |
| **Next Review Date** | 2026-03-30 |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | GDS Local Programme Team, Architecture Team, GDS Director General, MHCLG Digital, LGA |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-28 | ArcKit AI | Initial analysis from `/arckit:analyze` command | PENDING | PENDING |
| 2.0 | 2026-02-28 | ArcKit AI | Comprehensive re-analysis with full artifact inventory, UK Gov compliance assessment, and cross-artifact consistency checks | PENDING | PENDING |

---

## Executive Summary

**Overall Status**: ⚠️ Issues Found

**Key Metrics**:

- Total Requirements: 46 (6 BR, 10 FR, 20 NFR, 5 INT, 5 DR)
- Requirements Coverage: 46% (context diagram covers BRs/FRs/INTs; no HLD/DLD for NFR/DR coverage)
- Critical Issues: 3
- High Priority Issues: 6
- Medium Priority Issues: 4
- Low Priority Issues: 2

**Recommendation**: RESOLVE CRITICAL ISSUES FIRST

The GDS Local programme has an **exceptionally strong governance foundation** for a pre-Alpha programme. Comprehensive stakeholder analysis, well-structured requirements with stakeholder traceability, a thorough 20-risk register following HM Treasury Orange Book methodology, and a detailed 5-case SOBC with BCR 2.8:1 demonstrate rigorous governance discipline.

However, **three critical compliance gaps** must be addressed before entering Alpha: no Technology Code of Practice (TCoP) assessment, no Secure by Design (SECD) assessment, and no Data Protection Impact Assessment (DPIA) despite the programme processing citizen PII across organisational boundaries. These are mandatory for UK Government projects and are identified as blocking issues by the GDS Service Assessment preparation report (ARC-001-SVCASS-v1.0).

Additionally, six high-priority issues require attention: missing data model despite DR-xxx requirements, no formal traceability matrix, no formal ADRs, document owner placeholders across all artifacts, budget discrepancy between SOBC and PLAN, and NFR prefix inconsistency.

---

## Findings Summary

| ID | Category | Severity | Location(s) | Summary | Recommendation |
|----|----------|----------|-------------|---------|----------------|
| C1 | UK Gov Compliance | CRITICAL | Missing artifact | No TCoP assessment — mandatory for UK Gov projects | Run `/arckit:tcop` |
| C2 | UK Gov Compliance | CRITICAL | Missing artifact | No Secure by Design assessment despite handling citizen PII cross-organisationally | Run `/arckit:secure` |
| C3 | UK Gov Compliance | CRITICAL | Missing artifact | No DPIA despite cross-service citizen data sharing (UK GDPR Art. 35) | Run `/arckit:dpia` |
| H1 | Data Model | HIGH | Missing artifact | No data model despite 5 DR-xxx requirements | Run `/arckit:data-model` |
| H2 | Traceability | HIGH | Missing artifact | No formal traceability matrix | Run `/arckit:traceability` |
| H3 | Design Quality | HIGH | Missing artifact | No formal Architecture Decision Records (ADRs) | Run `/arckit:adr` |
| H4 | Document Quality | HIGH | All artifacts | Document owner `[OWNER_NAME_AND_ROLE]` placeholder in all 9 artifacts | Assign named owners |
| H5 | Consistency | HIGH | ARC-001-SOBC-v1.0, ARC-001-PLAN-v1.0 | Budget discrepancy: SOBC states £29M midpoint TCO; PLAN shows £31.6M+£3.9M contingency = £35.5M | Reconcile figures |
| H6 | Requirements Quality | HIGH | ARC-001-REQ-v1.0 | NFR prefix confusion: NFR-S-001 (Scalability) easily confused with Security prefix | Rename to NFR-SC-001 |
| M1 | Requirements Quality | MEDIUM | ARC-001-REQ-v1.0 | NFR count discrepancy: exec summary states 18 NFRs, actual count is 20 | Update exec summary |
| M2 | Design Coverage | MEDIUM | Missing artifact | No HLD/DLD (expected pre-Alpha per PLAN; flagged for tracking) | Produce during Alpha (weeks 21-24) |
| M3 | UK Gov Compliance | MEDIUM | ARC-001-SVCASS-v1.0 | Service Assessment: 9/14 points Amber, 0 Red — gaps are pre-Alpha expected | Address during Alpha phase |
| M4 | Requirements Quality | MEDIUM | ARC-001-REQ-v1.0 | No explicit open source code strategy (NFR-M-003 is SHOULD_HAVE) | Strengthen to MUST_HAVE per P23 |
| L1 | Document Quality | LOW | All artifacts | [PENDING] reviewer/approver fields across all documents | Expected for DRAFT status |
| L2 | Requirements Quality | LOW | ARC-001-REQ-v1.0 | Principle P2 "Scalability" referenced by NFR-S-001 and NFR-P-002 — minor redundancy | Clarify distinction |

---

## Requirements Analysis

### Requirements Inventory

| Category | Prefix | Count | MUST | SHOULD | MAY |
|----------|--------|-------|------|--------|-----|
| Business | BR-xxx | 6 | 6 | 0 | 0 |
| Functional | FR-xxx | 10 | 8 | 2 | 0 |
| Non-Functional (Performance) | NFR-P-xxx | 2 | 2 | 0 | 0 |
| Non-Functional (Availability) | NFR-A-xxx | 3 | 3 | 0 | 0 |
| Non-Functional (Scalability) | NFR-S-xxx | 1 | 1 | 0 | 0 |
| Non-Functional (Security) | NFR-SEC-xxx | 5 | 5 | 0 | 0 |
| Non-Functional (Compliance) | NFR-C-xxx | 4 | 4 | 0 | 0 |
| Non-Functional (Usability) | NFR-U-xxx | 2 | 1 | 1 | 0 |
| Non-Functional (Maintainability) | NFR-M-xxx | 3 | 2 | 1 | 0 |
| Integration | INT-xxx | 5 | 2 | 3 | 0 |
| Data | DR-xxx | 5 | — | — | — |
| **Total** | | **46** | **34** | **7** | **0** |

### Requirements Coverage Matrix

| Requirement ID | Type | Priority | Context Diagram | HLD | DLD | Status |
|----------------|------|----------|-----------------|-----|-----|--------|
| BR-001 | Business | MUST | ✅ | ❌ N/A | ❌ N/A | ⚠️ Partial |
| BR-002 | Business | MUST | ✅ | ❌ N/A | ❌ N/A | ⚠️ Partial |
| BR-003 | Business | MUST | ✅ | ❌ N/A | ❌ N/A | ⚠️ Partial |
| BR-004 | Business | MUST | ✅ | ❌ N/A | ❌ N/A | ⚠️ Partial |
| BR-005 | Business | MUST | ✅ | ❌ N/A | ❌ N/A | ⚠️ Partial |
| BR-006 | Business | MUST | ✅ | ❌ N/A | ❌ N/A | ⚠️ Partial |
| FR-001 to FR-010 | Functional | MUST/SHOULD | ✅ | ❌ N/A | ❌ N/A | ⚠️ Partial |
| NFR-P/A/S/SEC/C/U/M | Non-Functional | MUST/SHOULD | ❌ | ❌ N/A | ❌ N/A | ❌ Not Covered |
| INT-001 to INT-005 | Integration | MUST/SHOULD | ✅ | ❌ N/A | ❌ N/A | ⚠️ Partial |
| DR-001 to DR-005 | Data | — | ❌ | ❌ N/A | ❌ N/A | ❌ Not Covered |

**Statistics**:

- Total Requirements: 46
- Partially Covered (context diagram): 21 (46%)
- Not Covered: 25 (54%) — all NFRs and DRs lack design-level coverage
- Fully Covered (HLD+DLD): 0 (0%)

> **Note**: Design coverage is expected to be low at the pre-Alpha stage. The project plan schedules HLD for Alpha weeks 21-24 and DLD for Beta week 48. This finding is tracked for governance completeness.

### Requirements Quality Assessment

**Strengths**:

- All requirements have unique IDs with consistent prefixes
- Priority (MoSCoW) assigned to all functional and non-functional requirements
- Acceptance criteria defined for all 10 functional requirements using Given-When-Then format
- Requirements traced to stakeholder goals and architecture principles
- 5 use cases with full actor/flow/postcondition structure
- 5 user personas with realistic detail
- 2 requirement conflicts identified and resolved (C-1, C-2)

**Issues Found**:

1. **[H6] NFR Prefix Confusion**: `NFR-S-001` uses "S" for Scalability. Security requirements use `NFR-SEC-xxx`. The "S" prefix could be confused with Security. Recommend renaming to `NFR-SC-001` for clarity.

2. **[M1] NFR Count Discrepancy**: Executive summary states "18 non-functional requirements" but actual count is 20 NFRs (2 Performance + 3 Availability + 1 Scalability + 5 Security + 4 Compliance + 2 Usability + 3 Maintainability = 20). This discrepancy propagates to PLAN and SVCASS which cite the same "18 NFRs" figure.

3. **[M4] Open Source Requirement**: NFR-M-003 (Open Source Publication) is `SHOULD_HAVE` but Principle P23 states "Open Source by Default". This should be strengthened to `MUST_HAVE` to align with the architecture principle and GDS Service Standard Point 12.

---

## Architecture Principles Compliance

| # | Principle | Status | Evidence | Issues |
|---|-----------|--------|----------|--------|
| P1 | User Needs First | ✅ COMPLIANT | STKE: 11 drivers, 5 personas in REQ, REQ traces to stakeholder goals | None |
| P2 | Scalability and Elasticity | ✅ COMPLIANT | NFR-S-001, NFR-P-002 define scaling targets (50→333 councils) | None |
| P3 | Resilience and Fault Tolerance | ✅ COMPLIANT | NFR-A-001/002/003 define availability, DR, and graceful degradation | None |
| P4 | Interoperability and Open Standards | ✅ COMPLIANT | FR-001 (OIDC), FR-009 (API gateway), TC-2 mandates open standards | None |
| P5 | Security by Design (NON-NEGOTIABLE) | ⚠️ PARTIAL | NFR-SEC-001 to 005 define security requirements; but no SECD assessment or threat model exists | **[C2]** No SECD assessment |
| P6 | Accessibility by Default (NON-NEGOTIABLE) | ✅ COMPLIANT | NFR-C-002 mandates WCAG 2.2 AA; GOV.UK Design System mandated | None |
| P7 | Observability | ✅ COMPLIANT | NFR-M-001 defines telemetry requirements with detail | None |
| P8 | Central-Local Collaboration | ✅ COMPLIANT | BR-004 (co-design), FR-006 (community), voluntary adoption (BR-006) | None |
| P9 | Cross-Service Data Sharing | ✅ COMPLIANT | FR-004, FR-005, FR-010 define platform with governance | None |
| P10 | Federated Identity | ✅ COMPLIANT | FR-001 (OneLogin federation), INT-001 | None |
| P11 | Data Sovereignty and UK GDPR | ⚠️ PARTIAL | NFR-C-001 defines GDPR requirements; TC-4 mandates UK residency; but no DPIA exists | **[C3]** No DPIA |
| P13 | Reuse Government Platforms | ✅ COMPLIANT | BR-001 extends OneLogin, Notify, Pay; DIAG shows reuse | None |
| P14 | Loose Coupling | ✅ COMPLIANT | NFR-A-003 (circuit breakers), NFR-M-002 (API versioning) | None |
| P23 | Open Source by Default | ⚠️ PARTIAL | NFR-M-003 is SHOULD_HAVE not MUST_HAVE | **[M4]** Weaker than principle requires |
| P24 | GDS Service Standard | ✅ COMPLIANT | BR-005, NFR-C-003, SVCASS preparation done | None |
| P25 | Spend Controls and Value for Money | ✅ COMPLIANT | BR-003 (£50M savings target), SOBC (BCR 2.8:1) | None |

**Principles assessed**: 16 of 25 key principles (remaining 9 are technology-specific and will be validated at HLD stage)

**Critical Principle Violations**: 0 (principles partially compliant due to missing artifacts, not contradicted)

**Principles Compliance Score**: 81% (13 compliant, 3 partial)

---

## Stakeholder Traceability Analysis

**Stakeholder Analysis Exists**: ✅ Yes (ARC-001-STKE-v1.0)

**Stakeholder-Requirements Coverage**:

| Stakeholder | Driver ID | Goals | Requirements Traced | Status |
|-------------|-----------|-------|---------------------|--------|
| DSIT Minister | SD-1 | G-1, G-5 | BR-001, BR-005 | ✅ Complete |
| GDS Director General | SD-2 | G-1, G-3 | BR-001, BR-003 | ✅ Complete |
| MHCLG Digital Director | SD-3 | G-2 | BR-002, FR-004, FR-005 | ✅ Complete |
| LA Chief Executives | SD-4 | G-4 | BR-003, BR-006, FR-007 | ✅ Complete |
| LA Digital/IT Directors | SD-5 | G-3, G-6 | FR-002, FR-003, FR-006 | ✅ Complete |
| LGA | SD-6 | G-4, G-6 | BR-004, BR-006, FR-006, FR-007 | ✅ Complete |
| Citizens | SD-7 | G-1, G-2 | BR-001, BR-002, FR-001, FR-010 | ✅ Complete |
| ICO | SD-8 | G-2 | NFR-C-001, FR-004, FR-005, INT-005 | ✅ Complete |
| NAO | SD-9 | G-4, G-5 | BR-003, BR-005 | ✅ Complete |
| NCSC | SD-11 | — | NFR-SEC-001 to 005, NFR-C-004 | ✅ Complete |

**Summary**:

- Requirements traced to stakeholder goals: 100%
- Orphan requirements (no stakeholder justification): 0
- Requirement conflicts documented and resolved: ✅ Yes (C-1, C-2)

**RACI Governance Alignment**:

| Artifact | Role | Aligned with RACI? | Issues |
|----------|------|-------------------|--------|
| Risk Register | Risk Owners | ✅ Yes | All 20 risk owners from RACI matrix |
| SOBC | Benefits Owners | ✅ Yes | Benefits traced to stakeholder goals |
| Service Assessment | Service Owner | ✅ Yes | Liz Adams identified |

**Stakeholder Score**: 95%

---

## Risk Management Analysis

**Risk Register Exists**: ✅ Yes (ARC-001-RISK-v1.0)

**Risk Profile**:

- Total risks: 20 across 6 categories
- Inherent High (13-19): 8 risks → Residual High: 0 (all reduced to Medium)
- Inherent Medium (6-12): 12 risks → Residual Medium: 18
- Residual Low: 2
- Overall control effectiveness: 35% reduction
- Risks exceeding appetite: 7 (35%)

**High Residual Risks Requiring Attention**:

| Risk ID | Description | Category | Residual | Appetite | Excess | Required Action |
|---------|-------------|----------|----------|----------|--------|-----------------|
| R-001 | Insufficient local authority adoption | STRATEGIC | 12 | 9 | +3 | Funded onboarding team, pathfinder success stories |
| R-002 | Ministerial direction or MoG change | STRATEGIC | 10 | 9 | +1 | Cross-party engagement, LGA continuity |
| R-008 | Programme funding not sustained | FINANCIAL | 10 | 8 | +2 | Early benefits evidence, spending review bid |
| R-011 | Data sharing privacy breach | COMPLIANCE | 10 | 6 | +4 | DPIA completion (**[C3]**), ICO sandbox |
| R-004 | GDS platform team capacity | OPERATIONAL | 9 | 8 | +1 | Dedicated LA capacity ring-fenced |
| R-012 | UK GDPR non-compliance | COMPLIANCE | 8 | 6 | +2 | DPIA completion (**[C3]**), governance-first |
| R-015 | Parliamentary scrutiny | REPUTATIONAL | 9 | 8 | +1 | Joint LGA communications |

**Risk-SOBC Alignment**:

- Strategic risks reflected in Strategic Case "Why Now?": ✅ Yes
- Financial risks in Economic Case cost contingency: ✅ Yes (15% contingency)
- Risks included in Management Case: ✅ Yes (top 7 risks referenced)

**Risk-Requirements Alignment**:

- R-001 (adoption) → mitigated by BR-006 (voluntary), FR-002 (self-service), FR-006 (community): ✅
- R-011 (data breach) → mitigated by NFR-SEC-001 to 005, NFR-C-001, FR-004 (governance): ✅
- R-018 (platform delay) → mitigated by PLAN phased delivery, agile approach: ✅
- R-005 (skills gap) → mitigated by requirements for open standards (P4), DDaT framework: ✅

**Risk Governance**:

- Risk owners from stakeholder RACI: ✅ Yes (all 20 risks have named owners aligned with RACI)
- Monthly review cadence recommended: ✅ Yes

**Risk Management Score**: 88%

---

## Business Case Analysis

**SOBC Exists**: ✅ Yes (ARC-001-SOBC-v1.0)

**Benefits Traceability**:

| Benefit ID | Description | Stakeholder Goal | Requirements | Measurable? | Status |
|------------|-------------|------------------|--------------|-------------|--------|
| B-001 | Council procurement savings £50M | G-4 (LGA) | BR-003, FR-007 | ✅ Yes (audit) | ✅ Complete |
| B-002 | Technology cost avoidance £13M | G-1, G-3 | BR-001, FR-002, FR-003 | ✅ Yes (platform analytics) | ✅ Complete |
| B-003 | Coordination time reduction £4M | G-2 (O-2) | BR-002, FR-004 | ✅ Yes (time measurement) | ✅ Complete |
| B-004 | Citizen time savings £6.5M | G-1 (O-1) | BR-001, FR-001 | ⚠️ Partial (social value) | ⚠️ Confidence LOW |
| B-005 | IT staff productivity £5.5M | G-3 (O-3) | BR-001, FR-003 | ⚠️ Partial (survey) | ⚠️ Confidence LOW |
| B-006 | Compliance cost reduction £1.7M | G-5 | BR-005, NFR-C-xxx | ⚠️ Partial (estimate) | ⚠️ Confidence LOW |

**Benefits Coverage**:

- Total benefits: 6
- Benefits traced to stakeholder goals: 100%
- Benefits supported by requirements: 100%
- Benefits measurable and verifiable: 50% (3 of 6 are high confidence)

**Option Analysis Quality**:

- Do Nothing baseline included: ✅ Yes (Option 0)
- Options analyzed: 4 (Do Nothing, Minimal, Balanced, Comprehensive)
- Recommended option: Option 2 (Balanced) — best BCR at 2.8:1
- Justification: ✅ Strong (comparative analysis, sensitivity testing)

**SOBC-Requirements Alignment**:

- Strategic Case drivers in requirements: ✅ Yes (all 7 drivers mapped to BRs)
- Economic Case benefits achievable with requirements: ✅ Yes
- Financial Case budget adequate: ⚠️ Questionable — **[H5]** budget discrepancy

**Budget Discrepancy [H5]**:

| Source | Programme Cost | Operational | Contingency | Total TCO |
|--------|---------------|-------------|-------------|-----------|
| SOBC (Option 2) | £29.6M (high end) | £9.9M (3yr) | Included in £29.6M | £29-34M |
| PLAN | £27.7M | £5.5M (Year 1) | £3.9M (15%) | £38.2M (3yr) |

The SOBC states £24M midpoint (£29.6M high end) while the PLAN shows £31.6M before contingency (£35.5M with contingency). The PLAN's £38.2M "3-year TCO" includes Year 1 post-launch operational costs. These figures need reconciliation — different scoping assumptions may explain the gap, but this should be documented clearly.

**Business Case Score**: 82%

---

## Data Model Analysis

**Data Model Exists**: ❌ No

**DR-xxx Requirements Exist**: ✅ Yes (5 data requirements)

| DR ID | Description | Entity Mapping | GDPR Classification | Status |
|-------|-------------|----------------|---------------------|--------|
| DR-001 | Council registration data | ❌ No entity | OFFICIAL | ❌ Not modelled |
| DR-002 | Identity federation data | ❌ No entity | OFFICIAL-SENSITIVE | ❌ Not modelled |
| DR-003 | Data sharing audit logs | ❌ No entity | OFFICIAL-SENSITIVE | ❌ Not modelled |
| DR-004 | Data sharing agreements | ❌ No entity | OFFICIAL | ❌ Not modelled |
| DR-005 | Community and engagement data | ❌ No entity | OFFICIAL | ❌ Not modelled |

**Data Requirements Coverage**:

- Total DR-xxx requirements: 5
- DR-xxx mapped to entities: 0%
- Data model artifact: ❌ Missing

**Data Model Quality**: N/A — no data model exists

**Data Governance**: Partially addressed in requirements (NFR-C-001 covers GDPR, DR-003 covers audit trails) but no formal data governance matrix with owners, stewards, and custodians.

**Critical Issues**:

- **[H1]** 5 DR-xxx requirements with no entity mapping
- DR-002 and DR-003 are classified OFFICIAL-SENSITIVE but no data model documents handling requirements
- No entity-relationship diagram (ERD)

**Data Model Score**: 20%

---

## UK Government Compliance Analysis

### Technology Code of Practice (TCoP)

**TCoP Assessment Exists**: ❌ No — **[C1] CRITICAL**

**Indirect Evidence**:

Architecture principles (ARC-000-PRIN-v1.1) reference TCoP points:
- P1 maps to TCoP Point 1 (User needs)
- P4 maps to TCoP Point 4 (Open standards)
- P5 maps to TCoP Point 9 (Security)
- P6 maps to TCoP Point 5 (Accessibility)
- P13 maps to TCoP Point 8 (Share and reuse)
- P23 maps to TCoP Point 12 (Open source)

However, no formal assessment against all 13 TCoP points exists. This is **mandatory** for UK Government technology projects.

**TCoP Score**: Not assessed (0/130)

### Secure by Design

**SECD Assessment Exists**: ❌ No — **[C2] CRITICAL**

The programme handles citizen PII across organisational boundaries (cross-service data sharing between housing, health, and social care). Principle P5 (Security by Design) is marked **NON-NEGOTIABLE** and requires:
- Threat model completed and reviewed
- Security controls mapped to requirements
- NCSC Secure by Design checklist completed

None of these exist yet. The Service Assessment (ARC-001-SVCASS-v1.0) identifies this as a critical gap at Point 9.

### Data Protection Impact Assessment (DPIA)

**DPIA Exists**: ❌ No — **[C3] CRITICAL**

NFR-C-001 explicitly requires "Data Protection Impact Assessments (DPIAs) completed for all cross-service data sharing". The programme intends to share citizen data between housing, social care, and health services across local authority boundaries. Under UK GDPR Article 35, a DPIA is **mandatory** for:
- Large-scale processing of special categories of data
- Systematic monitoring of publicly accessible areas
- Processing that is likely to result in a high risk to rights and freedoms

Cross-service data sharing between housing and health/social care meets these criteria. R-011 (data sharing privacy breach, residual risk score 10, exceeds appetite by +4) further underscores the urgency.

### GDS Service Assessment

**Service Assessment Preparation Exists**: ✅ Yes (ARC-001-SVCASS-v1.0)

**Status**: 5/14 Green, 9/14 Amber, 0/14 Red

The service assessment preparation identifies the same critical gaps flagged in this analysis (SECD, DPIA) and provides detailed recommendations for converting Amber ratings to Green during Alpha.

**UK Gov Compliance Score**: 25%

---

## Design Quality Analysis

### HLD Analysis

**HLD Exists**: ❌ No

Per the Project Plan (ARC-001-PLAN-v1.0), HLD is scheduled for Alpha weeks 21-24 with an HLD Review gate at week 24. This is expected pre-Alpha. **[M2]**

### DLD Analysis

**DLD Exists**: ❌ No

Per the Project Plan, DLD Review is scheduled for Beta week 48. This is expected pre-Alpha.

### Architecture Decisions

**Formal ADRs Exist**: ❌ No — **[H3]**

However, the C4 Context Diagram (ARC-001-DIAG-001-v1.0) documents 4 key architecture decisions informally:
1. Extend existing GOV.UK platforms (not build new)
2. Purpose-limited API queries (not bulk data transfer)
3. Voluntary pathfinder adoption model
4. Open standards integration for council diversity

These should be formalised as Architecture Decision Records with full options analysis, consequences, and traceability to requirements and principles.

### C4 Context Diagram

**Context Diagram Exists**: ✅ Yes (ARC-001-DIAG-001-v1.0)

**Quality**: Strong — all 6 external systems mapped, requirements traceability table covers 21 requirements (6 BR + 10 FR + 5 INT = 100% of BRs, FRs, and INTs). Technology choices documented. Evolution stages assessed.

---

## Traceability Analysis

**Traceability Matrix Exists**: ❌ No — **[H2]**

**Informal Traceability** (from artifacts):

| Traceability Link | Status | Evidence |
|--------------------|--------|----------|
| Stakeholder Goals → Requirements | ✅ Complete | REQ traces all BRs to goals and stakeholders |
| Requirements → Principles | ✅ Complete | REQ includes principle alignment per requirement |
| Requirements → Context Diagram | ✅ Complete | DIAG-001 covers all BRs, FRs, INTs |
| Requirements → HLD | ❌ Missing | No HLD exists yet |
| Requirements → DLD | ❌ Missing | No DLD exists yet |
| Requirements → Tests | ❌ Missing | No test plan exists yet |
| Risks → Requirements | ✅ Partial | Risk register references BRs/FRs for mitigation |
| Benefits → Requirements | ✅ Complete | SOBC benefits traced to goals and requirements |

**Forward Traceability** (Requirements → Design → Tests):

- Requirements → Context Diagram: 46% (21 of 46 requirements)
- Requirements → HLD: 0% (no HLD)
- Requirements → DLD: 0% (no DLD)
- Requirements → Tests: 0% (no test plan)

**Backward Traceability** (Tests → Requirements):

- Not applicable — no tests exist at this stage

**Gap Summary**:

- 25 requirements with no design coverage (all NFRs and DRs)
- 0 orphan design elements (context diagram maps cleanly to requirements)
- Formal traceability matrix needed to consolidate informal traceability across artifacts

**Traceability Score**: 40%

---

## Consistency Across Artifacts

### Terminology Consistency

| Term | Usage Across Artifacts | Consistent? |
|------|----------------------|-------------|
| "GDS Local" | All artifacts | ✅ Yes |
| "OneLogin" / "GOV.UK OneLogin" | Varies between short and full form | ⚠️ Minor |
| "councils" / "local authorities" | Used interchangeably | ⚠️ Minor |
| "pathfinder councils" | SOBC, PLAN, REQ, RISK | ✅ Yes |
| "data sharing" | All artifacts | ✅ Yes |
| NFR count: "18" vs actual 20 | REQ exec summary, PLAN, SVCASS | ❌ **[M1]** |

### Budget/Cost Consistency

| Document | Programme Cost | Total 3-Year TCO |
|----------|---------------|------------------|
| SOBC (Option 2, midpoint) | £24M | £29M |
| SOBC (Option 2, high end) | £29.6M | £34M |
| PLAN | £27.7M + £3.9M contingency | £38.2M |
| PLAN (excl Year 1 post-launch ops) | £22.2M | £31.6M |

The discrepancy arises from different scoping: SOBC separates programme and operational costs differently from PLAN, and PLAN includes more granular Year 1 post-launch operational costs. **[H5]** — Needs formal reconciliation note.

### Technology Stack Consistency

All artifacts consistently reference:
- OIDC/SAML 2.0 for identity federation
- REST APIs with OpenAPI for integration
- OAuth 2.0 for API authentication
- TLS 1.3 for transport security
- AES-256 for data at rest encryption
- GOV.UK Design System for UI
- ✅ Technology stack is consistent

### Timeline Consistency

| Document | Programme Duration | Key Milestones |
|----------|-------------------|----------------|
| SOBC | "3-year programme" | — |
| PLAN | 68 weeks to go-live; 3 years to benefits | Discovery W12, Alpha W32, Beta W68 |
| REQ | "Q4 2027" for 50 councils | Consistent with PLAN |

✅ Timeline consistent across artifacts

---

## Security & Compliance Summary

### Security Posture

- Security requirements defined: ✅ Yes (NFR-SEC-001 to 005)
- Threat model documented: ❌ No — **[C2]**
- Security architecture in HLD: ❌ No HLD
- Security testing plan: ✅ Partial (NFR-SEC-005 defines approach)
- Zero-trust requirements: ✅ Yes (NFR-SEC-001)
- Encryption requirements: ✅ Yes (NFR-SEC-003)
- Audit logging requirements: ✅ Yes (NFR-SEC-004)
- Vulnerability management: ✅ Yes (NFR-SEC-005)
- Tenant isolation: ✅ Yes (NFR-SEC-002)

**Security Coverage**: 70% (requirements strong; assessment and design artifacts missing)

### Compliance Posture

- UK GDPR requirements identified: ✅ Yes (NFR-C-001)
- DPIA completed: ❌ No — **[C3]**
- Accessibility requirements: ✅ Yes (NFR-C-002, WCAG 2.2 AA)
- GDS Service Standard: ✅ Yes (NFR-C-003, SVCASS)
- NCSC security standards: ✅ Yes (NFR-C-004)
- TCoP assessed: ❌ No — **[C1]**

**Compliance Coverage**: 40% (requirements defined but assessments not completed)

---

## Recommendations

### Critical Actions (MUST resolve before Alpha phase)

1. **[C1] Complete Technology Code of Practice Assessment**: TCoP is mandatory for UK Government technology projects. Run `/arckit:tcop` to assess all 13 points and identify any technology decisions that conflict with TCoP.
   - **Effort**: 2-3 hours
   - **Owner**: Technical Architect
   - **Addresses**: Finding C1

2. **[C2] Complete Secure by Design Assessment**: The programme handles citizen PII across organisational boundaries. A threat model and SECD assessment are required by Principle P5 (NON-NEGOTIABLE) and GDS Service Standard Point 9. Run `/arckit:secure` to produce SECD assessment.
   - **Effort**: 4-6 hours
   - **Owner**: Security Architect
   - **Addresses**: Finding C2, R-011, SVCASS Point 9

3. **[C3] Complete Data Protection Impact Assessment (DPIA)**: Cross-service data sharing (housing-health, social care-benefits) processes citizen PII at scale. UK GDPR Article 35 mandates a DPIA before processing begins. Run `/arckit:dpia` to produce DPIA.
   - **Effort**: 4-6 hours
   - **Owner**: Data Protection Officer / MHCLG Digital Director
   - **Addresses**: Finding C3, R-011, R-012, NFR-C-001

### High Priority Actions (SHOULD resolve before Alpha phase)

4. **[H1] Create Data Model**: 5 DR-xxx requirements exist (including OFFICIAL-SENSITIVE data) but no data model with ERD, entity catalogue, or data governance matrix. Run `/arckit:data-model` to produce a comprehensive data model.
   - **Effort**: 3-4 hours
   - **Owner**: Data Architect

5. **[H2] Create Traceability Matrix**: Informal traceability exists across artifacts but no formal matrix. Run `/arckit:traceability` to consolidate all traceability links.
   - **Effort**: 2-3 hours
   - **Owner**: Business Analyst

6. **[H3] Formalise Architecture Decision Records**: 4 key decisions are documented informally in the context diagram. Run `/arckit:adr` to create formal ADRs with options analysis.
   - **Effort**: 2-3 hours per ADR
   - **Owner**: Technical Architect

7. **[H4] Assign Document Owners**: All 9 artifacts have `[OWNER_NAME_AND_ROLE]` placeholder. Assign named individuals before documents progress from DRAFT to IN_REVIEW.
   - **Effort**: 30 minutes
   - **Owner**: Programme Director

8. **[H5] Reconcile Budget Figures**: SOBC and PLAN show different TCO figures (£29M vs £38.2M). Add a reconciliation note to both documents explaining scoping differences.
   - **Effort**: 1 hour
   - **Owner**: Programme Director / Finance Lead

9. **[H6] Fix NFR Prefix Inconsistency**: Rename NFR-S-001 (Scalability) to NFR-SC-001 to avoid confusion with Security prefix. Update all references.
   - **Effort**: 30 minutes
   - **Owner**: Business Analyst

### Medium Priority Actions (Address during Alpha)

10. **[M1] Fix NFR Count**: Update REQ executive summary from "18 non-functional requirements" to "20 non-functional requirements". Update PLAN and SVCASS references.
    - **Effort**: 15 minutes

11. **[M2] Produce HLD During Alpha**: Scheduled for Alpha weeks 21-24 per PLAN. Ensure HLD covers all 46 requirements including NFRs and DRs.
    - **Effort**: Per PLAN schedule

12. **[M3] Address Service Assessment Amber Ratings**: 9 of 14 points are Amber. Key actions: conduct primary user research, prototype testing, create channel strategy, accessibility testing plan.
    - **Effort**: Per SVCASS recommendations

13. **[M4] Strengthen Open Source Requirement**: Upgrade NFR-M-003 from SHOULD_HAVE to MUST_HAVE to align with Principle P23 and GDS Service Standard Point 12.
    - **Effort**: 15 minutes

---

## Metrics Dashboard

### Requirement Quality

- Total Requirements: 46
- Ambiguous Requirements: 0
- Duplicate Requirements: 0
- Untestable Requirements: 0
- Priority Distribution: 34 MUST (74%), 7 SHOULD (15%), 0 MAY, 5 DR (11% unclassified)
- **Quality Score**: 85%

### Architecture Alignment

- Principles Assessed: 16 of 25 key principles
- Principles Compliant: 13
- Principles Partial: 3 (P5, P11, P23)
- Principles Violations: 0
- **Alignment Score**: 81%

### Traceability

- Requirements with stakeholder tracing: 46/46 (100%)
- Requirements with design coverage: 21/46 (46%)
- Requirements with full HLD/DLD coverage: 0/46 (0%)
- Orphan design elements: 0
- Formal traceability matrix: ❌ Missing
- **Traceability Score**: 40%

### Stakeholder Traceability

- Requirements traced to stakeholder goals: 100%
- Orphan requirements: 0
- Conflicts resolved: 100% (2/2)
- RACI governance alignment: 100%
- **Stakeholder Score**: 95%

### Risk Management

- Total risks: 20
- High/Very High risks mitigated: 100% (all 8 High reduced to Medium)
- Risks exceeding appetite: 7 (35%) — all documented with escalation paths
- Risk owners from RACI: 100%
- Risk-SOBC alignment: 100%
- **Risk Management Score**: 88%

### Business Case

- Benefits traced to stakeholder goals: 100%
- Benefits supported by requirements: 100%
- Benefits measurable: 50% (3 high confidence, 3 low confidence)
- Budget adequacy: ⚠️ Discrepancy needs reconciliation
- Do Nothing baseline: ✅ Yes
- Sensitivity analysis: ✅ Yes
- Optimism bias applied: ✅ Yes
- **Business Case Score**: 82%

### Data Model

- DR-xxx requirements: 5
- DR-xxx mapped to entities: 0%
- Data model artifact: ❌ Missing
- **Data Model Score**: 20%

### UK Government Compliance

- TCoP Assessment: ❌ Not done (0/130)
- SECD Assessment: ❌ Not done
- DPIA: ❌ Not done
- Service Assessment Preparation: ✅ Done (5 Green, 9 Amber)
- **UK Gov Compliance Score**: 25%

### Overall Governance Health

| Category | Weight | Score | Weighted |
|----------|--------|-------|----------|
| Requirements Quality | 15% | 85% | 12.8 |
| Architecture Alignment | 10% | 81% | 8.1 |
| Stakeholder Traceability | 10% | 95% | 9.5 |
| Risk Management | 10% | 88% | 8.8 |
| Business Case | 10% | 82% | 8.2 |
| Traceability | 15% | 40% | 6.0 |
| UK Gov Compliance | 15% | 25% | 3.8 |
| Data Model | 5% | 20% | 1.0 |
| Design Coverage | 10% | 30% | 3.0 |
| **Total** | **100%** | | **61.2** |

**Score**: 61/100
**Grade**: D (60-69%)

**Grade Thresholds**:

- A (90-100%): Excellent governance, ready to proceed
- B (80-89%): Good governance, minor issues
- C (70-79%): Adequate governance, address high-priority issues
- D (60-69%): Poor governance, major rework needed
- F ( < 60%): Insufficient governance, do not proceed

> **Context**: The D grade reflects three critical compliance gaps (TCoP, SECD, DPIA) and missing downstream artifacts (data model, traceability, HLD/DLD). The foundation artifacts (stakeholders, requirements, risk, SOBC) are excellent — scoring 85-95% individually. Addressing the 3 critical and 6 high-priority findings would raise the overall score to approximately 78% (Grade C), with further improvement to Grade B expected after Alpha HLD and traceability production.

---

## Next Steps

### Immediate Actions

1. **❌ DO NOT PROCEED** to Alpha without addressing the 3 CRITICAL issues:
   - Run: `/arckit:tcop` — Technology Code of Practice assessment
   - Run: `/arckit:secure` — Secure by Design assessment with threat model
   - Run: `/arckit:dpia` — Data Protection Impact Assessment for cross-service data sharing

2. **Address HIGH issues** in parallel with Alpha preparation:
   - Run: `/arckit:data-model` — Create data model with ERD and GDPR compliance
   - Run: `/arckit:traceability` — Generate formal traceability matrix
   - Run: `/arckit:adr` — Formalise architecture decision records
   - Assign document owners to all artifacts
   - Reconcile SOBC and PLAN budget figures

3. **Re-run analysis** after fixes:
   - Run: `/arckit:analyze` — Verify improvement in governance health score
   - Target: 78%+ (Grade C) before entering Alpha

### Suggested Command Sequence

```text
/arckit:tcop          → TCoP assessment (addresses C1)
/arckit:secure        → Secure by Design assessment (addresses C2)
/arckit:dpia          → Data Protection Impact Assessment (addresses C3)
/arckit:data-model    → Data model with ERD (addresses H1)
/arckit:adr           → Architecture Decision Records (addresses H3)
/arckit:traceability  → Formal traceability matrix (addresses H2)
/arckit:analyze       → Re-run analysis (verify improvement)
```

---

## Detailed Findings

### Finding C1: No Technology Code of Practice Assessment (CRITICAL)

**Severity**: CRITICAL
**Category**: UK Government Compliance
**Location**: Missing artifact — no `ARC-001-TCOP-*.md` in project directory

**Description**:
The Technology Code of Practice (TCoP) assessment is mandatory for all UK Government technology projects. GDS Local is a DSIT/GDS programme and must demonstrate compliance with all 13 TCoP points. No formal assessment exists.

**Impact**:
Without a TCoP assessment, the programme cannot demonstrate compliance to DSIT Spend Controls, Cabinet Office, or NAO audit. Technology decisions may inadvertently conflict with TCoP requirements. GDS Service Standard Point 12 (Make new source code open) and Point 13 (Use and contribute to open standards) directly reference TCoP.

**Recommendation**:
Run `/arckit:tcop` to produce a formal TCoP assessment. Architecture principles (ARC-000-PRIN-v1.1) already reference several TCoP points, providing a strong foundation for the assessment.

**Estimated Effort**: 2-3 hours

---

### Finding C2: No Secure by Design Assessment (CRITICAL)

**Severity**: CRITICAL
**Category**: UK Government Compliance
**Location**: Missing artifact — no `ARC-001-SECD-*.md` in project directory

**Description**:
The programme processes citizen PII across organisational boundaries (cross-service data sharing between housing, health, and social care). Architecture Principle P5 (Security by Design) is marked **NON-NEGOTIABLE** and requires a threat model, security controls mapping, and NCSC Secure by Design checklist. None of these exist. The Service Assessment (ARC-001-SVCASS-v1.0, Point 9) identifies this as a critical gap.

**Impact**:
Without a SECD assessment and threat model:
- Security architecture decisions may be made without systematic threat analysis
- NCSC engagement (planned for Alpha week 21-23 per PLAN) lacks a baseline document
- GDS Service Standard Point 9 assessment will likely fail
- Risk R-011 (data sharing privacy breach, residual 10, exceeds appetite by +4) is not systematically mitigated at the architecture level

**Evidence**:
- ARC-000-PRIN-v1.1, P5: "Security is NOT a feature to be added later — it is a foundational requirement"
- ARC-001-SVCASS-v1.0, Point 9: "No Secure by Design (SECD) assessment or DPIA despite cross-service citizen data sharing"
- ARC-001-REQ-v1.0, NFR-SEC-005: "NCSC Secure by Design review at architecture and design stages"

**Recommendation**:
Run `/arckit:secure` before entering Alpha. The threat model should cover:
- Cross-organisational data flows (STRIDE analysis)
- OneLogin federation attack surface
- Tenant isolation between councils
- API gateway threat model

**Estimated Effort**: 4-6 hours

---

### Finding C3: No Data Protection Impact Assessment (CRITICAL)

**Severity**: CRITICAL
**Category**: UK Government Compliance
**Location**: Missing artifact — no DPIA document in project directory

**Description**:
The programme intends to share citizen data between housing, social care, and health services across local authority boundaries. This constitutes large-scale processing of sensitive personal data. Under UK GDPR Article 35, a DPIA is **mandatory** before processing begins.

**Impact**:
Without a DPIA:
- The programme cannot lawfully begin data sharing pilots (ICO sandbox engagement requires DPIA evidence)
- Risk R-011 (data sharing privacy breach) and R-012 (UK GDPR non-compliance) both exceed risk appetite and lack their primary architectural mitigation
- NFR-C-001 explicitly requires "DPIAs completed for all cross-service data sharing" — this requirement is unmet
- ICO endorsement of the data sharing framework (a critical success factor per SOBC) is unlikely without completed DPIAs

**Evidence**:
- ARC-001-REQ-v1.0, NFR-C-001: "Data Protection Impact Assessments (DPIAs) completed for all cross-service data sharing"
- ARC-001-RISK-v1.0, R-011: "Data sharing privacy breach triggers ICO enforcement" (Residual 10, Appetite 6, Excess +4)
- ARC-001-SOBC-v1.0: "ICO endorsement" listed as Critical Success Factor #4
- ARC-001-PLAN-v1.0: DPIA approach scheduled for Alpha weeks 13-18

**Recommendation**:
Run `/arckit:dpia` to produce a DPIA covering:
- 3 pilot data sharing use cases (housing-health, social care-benefits, planning-transport)
- Lawful basis for each sharing arrangement
- Privacy risks and mitigations
- Citizen rights implementation

**Estimated Effort**: 4-6 hours

---

### Finding H1: No Data Model Despite DR-xxx Requirements (HIGH)

**Severity**: HIGH
**Category**: Data Model
**Location**: Missing artifact — no `ARC-001-DATA-*.md`

**Description**:
5 data requirements (DR-001 to DR-005) are defined in the requirements document, including OFFICIAL-SENSITIVE data (DR-002: identity federation data, DR-003: data sharing audit logs). No data model exists with entity-relationship diagrams, data governance matrix, or CRUD matrix.

**Recommendation**:
Run `/arckit:data-model` to create a comprehensive data model. Priority entities: council registration (DR-001), identity federation events (DR-002), data sharing audit trail (DR-003), data sharing agreements (DR-004).

**Estimated Effort**: 3-4 hours

---

### Finding H5: Budget Discrepancy Between SOBC and PLAN (HIGH)

**Severity**: HIGH
**Category**: Consistency
**Location**: ARC-001-SOBC-v1.0 and ARC-001-PLAN-v1.0

**Description**:
The SOBC states a midpoint 3-year TCO of £29M (range £24-34M) for Option 2. The Project Plan shows a 3-year TCO of £38.2M including Year 1 post-launch operational costs and 15% contingency. The difference (£29M vs £38.2M) represents a 32% discrepancy.

The likely explanation is different scoping:
- SOBC separates programme costs (£29.6M high end) from steady-state operational costs (£3.3M/year)
- PLAN includes Year 1 post-launch operational costs (£5.5M) and more granular team costs

**Impact**:
Budget inconsistency undermines confidence in financial planning. DSIT Finance and Cabinet Office Spend Controls will question which figure is authoritative. NAO audit would flag the discrepancy.

**Recommendation**:
Add a reconciliation note to both SOBC and PLAN explaining the different scoping assumptions. Confirm which figure is the authoritative spending envelope for DSIT Finance approval.

**Estimated Effort**: 1 hour

---

### Finding H6: NFR Prefix Inconsistency (HIGH)

**Severity**: HIGH
**Category**: Requirements Quality
**Location**: ARC-001-REQ-v1.0

**Description**:
NFR-S-001 uses the prefix "S" for Scalability. Security requirements use the prefix "SEC" (NFR-SEC-001 to NFR-SEC-005). The "S" prefix is commonly associated with Security in NFR taxonomies, creating potential confusion.

**Recommendation**:
Rename NFR-S-001 to NFR-SC-001 (Scalability) to eliminate ambiguity. Update all references in PLAN, SVCASS, and any downstream documents.

**Estimated Effort**: 30 minutes

---

## Appendix A: Artifacts Analyzed

| Artifact | Location | Last Modified | Status |
|----------|----------|---------------|--------|
| Architecture Principles | `projects/000-global/ARC-000-PRIN-v1.1.md` | 2026-02-16 | ✅ Analyzed |
| Stakeholder Drivers | `projects/001-gds-local/ARC-001-STKE-v1.0.md` | 2026-02-16 | ✅ Analyzed |
| Requirements | `projects/001-gds-local/ARC-001-REQ-v1.0.md` | 2026-02-16 | ✅ Analyzed |
| Risk Register | `projects/001-gds-local/ARC-001-RISK-v1.0.md` | 2026-02-17 | ✅ Analyzed |
| Business Case (SOBC) | `projects/001-gds-local/ARC-001-SOBC-v1.0.md` | 2026-02-17 | ✅ Analyzed |
| Project Plan | `projects/001-gds-local/ARC-001-PLAN-v1.0.md` | 2026-02-17 | ✅ Analyzed |
| Research v1.0 | `projects/001-gds-local/ARC-001-RSCH-v1.0.md` | 2026-02-16 | ✅ Noted |
| Research v2.0 | `projects/001-gds-local/ARC-001-RSCH-v2.0.md` | 2026-02-17 | ✅ Noted |
| Service Assessment | `projects/001-gds-local/ARC-001-SVCASS-v1.0.md` | 2026-02-28 | ✅ Analyzed |
| C4 Context Diagram | `projects/001-gds-local/diagrams/ARC-001-DIAG-001-v1.0.md` | 2026-02-26 | ✅ Analyzed |
| Previous Analysis | `projects/001-gds-local/ARC-001-ANAL-v1.0.md` | 2026-02-28 | ✅ Superseded by this report |
| TCoP Assessment | — | — | ❌ Not Found |
| Secure by Design | — | — | ❌ Not Found |
| DPIA | — | — | ❌ Not Found |
| Data Model | — | — | ❌ Not Found |
| Traceability Matrix | — | — | ❌ Not Found |
| ADRs | — | — | ❌ Not Found |
| HLD | — | — | ❌ Not Found (expected pre-Alpha) |
| DLD | — | — | ❌ Not Found (expected pre-Alpha) |

---

## Appendix B: Analysis Methodology

**Analysis Date**: 2026-02-28
**Analyzed By**: ArcKit `/arckit.analyze` command

**Checks Performed**:

- Requirements completeness, quality, and priority distribution (46 requirements)
- Architecture principles compliance (16 of 25 principles assessed)
- Stakeholder traceability (11 drivers, 6 goals)
- Risk coverage and mitigation (20 risks, 7 exceeding appetite)
- Business case alignment (5-case model, BCR 2.8:1)
- UK Government compliance (TCoP, SECD, DPIA, Service Standard)
- Data model coverage (5 DR-xxx requirements)
- Design quality (context diagram, no HLD/DLD)
- Cross-artifact consistency (terminology, budget, timeline, technology stack)
- Security and compliance posture

**Severity Classification**:

- CRITICAL: Blocks procurement/implementation, must resolve immediately — 3 findings
- HIGH: Significant risk, resolve before major milestones — 6 findings
- MEDIUM: Should be addressed, can proceed with caution — 4 findings
- LOW: Minor issues, address when convenient — 2 findings

**Total Findings**: 15

---

**Generated by**: ArcKit `/arckit:analyze` command
**Generated on**: 2026-02-28 22:15 GMT
**ArcKit Version**: 2.20.1
**Project**: GDS Local (Project 001)
**AI Model**: Claude Opus 4.6
**Generation Context**: Comprehensive analysis of 10 artifacts (ARC-000-PRIN-v1.1, ARC-001-STKE-v1.0, ARC-001-REQ-v1.0, ARC-001-RISK-v1.0, ARC-001-SOBC-v1.0, ARC-001-PLAN-v1.0, ARC-001-RSCH-v1.0/v2.0, ARC-001-SVCASS-v1.0, ARC-001-DIAG-001-v1.0). Identified 15 findings (3 CRITICAL, 6 HIGH, 4 MEDIUM, 2 LOW). Previous analysis v1.0 superseded.
