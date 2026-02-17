# Strategic Outline Business Case (SOBC): GDS Local

> **Template Status**: Live | **Version**: 2.4.5 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case (SOBC) |
| **Project** | GDS Local (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-02-17 |
| **Last Modified** | 2026-02-17 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-05-17 |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | GDS Local Programme Team, GDS Director General, DSIT Minister's Office, MHCLG Digital, LGA, DSIT Finance, Cabinet Office Spend Controls, NAO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-17 | ArcKit AI | Initial creation from `/arckit:sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case (SOBC) presents the high-level justification for investing in the GDS Local programme — a DSIT/GDS initiative to extend shared digital platforms to local government, enable cross-service data sharing, and support local authority digital transformation. It follows the HM Treasury Green Book 5-case model (Strategic, Economic, Commercial, Financial, Management) and is the first stage in the business case lifecycle (SOBC → OBC → FBC).

This document is intended for the GDS Director General (Programme Board Chair), DSIT Minister, DSIT Finance, Cabinet Office Spend Controls, and HM Treasury (if spend thresholds require Treasury approval).

---

## Executive Summary

**Purpose**: GDS Local exists to bridge the digital divide between central and local government by extending proven GDS platforms (OneLogin, Notify, Pay) to 333 local authorities, enabling cross-service data sharing that improves outcomes for vulnerable citizens, and delivering £50M in cumulative savings through shared technology and integrated purchasing.

**Problem Statement**: Local authorities spend over £5 billion annually on technology with limited sharing and duplicated procurement. Data silos between services prevent joined-up support for vulnerable citizens — currently taking 15 working days to coordinate multi-service housing-health-social care support. GDS platforms serve only central government while councils independently maintain bespoke identity, notification, and payment systems.

**Proposed Solution**: A 3-year programme to (1) extend GOV.UK OneLogin to 50 local authorities by Q4 2027, (2) establish a cross-service data sharing framework with 3 pilot use cases, (3) launch a shared component catalogue with 5 reusable components, (4) create an integrated purchasing framework, and (5) build a community of practice with 100+ active councils.

**Strategic Fit**: Directly delivers the GDS Local mandate announced November 2025. Aligns with DSIT digital transformation strategy, MHCLG local government modernisation agenda, and cross-government platform economy objectives. Supports Technology Code of Practice Points 3 (reuse platforms), 4 (open standards), 9 (security), and 12 (sustainability).

**Investment Required**: £24M over 3 years (ROM ±30%)
- Capital/Programme: £18-29M (midpoint £24M)
- Ongoing Operational: £3M/year post-programme

**Expected Benefits**: £65-85M over 3 years
- Council procurement savings: £50M (independently verifiable)
- Council technology cost avoidance: £10-20M (shared platforms vs. bespoke)
- Citizen time savings and improved outcomes: £5-15M (social value, qualitative)

**Return on Investment**:
- NPV (3.5% Green Book rate): +£22M over 3 years (ROM)
- Payback Period: ~24 months
- Benefit-Cost Ratio: ~2.7:1

**Recommended Option**: Option 2: Balanced GDS Local Programme

**Key Risks** (from ARC-001-RISK-v1.0):
1. R-001: Insufficient local authority adoption (Residual 12, exceeds appetite)
2. R-011: Data sharing privacy breach triggers ICO enforcement (Residual 10)
3. R-008: Programme funding not sustained beyond Year 1 (Residual 10)

**Go/No-Go Recommendation**: **PROCEED** to requirements and detailed design phase

**Rationale**: The programme delivers compelling public value (BCR 2.7:1), directly fulfils a ministerial commitment, addresses a genuine citizen need (joined-up services), and leverages proven GDS platforms at minimal marginal cost. All 20 identified risks are manageable with active mitigation. The voluntary adoption model and LGA co-leadership mitigate the primary risk of council resistance.

**Next Steps if Approved**:
1. Secure DSIT spending review allocation: Q1 2026
2. Detailed requirements already defined (ARC-001-REQ-v1.0) — validate with pathfinder councils
3. Develop Outline Business Case (OBC) with refined costs after pathfinder learning: Q4 2026
4. Launch procurement via Digital Marketplace: Q2 2026

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
Local government in England comprises 333 councils serving 56 million citizens. Each council independently procures and manages technology for identity, notifications, payments, and hundreds of service-specific systems. There is no shared digital infrastructure between central and local government, despite citizens interacting with both tiers for housing, social care, benefits, health, education, and planning.

**Specific Pain Points** (from Stakeholder Analysis ARC-001-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| DSIT Minister | SD-1 | Cannot demonstrate digital transformation at local level | Parliamentary questions unanswered, political risk | CRITICAL |
| GDS Director General | SD-2 | GDS platforms plateau without local government adoption | Platform economy model not validated | HIGH |
| MHCLG Digital Director | SD-3 | £5B+ annual council tech spend with minimal sharing | Duplicated procurement, inconsistent quality | HIGH |
| LA Chief Executives | SD-4 | Severe budget pressures, ageing tech, workforce shortages | Service quality declining, costs rising | CRITICAL |
| LA Digital/IT Directors | SD-5 | Small teams (10-50 staff) managing commodity tech | No capacity for innovation, vendor lock-in | HIGH |
| Citizens | SD-7 | 7+ separate logins, repeat information to each service | Service abandonment, vulnerable citizens fall through cracks | CRITICAL |
| ICO | SD-8 | Data sharing without governance creates regulatory risk | Potential enforcement action | HIGH |

**Consequences of Inaction**:
- **Financial**: Councils continue spending £5B+/year on fragmented technology — an estimated £500M-£1B in duplicated procurement across 333 councils over 3 years
- **Citizen**: Vulnerable citizens continue waiting 15 working days for coordinated multi-service support; 15% service abandonment rate at login due to multiple accounts
- **Political**: Minister unable to answer parliamentary questions about local digital improvement; opposition criticism of government inaction
- **Regulatory**: Uncoordinated data sharing attempts increase GDPR breach risk; ICO enforcement becomes more likely without a governance framework

### A1.2 Strategic Drivers

**Link to Stakeholder Analysis**: This business case is informed by stakeholder analysis documented in `ARC-001-STKE-v1.0.md`, which identified 11 stakeholder drivers, 6 goals, and 4 outcomes.

**Primary Drivers** (from Stakeholder Analysis):

| Driver ID | Stakeholder | Driver Type | Driver Description | Strategic Imperative | Intensity |
|-----------|-------------|-------------|-------------------|---------------------|-----------|
| SD-1 | DSIT Minister | STRATEGIC / POLITICAL | Demonstrate digital transformation at local level | Manifesto delivery, parliamentary accountability | CRITICAL |
| SD-2 | GDS Director General | STRATEGIC | Extend GDS platform economy to local government | Platform sustainability, cross-government value | HIGH |
| SD-3 | MHCLG Digital Director | STRATEGIC / OPERATIONAL | Accelerate local government technology modernisation | Data-driven policy, council efficiency | HIGH |
| SD-4 | LA Chief Executives | OPERATIONAL / FINANCIAL | Improve services within severe budget constraints | Cost savings, service quality | CRITICAL |
| SD-7 | Citizens | CUSTOMER | Seamless access to all government services | Citizen experience, digital inclusion | CRITICAL |
| SD-8 | ICO | COMPLIANCE | Ensure lawful, transparent cross-service data sharing | Regulatory compliance, citizen trust | HIGH |
| SD-11 | NCSC | COMPLIANCE | Secure cross-government architecture | National cyber security posture | HIGH |

**Strategic Alignment**:

- **DSIT Departmental Objectives**: GDS Local is a named DSIT initiative announced November 2025. Directly delivers departmental objective to "extend proven digital platforms across government"
- **Manifesto Commitment**: Supports the government's commitment to improve public services through technology and data sharing
- **Cross-Government Strategy**: Aligns with CDDO cross-government digital strategy for shared platforms and reuse
- **Architecture Principles** (ARC-000-PRIN-v1.1): Enforces P4 (Interoperability), P8 (Central-Local Collaboration), P9 (Cross-Service Data Sharing), P10 (Federated Identity), P13 (Reuse Government Platforms), P23 (Open Source), P24 (GDS Service Standard)
- **Technology Code of Practice**: Addresses Points 1 (user needs), 3 (use cloud), 4 (open standards), 5 (secure by design), 8 (share and reuse), 12 (sustainability)

### A1.3 Stakeholder Goals

**Goals Addressed** (from Stakeholder Analysis ARC-001-STKE-v1.0):

| Goal ID | Owner | SMART Goal | Current State | Target State | Timeline |
|---------|-------|------------|---------------|--------------|----------|
| G-1 | GDS Local Programme Director | Extend GOV.UK OneLogin to 50 local authorities | 0 councils using OneLogin | 50 councils live | Q4 2027 |
| G-2 | MHCLG Digital Director | Establish data sharing framework with 3 pilot use cases across 10 councils | No structured cross-service sharing | 3 pilots, 10 councils, ICO endorsed | Q2 2027 |
| G-3 | GDS Local Programme Director | Launch shared component catalogue with 5 reusable components, 20+ councils using | 0 GDS Local components | 5 components, 20+ council adopters | Q3 2027 |
| G-4 | LGA | Establish integrated purchasing framework saving £50M over 3 years | Individual procurement, 20% premium | £50M cumulative savings, 100+ councils | Q4 2028 |
| G-5 | GDS Local Programme Director | GDS Service Standard pass for all public-facing components | No GDS Local services assessed | 100% pass at alpha and beta | Ongoing |
| G-6 | LGA | Build community of practice with 100+ active councils | Email registration only | 100+ active councils, 200+ by Q4 2027 | Q4 2026 |

### A1.4 Scope

**In Scope**:
- GOV.UK OneLogin extension to local authorities via OIDC-based identity federation
- Cross-service data sharing platform with governance framework (3 pilot use cases: housing-health, social care-benefits, planning-transport)
- Shared technology component catalogue (5 new components)
- Integrated purchasing framework for common technology needs
- Community of practice platform and programme
- API gateway and developer portal for local authority integration
- Extension of GOV.UK Notify, Pay, and Design System to local authority contexts

**Out of Scope** (for this programme):
- Replacement of existing council line-of-business systems (housing, social care, planning)
- Devolved administration services (Scotland, Wales, Northern Ireland) — future phase
- Non-digital service delivery channels (phone, face-to-face)
- Council internal IT infrastructure (networks, endpoints, email)

**Interfaces**:
- GOV.UK OneLogin platform (OIDC federation)
- GOV.UK Notify (REST API, existing)
- GOV.UK Pay (REST API, existing)
- 333 council technology estates (diverse, via open standards)
- ICO regulatory engagement (manual/semi-automated)
- Crown Commercial Service (integrated purchasing)

**Assumptions**:
1. GOV.UK OneLogin will reach sufficient maturity for local authority federation by Q3 2026 (risk if wrong: G-1 delayed by 6-12 months)
2. At least 5 councils will volunteer as pathfinders for Phase 1 (risk if wrong: programme cannot demonstrate value early)
3. ICO will engage constructively with regulatory sandbox approach (risk if wrong: G-2 blocked or significantly delayed)
4. DSIT will provide sustained programme funding for at least 3 years (risk if wrong: R-008, programme cancelled)
5. Existing GDS platform APIs require minimal modification for local authority use (risk if wrong: additional cost £2-5M)

**Dependencies**:
- **Internal**: GOV.UK OneLogin platform team capacity and roadmap
- **External**: ICO regulatory sandbox engagement (Q2 2026); LGA pathfinder council recruitment; CCS alignment on purchasing framework
- **Political**: Continued ministerial support; no machinery of government change affecting DSIT/GDS

### A1.5 Why Now?

**Urgency Factors**:
- **Ministerial Commitment**: GDS Local announced November 2025 with visible public commitment — delay risks political embarrassment
- **Council Budget Crisis**: Local authorities face the most severe funding pressures in a decade — shared platforms offer immediate cost relief
- **OneLogin Momentum**: GOV.UK OneLogin is actively being extended (discovery phase Q1-Q2 2026) — missing this window means councils build bespoke alternatives
- **Data Sharing Demand**: COVID-19 revealed the cost of data silos in multi-agency support — political and public appetite for change is at its highest
- **Technology Window**: Cloud-native, API-first platforms make sharing feasible now in ways that weren't possible 5 years ago

**Opportunity Cost of Delay**:
- **£500M-£1B** in continued duplicated council procurement over 3 years
- **Citizen harm**: Vulnerable citizens continue waiting 15 days for coordinated support — delay costs measured in welfare outcomes
- **GDS platform risk**: Without local government adoption, GDS platform economy model weakens — threatening continued platform investment
- **Competitive window**: Councils are actively procuring replacement technology now — if GDS Local doesn't provide an alternative, councils will lock into new vendor contracts for 5-7 years

**Window of Opportunity**:
- 2025-2026 spending review provides window for funding allocation
- GDS OneLogin discovery phase creates natural integration point
- LGA actively supportive and ready to convene councils
- Cross-party political support for improving local public services
- MHCLG data sharing policy agenda creates alignment with data access goals

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

Before analyzing options, define what "success" looks like:

1. **Council Adoption at Scale**: At least 50 councils actively using GDS Local platforms by Q4 2027
   - **Measure**: Number of councils with at least one live integration
   - **Threshold**: 30 councils minimum (below this, programme fails to demonstrate scale)

2. **Measurable Cost Savings**: £50M cumulative council savings independently verifiable over 3 years
   - **Measure**: Procurement savings audit, council self-reporting
   - **Threshold**: £25M minimum (below this, NAO will question value for money)

3. **Citizen Outcome Improvement**: Vulnerable citizens receive faster joined-up support through data sharing
   - **Measure**: Multi-service coordination time in pilot councils
   - **Threshold**: 50% reduction (from 15 to 7.5 days)

4. **ICO Endorsement**: Data sharing framework endorsed by ICO as lawful and proportionate
   - **Measure**: Formal ICO regulatory sandbox outcome
   - **Threshold**: ICO does not block or formally object to pilot data sharing arrangements

5. **GDS Service Standard Compliance**: All public-facing components pass Service Standard assessment
   - **Measure**: GDS assessment pass rate
   - **Threshold**: 100% pass rate at beta

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: No GDS Local programme. Councils continue independent technology procurement. GDS platforms remain central-government only. No cross-service data sharing framework.

**Costs** (3-year):
- Capital: £0
- Operational: Status quo — councils continue spending £5B+/year on technology
- GDS: No additional spend
- Total programme cost: £0

**Benefits**: £0 — no improvement in council costs, citizen outcomes, or platform sharing

**Pros**:
- No upfront investment required
- No implementation risk
- No disruption to existing council operations
- No political risk from programme failure

**Cons**:
- Stakeholder goals not met (0% of 6 goals)
- Councils continue £500M-£1B duplicated procurement over 3 years
- Vulnerable citizens continue receiving fragmented support (15-day coordination)
- GOV.UK OneLogin does not extend to local government — citizen experience remains fragmented
- Minister cannot answer parliamentary questions about local digital improvement
- NAO may criticise government for not acting on known inefficiency
- GDS platform economy model weakens without new markets

**Risks if Do Nothing**:
- Political risk: Opposition criticism of government inaction on local services (HIGH)
- Financial risk: Councils independently procure at higher cost — £500M+ waste (HIGH)
- Citizen risk: Vulnerable citizens continue falling through service gaps (HIGH)
- Strategic risk: GDS platform investment harder to justify without local government adoption (MEDIUM)

**Stakeholder Goals Met**: 0%

**Recommendation**: **Reject** — Unacceptable baseline. Costs and risks escalate while citizen outcomes worsen. The ministerial commitment to GDS Local creates a political requirement to act.

---

### Option 1: Minimal — Platform Extension Only

**Description**: Extend existing GOV.UK platforms (OneLogin, Notify, Pay) to local authorities with self-service onboarding. No custom data sharing platform. No integrated purchasing framework. Basic community engagement through existing GDS channels.

**Scope**:
- GOV.UK OneLogin extension via OIDC federation gateway (self-service)
- GOV.UK Notify extension (already available to councils)
- GOV.UK Pay extension (already available to councils)
- Self-service onboarding portal for councils
- Basic documentation and developer guidance
- No cross-service data sharing platform
- No shared component catalogue beyond existing GDS platforms
- No integrated purchasing framework
- Basic community via existing Cross-Government Slack

**Costs** (3-year) — ROM (±40%):

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Programme team (15 FTEs) | £3M | £3M | £2M | £8M |
| OneLogin federation gateway | £1M | £0.5M | £0 | £1.5M |
| Onboarding portal | £0.5M | £0.2M | £0.1M | £0.8M |
| Documentation & developer support | £0.3M | £0.2M | £0.2M | £0.7M |
| Security & compliance | £0.3M | £0.2M | £0.2M | £0.7M |
| **Total Capital** | **£5.1M** | **£4.1M** | **£2.5M** | **£11.7M** |
| Operational (hosting, support) | £0.5M | £1M | £1.5M | £3M |
| **Total 3-Year TCO** | | | | **£14.7M** |

**Benefits** (3-year) — ROM:

| Benefit | Source | Type | 3-Year Value | Confidence |
|---------|--------|------|--------------|------------|
| B-001: Council identity cost savings | G-1 | FINANCIAL | £8-12M | MEDIUM |
| B-002: Notification cost savings | G-3 | FINANCIAL | £3-5M | HIGH |
| B-003: Payment processing savings | G-3 | FINANCIAL | £2-3M | HIGH |
| B-004: Citizen time savings (single sign-on) | O-1 | SOCIAL VALUE | £2-4M | LOW |
| **Total** | | | **£15-24M** | |

**Net Benefit** (ROM): £15-24M benefits - £14.7M costs = **£0.3-9.3M** net

**Pros**:
- Lower upfront investment (£14.7M vs £24M)
- Leverages existing, proven GDS platforms — lower delivery risk
- Faster to deploy — platform extensions within 6 months
- GOV.UK Notify and Pay already available to councils (minimal new development)
- Lower change management burden

**Cons**:
- Only ~40% of stakeholder goals met (G-1 partially, G-5 partially, G-6 partially)
- G-2 (data sharing) completely unaddressed — vulnerable citizens see no improvement
- G-4 (£50M savings) largely unmet — no integrated purchasing framework
- No shared component catalogue — councils still procure individually for non-GDS needs
- Insufficient to meet ministerial ambition for "GDS Local"
- Community of practice under-resourced — likely poor engagement
- NAO may question whether programme achieves sufficient public value

**Stakeholder Impact**:
- DSIT Minister (SD-1): Partially met — OneLogin extension provides headline metric
- GDS DG (SD-2): Partially met — platform extension validated but limited scope
- MHCLG Digital (SD-3): Not met — no data sharing, no modernisation support
- LA Chief Executives (SD-4): Partially met — some platform savings but no purchasing framework
- Citizens (SD-7): Partially met — single sign-on improves but no joined-up data
- ICO (SD-8): Not applicable — no data sharing to govern

**Stakeholder Goals Met**: ~40%

---

### Option 2: Balanced GDS Local Programme (RECOMMENDED)

**Description**: Full GDS Local programme delivering all three strategic focus areas: platform extension, cross-service data sharing, and shared technology/purchasing. Phased delivery starting with pathfinder councils, scaling to 50+ councils. Data sharing framework co-designed with ICO. Integrated purchasing via LGA partnership. Active community of practice.

**Scope**:
- GOV.UK OneLogin federation gateway with council self-service onboarding
- Cross-service data sharing platform with governance framework (3 pilot use cases)
- Data sharing governance dashboard with DSA management and audit trails
- Shared component catalogue (5 new components co-designed with councils)
- Citizen consent management platform
- API gateway and developer portal
- Integrated purchasing framework (via LGA partnership)
- Community of practice platform (Discourse-based) and programme
- Council onboarding support team
- GOV.UK Notify, Pay, Design System extension to local authority contexts
- Status page and per-council health dashboards

**Costs** (3-year) — ROM (±30%):

| Item | Year 1 | Year 2 | Year 3 | Total |
|------|--------|--------|--------|-------|
| Programme team (35 FTEs) | £5M | £4.5M | £3.5M | £13M |
| Data sharing platform (custom build) | £2M | £1.5M | £0.5M | £4M |
| OneLogin federation & onboarding | £1M | £0.3M | £0.2M | £1.5M |
| Shared component development | £0.5M | £1M | £0.5M | £2M |
| API gateway & developer portal | £0.5M | £0.3M | £0.2M | £1M |
| Community of practice platform | £0.3M | £0.2M | £0.2M | £0.7M |
| Council onboarding support | £1M | £1M | £0.5M | £2.5M |
| Security & compliance (pen test, NCSC, DPIAs) | £0.5M | £0.3M | £0.2M | £1M |
| Contingency (15%) | £1.6M | £1.4M | £0.9M | £3.9M |
| **Total Capital/Programme** | **£12.4M** | **£10.5M** | **£6.7M** | **£29.6M** |

*Note: High end of ROM range shown. Midpoint estimate: £24M. Low end: £18M.*

| Operational Costs | Annual | 3-Year | Notes |
|-------------------|--------|--------|-------|
| Platform hosting (AWS UK) | £2M | £6M | Data sharing platform, API gateway, portals |
| Community management | £0.5M | £1.5M | 3 FTEs, events, travel |
| Security operations | £0.3M | £0.9M | SOC, monitoring, incident response |
| Support (council helpdesk) | £0.5M | £1.5M | L2/L3 support for council integrations |
| **Total Operational** | **£3.3M/year** | **£9.9M** | |

*Note: Year 1 operational costs lower (£1.5M) as platform ramps up. Year 3 represents steady-state.*

**Total 3-Year TCO** (ROM): **£24-34M** (midpoint: £29M including operational)

**Benefits** (3-year) — ROM:

| Benefit ID | Description | Stakeholder Goal | Type | Year 1 | Year 2 | Year 3 | 3-Year Total |
|------------|-------------|------------------|------|--------|--------|--------|--------------|
| B-001 | Council procurement savings (integrated purchasing) | G-4 (CFO Goal) | FINANCIAL | £2M | £18M | £30M | £50M |
| B-002 | Council technology cost avoidance (shared platforms) | G-1, G-3 | FINANCIAL | £1M | £4M | £8M | £13M |
| B-003 | Reduced multi-service coordination time | G-2 (O-2) | OPERATIONAL | £0 | £1M | £3M | £4M |
| B-004 | Citizen time savings (single sign-on) | G-1 (O-1) | SOCIAL VALUE | £0.5M | £2M | £4M | £6.5M |
| B-005 | Council IT staff productivity (freed from commodity) | G-3 (O-3) | OPERATIONAL | £0.5M | £2M | £3M | £5.5M |
| B-006 | Compliance cost reduction (shared DPIA, security) | G-5 | RISK | £0.2M | £0.5M | £1M | £1.7M |
| **Total Benefits** | | | | **£4.2M** | **£27.5M** | **£49M** | **£80.7M** |

*Note: B-001 (£50M procurement savings) is the primary quantified benefit, directly from G-4 target. Other benefits are ROM estimates. Benefits ramp as council adoption increases.*

**Qualitative Benefits** (not quantified):
- Vulnerable citizen welfare improvement — faster support, fewer people falling through gaps
- Government digital transformation narrative — ministerial and parliamentary value
- Improved council staff satisfaction — less time on commodity, more on innovation
- UK public sector as exemplar of shared digital infrastructure

**Economic Appraisal** (Qualitative, appropriate for SOBC stage):

| Metric | Value | Assessment |
|--------|-------|------------|
| Total 3-Year Benefits (ROM) | £65-85M | Strong — driven by £50M procurement savings |
| Total 3-Year Costs (ROM) | £24-34M | Reasonable for 3-year national programme |
| Net Benefit (ROM) | £31-51M | Clearly positive |
| Benefit-Cost Ratio (ROM) | 2.3:1 to 2.8:1 | Good VfM — above 2:1 threshold |
| Payback Period (ROM) | ~24 months | Acceptable — benefits ramp in Year 2 |
| Expected ROI (ROM) | 130-190% | Strong return for public sector investment |

*Optimism Bias: UK Government IT projects carry standard 40% optimism bias uplift. With uplift, costs rise to £34-48M. Benefits still exceed costs (BCR 1.6:1 to 2.0:1 with bias applied). Bias will be refined at OBC stage.*

**Pros**:
- 85% of stakeholder goals met (all 6 goals addressed)
- Strong NPV even with optimism bias applied
- Addresses all three GDS Local strategic focus areas
- Phased delivery reduces implementation risk (pathfinders before scale)
- Data sharing framework with ICO endorsement creates precedent
- Integrated purchasing delivers largest single financial benefit
- Community of practice builds sustainable engagement beyond programme team

**Cons**:
- Higher upfront investment than Option 1 (£24M vs £15M)
- Custom data sharing platform is highest-risk delivery element (12-18 months build)
- Depends on council voluntary adoption — cannot guarantee 50-council target
- Requires sustained 3-year funding commitment
- 35 FTE programme team is a significant resource commitment
- 7 risks exceed programme risk appetite (from ARC-001-RISK-v1.0)

**Stakeholder Impact**:
- DSIT Minister (SD-1): Met — visible progress across all three focus areas
- GDS DG (SD-2): Met — platform economy validated with local government
- MHCLG Digital (SD-3): Met — data sharing framework and modernisation support
- LA Chief Executives (SD-4): Met — £50M savings, free platforms, co-design model
- LA Digital/IT Directors (SD-5): Met — practical tools, community, onboarding support
- LGA (SD-6): Met — co-leadership role, purchasing framework, community
- Citizens (SD-7): Met — single sign-on, faster joined-up support for vulnerable citizens
- ICO (SD-8): Met — governance-first approach, regulatory sandbox
- NAO (SD-9): Met — clear VfM case, measurable benefits, audit-ready tracking
- NCSC (SD-11): Met — security by design, NCSC review at design stage

**Stakeholder Goals Met**: ~85%

---

### Option 3: Comprehensive — Accelerated National Programme

**Description**: Everything in Option 2 plus accelerated delivery targeting all 333 councils within 3 years, 10+ data sharing use cases, AI-enhanced analytics, full GOV.UK App extension, and proactive council migration support including funded system replacement for smaller councils.

**Scope** (in addition to Option 2):
- Target 150 councils by Year 2, 333 by Year 3 (vs. 50 in Option 2)
- 10 data sharing use cases (vs. 3 pilots)
- AI-enhanced predictive analytics for cross-service risk identification
- Full GOV.UK App extension to local government
- Funded council system migration for 50 smallest councils
- Dedicated regional support hubs (5 across England)
- National marketing campaign for citizen awareness

**Costs** (3-year) — ROM (±40%):

| Item | Total |
|------|-------|
| Programme team (60+ FTEs) | £22M |
| Platform development (all components) | £12M |
| Council migration funding (50 councils) | £10M |
| Regional support hubs (5) | £5M |
| AI/analytics development | £3M |
| Marketing and communications | £2M |
| Security and compliance | £2M |
| Contingency (20%) | £11M |
| **Total Capital/Programme** | **£67M** |
| Operational (3-year) | £15M |
| **Total 3-Year TCO** | **£82M** |

**Benefits** (3-year) — ROM:

| Benefit | 3-Year Total |
|---------|--------------|
| Council procurement savings (larger volume) | £75M |
| Technology cost avoidance | £25M |
| Citizen time savings | £15M |
| AI-driven outcome improvement | £5M |
| **Total** | **£120M** |

**Net Benefit** (ROM): £120M - £82M = £38M — similar to Option 2 in net terms

**Pros**:
- 100% of stakeholder goals met and exceeded
- National coverage within 3 years
- AI capabilities provide future-proofing
- Strongest citizen outcome improvement
- Funded migration removes barrier for smallest councils

**Cons**:
- Cost more than doubles vs. Option 2 (£82M vs £29M) for marginal additional benefit
- Significantly higher delivery risk — managing 333 council integrations simultaneously
- 60+ FTE programme team difficult to recruit in government pay scales
- Funded council migration creates dependency and moral hazard
- AI predictive analytics may face ethical and privacy challenges
- National marketing may backfire if programme not yet proven
- Over-engineering risk — building for full scale before validating model works
- HM Treasury unlikely to approve without phased evidence of success
- Diminishing returns: £82M cost for £120M benefit (BCR 1.5:1) vs £29M for £81M (BCR 2.8:1)

**Stakeholder Goals Met**: 100%

**Recommendation**: **Reject** — Diminishing returns and significantly higher risk. Costs double but net benefit is similar to Option 2. Better to succeed at scale with Option 2 and expand to Option 3 scope in subsequent phases with evidence.

---

## B3. Options Comparison

| Criteria | Option 0: Do Nothing | Option 1: Minimal | Option 2: Balanced | Option 3: Comprehensive |
|----------|---------------------|-------------------|--------------------|-----------------------|
| 3-Year Cost (ROM) | £0 | £15M | £29M | £82M |
| 3-Year Benefits (ROM) | £0 | £20M | £81M | £120M |
| Net Benefit (ROM) | £0 | +£5M | +£52M | +£38M |
| BCR | N/A | 1.3:1 | 2.8:1 | 1.5:1 |
| Payback Period | N/A | 30 months | 24 months | 30 months |
| Goals Met | 0% | 40% | 85% | 100% |
| Delivery Risk | None | LOW | MEDIUM | HIGH |
| Political Risk | HIGH | MEDIUM | LOW | MEDIUM |
| Council Adoption Target | 0 | 30 | 50 | 333 |
| Data Sharing | None | None | 3 pilots | 10 use cases |

## B4. Recommended Option

**Recommendation**: **Option 2: Balanced GDS Local Programme**

**Rationale**:
1. **Best Value for Money**: Highest BCR at 2.8:1 — clearly the most efficient use of public funds
2. **Stakeholder Satisfaction**: Meets 85% of goals across all 11 stakeholder groups
3. **Acceptable Risk**: 20 risks identified, all manageable with active mitigation (ARC-001-RISK-v1.0). No critical (20-25) residual risks
4. **Deliverability**: Phased approach (5 pathfinders → 20 → 50 councils) provides evidence before scale
5. **Political Alignment**: Meets ministerial commitment while maintaining voluntary adoption model
6. **Scalability**: Architecture designed for 333 councils — Option 3 scope achievable as a future phase
7. **ICO Support**: Governance-first approach for data sharing maximises likelihood of regulatory endorsement

**Sensitivity Analysis** (ROM, to be refined at OBC):
- If costs increase 30%: BCR drops to 2.1:1 — still positive, still above 2:1 threshold
- If benefits reduce 30%: BCR drops to 1.9:1 — marginal but still positive
- If both costs +30% and benefits -30%: BCR 1.5:1 — break-even acceptable for public sector
- If council adoption reaches only 30 (not 50): Benefits reduce ~40%, BCR 1.7:1 — still viable
- If data sharing pilots delayed 12 months: B-003 reduced, overall BCR 2.5:1 — minimal impact

**Optimism Bias Assessment** (UK Government Green Book):
- Standard uplift for IT-enabled business change: +40% on costs
- Adjusted 3-Year Cost: £29M × 1.4 = **£40.6M**
- NPV with optimism bias: Benefits £81M - Costs £40.6M = **+£40.4M** (still strongly positive)
- BCR with optimism bias: **2.0:1** — above minimum threshold
- Conclusion: Investment remains good value for money even with maximum optimism bias

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

### C1.1 Market Assessment

**Market Maturity**: The GDS Local programme has a unique commercial position:
- **Core platforms** (OneLogin, Notify, Pay) are provided by GDS at no cost — no procurement required
- **Custom development** (data sharing platform, governance dashboard) requires specialist delivery capability
- **Supporting components** (API gateway, community platform, status page) have mature commercial markets
- **Integrated purchasing** is led by LGA with Crown Commercial Service — procurement framework, not technology procurement

**Supplier Landscape**:
- **GOV.UK Platforms**: No procurement — GDS in-house (OneLogin, Notify, Pay, Design System)
- **Custom Development**: Digital agencies with UK Government experience (DOS framework)
  - Tier 1: Large firms (Deloitte Digital, Kainos, Methods, Thoughtworks)
  - Tier 2: Specialist GDS-experienced SMEs (dxw, Made Tech, Hippo Digital, FutureGov)
  - Tier 3: Niche data sharing / privacy tech specialists
- **Cloud Infrastructure**: AWS (UK Gov preferred under CCS framework), Azure, GCP
- **Open Source**: Discourse (community), Cachet (status page) — no vendor required

**UK Government Digital Marketplace Assessment**:
- **G-Cloud 14**: 6,000+ cloud services; relevant categories include cloud hosting, API management, monitoring, security
- **DOS 6**: 4,000+ suppliers for digital outcomes and specialists; ideal for data sharing platform build
- **SME Participation**: >80% of DOS suppliers are SMEs — supports social value commitments

### C1.2 Sourcing Route

**Recommended Route** (by component):

| Component | Route | Framework | Rationale |
|-----------|-------|-----------|-----------|
| GOV.UK Platforms | In-house (GDS) | N/A | Government-provided, free at point of use |
| Data sharing platform | DOS Outcomes | DOS 6 | Custom build, agile delivery, competitive market |
| API gateway | G-Cloud | G-Cloud 14 | Managed service, commodity offering |
| Cloud hosting | G-Cloud | G-Cloud 14 | AWS, standard call-off |
| Security testing | DOS Specialists | DOS 6 | CHECK-certified penetration testing |
| Council onboarding support | Mixed | In-house + DOS | Core team in-house, surge via DOS |
| Community platform | Open source self-hosted | G-Cloud (hosting) | Discourse, minimal procurement |
| Integrated purchasing | LGA-led | CCS frameworks | LGA convenes, CCS provides framework |

**Multi-Supplier Strategy**: The programme deliberately avoids a single large vendor contract. Components are procured independently through appropriate frameworks, maintaining competitive pressure and SME access. GDS retains architecture ownership and integration responsibility.

### C1.3 Contract Approach

**Data Sharing Platform** (largest procurement):
- **Contract Type**: Time and materials with sprint-based delivery and acceptance gates
- **Duration**: 18 months initial (build), 12 months support extension option
- **Value**: £3-5M (within DSIT digital spend controls threshold)
- **Payment**: Monthly against sprint deliverables, 10% retention for 3 months post-live
- **IP**: Crown copyright — all code open source (GDS Service Standard Point 12)
- **Exit**: Code, documentation, and knowledge transfer included in contract

**Cloud Hosting**:
- **Contract Type**: G-Cloud call-off, consumption-based pricing
- **Duration**: 12 months, rolling renewal
- **Value**: £1-2M/year
- **Exit**: Multi-cloud architecture ensures portability (Architecture Principle P15)

### C1.4 Social Value

**UK Government Requirement**: Minimum 10% weighting on social value in all procurements above £10M.

**Social Value Themes for GDS Local**:
1. **Economic**: Apprenticeship commitments (2 per supplier); regional employment (outside London preference); SME subcontracting (minimum 30% of contract value)
2. **Social**: Diversity & inclusion in delivery team; accessibility expertise mandatory; open source contribution back to community
3. **Environmental**: Carbon-neutral cloud hosting commitment; remote-first delivery reducing travel; sustainable procurement principles

**Evaluation Approach** (for DOS procurement):
- Technical capability: 60%
- Cost: 25%
- Social Value: 15% (above minimum 10% — reflecting programme's public value mission)

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment Required**: £24-34M over 3 years (ROM ±30%)
- Midpoint estimate: **£29M** (including contingency and operational)

### D1.1 Capital/Programme Expenditure

| Item | Year 1 (2026-27) | Year 2 (2027-28) | Year 3 (2028-29) | Total |
|------|-------------------|-------------------|-------------------|-------|
| Programme team (35 FTEs) | £5.0M | £4.5M | £3.5M | £13.0M |
| Data sharing platform build | £2.0M | £1.5M | £0.5M | £4.0M |
| OneLogin federation & onboarding | £1.0M | £0.3M | £0.2M | £1.5M |
| Shared component development | £0.5M | £1.0M | £0.5M | £2.0M |
| API gateway & developer portal | £0.5M | £0.3M | £0.2M | £1.0M |
| Community platform | £0.3M | £0.2M | £0.2M | £0.7M |
| Council onboarding support | £1.0M | £1.0M | £0.5M | £2.5M |
| Security & compliance | £0.5M | £0.3M | £0.2M | £1.0M |
| Contingency (15%) | £1.6M | £1.4M | £0.9M | £3.9M |
| **Total Programme** | **£12.4M** | **£10.5M** | **£6.7M** | **£29.6M** |

*Note: Programme team costs assume mix of civil servants (60%) and contractor/vendor resources (40%). Civil servant costs at average £80K total cost of employment. Contractor rates at DOS framework rates.*

### D1.2 Operational Expenditure (Steady-State from Year 2)

| Item | Year 1 | Year 2 | Year 3 | Annual (post-programme) |
|------|--------|--------|--------|------------------------|
| Platform hosting (AWS UK) | £1.0M | £2.0M | £2.5M | £2.5M |
| Community management (3 FTEs) | £0.2M | £0.5M | £0.5M | £0.5M |
| Security operations | £0.1M | £0.3M | £0.3M | £0.3M |
| Council support (L2/L3) | £0.2M | £0.5M | £0.5M | £0.5M |
| **Total Operational** | **£1.5M** | **£3.3M** | **£3.8M** | **£3.8M** |

*Note: Operational costs included in overall programme budget for Years 1-3. Post-programme operational budget of £3.8M/year required from Year 4 onwards.*

### D1.3 Total Cost of Ownership (3-Year)

| | Year 1 | Year 2 | Year 3 | 3-Year Total |
|---|--------|--------|--------|--------------|
| Programme | £12.4M | £10.5M | £6.7M | £29.6M |
| Operational | £1.5M | £3.3M | £3.8M | £8.6M |
| **Total TCO** | **£13.9M** | **£13.8M** | **£10.5M** | **£38.2M** |

*Note: Total TCO of £38.2M includes both programme delivery and operational running costs. Capital/programme element is £29.6M. All costs in 2026 prices, excluding VAT.*

**With HM Treasury Optimism Bias (+40%)**:
- Programme costs with uplift: £29.6M × 1.4 = **£41.4M**
- Operational costs (no uplift — consumption-based): **£8.6M**
- **Total TCO with bias: £50.0M**

## D2. Funding Source

**Budget Allocation**:
- **Source**: DSIT Spending Review settlement (2025-2028) — Digital Transformation Programme allocation
- **Amount Available**: Subject to spending review outcome — request for £30M capital over 3 years
- **Timing**: Financial year aligned (April-March): FY 2026-27, 2027-28, 2028-29

**Co-funding**:
- GOV.UK platform costs (OneLogin, Notify, Pay) — funded within existing GDS platform budget, not additional to GDS Local
- LGA contribution to integrated purchasing framework — £1-2M LGA budget for framework management
- Council-side integration costs — borne by individual councils (estimated £20-50K per council, from existing IT budgets)

**Budget Approval Path**:
1. **GDS Director General**: Up to £5M per component (within DSIT delegated authority)
2. **DSIT Permanent Secretary**: Up to £25M total programme (DSIT investment committee)
3. **Cabinet Office Spend Controls**: Technology spend above £1M requires CDDO approval
4. **HM Treasury**: Total programme >£25M likely requires Treasury approval via SOBC/OBC/FBC process

**Funding Gaps**:
- Gap: If spending review allocation is <£30M, scope must be reduced
- **Mitigation**: Prioritise OneLogin extension (G-1) and community (G-6) as lowest-cost, highest-impact elements. Defer data sharing platform to subsequent spending review if necessary

## D3. Affordability

**DSIT Budget Context**:
- Total DSIT digital/technology budget: ~£500M/year (estimated)
- GDS Local programme: ~£10-14M/year (2-3% of DSIT digital budget)
- Assessment: **Affordable** — within normal programme scale for DSIT

**Cash Flow Impact**:
- Largest single quarter: ~£4M (Q1 Year 1 — programme mobilisation and platform build start)
- **Cashflow Risk**: LOW — phased delivery smooths expenditure
- **Mitigation**: Monthly invoicing against sprint deliverables; cloud costs consumption-based

**Ongoing Affordability**:
- Post-programme operational costs: £3.8M/year
- Funded by: Reallocation from GDS platform budget (marginal cost of serving local government); DSIT operational budget allocation
- As council adoption grows, potential for modest cost-recovery model (not in scope for this SOBC — to be explored at OBC stage)

## D4. Financial Appraisal

### D4.1 Value for Money Assessment (Qualitative — SOBC Stage)

This SOBC uses strategic estimates (ROM) appropriate for the SOBC stage. Full quantitative NPV with sensitivity analysis will be produced at OBC stage with refined costs from pathfinder council experience.

**Qualitative VfM Assessment**:

| Criterion | Assessment | Evidence |
|-----------|------------|---------|
| **Economy** | STRONG | Digital Marketplace procurement ensures competitive pricing; GOV.UK platforms free; open source components where viable |
| **Efficiency** | STRONG | Shared platforms serve 333 councils vs. 333 individual procurements; shared component model eliminates duplication |
| **Effectiveness** | STRONG | 85% of stakeholder goals met; £50M savings target independently verifiable; citizen outcomes measurable |
| **Equity** | STRONG | Programme specifically designed to benefit smaller/less-resourced councils; free platforms reduce digital divide |

**Overall VfM Rating**: **HIGH**

**Justification**: The programme spends £29-38M (with ops) to deliver £65-85M in public value over 3 years (BCR 2.0-2.8:1). Even with 40% optimism bias, the BCR exceeds 1.5:1. The programme uniquely combines financial savings (quantifiable) with citizen welfare improvements (qualitative) and government digital capability (strategic). The voluntary adoption model ensures councils only adopt where value is demonstrated, creating a natural market test.

### D4.2 Indicative NPV Calculation (to be refined at OBC)

**Discount Rate**: 3.5% (HMT Green Book standard social time preference rate)

| Year | Costs (ROM) | Benefits (ROM) | Net | Discount Factor | Present Value |
|------|-------------|----------------|-----|-----------------|---------------|
| 0 (2026-27) | £13.9M | £4.2M | -£9.7M | 1.000 | -£9.7M |
| 1 (2027-28) | £13.8M | £27.5M | +£13.7M | 0.966 | +£13.2M |
| 2 (2028-29) | £10.5M | £49.0M | +£38.5M | 0.934 | +£36.0M |
| **Total** | **£38.2M** | **£80.7M** | **+£42.5M** | | **+£39.5M (NPV)** |

**NPV**: +£39.5M (strongly positive — investment justified)

*Caveat: These are ROM estimates appropriate for SOBC stage. NPV will be refined at OBC with actual pathfinder costs and validated benefit assumptions.*

---

# PART E: MANAGEMENT CASE

## E1. Governance

### E1.1 Roles & Responsibilities (from RACI in ARC-001-STKE-v1.0)

| Decision/Activity | Responsible | Accountable | Consulted | Informed |
|-------------------|-------------|-------------|-----------|----------|
| Programme strategy and scope | GDS Local Programme Director | GDS Director General | MHCLG Digital, LGA, CDDO | All stakeholders |
| Budget allocation | DSIT Finance | GDS Director General | Programme Director, MHCLG | NAO, Cabinet Office |
| Shared component prioritisation | Programme Director | GDS DG | LA Digital/IT Directors (via CoP), LGA | Suppliers, MHCLG |
| Data sharing governance framework | Programme Director | MHCLG Digital Director | ICO, LA Chief Executives, NCSC | Citizens (transparency) |
| Technology architecture decisions | Programme Architect | Programme Director | GDS Platform Teams, NCSC, LA technical reps | Socitm, Suppliers |
| Council onboarding prioritisation | Programme Director | LGA | LA Chief Executives | DSIT Minister |
| Service Standard assessment | GDS Assessment Team | GDS DG | Programme Director | All stakeholders |
| Integrated purchasing framework | LGA | LGA Chair | Programme Director, CCS, LA Finance | Suppliers, NAO |

**Senior Responsible Owner (SRO)**: GDS Director General
- Accountable for programme delivery and benefits realisation
- Chairs Programme Board
- Reports to DSIT Permanent Secretary and Minister

**Programme Board** (meets monthly):
- GDS Director General (Chair, SRO)
- MHCLG Digital Director (Co-sponsor)
- LGA Digital Lead (Council representative)
- DSIT Finance Director (Financial authority)
- GDS Local Programme Director (Delivery lead)
- Cabinet Office Spend Controls representative (quarterly attendance)

### E1.2 Approval Gates

| Gate | Criteria | Approving Body | Timing |
|------|----------|----------------|--------|
| **Gate 0: SOBC Approval** | This document approved, funding allocated | Programme Board + DSIT Investment Committee | Q1 2026 |
| **Gate 1: Pathfinder Selection** | 5 councils confirmed, onboarding plan approved | Programme Board | Q2 2026 |
| **Gate 2: Data Sharing Framework** | ICO sandbox engaged, DPIA approach agreed | Programme Board + ICO | Q2 2026 |
| **Gate 3: Alpha Assessment** | GDS Service Standard alpha pass for first component | GDS Assessment Team | Q3 2026 |
| **Gate 4: Pathfinder Go-Live** | First 5 councils live with OneLogin | Programme Board | Q3 2026 |
| **Gate 5: Scale Decision** | Pathfinder success evidence, OBC approved | Programme Board + DSIT | Q4 2026 |
| **Gate 6: Beta Assessment** | GDS Service Standard beta pass | GDS Assessment Team | Q2 2027 |
| **Gate 7: 50-Council Target** | 50 councils live, benefits tracking active | Programme Board | Q4 2027 |
| **Gate 8: Benefits Realisation** | 12-month post-scale benefits audit | Programme Board + NAO readiness | Q4 2028 |

## E2. Delivery Approach

**Methodology**: Agile delivery (Scrum) within GDS Service Manual framework, with stage-gate governance

**Phases**:

1. **Discovery & Mobilisation** (Q1-Q2 2026): Team recruitment, pathfinder council selection, data sharing framework design, ICO sandbox engagement, technology architecture
2. **Alpha** (Q3-Q4 2026): OneLogin federation gateway build, pathfinder council integration, data sharing platform MVP, community of practice launch, GDS Service Standard alpha assessment
3. **Private Beta** (Q1-Q2 2027): Scale to 20 councils, data sharing pilots (3 use cases, 10 councils), shared component catalogue (first 3 components), integrated purchasing framework launch
4. **Public Beta** (Q3-Q4 2027): Scale to 50+ councils, full shared component catalogue (5 components), GDS Service Standard beta assessment
5. **Live & Scale** (2028+): Continued scaling, benefits realisation, potential FBC for expansion

**Delivery Model**:
- **In-house (GDS)**: Programme management, architecture, product management, stakeholder engagement
- **In-house (MHCLG)**: Data sharing governance, policy, ICO engagement
- **LGA**: Council recruitment, community of practice, integrated purchasing
- **Vendor (via DOS)**: Data sharing platform build, specialist security testing
- **Open Source**: Community platform (Discourse), status page, developer tools

## E3. Key Milestones

| Milestone | Target Date | Dependencies | Owner |
|-----------|-------------|--------------|-------|
| SOBC Approval (this document) | Q1 2026 | This document reviewed and approved | GDS Director General |
| Programme team recruited (35 FTEs) | Q2 2026 | Funding confirmed, recruitment launched | GDS Local Programme Director |
| 5 pathfinder councils confirmed | Q2 2026 | LGA engagement, council willingness | LGA |
| ICO sandbox engagement agreed | Q2 2026 | ICO relationship, DPIA approach | MHCLG Digital Director |
| OneLogin federation gateway live | Q3 2026 | OneLogin platform readiness | GDS Platform Team |
| Community of practice: 100+ councils | Q4 2026 | Platform launched, LGA convening | LGA |
| GDS Service Standard alpha pass | Q4 2026 | Assessment capacity | GDS Assessment Team |
| 20 councils live with OneLogin | Q4 2026 | Pathfinder success, onboarding portal | Programme Director |
| Data sharing framework ICO endorsed | Q1 2027 | ICO sandbox completion | MHCLG Digital Director |
| 3 data sharing pilots operational | Q2 2027 | Framework approved, council readiness | Programme Director |
| 5 shared components published | Q3 2027 | Co-design with councils, development | Programme Director |
| **50 councils live with GDS Local** | **Q4 2027** | All above | Programme Director |
| £50M savings milestone | Q4 2028 | Purchasing framework, council adoption | LGA |
| Benefits realisation review | Q4 2028 | 12 months post-50-council target | GDS Director General |

**Critical Path**: OneLogin platform readiness (external dependency) → Pathfinder council onboarding → Scale decision at Gate 5 → 50-council target. Any delay to OneLogin readiness shifts the entire programme.

## E4. Resource Requirements

### E4.1 Team Structure

**Core Programme Team** (35 FTEs at peak):

| Role | FTEs | Duration | Grade/Level |
|------|------|----------|-------------|
| Programme Director | 1 | 36 months | SCS1 (Senior Civil Service) |
| Deputy Programme Director | 1 | 36 months | G6 |
| Product Managers (3 products) | 3 | 36 months | G7 |
| Delivery Managers | 2 | 36 months | G7/SEO |
| Technical Architect | 2 | 36 months | G7 (specialist) |
| Software Engineers | 6 | 30 months | HEO-G7 (specialist) |
| Data Sharing Policy Lead | 1 | 36 months | G7 |
| User Researchers | 2 | 24 months | SEO/G7 |
| Content Designers | 2 | 24 months | SEO |
| Council Onboarding Team | 5 | 30 months | HEO/SEO |
| Community Manager | 2 | 36 months | SEO |
| Business Analyst | 2 | 24 months | SEO/G7 |
| Security Architect | 1 | 36 months | G7 (specialist) |
| Performance Analyst | 1 | 24 months | SEO |
| Programme PMO | 2 | 36 months | HEO/SEO |
| Commercial Lead | 1 | 24 months | G7 |
| Comms/Stakeholder Lead | 1 | 36 months | G7/SEO |

**Vendor Resources** (via DOS framework):
- Data sharing platform build team: 6-8 people, 18 months
- Penetration testing: CHECK-certified provider, quarterly
- Accessibility audit: Specialist auditor, bi-annually

### E4.2 Skills Gaps

| Skill | Availability | Gap | Mitigation |
|-------|-------------|-----|------------|
| Local government domain knowledge | Limited in GDS | HIGH | MHCLG secondees, council practitioner advisory group |
| Privacy engineering (data sharing) | Rare in government | HIGH | Specialist contractor via DOS, ICO advisory |
| OIDC federation at scale | Available in OneLogin team | LOW | Knowledge transfer from GDS OneLogin team |
| Community management | Limited in GDS | MEDIUM | LGA partnership, dedicated community hires |
| Multi-tenant cloud architecture | Available via contractors | MEDIUM | Vendor team expertise, cloud architecture review |

## E5. Change Management

### E5.1 Stakeholder Engagement Strategy

| Stakeholder | Engagement Approach | Frequency | Owner |
|-------------|---------------------|-----------|-------|
| DSIT Minister | Quarterly briefing with dashboard and PQ pack | Quarterly | GDS DG |
| GDS Director General | Programme Board chair, weekly SRO update | Weekly/Monthly | Programme Director |
| MHCLG Digital Director | Fortnightly co-design sessions, joint governance | Fortnightly | Programme Director |
| LGA | Strategic partnership meetings, joint communications | Monthly | Programme Director |
| LA Chief Executives | Chief Executive briefings via LGA | Quarterly | LGA |
| LA Digital/IT Directors | Community of practice, co-design workshops | Monthly | Community Manager |
| ICO | Regulatory sandbox sessions, DPIA reviews | Bi-monthly | Data Sharing Policy Lead |
| NCSC | Security architecture reviews at design gates | At gates | Security Architect |
| NAO | Annual audit preparation, VfM evidence | Annual + ad hoc | Programme PMO |
| Technology Suppliers | Market engagement events, API documentation | Quarterly | Commercial Lead |

### E5.2 Resistance Management

**Anticipated Resistance** (from Stakeholder Conflict Analysis, ARC-001-STKE-v1.0):

| Source | Reason | Risk | Mitigation |
|--------|--------|------|------------|
| Councils with recent large procurements | Locked into 5-7 year vendor contracts | MEDIUM | Target for later phases; include in community for future adoption |
| Incumbent technology suppliers | Revenue threatened by shared components | HIGH | Early market engagement; open APIs for integration; partnership positioning |
| Risk-averse council legal teams | Data sharing liability concerns | MEDIUM | ICO-endorsed framework; template DSAs; LGA legal guidance |
| Council staff change fatigue | Multiple central initiatives competing for attention | MEDIUM | Co-design approach; voluntary model; demonstrate value before asking for commitment |
| GDS platform teams | Capacity concerns, local gov complexity | MEDIUM | Dedicated GDS Local capacity; clear prioritisation framework |

### E5.3 Change Champions
- **Pathfinder council digital leads**: First 5 councils become advocates
- **LGA Digital team**: Strategic partnership, co-convening
- **Socitm members**: Professional network advocacy
- **GDS Local Programme Director**: Visible leadership, conference keynotes

## E6. Benefits Realisation

### E6.1 Benefits Profiles

**Benefit B-001: Council Procurement Savings (£50M over 3 years)**
- **Owner**: LGA
- **Stakeholder Goal**: G-4
- **Baseline**: Individual council procurement at estimated 20% premium
- **Target**: £50M cumulative savings
- **Measurement**: Procurement savings calculator; council finance reporting; CCS data; annual savings audit
- **Timeline**: £2M Year 1 → £18M Year 2 → £30M Year 3
- **Assumptions**: 100+ councils participating in integrated purchasing by Year 2
- **Dependencies**: CCS framework alignment; sufficient council participation for volume discounts

**Benefit B-002: Council Technology Cost Avoidance (£13M over 3 years)**
- **Owner**: GDS Local Programme Director
- **Stakeholder Goals**: G-1, G-3
- **Baseline**: Council spend on bespoke identity, notification, payment systems
- **Target**: £13M avoided cost through adoption of free GOV.UK platforms and shared components
- **Measurement**: Council self-reporting; platform usage analytics; avoided procurement evidence
- **Timeline**: £1M Year 1 → £4M Year 2 → £8M Year 3

**Benefit B-003: Vulnerable Citizen Outcome Improvement (£4M social value over 3 years)**
- **Owner**: MHCLG Digital Director
- **Stakeholder Goal**: G-2 (O-2)
- **Baseline**: 15 working days to coordinate multi-service support
- **Target**: 5 working days (67% reduction)
- **Measurement**: Pilot council case management systems; citizen experience surveys
- **Value**: Estimated £500-1,000 per case in staff time savings and earlier intervention value
- **Timeline**: Benefits from Year 2 when data sharing pilots are operational

**Benefit B-004: Citizen Time Savings (£6.5M social value over 3 years)**
- **Owner**: GDS Local Programme Director
- **Stakeholder Goal**: G-1 (O-1)
- **Baseline**: Citizens maintain 7+ separate accounts, 15% abandonment at login
- **Target**: Single sign-on across central and local services; abandonment reduced to 5%
- **Measurement**: OneLogin analytics; council service completion rates
- **Value**: Estimated £2-5 per citizen interaction saved (based on GDS transaction cost benchmarks)

### E6.2 Benefits Measurement Framework

**Monitoring Approach**:
- Monthly benefits tracker (automated from platform analytics where possible)
- Quarterly benefits review at Programme Board
- Annual independent benefits audit (NAO-ready)

**Responsibility**:
- **SRO (GDS DG)**: Overall benefits realisation accountability
- **LGA**: Procurement savings tracking and verification
- **MHCLG**: Citizen outcome measurement
- **Programme Director**: Platform adoption and usage metrics

**Reporting**:
- Monthly: Benefits RAG status in Programme Board papers
- Quarterly: Detailed benefits report with trend analysis
- Annually: Independent assessment for NAO readiness

## E7. Risk Management

### E7.1 Top 10 Strategic Risks (from ARC-001-RISK-v1.0)

| Rank | Risk ID | Category | Description | Residual Score | Response | Owner |
|------|---------|----------|-------------|----------------|----------|-------|
| 1 | R-001 | STRATEGIC | Insufficient local authority adoption | 12 | Treat | LGA |
| 2 | R-002 | STRATEGIC | Ministerial direction or MoG change | 10 | Tolerate | GDS DG |
| 3 | R-008 | FINANCIAL | Programme funding not sustained | 10 | Treat | GDS DG |
| 4 | R-011 | COMPLIANCE | Data sharing privacy breach | 10 | Treat | MHCLG Digital |
| 5 | R-003 | STRATEGIC | "Whitehall imposing" perception | 9 | Treat | Programme Dir |
| 6 | R-004 | OPERATIONAL | GDS platform team capacity | 9 | Treat | GDS DG |
| 7 | R-015 | REPUTATIONAL | Parliamentary scrutiny and media | 9 | Tolerate | GDS DG |
| 8 | R-018 | TECHNOLOGY | Data sharing platform delays | 9 | Treat | Programme Dir |
| 9 | R-010 | FINANCIAL | £50M savings target not achieved | 8 | Treat | LGA |
| 10 | R-012 | COMPLIANCE | UK GDPR non-compliance | 8 | Treat | MHCLG Digital |

**Risk Profile Summary** (ARC-001-RISK-v1.0):
- **Total Risks**: 20 across 6 categories
- **Critical (20-25)**: 0
- **High (13-19)**: 0 residual (8 inherent reduced through controls)
- **Medium (6-12)**: 18 residual
- **Low (1-5)**: 2 residual
- **Control Effectiveness**: 35% reduction from inherent to residual
- **Risks Exceeding Appetite**: 7 (require escalation approval)

**Risk Appetite** (Programme-specific):

| Category | Appetite Threshold | Risks Within | Risks Exceeding | Action |
|----------|-------------------|--------------|-----------------|--------|
| STRATEGIC | ≤9 | 1 | 2 (R-001, R-002) | Escalate to Programme Board |
| OPERATIONAL | ≤8 | 3 | 1 (R-004) | Escalate to GDS DG |
| FINANCIAL | ≤8 | 1 | 2 (R-008, implied) | Escalate to DSIT Finance |
| COMPLIANCE | ≤6 | 1 | 2 (R-011, R-012) | Escalate to MHCLG Digital + ICO |
| REPUTATIONAL | ≤8 | 2 | 1 (R-015) | Escalate to GDS DG |
| TECHNOLOGY | ≤12 | 4 | 0 | Monitor |

### E7.2 Key Risk Mitigations

**R-001 (Adoption)**: Pathfinder approach with 5 willing councils; free platforms; LGA co-leadership; funded onboarding support; peer advocacy. Target: reduce from 12 to 8.

**R-011 (Privacy Breach)**: Governance-before-technology approach; ICO regulatory sandbox; DPIAs before any data sharing; purpose limitation enforced technically; comprehensive audit trails. Target: reduce from 10 to 6.

**R-008 (Funding)**: Multi-year spending review bid; phased delivery allowing scope adjustment; early benefits evidence to justify continued funding; LGA co-funding for purchasing framework. Target: reduce from 10 to 6.

**R-018 (Platform Delays)**: Agile delivery with sprint-based acceptance; experienced vendor via DOS; architecture review before build; MVP approach for first pilot. Target: reduce from 9 to 6.

### E7.3 Risk Monitoring

- **Review Frequency**: Monthly for all risks; weekly for Critical/High if any emerge
- **Escalation**: Any risk increasing by 5+ points; any new Critical risk; any risk exceeding appetite by >3 points
- **Reporting**: Monthly risk report to Programme Board; quarterly to DSIT Investment Committee
- **Full Risk Register**: ARC-001-RISK-v1.0 (20 risks, Orange Book compliant)

---

# PART F: RECOMMENDATION & NEXT STEPS

## F1. Summary of Recommendation

**Recommended Option**: **Option 2: Balanced GDS Local Programme**

| Metric | Value |
|--------|-------|
| Investment (3-year, ROM) | £29M programme + £8.6M operational = £38M |
| Expected Benefits (3-year, ROM) | £65-85M (£50M procurement savings + £13M cost avoidance + £18M social value) |
| Net Benefit (ROM) | +£42.5M |
| NPV (3.5% discount, ROM) | +£39.5M |
| Benefit-Cost Ratio (ROM) | 2.8:1 (2.0:1 with optimism bias) |
| Payback Period (ROM) | ~24 months |
| Stakeholder Goals Met | 85% (all 6 goals addressed, all 4 outcomes targeted) |
| Council Adoption Target | 50 by Q4 2027 |
| Data Sharing Pilots | 3 use cases across 10 councils |
| Risks | 20 identified, 0 critical, 7 exceeding appetite (all with mitigations) |

**Go/No-Go Recommendation**: **PROCEED** to requirements validation and programme mobilisation

## F2. Conditions for Approval

**Mandatory Conditions**:
1. DSIT spending review allocation confirmed: minimum £24M capital over 3 years
2. GDS Director General accepts SRO role for programme
3. Programme Board established with MHCLG and LGA representation
4. Cabinet Office CDDO digital spend control approval obtained
5. HM Treasury approval (if spend exceeds Treasury threshold)

**Recommended Conditions**:
1. GOV.UK OneLogin team confirms local authority federation feasibility (by Q2 2026)
2. At least 5 pathfinder councils confirmed (via LGA engagement by Q2 2026)
3. ICO confirms willingness to engage in regulatory sandbox (by Q2 2026)
4. Programme Director appointed (SCS1 level) by Q1 2026

## F3. Next Steps if Approved

**Immediate Actions** (Month 1-2):
1. **Appoint Programme Director**: SCS1 recruitment — Target: March 2026
2. **Establish Programme Board**: GDS DG, MHCLG Digital, LGA, DSIT Finance — Target: March 2026
3. **Commence recruitment**: 35 FTE programme team — Target: April 2026
4. **Engage ICO**: Formal regulatory sandbox proposal — Target: March 2026
5. **LGA pathfinder recruitment**: 5 councils confirmed — Target: April 2026

**Phase 1: Discovery & Mobilisation** (Q1-Q2 2026):
1. **Validate requirements** with pathfinder councils (ARC-001-REQ-v1.0 exists — validate and refine)
2. **Technology architecture**: Detailed design for OneLogin gateway and data sharing platform
3. **Procurement launch**: DOS competition for data sharing platform build
4. **Security review**: NCSC engagement for architecture review

**Phase 2: OBC Development** (Q4 2026):
1. **Outline Business Case**: Refine costs with pathfinder learning and vendor pricing
2. **Benefits validation**: Early adoption metrics from pathfinder councils
3. **Risk update**: Refresh ARC-001-RISK-v1.0 with delivery experience

**Business Case Lifecycle**:
- **SOBC** (this document): Strategic justification — Q1 2026
- **OBC**: Refined costs after pathfinder — Q4 2026
- **FBC**: Final approval with accurate costs — Q2 2027 (if required)

## F4. Next Steps if Not Approved

If this SOBC is not approved:

1. **Understand Objections**: GDS DG meets with approving body to understand concerns
2. **Revise SOBC**: Address concerns — likely scope reduction to Option 1 (Minimal)
3. **Re-submit**: Present revised SOBC within 4 weeks
4. **Communicate**: Inform stakeholders, particularly LGA and councils who have expressed interest

**Consequences of Not Proceeding**:
- Ministerial commitment (November 2025) not delivered — political and reputational damage
- Councils continue fragmented procurement — £500M+ waste over 3 years
- Vulnerable citizens continue receiving uncoordinated support
- GDS platform economy model weakens
- LGA and council trust in central government digital collaboration erodes

---

# APPENDICES

## Appendix A: Stakeholder Analysis Summary

**Source**: `projects/001-gds-local/ARC-001-STKE-v1.0.md`

**Key Stakeholders** (11 drivers, 6 goals, 4 outcomes):
1. DSIT Minister (SD-1): Demonstrate digital transformation — CRITICAL
2. GDS Director General (SD-2): Platform economy extension — HIGH
3. MHCLG Digital Director (SD-3): Local gov modernisation — HIGH
4. LA Chief Executives (SD-4): Services within budget constraints — CRITICAL
5. LA Digital/IT Directors (SD-5): Practical technology that works — HIGH
6. LGA (SD-6): Represent and protect council interests — HIGH
7. Citizens (SD-7): Seamless accessible services — CRITICAL
8. ICO (SD-8): Lawful transparent data sharing — HIGH
9. NAO (SD-9): Value for money and effective delivery — MEDIUM
10. Technology Suppliers (SD-10): Market clarity and opportunity — HIGH
11. NCSC (SD-11): Secure cross-government architecture — HIGH

**Traceability**: Every benefit in this SOBC traces to at least one stakeholder goal:

| Benefit | Stakeholder Goal | Stakeholder Driver |
|---------|-----------------|-------------------|
| B-001: Procurement savings (£50M) | G-4 | SD-4 (LA CEOs), SD-9 (NAO) |
| B-002: Technology cost avoidance (£13M) | G-1, G-3 | SD-2 (GDS DG), SD-5 (LA IT) |
| B-003: Vulnerable citizen outcomes (£4M) | G-2 | SD-3 (MHCLG), SD-7 (Citizens), SD-8 (ICO) |
| B-004: Citizen time savings (£6.5M) | G-1 | SD-1 (Minister), SD-7 (Citizens) |
| B-005: Council IT productivity (£5.5M) | G-3 | SD-5 (LA IT), SD-4 (LA CEOs) |
| B-006: Compliance cost reduction (£1.7M) | G-5 | SD-8 (ICO), SD-11 (NCSC) |

## Appendix B: Architecture Principles Alignment

**Source**: `projects/000-global/ARC-000-PRIN-v1.1.md`

**Key Principles Enforced by GDS Local**:
- P1 (User Needs First): Co-design with councils and citizen user research
- P4 (Interoperability): Open standards (OIDC, REST) for all integrations
- P5 (Security by Design): Zero-trust, NCSC review, end-to-end encryption
- P6 (Accessibility by Default): WCAG 2.2 AA, GOV.UK Design System
- P8 (Central-Local Collaboration): Core programme principle — partnership model
- P9 (Cross-Service Data Sharing): Data sharing framework with privacy protections
- P10 (Federated Identity): GOV.UK OneLogin federation to councils
- P11 (Data Sovereignty): UK data residency, UK GDPR compliance
- P13 (Reuse Government Platforms): OneLogin, Notify, Pay extension
- P23 (Open Source): All code published, community contributions welcomed
- P24 (GDS Service Standard): All components assessed against Service Standard
- P25 (Value for Money): BCR 2.8:1, audit-ready benefits tracking

## Appendix C: Risk Register Summary

**Source**: `projects/001-gds-local/ARC-001-RISK-v1.0.md`

**20 risks identified** following HM Treasury Orange Book methodology:
- STRATEGIC: 3 risks (R-001 to R-003)
- OPERATIONAL: 4 risks (R-004 to R-007)
- FINANCIAL: 3 risks (R-008 to R-010)
- COMPLIANCE: 3 risks (R-011 to R-013)
- REPUTATIONAL: 3 risks (R-014 to R-016)
- TECHNOLOGY: 4 risks (R-017 to R-020)

**Risk Profile**: Inherent total 248, Residual total 160 (35% reduction). 7 risks exceed appetite. Full risk register with inherent/residual matrices, 4Ts analysis, action plans, and monitoring framework in ARC-001-RISK-v1.0.

## Appendix D: Technology Research Summary

**Source**: `projects/001-gds-local/ARC-001-RSCH-v1.0.md`

**Key Technology Decisions**:
- GOV.UK OneLogin: Mandatory, OIDC only (no SAML), free
- Data Sharing Platform: Custom build required (no COTS meets UK GDPR cross-service requirements)
- API Gateway: AWS API Gateway (£1/million HTTP API calls)
- Community Platform: Discourse (open source, free self-hosted)
- Blended 3-year technology TCO: £1.2M (platform costs only, excluding programme team)

## Appendix E: Assumptions Register

| ID | Assumption | Basis | Risk if Wrong | Validation |
|----|-----------|-------|---------------|------------|
| A-1 | OneLogin ready for LA federation by Q3 2026 | GDS roadmap, discovery programme | G-1 delayed 6-12 months | OneLogin team engagement Q1 2026 |
| A-2 | 5+ pathfinder councils volunteer | LGA engagement, early interest | Programme cannot demonstrate value | LGA recruitment Q1-Q2 2026 |
| A-3 | ICO engages constructively with sandbox | ICO stated openness to innovation | G-2 blocked | ICO pre-engagement Q1 2026 |
| A-4 | GDS platforms need minimal modification | Technical review of APIs | Additional £2-5M cost | GDS platform review Q1 2026 |
| A-5 | 3-year DSIT funding sustained | Spending review commitment | Programme cancelled mid-delivery | Spending review Q1 2026 |
| A-6 | Councils achieve 20% savings through collective procurement | Market analysis, CCS data | £50M target not reached | Pilot procurement Q3 2026 |
| A-7 | Council IT teams can integrate via OIDC | Industry standard, 80%+ support | Slower onboarding, bridge needed | Pathfinder technical assessment |
| A-8 | No major cyber incident affects programme | NCSC guidance, security by design | Reputational damage, pause | Quarterly security review |

## Appendix F: Glossary

| Term | Definition |
|------|------------|
| SOBC | Strategic Outline Business Case — first stage with high-level estimates |
| OBC | Outline Business Case — second stage with refined costs after requirements |
| FBC | Full Business Case — final stage with accurate costs before implementation |
| NPV | Net Present Value — sum of discounted benefits minus costs |
| BCR | Benefit-Cost Ratio — total discounted benefits divided by total discounted costs |
| ROM | Rough Order of Magnitude — strategic cost estimate (±30-40%) |
| SRO | Senior Responsible Owner — accountable for programme delivery |
| TCO | Total Cost of Ownership — capital + operational costs over lifecycle |
| DOS | Digital Outcomes and Specialists — Digital Marketplace framework |
| G-Cloud | Government Cloud framework on Digital Marketplace |
| OIDC | OpenID Connect — identity federation standard |
| DSA | Data Sharing Agreement |
| DPIA | Data Protection Impact Assessment |
| 4Ts | Tolerate, Treat, Transfer, Terminate (Orange Book risk responses) |
| GDS | Government Digital Service |
| DSIT | Department for Science, Innovation and Technology |
| MHCLG | Ministry of Housing, Communities and Local Government |
| LGA | Local Government Association |
| CCS | Crown Commercial Service |
| CDDO | Central Digital and Data Office |
| NCSC | National Cyber Security Centre |
| ICO | Information Commissioner's Office |
| NAO | National Audit Office |

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| [Name] | GDS Director General (SRO) | | |
| [Name] | MHCLG Digital Director (Co-sponsor) | | |
| [Name] | DSIT Finance Director | | |
| [Name] | LGA Digital Lead (Partnership) | | |
| [Name] | DSIT Permanent Secretary (if >£25M) | | |

**Approval Decision**: **APPROVED** | **APPROVED WITH CONDITIONS** | **REJECTED** | **DEFERRED**

**Conditions** (if any):
1. [Condition 1]
2. [Condition 2]

**Approval Date**: [Date]

**Next Review Date**: Q4 2026 (OBC submission)

---

**END OF STRATEGIC OUTLINE BUSINESS CASE**

*Document created using ArcKit `/arckit:sobc` command*
*Green Book compliant: Yes (HM Treasury 5-case model)*
*Business case lifecycle stage: SOBC (strategic outline — first of three stages)*

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-001-STKE-v1.0 | Stakeholder Analysis | ArcKit | 11 drivers, 6 goals, 4 outcomes, RACI matrix, conflict analysis | projects/001-gds-local/ARC-001-STKE-v1.0.md |
| ARC-000-PRIN-v1.1 | Architecture Principles | ArcKit | 25 principles including GDS Local-specific | projects/000-global/ARC-000-PRIN-v1.1.md |
| ARC-001-REQ-v1.0 | Requirements | ArcKit | 6 BRs, 10 FRs, 18 NFRs, budget estimates | projects/001-gds-local/ARC-001-REQ-v1.0.md |
| ARC-001-RISK-v1.0 | Risk Register | ArcKit | 20 risks, Orange Book compliant | projects/001-gds-local/ARC-001-RISK-v1.0.md |
| ARC-001-RSCH-v1.0 | Technology Research | ArcKit | Build vs buy, vendor recommendations | projects/001-gds-local/ARC-001-RSCH-v1.0.md |
| GDS Local Guidance | Programme | GOV.UK | Programme purpose, 3 focus areas | gov.uk/guidance/gds-local |

---

**Generated by**: ArcKit `/arckit:sobc` command
**Generated on**: 2026-02-17
**ArcKit Version**: 2.4.5
**Project**: GDS Local (Project 001)
**AI Model**: Claude Opus 4.6
