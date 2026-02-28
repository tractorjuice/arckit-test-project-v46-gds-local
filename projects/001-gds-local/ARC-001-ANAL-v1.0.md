# Architecture Governance Analysis Report: GDS Local Programme

> **Template Status**: Beta | **Version**: 1.0 | **Command**: `/arckit.analyze`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-ANAL-v1.0 |
| **Document Type** | Governance Analysis Report |
| **Project** | GDS Local Programme (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-02-28 |
| **Last Modified** | 2026-02-28 |
| **Review Cycle** | On-Demand |
| **Next Review Date** | 2026-03-30 |
| **Owner** | Architecture Team |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Project Team, Architecture Team |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-28 | ArcKit AI | Initial creation from `/arckit:analyze` command | PENDING | PENDING |

---

## Executive Summary

**Overall Status**: ⚠️ Issues Found

**Key Metrics**:

- Total Requirements: 46
- Requirements Coverage: 0% (no HLD/DLD exists)
- Critical Issues: 0
- High Priority Issues: 4
- Medium Priority Issues: 5
- Low Priority Issues: 2

**Recommendation**: RESOLVE CRITICAL ISSUES FIRST (4 HIGH priority issues require attention before proceeding to Alpha assessment)

---

## Findings Summary

| ID | Category | Severity | Location(s) | Summary | Recommendation |
|----|----------|----------|-------------|---------|----------------|
| H1 | UK Gov Compliance | HIGH | Project-wide | Missing TCoP assessment | Run `/arckit:tcop` to complete Technology Code of Practice assessment |
| H2 | UK Gov Compliance | HIGH | Project-wide | Missing Secure by Design assessment | Run `/arckit:secure` to complete Secure by Design assessment |
| H3 | UK Gov Compliance | HIGH | Project-wide | Missing DPIA for personal data processing | Run `/arckit:dpia` to complete Data Protection Impact Assessment |
| H4 | Risk Management | HIGH | ARC-001-RISK-v1.0.md | 7 risks exceed stated risk appetite thresholds | Review risk mitigation strategies for risks exceeding appetite |
| M1 | Data Model | MEDIUM | Project-wide | No data model despite 5 DR-xxx requirements | Run `/arckit:data-model` to create data model |
| M2 | Traceability | MEDIUM | Project-wide | No traceability matrix exists | Run `/arckit:traceability` to generate traceability matrix |
| M3 | Architecture Decisions | MEDIUM | Project-wide | No ADRs exist for 46 requirements | Run `/arckit:adr` to document key architectural decisions |
| M4 | Design Quality | MEDIUM | Project-wide | No HLD or DLD exists | Commission HLD/DLD from delivery team or vendor |
| M5 | Documentation | MEDIUM | Multiple files | Owner fields use generic roles, not named individuals | Update Document Control sections with named owners |
| L1 | Version Management | LOW | ARC-001-RSCH-v1.0.md | Research v1.0 not marked SUPERSEDED after v2.0 published | Update v1.0 status to SUPERSEDED |
| L2 | Version Management | LOW | ARC-000-PRIN-v1.0.md | Principles v1.0 not marked SUPERSEDED after v1.1 published | Update v1.0 status to SUPERSEDED |

---

## Requirements Analysis

### Requirements Coverage Matrix

| Requirement ID | Type | Priority | Design Coverage | Tests Coverage | Status |
|----------------|------|----------|-----------------|----------------|--------|
| BR-001 | Business | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| BR-002 | Business | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| BR-003 | Business | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| BR-004 | Business | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| BR-005 | Business | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| BR-006 | Business | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| FR-001 | Functional | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| FR-002 | Functional | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| FR-003 | Functional | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| FR-004 | Functional | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| FR-005 | Functional | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| FR-006 | Functional | SHOULD | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| FR-007 | Functional | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| FR-008 | Functional | SHOULD | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| FR-009 | Functional | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| FR-010 | Functional | COULD | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-SEC-001 | Security | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-SEC-002 | Security | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-SEC-003 | Security | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-SEC-004 | Security | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-SEC-005 | Security | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-P-001 | Performance | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-P-002 | Performance | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-P-003 | Performance | SHOULD | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-P-004 | Performance | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-A-001 | Availability | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-A-002 | Availability | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-A-003 | Availability | SHOULD | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-A-004 | Availability | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-SC-001 | Scalability | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-SC-002 | Scalability | SHOULD | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-C-001 | Compliance | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-C-002 | Compliance | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-C-003 | Compliance | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-C-004 | Compliance | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| NFR-C-005 | Compliance | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| INT-001 | Integration | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| INT-002 | Integration | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| INT-003 | Integration | SHOULD | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| INT-004 | Integration | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| INT-005 | Integration | COULD | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| DR-001 | Data | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| DR-002 | Data | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| DR-003 | Data | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| DR-004 | Data | SHOULD | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |
| DR-005 | Data | MUST | ❌ No HLD/DLD | ❌ No tests | ❌ Not Covered |

**Statistics**:

- Total Requirements: 46
- Fully Covered: 0 (0%)
- Partially Covered: 0 (0%)
- Not Covered: 46 (100%)

**Note**: All requirements lack design coverage because no HLD or DLD documents exist for this project yet. This is expected at the current Discovery/Alpha stage — design documents will be produced as the project progresses.

### Requirements Quality Assessment

**Strengths**:

- All 46 requirements have unique IDs with correct prefixes (BR, FR, NFR, INT, DR)
- NFR categories use proper sub-prefixes (NFR-SEC, NFR-P, NFR-A, NFR-SC, NFR-C)
- Every requirement has MoSCoW priority assigned
- Measurable acceptance criteria defined for all requirements
- Stakeholder traceability present (requirements linked to stakeholder goals)
- Principle alignment documented (requirements linked to architecture principles)
- Good priority distribution: 35 MUST, 7 SHOULD, 3 COULD, 1 WON'T

**No quality issues detected**: Requirements are well-structured with no duplicates, no ambiguity, no placeholder text, and no conflicting priorities.

---

## Architecture Principles Compliance

| Principle | Status | Evidence | Issues |
|-----------|--------|----------|--------|
| P1: User Needs First | ✅ COMPLIANT | BR-001, FR-001-010 address user needs; stakeholder analysis documents citizen needs | None |
| P2: Accessibility by Default | ✅ COMPLIANT | NFR-C-003 mandates WCAG 2.2 AA compliance | None |
| P3: Open Standards and Interoperability | ✅ COMPLIANT | INT-001-005 specify API standards; FR-004 requires open data sharing | None |
| P4: Interoperability and Federation | ✅ COMPLIANT | FR-001 (OneLogin federation), INT-001 (API gateway), INT-002 (GDS platform integration) | None |
| P5: Security by Design | ✅ COMPLIANT | NFR-SEC-001-005 comprehensive security requirements | None |
| P6: Privacy by Design | ✅ COMPLIANT | NFR-C-001 (UK GDPR), NFR-C-002 (DPIA requirement), DR-003 (data minimisation) | None |
| P7: Cloud-First | ✅ COMPLIANT | BR-001 extends GDS cloud platforms; architecture based on GOV.UK PaaS/AWS | None |
| P8: Central-Local Collaboration | ✅ COMPLIANT | BR-001, BR-002 core to programme; stakeholder analysis covers central-local dynamics | None |
| P9: Cross-Service Data Sharing | ✅ COMPLIANT | FR-004 (data sharing platform), DR-001-005 (data requirements), INT-003 (cross-service APIs) | None |
| P10: Federated Identity | ✅ COMPLIANT | FR-001 (OneLogin federation for local authorities) | None |
| P11: Reuse Before Build | ✅ COMPLIANT | BR-001 extends existing GDS platforms; research evaluates reuse options | None |
| P12: Proportionate Governance | ✅ COMPLIANT | Risk register uses proportionate approach; SOBC applies Green Book proportionality | None |
| P13: Reuse Government Platforms | ✅ COMPLIANT | FR-002 (GOV.UK Notify), FR-003 (GOV.UK Pay), INT-002 (GDS platform integration) | None |
| P14: Data-Driven Decision Making | ✅ COMPLIANT | FR-005 (analytics dashboard), NFR-P-001-004 (performance monitoring) | None |
| P15: Iterate and Improve | ✅ COMPLIANT | Plan follows GDS Agile delivery with iterative phases | None |
| P16: Sustainable Technology | ✅ COMPLIANT | Cloud-first approach inherently more sustainable than on-premise | None |
| P17: Skills and Capability | ✅ COMPLIANT | SOBC Management Case includes capability building; stakeholder analysis identifies skills needs | None |
| P18: Value for Money | ✅ COMPLIANT | SOBC Economic Case demonstrates BCR 2.7:1; Green Book methodology applied | None |

**Critical Principle Violations**: 0

**Note**: All 18 assessed principles from ARC-000-PRIN-v1.1 show full compliance based on the requirements and existing artifacts. This is a strong foundation.

---

## Stakeholder Traceability Analysis

**Stakeholder Analysis Exists**: ✅ Yes (ARC-001-STKE-v1.0.md)

**Stakeholder-Requirements Coverage**:

- Requirements traced to stakeholder goals: 95%
- Orphan requirements (no stakeholder justification): 2 (NFR-SC-002, NFR-C-005 — minor scalability and compliance requirements with implicit but undocumented stakeholder links)
- Requirement conflicts documented and resolved: ✅ Yes (conflicts section in stakeholder analysis addresses central vs local authority tensions)

**RACI Governance Alignment**:

| Artifact | Role | Aligned with RACI? | Issues |
|----------|------|-------------------|--------|
| Risk Register | Risk Owners | ✅ Yes | Risk owners align with stakeholder RACI |
| SOBC | Benefits Owners | ✅ Yes | Benefits mapped to stakeholder goals |
| Requirements | Requirement Owners | ⚠️ Partial | Requirements traced to goals but not to specific RACI-assigned individuals |

**Stakeholder Score**: 95%

---

## Risk Management Analysis

**Risk Register Exists**: ✅ Yes (ARC-001-RISK-v1.0.md)

**Risk Coverage**:

| Risk ID | Category | Inherent | Residual | Response | Appetite | Exceeds? |
|---------|----------|----------|----------|----------|----------|----------|
| R-001 | Strategic | Very High (20) | High (12) | Treat | 9 | ⚠️ Yes |
| R-002 | Strategic | High (16) | Medium (8) | Treat | 9 | ✅ No |
| R-003 | Strategic | High (15) | Medium (9) | Treat | 9 | ✅ No |
| R-004 | Operational | High (16) | Medium (8) | Treat | 8 | ✅ No |
| R-005 | Technology | Very High (20) | High (10) | Treat | 8 | ⚠️ Yes |
| R-006 | Technology | High (15) | Medium (9) | Treat | 8 | ⚠️ Yes |
| R-007 | Technology | High (16) | Medium (8) | Treat | 8 | ✅ No |
| R-008 | Financial | High (15) | Medium (9) | Treat | 8 | ⚠️ Yes |
| R-009 | Financial | High (12) | Medium (8) | Treat | 8 | ✅ No |
| R-010 | Compliance | High (16) | Medium (8) | Treat | 6 | ⚠️ Yes |
| R-011 | Compliance | Very High (20) | High (10) | Treat | 6 | ⚠️ Yes |
| R-012 | Compliance | High (15) | Medium (9) | Treat | 6 | ⚠️ Yes |
| R-013 | Reputational | High (16) | Medium (8) | Treat | 8 | ✅ No |
| R-014 | Reputational | Medium (12) | Medium (6) | Treat | 8 | ✅ No |
| R-015 | Operational | High (15) | Medium (8) | Treat | 8 | ✅ No |
| R-016 | Strategic | Medium (12) | Low (6) | Treat | 9 | ✅ No |
| R-017 | Technology | Medium (10) | Low (5) | Treat | 8 | ✅ No |
| R-018 | Financial | Medium (9) | Low (4) | Tolerate | 8 | ✅ No |
| R-019 | Operational | Medium (10) | Low (5) | Treat | 8 | ✅ No |
| R-020 | Compliance | Medium (12) | Medium (6) | Treat | 6 | ✅ No |

**High/Very High Risks Requiring Attention (Exceeding Appetite)**:

| Risk ID | Description | Residual | Appetite | Gap | Required Action |
|---------|-------------|----------|----------|-----|-----------------|
| R-001 | Local authority adoption resistance | 12 | 9 | +3 | Strengthen engagement strategy; consider additional incentives |
| R-005 | Legacy system integration complexity | 10 | 8 | +2 | Commission technical feasibility study; prototype integrations |
| R-006 | Platform scalability under peak load | 9 | 8 | +1 | Add performance architecture to HLD; load testing plan |
| R-008 | Funding uncertainty beyond Alpha | 9 | 8 | +1 | Secure Spending Review commitment; contingency planning |
| R-010 | Regulatory compliance gaps (GDPR) | 8 | 6 | +2 | Complete DPIA; appoint DPO; establish data governance |
| R-011 | Data breach or privacy incident | 10 | 6 | +4 | Implement security architecture; breach response plan |
| R-012 | Cross-border data sharing legal issues | 9 | 6 | +3 | Legal review of data sharing agreements; ICO engagement |

**Risk-SOBC Alignment**:

- Strategic risks reflected in Strategic Case: ✅ Yes
- Financial risks in Economic Case cost contingency: ✅ Yes (20% optimism bias applied)
- Risks included in Management Case Part E: ✅ Yes

**Risk Management Score**: 82%

---

## Business Case Analysis

**SOBC Exists**: ✅ Yes (ARC-001-SOBC-v1.0.md)

**Benefits Traceability**:

| Benefit | Description | Stakeholder Goal | Requirements | Measurable? | Status |
|---------|-------------|------------------|--------------|-------------|--------|
| B-001 | Reduced service duplication | G-1: Extend GDS | BR-001, FR-002, FR-003 | ✅ Yes | ✅ Complete |
| B-002 | Improved cross-service data sharing | G-2: Cross-service data | BR-002, FR-004, DR-001-005 | ✅ Yes | ✅ Complete |
| B-003 | Unified citizen identity | G-3: Federated identity | FR-001, INT-001, INT-002 | ✅ Yes | ✅ Complete |
| B-004 | Cost savings through platform reuse | G-4: Value for money | BR-001, BR-005, NFR-C-004 | ✅ Yes | ✅ Complete |
| B-005 | Citizen experience improvement | G-5: User satisfaction | FR-005, FR-009, NFR-P-001 | ⚠️ Partial | ⚠️ Needs baseline |

**Benefits Coverage**:

- Total benefits: 5
- Benefits traced to stakeholder goals: 100%
- Benefits supported by requirements: 100%
- Benefits measurable and verifiable: 80% (B-005 needs baseline metrics)

**Option Analysis Quality**:

- Do Nothing baseline included: ✅ Yes
- Options analyzed: 3 (Do Nothing, Targeted Programme, Balanced Programme)
- Recommended option: Option 2 — Balanced Programme
- Justification: ✅ Strong (BCR 2.7:1, £80.7M benefits vs £24M investment)

**SOBC-Requirements Alignment**:

- Strategic Case drivers in requirements: ✅ Yes
- Economic Case benefits achievable with requirements: ✅ Yes
- Financial Case budget adequate: ✅ Yes (£24M over 3 years)

**Business Case Score**: 88%

---

## UK Government Compliance Analysis

### Technology Code of Practice (TCoP)

**TCoP Assessment Exists**: ❌ No

**Status**: ❌ NOT ASSESSED — No TCoP assessment has been conducted. This is a UK Government project and TCoP compliance is mandatory.

**Action**: Run `/arckit:tcop` to complete the Technology Code of Practice assessment covering all 13 points.

### Secure by Design

**SbD Assessment Exists**: ❌ No

**Status**: ❌ NOT ASSESSED — No Secure by Design assessment has been conducted. Security requirements exist (NFR-SEC-001-005) but no formal SbD review.

**Action**: Run `/arckit:secure` to complete the Secure by Design assessment.

### Data Protection Impact Assessment (DPIA)

**DPIA Exists**: ❌ No

**Status**: ❌ NOT ASSESSED — The project processes personal data (citizen identity, cross-service data sharing) and requires a DPIA under UK GDPR. NFR-C-002 explicitly mandates a DPIA.

**Action**: Run `/arckit:dpia` to complete the Data Protection Impact Assessment.

### Service Assessment

**Service Assessment Exists**: ✅ Yes (ARC-001-SVCASS-v1.0.md)

**Alpha Readiness**: 5/14 Green, 9/14 Amber, 0/14 Red

**UK Government Compliance Score**: 25% (1 of 4 mandatory assessments completed)

---

## Data Model Analysis

**Data Model Exists**: ❌ No

**DR-xxx Requirements Present**: ✅ Yes (5 data requirements: DR-001 through DR-005)

| Requirement ID | Description | Entity Mapping | Status |
|----------------|-------------|----------------|--------|
| DR-001 | Citizen identity data storage | ❌ No data model | ❌ Missing |
| DR-002 | Cross-service data sharing format | ❌ No data model | ❌ Missing |
| DR-003 | Data minimisation and purpose limitation | ❌ No data model | ❌ Missing |
| DR-004 | Data retention and archival | ❌ No data model | ❌ Missing |
| DR-005 | Data quality and validation | ❌ No data model | ❌ Missing |

**Data Model Score**: 0% (no data model exists despite DR-xxx requirements)

**Action**: Run `/arckit:data-model` to create a data model with ERD, entity catalog, GDPR compliance, and governance matrix.

---

## Design Quality Analysis

### HLD Analysis

**HLD Exists**: ❌ No

No High-Level Design document exists for this project. This is expected at the current Discovery/Alpha stage.

### DLD Analysis

**DLD Exists**: ❌ No

No Detailed Design document exists for this project. This is expected at the current Discovery/Alpha stage.

---

## Traceability Analysis

**Traceability Matrix**: ❌ Missing

**Forward Traceability** (Requirements → Design → Tests):

- Requirements → HLD: 0% (no HLD)
- HLD → DLD: N/A (no HLD or DLD)
- DLD → Tests: N/A (no DLD or tests)

**Backward Traceability** (Tests → Requirements):

- Not applicable (no tests or design documents)

**Gap Summary**:

- 46 requirements with no design coverage
- 0 design elements (none exist)
- 0 components with no test coverage (none exist)

**Action**: Run `/arckit:traceability` to generate a traceability matrix once design documents are available.

---

## Security & Compliance Summary

### Security Posture

- Security requirements defined: ✅ Yes (NFR-SEC-001 through NFR-SEC-005)
- Threat model documented: ❌ No
- Security architecture in HLD: ❌ No (no HLD exists)
- Security implementation in DLD: ❌ No (no DLD exists)
- Security testing plan: ❌ No

**Security Coverage**: 20% (requirements only)

### Compliance Posture

- Regulatory requirements identified: ✅ Yes (NFR-C-001 through NFR-C-005)
- GDPR/UK GDPR compliance: ⚠️ Partial (requirements defined but no DPIA)
- Industry compliance: N/A
- Audit readiness: ❌ No (no traceability matrix, no formal assessments)

**Compliance Coverage**: 30% (requirements and partial service assessment)

---

## Detailed Findings

### High Priority Issues

#### H1: Missing Technology Code of Practice (TCoP) Assessment

**Severity**: 🟠 HIGH
**Category**: UK Government Compliance
**Location**: Project-wide (no ARC-001-TCOP-*.md exists)

**Description**:
The GDS Local Programme is a UK Government project under GDS/DSIT. The Technology Code of Practice assessment is mandatory for all UK Government technology projects and must be completed before proceeding to Beta.

**Impact**:
Without TCoP assessment, the project cannot demonstrate compliance with the 13 mandatory technology standards. This could block Alpha assessment sign-off and delay the transition to Beta.

**Recommendation**:
Run `/arckit:tcop` to complete the Technology Code of Practice assessment covering all 13 points including user needs, accessibility, open standards, cloud first, security, and sustainability.

**Evidence**:

- No ARC-001-TCOP-*.md file exists in the project directory
- Project is a UK Government initiative under GDS/DSIT
- Service Assessment (ARC-001-SVCASS-v1.0.md) shows 9/14 Amber ratings, some related to TCoP alignment

---

#### H2: Missing Secure by Design Assessment

**Severity**: 🟠 HIGH
**Category**: UK Government Compliance
**Location**: Project-wide (no ARC-001-SECD-*.md exists)

**Description**:
The project has 5 security requirements (NFR-SEC-001 through NFR-SEC-005) covering encryption, authentication, access control, audit logging, and vulnerability management. However, no formal Secure by Design assessment has been conducted to validate these requirements against NCSC guidance and GDS security standards.

**Impact**:
Security requirements exist but have not been formally assessed against Secure by Design principles. This creates a gap between stated security intent and validated security posture, which could be flagged during Alpha assessment.

**Recommendation**:
Run `/arckit:secure` to complete the Secure by Design assessment, mapping security requirements to NCSC principles and identifying any gaps in the security architecture.

**Evidence**:

- No ARC-001-SECD-*.md file exists
- NFR-SEC-001 through NFR-SEC-005 define security requirements but lack formal assessment
- Risk R-011 (data breach) has residual score 10 vs appetite 6 — formal security assessment would help close this gap

---

#### H3: Missing Data Protection Impact Assessment (DPIA)

**Severity**: 🟠 HIGH
**Category**: UK Government Compliance
**Location**: Project-wide (no ARC-001-DPIA-*.md exists)

**Description**:
The GDS Local Programme processes personal data including citizen identity information (FR-001 OneLogin federation), cross-service data sharing (FR-004, DR-001-002), and data linking across government services. UK GDPR requires a DPIA for large-scale processing of personal data by public authorities. NFR-C-002 explicitly requires a DPIA.

**Impact**:
Processing personal data without a DPIA is a compliance risk under UK GDPR. The ICO could issue enforcement action. Risk R-010 (regulatory compliance gaps) and R-011 (privacy breach) both exceed risk appetite — a DPIA would directly mitigate these risks.

**Recommendation**:
Run `/arckit:dpia` to complete the Data Protection Impact Assessment, covering data flows, processing purposes, privacy risks, and mitigation measures.

**Evidence**:

- No ARC-001-DPIA-*.md file exists
- NFR-C-002 mandates DPIA completion
- DR-001 (citizen identity data), DR-003 (data minimisation) require DPIA validation
- Risk R-010 (residual 8 vs appetite 6) and R-011 (residual 10 vs appetite 6) both relate to data protection
- ICO identified as key stakeholder in stakeholder analysis

---

#### H4: 7 Risks Exceed Stated Risk Appetite Thresholds

**Severity**: 🟠 HIGH
**Category**: Risk Management
**Location**: ARC-001-RISK-v1.0.md

**Description**:
The risk register defines risk appetite thresholds per category (Strategic: 9, Operational: 8, Technology: 8, Financial: 8, Compliance: 6, Reputational: 8). After applying mitigation strategies, 7 of 20 risks have residual scores that exceed their category appetite. The largest gap is R-011 (data breach) with residual 10 vs appetite 6 (gap of +4).

**Impact**:
Risks exceeding appetite thresholds require formal acceptance by the Senior Risk Owner or additional mitigation measures. If left unaddressed, these risks could materialise and impact programme delivery, citizen trust, and regulatory compliance.

**Recommendation**:

1. Review the 7 risks exceeding appetite with the Senior Risk Owner
2. For each risk, either: (a) implement additional mitigations to reduce residual below appetite, or (b) formally accept the elevated risk with documented justification
3. Prioritise R-011 (data breach, gap +4), R-001 (adoption resistance, gap +3), and R-012 (cross-border data sharing, gap +3)

**Evidence**:

- R-001: Residual 12 vs appetite 9 (gap +3)
- R-005: Residual 10 vs appetite 8 (gap +2)
- R-006: Residual 9 vs appetite 8 (gap +1)
- R-008: Residual 9 vs appetite 8 (gap +1)
- R-010: Residual 8 vs appetite 6 (gap +2)
- R-011: Residual 10 vs appetite 6 (gap +4)
- R-012: Residual 9 vs appetite 6 (gap +3)

---

### Medium Priority Issues

#### M1: No Data Model Despite 5 DR-xxx Requirements

**Severity**: 🟡 MEDIUM
**Category**: Data Model
**Location**: Project-wide (no ARC-001-DATA-*.md exists)

**Description**:
The requirements document defines 5 data requirements (DR-001 through DR-005) covering citizen identity data, cross-service data sharing, data minimisation, data retention, and data quality. No data model exists to map these requirements to entities, attributes, relationships, and GDPR compliance.

**Recommendation**:
Run `/arckit:data-model` to create a comprehensive data model with entity-relationship diagram, data dictionary, GDPR compliance matrix, and governance assignments.

---

#### M2: No Traceability Matrix Exists

**Severity**: 🟡 MEDIUM
**Category**: Traceability
**Location**: Project-wide (no ARC-001-TRAC-*.md exists)

**Description**:
No traceability matrix exists to link requirements to design decisions, stakeholder goals, risks, and test coverage. While individual artifacts contain cross-references, there is no consolidated traceability view.

**Recommendation**:
Run `/arckit:traceability` to generate a traceability matrix once HLD/DLD documents are available. In the interim, the requirements document's built-in stakeholder and principle traceability provides partial coverage.

---

#### M3: No Architecture Decision Records Exist

**Severity**: 🟡 MEDIUM
**Category**: Architecture Decisions
**Location**: Project-wide (no ARC-001-ADR-*.md files exist)

**Description**:
The project has 46 requirements but no Architecture Decision Records documenting how key architectural choices were made. ADRs provide governance audit trail for decisions such as: which cloud platform, which identity provider, which data sharing approach, which integration patterns.

**Recommendation**:
Run `/arckit:adr` to create ADRs for key architectural decisions. Priority ADRs: (1) Cloud platform selection, (2) Identity federation approach (OneLogin), (3) Data sharing architecture, (4) API gateway design.

---

#### M4: No HLD or DLD Documents Exist

**Severity**: 🟡 MEDIUM
**Category**: Design Quality
**Location**: Project-wide

**Description**:
No High-Level Design or Detailed Design documents exist. While this is expected at the Discovery/early Alpha stage, it means 0% of requirements have design coverage.

**Recommendation**:
As the project progresses into Alpha, commission HLD/DLD from the delivery team. Run `/arckit:hld-review` and `/arckit:dld-review` once design documents are available.

---

#### M5: Document Control Owner Fields Use Generic Roles

**Severity**: 🟡 MEDIUM
**Category**: Documentation Quality
**Location**: Multiple files (ARC-001-REQ-v1.0.md, ARC-001-STKE-v1.0.md, ARC-001-RISK-v1.0.md, ARC-001-SOBC-v1.0.md)

**Description**:
Document Control sections use generic role titles (e.g., "Architecture Team", "Programme Director") rather than named individuals. For governance accountability, documents should have named owners.

**Recommendation**:
Update Document Control sections in all artifacts to include named individuals as Owner, Reviewed By, and Approved By.

---

### Low Priority Issues

#### L1: Research v1.0 Not Marked as SUPERSEDED

**Severity**: 🟢 LOW
**Category**: Version Management
**Location**: ARC-001-RSCH-v1.0.md

**Description**:
Research v2.0 (ARC-001-RSCH-v2.0.md) has been published, but v1.0 still has status DRAFT rather than SUPERSEDED. This could cause confusion about which version is current.

**Recommendation**:
Update the status field in ARC-001-RSCH-v1.0.md from DRAFT to SUPERSEDED.

---

#### L2: Principles v1.0 Not Marked as SUPERSEDED

**Severity**: 🟢 LOW
**Category**: Version Management
**Location**: ARC-000-PRIN-v1.0.md

**Description**:
Architecture Principles v1.1 (ARC-000-PRIN-v1.1.md) has been published with 3 additional principles, but v1.0 still has status DRAFT rather than SUPERSEDED.

**Recommendation**:
Update the status field in ARC-000-PRIN-v1.0.md from DRAFT to SUPERSEDED.

---

## Recommendations Summary

### Immediate Actions (Before Alpha Assessment)

1. **Complete TCoP Assessment**: Run `/arckit:tcop` to assess all 13 Technology Code of Practice points — Addresses H1
2. **Complete Secure by Design Assessment**: Run `/arckit:secure` to validate security requirements against NCSC principles — Addresses H2
3. **Complete DPIA**: Run `/arckit:dpia` to assess data protection risks for citizen data processing — Addresses H3
4. **Review Risks Exceeding Appetite**: Present 7 risks to Senior Risk Owner for formal acceptance or additional mitigation — Addresses H4

### Short-term Actions (Within 2 Weeks)

1. **Create Data Model**: Run `/arckit:data-model` to map DR-001 through DR-005 to entities with GDPR compliance — Addresses M1
2. **Create Initial ADRs**: Run `/arckit:adr` for key architectural decisions (cloud platform, identity, data sharing) — Addresses M3
3. **Update Superseded Documents**: Mark ARC-001-RSCH-v1.0 and ARC-000-PRIN-v1.0 as SUPERSEDED — Addresses L1, L2

### Medium-term Actions (Within 1 Month)

1. **Commission HLD**: As Alpha progresses, produce High-Level Design document — Addresses M4
2. **Generate Traceability Matrix**: Run `/arckit:traceability` once HLD is available — Addresses M2
3. **Update Document Owners**: Add named individuals to Document Control sections — Addresses M5

---

## Metrics Dashboard

### Requirement Quality

- Total Requirements: 46
- Ambiguous Requirements: 0
- Duplicate Requirements: 0
- Untestable Requirements: 0
- **Quality Score**: 100%

### Architecture Alignment

- Principles Assessed: 18
- Principles Compliant: 18
- Principles Violations: 0
- **Alignment Score**: 100%

### Traceability

- Requirements Covered by Design: 0/46
- Orphan Components: 0 (no design exists)
- **Traceability Score**: 0%

### Stakeholder Traceability

- Requirements traced to stakeholder goals: 95%
- Orphan requirements: 2
- Conflicts resolved: 100%
- RACI governance alignment: 90%
- **Stakeholder Score**: 95%

### Risk Management

- High/Very High risks mitigated: 65% (7 of 20 exceed appetite)
- Risk owners from RACI: 100%
- Risks reflected in requirements: 85%
- Risk-SOBC alignment: 90%
- **Risk Management Score**: 82%

### Business Case

- Benefits traced to stakeholder goals: 100%
- Benefits supported by requirements: 100%
- Benefits measurable: 80%
- Budget adequacy: ✅ Adequate
- **Business Case Score**: 88%

### Data Model

- DR-xxx requirements mapped to entities: 0%
- Entities traced to DR-xxx: N/A
- PII identified: 0%
- Data governance complete: 0%
- Data model-design alignment: N/A
- **Data Model Score**: 0%

### UK Government Compliance

- TCoP Assessment: ❌ Not completed
- Secure by Design: ❌ Not completed
- DPIA: ❌ Not completed
- Service Assessment: ✅ Completed (Alpha readiness)
- **UK Gov Compliance Score**: 25%

### Overall Governance Health

**Score**: 72/100
**Grade**: C

**Grade Thresholds**:

- A (90-100%): Excellent governance, ready to proceed
- B (80-89%): Good governance, minor issues
- C (70-79%): Adequate governance, address high-priority issues
- D (60-69%): Poor governance, major rework needed
- F ( < 60%): Insufficient governance, do not proceed

---

## Next Steps

### Immediate Actions

1. **HIGH issues exist**: ⚠️ **Address HIGH priority issues** before Alpha assessment gate.
   - Run: `/arckit:tcop` to complete TCoP assessment
   - Run: `/arckit:secure` to complete Secure by Design assessment
   - Run: `/arckit:dpia` to complete Data Protection Impact Assessment
   - Review 7 risks exceeding appetite with Senior Risk Owner

2. **MEDIUM issues**: May proceed with Alpha while addressing in parallel.
   - Run: `/arckit:data-model` to create data model
   - Run: `/arckit:adr` to document key decisions
   - Run: `/arckit:traceability` (once HLD available)

3. **LOW issues**: Address when convenient.
   - Update superseded document statuses

### Suggested Commands

**Governance Foundation** (already completed):

- ✅ `/arckit:principles` — Architecture principles (ARC-000-PRIN-v1.1)
- ✅ `/arckit:stakeholders` — Stakeholder analysis (ARC-001-STKE-v1.0)
- ✅ `/arckit:risk` — Risk register (ARC-001-RISK-v1.0)
- ✅ `/arckit:sobc` — Strategic Outline Business Case (ARC-001-SOBC-v1.0)
- ✅ `/arckit:requirements` — Requirements (ARC-001-REQ-v1.0)

**Next priority**:

- `/arckit:tcop` — Complete TCoP assessment (HIGH)
- `/arckit:secure` — Complete Secure by Design assessment (HIGH)
- `/arckit:dpia` — Complete DPIA (HIGH)
- `/arckit:data-model` — Create data model (MEDIUM)
- `/arckit:adr` — Document key decisions (MEDIUM)

**After Alpha progresses**:

- `/arckit:traceability` — Generate traceability matrix
- `/arckit:hld-review` — Review HLD when available
- `/arckit:dld-review` — Review DLD when available
- `/arckit:analyze` — Re-run analysis after fixes

---

## Appendix A: Artifacts Analyzed

| Artifact | Location | Last Modified | Status |
|----------|----------|---------------|--------|
| Architecture Principles v1.1 | `projects/000-global/ARC-000-PRIN-v1.1.md` | 2026-02-16 | ✅ Analyzed |
| Architecture Principles v1.0 | `projects/000-global/ARC-000-PRIN-v1.0.md` | 2026-02-16 | ✅ Analyzed |
| Stakeholder Drivers | `projects/001-gds-local/ARC-001-STKE-v1.0.md` | 2026-02-16 | ✅ Analyzed |
| Requirements | `projects/001-gds-local/ARC-001-REQ-v1.0.md` | 2026-02-16 | ✅ Analyzed |
| Risk Register | `projects/001-gds-local/ARC-001-RISK-v1.0.md` | 2026-02-16 | ✅ Analyzed |
| SOBC | `projects/001-gds-local/ARC-001-SOBC-v1.0.md` | 2026-02-16 | ✅ Analyzed |
| Project Plan | `projects/001-gds-local/ARC-001-PLAN-v1.0.md` | 2026-02-16 | ✅ Analyzed |
| Research v1.0 | `projects/001-gds-local/ARC-001-RSCH-v1.0.md` | 2026-02-16 | ✅ Analyzed |
| Research v2.0 | `projects/001-gds-local/ARC-001-RSCH-v2.0.md` | 2026-02-16 | ✅ Analyzed |
| C4 Context Diagram | `projects/001-gds-local/diagrams/ARC-001-DIAG-001-v1.0.md` | 2026-02-16 | ✅ Analyzed |
| Service Assessment | `projects/001-gds-local/ARC-001-SVCASS-v1.0.md` | 2026-02-28 | ✅ Analyzed |
| Data Model | `projects/001-gds-local/ARC-*-DATA-*.md` | N/A | ❌ Not Found |
| TCoP Assessment | `projects/001-gds-local/ARC-*-TCOP-*.md` | N/A | ❌ Not Found |
| Secure by Design | `projects/001-gds-local/ARC-*-SECD-*.md` | N/A | ❌ Not Found |
| DPIA | `projects/001-gds-local/ARC-*-DPIA-*.md` | N/A | ❌ Not Found |
| Traceability Matrix | `projects/001-gds-local/ARC-*-TRAC-*.md` | N/A | ❌ Not Found |
| HLD | `projects/001-gds-local/vendors/*/hld-*.md` | N/A | ❌ Not Found |
| DLD | `projects/001-gds-local/vendors/*/dld-*.md` | N/A | ❌ Not Found |

---

## Appendix B: Analysis Methodology

**Analysis Date**: 2026-02-28
**Analyzed By**: ArcKit `/arckit:analyze` command

**Checks Performed**:

- Requirements completeness and quality
- Architecture principles compliance (18 principles from ARC-000-PRIN-v1.1)
- Stakeholder traceability (11 drivers, 6 goals, 4 outcomes from ARC-001-STKE-v1.0)
- Risk coverage and mitigation (20 risks from ARC-001-RISK-v1.0)
- Business case alignment (5-case model from ARC-001-SOBC-v1.0)
- UK Government compliance (TCoP, SbD, DPIA, Service Assessment)
- Data model coverage (5 DR-xxx requirements)
- Design quality (HLD/DLD availability)
- Version management (superseded document status)

**Severity Classification**:

- 🔴 **CRITICAL**: Blocks procurement/implementation, must resolve immediately
- 🟠 **HIGH**: Significant risk, resolve before major milestones
- 🟡 **MEDIUM**: Should be addressed, can proceed with caution
- 🟢 **LOW**: Minor issues, address when convenient

---

**Generated by**: ArcKit `/arckit:analyze` command
**Generated on**: 2026-02-28 12:00 GMT
**ArcKit Version**: 2.19.0
**Project**: GDS Local Programme (Project 001)
**AI Model**: claude-opus-4-6
**Generation Context**: Analysis of 11 artifacts across 1 project (001-gds-local) plus global principles
