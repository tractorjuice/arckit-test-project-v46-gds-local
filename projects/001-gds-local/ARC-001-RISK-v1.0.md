# Risk Register: GDS Local

> **Template Status**: Live | **Version**: 2.4.5 | **Command**: `/arckit.risk`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-RISK-v1.0 |
| **Document Type** | Risk Register |
| **Project** | GDS Local (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-02-17 |
| **Last Modified** | 2026-02-17 |
| **Review Cycle** | Monthly |
| **Next Review Date** | 2026-03-17 |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | GDS Local Programme Team, GDS Director General, MHCLG Digital, LGA, DSIT Finance, NCSC, ICO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-17 | ArcKit AI | Initial creation from `/arckit:risk` command | PENDING | PENDING |

---

## Executive Summary

### Risk Profile Overview

**Total Risks Identified:** 20 risks across 6 categories

| Risk Level | Inherent | Residual | Change |
|------------|----------|----------|--------|
| **Critical** (20-25) | 0 | 0 | -- |
| **High** (13-19) | 8 | 0 | -100% |
| **Medium** (6-12) | 12 | 18 | +50% |
| **Low** (1-5) | 0 | 2 | -- |
| **TOTAL** | 248 | 160 | -35% |

### Risk Category Distribution

| Category | Count | Avg Inherent | Avg Residual | Control Effectiveness |
|----------|-------|--------------|--------------|----------------------|
| **STRATEGIC** | 3 | 15.7 | 10.3 | 34% reduction |
| **OPERATIONAL** | 4 | 9.8 | 6.3 | 36% reduction |
| **FINANCIAL** | 3 | 12.0 | 8.0 | 33% reduction |
| **COMPLIANCE** | 3 | 11.7 | 7.3 | 37% reduction |
| **REPUTATIONAL** | 3 | 12.0 | 8.3 | 31% reduction |
| **TECHNOLOGY** | 4 | 13.8 | 7.8 | 44% reduction |

### Overall Risk Assessment

**Overall Residual Risk Score:** 160/500
**Risk Reduction from Controls:** 35% reduction from inherent risk
**Risk Profile Status:** Concerning — 7 risks exceed programme risk appetite; 0 critical but significant High concentration pre-controls

### Risks Exceeding Appetite

**Number of risks exceeding programme risk appetite:** 7 risks (35%)

| Risk ID | Title | Category | Residual | Appetite | Excess | Escalation |
|---------|-------|----------|----------|----------|--------|------------|
| R-001 | Insufficient local authority adoption | STRATEGIC | 12 | 9 | +3 | Programme Board |
| R-002 | Ministerial direction or MoG change | STRATEGIC | 10 | 9 | +1 | GDS DG / DSIT SoS |
| R-004 | GDS platform team capacity constraints | OPERATIONAL | 9 | 8 | +1 | GDS DG |
| R-008 | Programme funding not sustained | FINANCIAL | 10 | 8 | +2 | GDS DG / DSIT Finance |
| R-011 | Data sharing privacy breach | COMPLIANCE | 10 | 6 | +4 | MHCLG Digital Director / ICO |
| R-012 | UK GDPR non-compliance in cross-authority data | COMPLIANCE | 8 | 6 | +2 | MHCLG Digital Director |
| R-015 | Parliamentary scrutiny and media criticism | REPUTATIONAL | 9 | 8 | +1 | GDS DG / DSIT Minister |

### Top 5 Risks Requiring Immediate Attention

1. **R-001** (STRATEGIC, Residual 12): Insufficient local authority adoption — Owner: LGA
2. **R-002** (STRATEGIC, Residual 10): Ministerial direction or MoG change — Owner: GDS Director General
3. **R-008** (FINANCIAL, Residual 10): Programme funding not sustained — Owner: GDS Director General
4. **R-011** (COMPLIANCE, Residual 10): Data sharing privacy breach triggers ICO enforcement — Owner: MHCLG Digital Director
5. **R-018** (TECHNOLOGY, Residual 9): Custom data sharing platform development delays — Owner: GDS Local Programme Director

### Key Findings and Recommendations

**Key Findings:**
- Heavy concentration of COMPLIANCE risks exceeding appetite — both data sharing risks (R-011, R-012) exceed the low compliance threshold, reflecting the inherent challenge of cross-authority data sharing under UK GDPR
- TECHNOLOGY risks have the highest control effectiveness (44%) due to established technical practices, but the custom data sharing platform (R-018) remains the programme's most complex delivery risk
- No critical (20-25) residual risks, but 7 risks exceed appetite — the programme can proceed but requires active risk management and escalation approvals
- STRATEGIC risks (adoption and political) are the hardest to mitigate because they depend on external factors (council willingness, ministerial stability)

**Recommendations:**
1. Escalate R-011 and R-012 (COMPLIANCE) to Programme Board and MHCLG Digital Director — compliance risks exceed appetite by the widest margin
2. Obtain GDS DG formal acceptance of R-001 (STRATEGIC) — largest single residual risk score (12) and central to programme success
3. Prioritise governance-first approach for data sharing to reduce R-011 and R-012 before technology delivery
4. Establish monthly risk review cadence with all risk owners before first pathfinder council onboarding

---

## A. Risk Matrix Visualization

### Inherent Risk Matrix (Before Controls)

**5x5 Likelihood x Impact Matrix**

```
                                    IMPACT
              1-Minimal   2-Minor    3-Moderate   4-Major    5-Severe
           +------------+-----------+-----------+-----------+-----------+
5-Almost   |            |           |           |           |           |
Certain    |     5      |    10     |    15     |    20     |    25     |
           +------------+-----------+-----------+-----------+-----------+
4-Likely   |            |           | R-004     | R-001     |           |
           |     4      |     8     | R-015     | R-003     |    20     |
           |            |           |           | R-018     |           |
           +------------+-----------+-----------+-----------+-----------+
3-Possible |            |           | R-005     | R-010     | R-002     |
           |     3      |     6     | R-006     | R-012     | R-008     |
           |            |           | R-007     | R-014     | R-011     |
           |            |           | R-009     | R-016     | R-017     |
           |            |           | R-020     |           | R-019     |
           +------------+-----------+-----------+-----------+-----------+
2-Unlikely |            |           |           | R-013     |           |
           |     2      |     4     |     6     |     8     |    10     |
           +------------+-----------+-----------+-----------+-----------+
1-Rare     |            |           |           |           |           |
           |     1      |     2     |     3     |     4     |     5     |
           +------------+-----------+-----------+-----------+-----------+

Legend: Critical (20-25)  High (13-19)  Medium (6-12)  Low (1-5)
```

**Inherent Risk Zones:**
- **Critical (20-25)**: None
- **High (13-19)**: R-001, R-002, R-003, R-008, R-011, R-017, R-018, R-019 (8 risks)
- **Medium (6-12)**: R-004, R-005, R-006, R-007, R-009, R-010, R-012, R-013, R-014, R-015, R-016, R-020 (12 risks)
- **Low (1-5)**: None

### Residual Risk Matrix (After Controls)

**5x5 Likelihood x Impact Matrix — After Controls Applied**

```
                                    IMPACT
              1-Minimal   2-Minor    3-Moderate   4-Major    5-Severe
           +------------+-----------+-----------+-----------+-----------+
5-Almost   |            |           |           |           |           |
Certain    |     5      |    10     |    15     |    20     |    25     |
           +------------+-----------+-----------+-----------+-----------+
4-Likely   |            |           |           |           |           |
           |     4      |     8     |    12     |    16     |    20     |
           +------------+-----------+-----------+-----------+-----------+
3-Possible |            |           | R-003     | R-001     |           |
           |     3      |     6     | R-004     |           |    15     |
           |            |           | R-015     |           |           |
           |            |           | R-018     |           |           |
           +------------+-----------+-----------+-----------+-----------+
2-Unlikely |            |           | R-005     | R-010     | R-002     |
           |     2      |     4     | R-007     | R-012     | R-008     |
           |            |           | R-009     | R-014     | R-011     |
           |            |           | R-020     | R-016     |           |
           |            |           |           | R-017     |           |
           |            |           |           | R-019     |           |
           +------------+-----------+-----------+-----------+-----------+
1-Rare     |            |           |           | R-006     |           |
           |     1      |     2     |     3     | R-013     |     5     |
           +------------+-----------+-----------+-----------+-----------+

Legend: Critical (20-25)  High (13-19)  Medium (6-12)  Low (1-5)
```

**Risk Movement Analysis:**
- **Significant Improvement**: All 8 High risks reduced to Medium — controls effective across the board
- **Largest Reductions**: R-006 (9 to 4, -56%), R-013 (8 to 4, -50%), R-017 (15 to 8, -47%)
- **Smallest Reductions**: R-001 (16 to 12, -25%), R-015 (12 to 9, -25%) — strategic and reputational risks harder to mitigate
- **2 risks reduced to Low**: R-006 (Community of practice), R-013 (Accessibility)

---

## B. Top 10 Risks (Ranked by Residual Score)

| Rank | ID | Title | Category | Inherent | Residual | Owner | Status | Response |
|------|----|-------|----------|----------|----------|-------|--------|----------|
| 1 | R-001 | Insufficient local authority adoption | STRATEGIC | 16 | 12 | LGA | Open | Treat |
| 2 | R-002 | Ministerial direction or MoG change | STRATEGIC | 15 | 10 | GDS Director General | Open | Tolerate |
| 3 | R-008 | Programme funding not sustained | FINANCIAL | 15 | 10 | GDS Director General | Open | Treat |
| 4 | R-011 | Data sharing privacy breach | COMPLIANCE | 15 | 10 | MHCLG Digital Director | Open | Treat |
| 5 | R-003 | "Whitehall imposing on councils" perception | STRATEGIC | 16 | 9 | GDS Local Programme Director | Open | Treat |
| 6 | R-004 | GDS platform team capacity constraints | OPERATIONAL | 12 | 9 | GDS Director General | Open | Treat |
| 7 | R-015 | Parliamentary scrutiny and media criticism | REPUTATIONAL | 12 | 9 | GDS Director General | Open | Tolerate |
| 8 | R-018 | Custom data sharing platform development delays | TECHNOLOGY | 16 | 9 | GDS Local Programme Director | Open | Treat |
| 9 | R-010 | Savings target (£50M) not achieved | FINANCIAL | 12 | 8 | LGA | Open | Treat |
| 10 | R-012 | UK GDPR non-compliance in cross-authority data | COMPLIANCE | 12 | 8 | MHCLG Digital Director | Open | Treat |

---

## C. Detailed Risk Register

### Risk R-001: Insufficient Local Authority Adoption

**Category:** STRATEGIC
**Status:** Open
**Risk Owner:** LGA (from RACI: Accountable for council onboarding prioritisation)
**Action Owner:** GDS Local Programme Director

#### Risk Identification

**Risk Description:**
Local authorities do not adopt GDS Local shared components in sufficient numbers, resulting in the programme failing to achieve critical mass (50 councils by Q4 2027) and demonstrable outcomes. This could occur due to competing council priorities, insufficient IT capacity in smaller councils, perception that components don't meet local needs, or change fatigue from multiple central government initiatives.

**Root Cause:**
Local authorities are independent democratic bodies with severe budget pressures, competing priorities, and limited IT capacity. Adoption requires councils to invest time and resources in integration with no guarantee of return. Previous central government digital initiatives have under-delivered, creating scepticism.

**Trigger Events:**
- Pathfinder councils report poor integration experience or lack of value
- LGA Chief Executives' Briefing raises concerns about GDS Local approach
- Competing MHCLG or DLUHC initiative diverts council attention
- First shared components launched without adequate council co-design input

**Consequences if Realized:**
- Programme misses 50-council target by Q4 2027 — ministerial commitment not met
- GDS Local business case undermined — NAO audit questions value for money
- Shared components become expensive infrastructure serving few councils
- Political narrative shifts to "another failed government IT initiative"

**Affected Stakeholders:**
- **DSIT Minister** (SD-1): Cannot demonstrate digital transformation progress
- **GDS Director General** (SD-2): Platform economy model not validated
- **LA Chief Executives** (SD-4): Don't receive cost savings or service improvements
- **NAO** (SD-9): Questions value for money of programme spend

**Related Objectives:**
- Goal G-1 (OneLogin to 50 councils): Directly threatened
- Goal G-3 (5 shared components): Components unused without adoption
- Goal G-4 (£50M savings): Savings depend on volume participation

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Government digital adoption programmes historically achieve lower-than-projected uptake. 333 diverse councils with competing priorities make mass adoption inherently challenging. |
| **Impact** | 4 - Major | Insufficient adoption threatens the entire programme rationale — shared components only deliver value at scale. Would trigger NAO scrutiny and political embarrassment. |
| **Inherent Risk Score** | **16** (High) | 4 x 4 = 16 |

#### Current Controls and Mitigations

1. **Pathfinder approach**: Start with 5 enthusiastic, willing councils (not mandated adoption)
   - Effectiveness: **Adequate** — proven in GDS programmes but untested at local gov scale
2. **GDS platforms free at point of use**: GOV.UK Notify, Pay, OneLogin offered free
   - Effectiveness: **Strong** — removes primary financial barrier; Notify already used by 250+ councils
3. **LGA co-leadership**: LGA as visible partner, convening councils via existing networks
   - Effectiveness: **Adequate** — LGA has convening power but councils make independent decisions
4. **Voluntary adoption model (BR-006)**: No mandates; adoption driven by demonstrated value
   - Effectiveness: **Adequate** — reduces political resistance but makes targets harder to guarantee
5. **Community of practice (G-6)**: Peer advocacy and learning between councils
   - Effectiveness: **Weak** — not yet established; effectiveness depends on early momentum

**Overall Control Effectiveness:** Adequate (reduces risk from 16 to 12)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Free platforms and pathfinder approach reduce barriers, but council decision-making timelines and competing priorities remain. |
| **Impact** | 4 - Major | Even with some adoption, falling significantly short of 50 councils undermines the programme's strategic case. |
| **Residual Risk Score** | **12** (Medium) | 3 x 4 = 12 |

#### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

**Rationale:** Risk exceeds appetite (12 > 9) but can be further reduced through active engagement, funded onboarding support, and early value demonstration. Termination is not viable — adoption is the programme's core purpose.

#### Action Plan

1. **Fund dedicated council onboarding support team** (5 FTEs)
   - Owner: GDS Local Programme Director
   - Due Date: 2026-04-30
   - Expected Impact: Reduce likelihood from 3 to 2

2. **Launch pathfinder council programme with 5 councils by Q2 2026**
   - Owner: LGA
   - Due Date: 2026-06-30
   - Expected Impact: Generate peer advocacy evidence

3. **Publish council savings calculator showing projected ROI per council**
   - Owner: GDS Local Programme Director
   - Due Date: 2026-05-31
   - Expected Impact: Strengthen value proposition

**Target Residual Risk:** L=2, I=4 = 8 (Medium, within appetite)

---

### Risk R-002: Ministerial Direction or Machinery of Government Change

**Category:** STRATEGIC
**Status:** Open
**Risk Owner:** GDS Director General (from RACI: Accountable for programme strategy)
**Action Owner:** GDS Director General

#### Risk Identification

**Risk Description:**
A change in ministerial priority, machinery of government restructuring (e.g., GDS moved to different department), or general election shifts the political environment, causing GDS Local to lose sponsorship, funding, or strategic direction. GDS has historically been affected by machinery of government changes.

**Root Cause:**
Government digital programmes are inherently vulnerable to political cycles. GDS has moved between departments multiple times. Ministerial reshuffles change priorities. A general election could bring a new government with different digital strategy.

**Trigger Events:**
- Cabinet reshuffle moves DSIT Secretary of State or AI/Digital Minister
- Machinery of government change moves GDS out of DSIT
- General election changes government with different technology priorities
- Spending review reprioritises DSIT budget away from GDS Local

**Consequences if Realized:**
- Programme loses political sponsorship and ministerial advocacy
- Funding cut or redirected mid-programme
- Strategic direction changed, requiring significant rework
- Council partners lose confidence in programme longevity

**Affected Stakeholders:**
- **DSIT Minister** (SD-1): New minister may not prioritise GDS Local
- **GDS Director General** (SD-2): Strategic direction disrupted
- **LA Chief Executives** (SD-4): Lose confidence in central commitment
- **LGA** (SD-6): Partnership model disrupted

**Related Objectives:**
- All goals threatened — political sponsorship underpins the entire programme

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | UK parliament must hold general election by Jan 2030. Cabinet reshuffles occur 1-2 times per parliament. MoG changes have affected GDS before (moved from Cabinet Office to DSIT in 2023). |
| **Impact** | 5 - Catastrophic | Loss of ministerial sponsorship typically means loss of funding and strategic mandate. Previous GDS restructures caused significant programme disruption. |
| **Inherent Risk Score** | **15** (High) | 3 x 5 = 15 |

#### Current Controls and Mitigations

1. **Cross-party appeal**: Improving local services has cross-party support
   - Effectiveness: **Adequate**
2. **Embedded in DSIT strategy**: GDS Local announced as strategic initiative Nov 2025
   - Effectiveness: **Weak** — strategies change with ministers
3. **LGA partnership**: Non-partisan body provides continuity regardless of government
   - Effectiveness: **Adequate**

**Overall Control Effectiveness:** Adequate (reduces risk from 15 to 10)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Cross-party appeal and LGA partnership provide some insulation, but MoG changes remain possible. |
| **Impact** | 5 - Catastrophic | Even with cross-party support, a MoG change could cause significant disruption to the programme. |
| **Residual Risk Score** | **10** (Medium) | 2 x 5 = 10 |

#### Risk Response (4Ts Framework)

**Primary Response:** TOLERATE

**Rationale:** Political change cannot be prevented or transferred. The programme can build resilience by delivering early value that makes it politically costly to cancel, and by ensuring the LGA partnership provides continuity.

---

### Risk R-003: "Whitehall Imposing on Councils" Perception

**Category:** STRATEGIC
**Status:** Open
**Risk Owner:** GDS Local Programme Director (jointly with LGA)
**Action Owner:** Programme Comms Lead

#### Risk Identification

**Risk Description:**
GDS Local is perceived by councils, media, or local government commentators as another top-down central government initiative that imposes technology without understanding local government. This perception undermines the partnership model, triggers LGA resistance, and reduces council willingness to engage.

**Root Cause:**
Historical tension between central and local government on technology mandates. Councils are independent democratic bodies that resist central direction. Media framing of "Whitehall IT projects" is typically negative. Any misstep in communication or co-design can trigger this narrative.

**Trigger Events:**
- GDS Local launches component without visible council co-design input
- Media article framing GDS Local as "centralising council IT"
- Council leader or LGA official publicly criticises approach
- Component released that doesn't work for smaller/rural councils

**Consequences if Realized:**
- LGA withdraws active co-leadership, becoming passive or adversarial
- Councils refuse to engage or actively discourage peers from adopting
- Media narrative entrenches, making adoption politically difficult for council leaders
- Programme team morale affected; recruitment of local gov secondees becomes harder

**Affected Stakeholders:**
- **LA Chief Executives** (SD-4): Political sensitivity to central imposition
- **LGA** (SD-6): Reputation risk if seen as rubber-stamping central agenda
- **DSIT Minister** (SD-1): Negative media coverage

**Related Objectives:**
- All goals — undermines the partnership model that GDS Local depends on

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Central-local tensions are structural; similar perceptions have affected previous initiatives. |
| **Impact** | 4 - Major | Once the "imposition" narrative takes hold, it is extremely difficult to reverse. |
| **Inherent Risk Score** | **16** (High) | 4 x 4 = 16 |

#### Current Controls and Mitigations

1. **LGA as visible co-lead**: LGA partnership in governance provides credibility
   - Effectiveness: **Strong**
2. **Voluntary adoption model (BR-006)**: No mandates
   - Effectiveness: **Strong**
3. **Co-design with council practitioners (BR-004)**: Direct involvement of LA Digital/IT Directors
   - Effectiveness: **Adequate** — depends on quality of engagement
4. **Joint communications**: LGA and GDS Local joint announcements
   - Effectiveness: **Adequate**

**Overall Control Effectiveness:** Strong (reduces risk from 16 to 9)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Strong controls significantly reduce likelihood, but a single misstep could still trigger the perception. |
| **Impact** | 3 - Moderate | Voluntary model and LGA co-leadership limit damage if perception does emerge — it can be corrected. |
| **Residual Risk Score** | **9** (Medium) | 3 x 3 = 9 |

#### Risk Response (4Ts Framework)

**Primary Response:** TREAT

**Rationale:** Active prevention through communications strategy, council practitioner engagement, and LGA co-leadership. Within appetite (9 = threshold).

---

### Risk R-004: GDS Platform Team Capacity Constraints

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** GDS Director General (from RACI: Accountable for budget and resource allocation)
**Action Owner:** GDS Local Programme Director

#### Risk Identification

**Risk Description:**
GDS platform teams (OneLogin, Notify, Pay) are already stretched meeting central government commitments. Extending to local government may result in poor quality council onboarding, slow feature delivery, or neglect of central government users — creating a lose-lose situation.

**Root Cause:**
GDS platform teams were established and resourced for central government. Local authority extension was not in original resourcing plans. The teams have existing commitments, backlogs, and service level obligations to central government departments.

**Trigger Events:**
- Major central government department demands priority OneLogin features
- OneLogin team cannot onboard pathfinder councils within agreed timeline
- Platform incident response delays due to competing central/local priorities
- Key platform engineers leave due to increased workload

**Consequences if Realized:**
- Council onboarding delays — pathfinder councils frustrated, peer advocacy damaged
- Central government departments complain about platform quality degradation
- Programme Director unable to deliver against G-1 (50 councils) timeline
- Platform reliability falls below 99.9% SLA

**Affected Stakeholders:**
- **GDS Platform Teams**: Overwork, morale issues
- **LA Digital/IT Directors** (SD-5): Poor onboarding experience
- **GDS Director General** (SD-2): Central government service quality at risk

**Related Objectives:**
- Goal G-1 (OneLogin to 50 councils): Directly dependent on platform team capacity
- Goal G-3 (Shared components): Requires platform team support for extensions

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | GDS platform teams are already at capacity with central government demand. Local gov is additive workload. |
| **Impact** | 3 - Moderate | Delays onboarding and reduces quality but doesn't threaten programme existence. Workarounds exist. |
| **Inherent Risk Score** | **12** (Medium) | 4 x 3 = 12 |

#### Current Controls and Mitigations

1. **Dedicated GDS Local capacity within platform teams**: Ring-fenced resources for local gov work
   - Effectiveness: **Adequate** — subject to funding approval
2. **Standards-based integration (OIDC)**: Reduces custom work per council
   - Effectiveness: **Strong** — OIDC is well-understood; standard integration pattern
3. **Self-service onboarding portal (FR-002)**: Reduces per-council support burden
   - Effectiveness: **Weak** — not yet built

**Overall Control Effectiveness:** Adequate (reduces risk from 12 to 9)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Dedicated capacity helps but competing priorities will still arise. |
| **Impact** | 3 - Moderate | Impact unchanged — delays rather than failures. |
| **Residual Risk Score** | **9** (Medium) | 3 x 3 = 9 |

#### Risk Response (4Ts Framework)

**Primary Response:** TREAT

---

### Risk R-005: Skills Gap in Cross-Authority Data Sharing Architecture

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** GDS Local Programme Director
**Action Owner:** Programme Architect

#### Risk Identification

**Risk Description:**
The programme lacks sufficient expertise in privacy-preserving data sharing architecture, cross-organisational data governance, and UK GDPR compliance at scale. The custom data sharing platform (FR-004) requires specialist skills that are scarce in the government digital talent market.

**Root Cause:**
Cross-authority data sharing with purpose limitation, DSA enforcement, and privacy-preserving technology is a niche domain. Few government teams have built this at scale. The intersection of data engineering, privacy engineering, and UK public sector governance is a narrow talent pool.

**Trigger Events:**
- Unable to recruit specialist data sharing architects within 3 months
- Architecture design phase produces inadequate security/privacy model
- ICO raises concerns about technical approach during sandbox engagement

**Consequences if Realized:**
- Data sharing platform design delayed by 3-6 months
- Suboptimal architecture creates privacy or security vulnerabilities
- ICO withholds endorsement due to technical inadequacy
- Programme forced to use expensive contractors without knowledge transfer

**Affected Stakeholders:**
- **MHCLG Digital Director** (SD-3): Data sharing is their primary driver
- **ICO** (SD-8): Technical approach must meet regulatory expectations

**Related Objectives:**
- Goal G-2 (Data sharing framework): Directly dependent on expertise

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Specialist skills are scarce but government can attract talent through mission appeal and DDaT pay framework. |
| **Impact** | 3 - Moderate | Delays data sharing workstream but doesn't block other programme elements. |
| **Inherent Risk Score** | **9** (Medium) | 3 x 3 = 9 |

#### Current Controls and Mitigations

1. **DDaT pay framework**: Competitive salaries for specialist roles
   - Effectiveness: **Adequate**
2. **Contractor market**: Privacy engineering contractors available on G-Cloud
   - Effectiveness: **Strong** — provides short-term capability while permanent team builds
3. **ICO regulatory sandbox**: Early engagement provides architectural guidance
   - Effectiveness: **Adequate**

**Overall Control Effectiveness:** Adequate (reduces risk from 9 to 6)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Combination of DDaT framework and contractor market makes total skills gap unlikely. |
| **Impact** | 3 - Moderate | Even with delay, workarounds exist. |
| **Residual Risk Score** | **6** (Medium) | 2 x 3 = 6 |

#### Risk Response (4Ts Framework)

**Primary Response:** TREAT — Recruit specialists and engage contractors in parallel.

---

### Risk R-006: Community of Practice Fails to Achieve Critical Mass

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** LGA (from RACI: jointly Accountable for community)
**Action Owner:** Community Manager

#### Risk Identification

**Risk Description:**
The GDS Local community of practice does not achieve 100+ council participation by Q4 2026, resulting in insufficient co-design input, weak peer advocacy, and lack of feedback loop for shared component improvement.

**Root Cause:**
Council staff are time-poor with heavy operational demands. Participation in central government communities competes with day-job priorities. Previous government communities have started strong and faded. Small/rural councils may lack capacity to participate at all.

**Trigger Events:**
- Fewer than 30 councils registered after 6 months
- Community becomes "broadcast" from GDS rather than genuine collaboration
- Digitally mature councils dominate, excluding smaller councils
- No dedicated community manager resource allocated

**Consequences if Realized:**
- Shared components designed without diverse council input — poor fit
- Adoption relies on top-down marketing rather than peer advocacy
- Programme loses early-warning system for component issues
- LGA partnership weakened (community was a co-led initiative)

**Affected Stakeholders:**
- **LA Digital/IT Directors** (SD-5): Miss peer learning opportunity
- **LGA** (SD-6): Key initiative they co-own fails

**Related Objectives:**
- Goal G-6 (Community 100+ councils): Directly threatened

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Government communities have mixed track records. Council staff capacity is genuinely constrained. |
| **Impact** | 3 - Moderate | Programme can function without community but co-design quality and adoption speed suffer. |
| **Inherent Risk Score** | **9** (Medium) | 3 x 3 = 9 |

#### Current Controls and Mitigations

1. **LGA convening power**: LGA network reaches all 333 councils through existing channels
   - Effectiveness: **Strong**
2. **Funded participation**: Central funding for council staff time to participate
   - Effectiveness: **Adequate** — subject to budget approval
3. **Socitm partnership**: Professional body amplifies reach to IT directors
   - Effectiveness: **Adequate**

**Overall Control Effectiveness:** Strong (reduces risk from 9 to 4)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 1 - Rare | LGA convening power combined with funded participation and Socitm make failure to achieve basic participation unlikely. |
| **Impact** | 4 - Major | Raised impact slightly because if community fails despite these controls, it signals deeper engagement problems. |
| **Residual Risk Score** | **4** (Low) | 1 x 4 = 4 |

#### Risk Response (4Ts Framework)

**Primary Response:** TREAT — Invest in community management and funded council participation.

---

### Risk R-007: GDS Service Assessment Failure

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** GDS Local Programme Director
**Action Owner:** Service Owner

#### Risk Identification

**Risk Description:**
GDS Local public-facing components fail GDS Service Standard assessment at alpha or beta, requiring significant rework and delaying deployment. Shared components may not map neatly to the standard service assessment model (designed for transactional services, not platform components).

**Root Cause:**
GDS Service Standard was designed for end-to-end citizen services, not shared platform components. Assessment criteria may need interpretation for GDS Local's context. Assessment team capacity is limited.

**Trigger Events:**
- Alpha assessment fails on accessibility or security points
- Assessment team interprets standard narrowly, not recognising shared component context
- User research insufficient for assessment requirements
- Assessment scheduling delays due to team capacity

**Consequences if Realized:**
- 3-6 month delay while assessment findings addressed
- Rework costs of £200K-500K depending on scope of findings
- Ministerial embarrassment — GDS's own Service Standard not met by GDS programme

**Affected Stakeholders:**
- **GDS Local Programme Director**: Delivery timeline at risk
- **DSIT Minister** (SD-1): Embarrassing if GDS fails its own standard
- **GDS Assessment Team**: Capacity pressure

**Related Objectives:**
- Goal G-5 (Service Standard compliance): Directly threatened

#### Inherent and Residual Risk Assessment

| Assessment | Inherent | Residual |
|------------|----------|----------|
| **Likelihood** | 3 - Possible | 2 - Unlikely |
| **Impact** | 3 - Moderate | 3 - Moderate |
| **Score** | **9** (Medium) | **6** (Medium) |

**Controls:** Early assessment team engagement; user research embedded in programme; accessibility expertise in team; "pre-assessment" review before formal assessment.

#### Risk Response: TREAT

---

### Risk R-008: Programme Funding Not Sustained

**Category:** FINANCIAL
**Status:** Open
**Risk Owner:** GDS Director General (from RACI: Accountable for budget allocation)
**Action Owner:** DSIT Finance

#### Risk Identification

**Risk Description:**
DSIT does not provide sustained 3-year programme funding (estimated £18-29M), either due to Spending Review outcomes, competing DSIT priorities, or failure to demonstrate sufficient early value. The programme depends on Assumption A-5 (DSIT provides sustained funding for at least 3 years).

**Root Cause:**
Government funding is subject to annual budgets, Spending Reviews, and ministerial prioritisation. DSIT has many competing priorities (AI Safety, semiconductors, broadband). GDS Local is one programme among many seeking sustained investment.

**Trigger Events:**
- Spending Review allocates less than requested to DSIT
- DSIT internal prioritisation ranks GDS Local below other programmes
- Treasury questions GDS Local value for money in absence of early results
- Change of minister deprioritises local government digital

**Consequences if Realized:**
- Programme scaled back or terminated mid-delivery
- Councils that began integration left without support
- Sunk costs of £5-10M with limited outcomes to show
- Damage to GDS credibility with local government sector

**Affected Stakeholders:**
- **GDS Director General** (SD-2): Programme delivery and GDS reputation
- **LA Chief Executives** (SD-4): Lose access to shared platforms
- **NAO** (SD-9): Audit questions value of expenditure to date

**Related Objectives:**
- All goals dependent on sustained funding

#### Inherent and Residual Risk Assessment

| Assessment | Inherent | Residual |
|------------|----------|----------|
| **Likelihood** | 3 - Possible | 2 - Unlikely |
| **Impact** | 5 - Catastrophic | 5 - Catastrophic |
| **Score** | **15** (High) | **10** (Medium) |

**Controls:** Strong business case with NAO-ready evidence; early value demonstration through pathfinder councils; Notify already free to councils (low ongoing cost); phased investment model reducing upfront commitment.

#### Risk Response: TREAT — Build compelling early evidence and phase investment to reduce annual funding commitment.

---

### Risk R-009: Cloud Infrastructure Costs Exceed Projections

**Category:** FINANCIAL
**Status:** Open
**Risk Owner:** GDS Local Programme Director
**Action Owner:** Technical Lead

#### Risk Identification

**Risk Description:**
Cloud hosting costs for GDS Local shared platforms exceed budget projections as council adoption grows, particularly for data-intensive services (data sharing platform, API gateway, audit logging). Research indicates £2-3M/year operational costs at scale.

**Root Cause:**
Cloud costs are variable and scale with usage. Scaling from 50 to 333 councils significantly increases compute, storage, and network costs. Audit log retention (7 years) creates growing storage costs. Data sharing query volumes are difficult to predict.

**Trigger Events:**
- Monthly cloud bill exceeds forecast by >20% for 3 consecutive months
- Data sharing audit logs grow faster than projected
- API gateway costs spike due to council integration testing volumes

**Consequences if Realized:**
- Programme budget consumed faster than planned — either scale back or request additional funding
- Cloud cost narrative undermines "saving councils money" messaging

**Affected Stakeholders:**
- **DSIT Finance**: Budget overrun
- **GDS Local Programme Director**: Delivery trade-offs required

**Related Objectives:**
- Goal G-3 (Shared components): May need to defer components to manage costs

#### Inherent and Residual Risk Assessment

| Assessment | Inherent | Residual |
|------------|----------|----------|
| **Likelihood** | 3 - Possible | 2 - Unlikely |
| **Impact** | 3 - Moderate | 3 - Moderate |
| **Score** | **9** (Medium) | **6** (Medium) |

**Controls:** FinOps monitoring from day one; auto-scaling limits and cost alerts; reserved/committed-use discounts; right-sizing reviews monthly.

#### Risk Response: TREAT

---

### Risk R-010: Savings Target (£50M Over 3 Years) Not Achieved

**Category:** FINANCIAL
**Status:** Open
**Risk Owner:** LGA (from RACI: Accountable for integrated purchasing framework)
**Action Owner:** GDS Local Programme Director

#### Risk Identification

**Risk Description:**
The programme fails to deliver the £50M cumulative savings target (Goal G-4) over 3 years because: insufficient councils participate in integrated purchasing, savings are difficult to attribute (counterfactual problem), or actual savings per council are lower than projected.

**Root Cause:**
£50M savings assumes 100+ councils participating with an average 20% procurement premium eliminated. This depends on demand aggregation, supplier willingness, and council willingness to change existing contracts. The counterfactual (what would they have spent individually?) is inherently difficult to measure.

**Trigger Events:**
- Fewer than 50 councils join integrated purchasing in Year 1
- Major suppliers refuse to participate in framework terms
- Council procurement teams resist changing established supplier relationships
- Independent audit cannot verify savings methodology

**Consequences if Realized:**
- Programme's primary financial value proposition undermined
- NAO audit questions value for money
- Councils that joined find savings disappointing — reduces future adoption
- Minister cannot cite savings figure in parliamentary responses

**Affected Stakeholders:**
- **LA Chief Executives** (SD-4): Primary financial driver not met
- **NAO** (SD-9): Value for money in question
- **DSIT Minister** (SD-1): Transformation narrative weakened

**Related Objectives:**
- Goal G-4 (£50M savings): Directly threatened
- Outcome O-3 (Council savings): Not achieved

#### Inherent and Residual Risk Assessment

| Assessment | Inherent | Residual |
|------------|----------|----------|
| **Likelihood** | 3 - Possible | 2 - Unlikely |
| **Impact** | 4 - Major | 4 - Major |
| **Score** | **12** (Medium) | **8** (Medium) |

**Controls:** Benefits tracking from inception; pilot procurement in Year 1 to validate savings model; independent savings methodology agreed with NAO; phased targets (£5M Year 1, £15M Year 2, £30M Year 3).

#### Risk Response: TREAT

---

### Risk R-011: Data Sharing Privacy Breach Triggers ICO Enforcement

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** MHCLG Digital Director (from RACI: Accountable for data sharing governance)
**Action Owner:** Data Protection Officer

#### Risk Identification

**Risk Description:**
A privacy breach or misuse of cross-service data sharing erodes citizen trust, triggers ICO enforcement action (including potential fines), and derails the data sharing programme. This is the highest-consequence compliance risk given the programme's data access improvement ambition (Strategic Focus Area 2).

**Root Cause:**
Cross-service data sharing inherently involves processing personal data across organisational boundaries. Housing accessing health/social care data involves sensitive special category data. Multiple data controllers create complex governance. History of government data sharing controversies (care.data, National Pupil Database) means low public tolerance for incidents.

**Trigger Events:**
- Unauthorised access to cross-service data (officer accesses data without valid purpose)
- Data sharing agreement expired but technical access still active
- Bulk data extraction or export beyond purpose limitation
- Security vulnerability in data sharing platform exposes personal data
- Council system breach exposes data received via cross-service sharing

**Consequences if Realized:**
- ICO enforcement notice or monetary penalty (up to £17.5M or 4% of turnover)
- ICO withdraws regulatory sandbox endorsement
- All cross-service data sharing suspended pending investigation
- Citizen trust survey results collapse — data sharing programme may be permanently damaged
- Parliamentary questions and media scrutiny
- Affected individuals may suffer harm (e.g., domestic violence victim's location exposed)

**Affected Stakeholders:**
- **ICO** (SD-8): Enforcement action required
- **Citizens** (SD-7): Personal data exposed; trust destroyed
- **DSIT Minister** (SD-1): Political accountability for programme
- **LA Chief Executives** (SD-4): Data controllers liable

**Related Objectives:**
- Goal G-2 (Data sharing framework): Directly threatened — may be permanently damaged
- Outcome O-2 (Joined-up support): Cannot continue without trust

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Data breaches occur regularly in government (ICO annual report shows hundreds of incidents). Cross-organisational sharing increases attack surface. |
| **Impact** | 5 - Catastrophic | ICO enforcement, citizen harm, programme-ending consequences for data sharing workstream. |
| **Inherent Risk Score** | **15** (High) | 3 x 5 = 15 |

#### Current Controls and Mitigations

1. **Governance-first approach**: DSAs, DPIAs, ICO sandbox before any data sharing
   - Effectiveness: **Strong** — prevents premature data sharing
2. **Purpose limitation enforced technically** (FR-004): Not just policy — architecture enforces access controls
   - Effectiveness: **Adequate** — depends on platform quality (not yet built)
3. **Comprehensive audit trails** (NFR-SEC-004): Who, what, when, why, lawful basis
   - Effectiveness: **Strong** — enables detection and investigation
4. **Starting with 3 tightly-scoped pilot use cases**: Limits blast radius
   - Effectiveness: **Strong** — constrains scope of any incident
5. **Incident response plan co-developed with ICO**: Rapid response if breach occurs
   - Effectiveness: **Adequate** — not yet developed

**Overall Control Effectiveness:** Strong (reduces risk from 15 to 10)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Governance-first approach and pilot scope significantly reduce likelihood. |
| **Impact** | 5 - Catastrophic | Impact remains catastrophic regardless of controls — a breach in government data sharing would be severely damaging. |
| **Residual Risk Score** | **10** (Medium) | 2 x 5 = 10 |

#### Risk Response (4Ts Framework)

**Primary Response:** TREAT

**Rationale:** Risk exceeds compliance appetite (10 > 6) and must be actively managed. Cannot be tolerated (regulatory), transferred (data controller liability), or terminated (data sharing is a core programme objective). Must reduce through robust governance and technical controls.

#### Action Plan

1. **Complete ICO regulatory sandbox engagement before any pilot data sharing**
   - Owner: MHCLG Digital Director
   - Due Date: 2026-06-30
   - Expected Impact: ICO endorsement provides governance assurance

2. **Develop incident response plan jointly with ICO**
   - Owner: Data Protection Officer
   - Due Date: 2026-05-31
   - Expected Impact: Rapid response reduces impact of any breach

3. **Implement automated DSA expiry enforcement** — technical prevention of access after DSA expires
   - Owner: Programme Architect
   - Due Date: 2026-09-30
   - Expected Impact: Eliminates a key trigger event

**Target Residual Risk:** L=1, I=5 = 5 (Low, within appetite)

---

### Risk R-012: UK GDPR Non-Compliance in Cross-Authority Data Flows

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** MHCLG Digital Director
**Action Owner:** Data Protection Officer

#### Risk Identification

**Risk Description:**
Cross-authority data sharing arrangements fail to comply with UK GDPR requirements: lawful basis not adequately established, DPIAs insufficient, data controller/processor relationships unclear between 10+ participating organisations, or data subject rights (access, erasure) cannot be fulfilled across organisational boundaries.

**Root Cause:**
Cross-authority data sharing under UK GDPR is legally complex. Multiple data controllers with independent legal obligations, joint controllership considerations, and varying council legal team interpretations create compliance uncertainty. Data subject rights (e.g., right to erasure) are technically challenging across distributed systems.

**Trigger Events:**
- Council legal team refuses to sign DSA citing GDPR concerns
- ICO questions lawful basis during sandbox review
- Citizen exercises right to erasure — system cannot fulfil across all authorities
- Data originally collected for one purpose shared beyond purpose limitation

**Consequences if Realized:**
- Data sharing pilots delayed 6-12 months while legal framework reworked
- ICO formal investigation
- Council legal teams advise chief executives against participation
- Citizen complaint escalates to ICO

**Affected Stakeholders:**
- **ICO** (SD-8): Regulatory compliance in question
- **MHCLG Digital Director** (SD-3): Data sharing ambition blocked
- **LA Chief Executives** (SD-4): Legal liability concerns

**Related Objectives:**
- Goal G-2 (Data sharing framework): Blocked by legal uncertainty

#### Inherent and Residual Risk Assessment

| Assessment | Inherent | Residual |
|------------|----------|----------|
| **Likelihood** | 3 - Possible | 2 - Unlikely |
| **Impact** | 4 - Major | 4 - Major |
| **Score** | **12** (Medium) | **8** (Medium) |

**Controls:** ICO regulatory sandbox (early legal guidance); template DSAs co-developed with LGA legal team; DPIAs completed before any data sharing; data subject rights impact assessment; legal advice from specialist government data sharing lawyers.

#### Risk Response: TREAT — Exceeds compliance appetite (8 > 6). Invest in specialist legal advice and ICO pre-engagement.

---

### Risk R-013: Accessibility Non-Compliance (WCAG 2.2 AA / PSBAR 2018)

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** GDS Local Programme Director
**Action Owner:** Service Designer

#### Risk Identification

**Risk Description:**
Citizen-facing GDS Local components fail to meet WCAG 2.2 Level AA accessibility standards or the Public Sector Bodies Accessibility Regulations 2018, creating legal non-compliance and excluding users with disabilities.

**Root Cause:**
Accessibility is technically challenging to implement correctly across all interaction patterns. Custom components (data sharing consent screens, cross-service data views) may not have existing GOV.UK Design System patterns to follow.

**Trigger Events:**
- Accessibility audit fails at beta assessment
- Citizen complaint to EHRC about inaccessible service
- Automated accessibility scanning reveals WCAG failures

**Consequences if Realized:**
- Legal non-compliance with PSBAR 2018
- GDS Service Standard assessment failure (Point 5)
- Citizen exclusion — particularly affects users in local authority services (elderly, disabled)
- Rework delays of 2-3 months

**Affected Stakeholders:**
- **Citizens** (SD-7): Excluded from digital services
- **DSIT Minister** (SD-1): Legal compliance failure in GDS-led programme

**Related Objectives:**
- Goal G-5 (Service Standard): Point 5 compliance at risk

#### Inherent and Residual Risk Assessment

| Assessment | Inherent | Residual |
|------------|----------|----------|
| **Likelihood** | 2 - Unlikely | 1 - Rare |
| **Impact** | 4 - Major | 4 - Major |
| **Score** | **8** (Medium) | **4** (Low) |

**Controls:** GOV.UK Design System patterns used by default (P6 — non-negotiable principle); automated WCAG testing in CI/CD pipeline; accessibility specialist in team; assistive technology testing (JAWS, NVDA, VoiceOver); progressive enhancement.

#### Risk Response: TREAT — Controls are strong; maintain vigilance.

---

### Risk R-014: High-Profile Service Outage Affecting Multiple Councils

**Category:** REPUTATIONAL
**Status:** Open
**Risk Owner:** GDS Local Programme Director
**Action Owner:** Head of Operations

#### Risk Identification

**Risk Description:**
A significant outage of a GDS Local shared component (especially OneLogin federation gateway or data sharing platform) affects services across multiple councils simultaneously, generating media coverage and undermining confidence in the shared platform model.

**Root Cause:**
Shared components create shared risk — single points of failure can affect all connected councils. The amplified blast radius (one outage = multiple councils affected) creates a "concentration risk" inherent to the platform model.

**Trigger Events:**
- OneLogin federation gateway outage during council peak hours
- Data sharing platform unavailable for 4+ hours
- API gateway failure causing cascading errors across council integrations
- Cloud provider availability zone failure affecting GDS Local infrastructure

**Consequences if Realized:**
- Multiple councils unable to authenticate citizens or access cross-service data
- Media coverage: "Government IT failure affects council services across England"
- Councils reconsider shared platform dependency — some may withdraw
- Parliamentary question about GDS Local reliability

**Affected Stakeholders:**
- **Citizens** (SD-7): Cannot access council services
- **LA Chief Executives** (SD-4): Service disruption they cannot control
- **DSIT Minister** (SD-1): Political accountability for outage
- **Technology Suppliers** (SD-10): Use incident to argue against centralisation

**Related Objectives:**
- Goal G-1 (OneLogin adoption): Trust in platform undermined
- Outcome O-1 (Single sign-on): Interrupted

#### Inherent and Residual Risk Assessment

| Assessment | Inherent | Residual |
|------------|----------|----------|
| **Likelihood** | 3 - Possible | 2 - Unlikely |
| **Impact** | 4 - Major | 4 - Major |
| **Score** | **12** (Medium) | **8** (Medium) |

**Controls:** 99.9% availability SLA (NFR-A-001); multi-AZ deployment; bulkhead isolation per council (NFR-A-003); mandatory council fallback authentication (UC-1 Alt); status page (FR-008); incident response runbooks; regular DR testing.

#### Risk Response: TREAT

---

### Risk R-015: Parliamentary Scrutiny and Media Criticism

**Category:** REPUTATIONAL
**Status:** Open
**Risk Owner:** GDS Director General
**Action Owner:** DSIT Communications

#### Risk Identification

**Risk Description:**
GDS Local attracts negative parliamentary scrutiny (PQs, Select Committee inquiry) or media criticism, either due to delivery problems, council complaints, or adverse comparison with previous government IT programmes. Government digital programmes receive disproportionate media attention.

**Root Cause:**
Government IT has a well-established negative media narrative. GDS Local's central-local government dimension adds political sensitivity. Slow adoption, cost overruns, or council complaints provide ammunition for parliamentary questions.

**Trigger Events:**
- NAO report questions value for money
- Council leader publicly criticises programme
- Select Committee inquiry into government digital programmes
- Adoption numbers below target at annual review
- FOI request reveals embarrassing internal communications

**Consequences if Realized:**
- Programme reputation damaged — harder to recruit council partners
- Ministerial confidence reduced — programme deprioritised
- Team morale affected
- Negative narrative becomes self-fulfilling — councils avoid "controversial" programme

**Affected Stakeholders:**
- **DSIT Minister** (SD-1): Political exposure
- **GDS Director General** (SD-2): GDS institutional reputation
- **LGA** (SD-6): Association with programme becomes reputational risk

**Related Objectives:**
- All goals — negative narrative undermines adoption and confidence

#### Inherent and Residual Risk Assessment

| Assessment | Inherent | Residual |
|------------|----------|----------|
| **Likelihood** | 4 - Likely | 3 - Possible |
| **Impact** | 3 - Moderate | 3 - Moderate |
| **Score** | **12** (Medium) | **9** (Medium) |

**Controls:** Quarterly ministerial briefings with dashboard; PQ preparation packs; proactive GOV.UK blog posts; success stories from pathfinder councils; NAO-ready evidence base; joint LGA communications.

#### Risk Response: TOLERATE — Parliamentary scrutiny is inherent to government programmes and cannot be eliminated. Manage through proactive communications.

---

### Risk R-016: Citizen Trust Erosion from Data Sharing Concerns

**Category:** REPUTATIONAL
**Status:** Open
**Risk Owner:** MHCLG Digital Director
**Action Owner:** Programme Comms Lead

#### Risk Identification

**Risk Description:**
Citizens become concerned about cross-service data sharing between councils and central government, leading to low trust survey scores (<60% target), resistance to using shared services, and public opposition that creates political pressure to curtail the data sharing programme.

**Root Cause:**
Public trust in government data handling is fragile. High-profile incidents (care.data, NHS data sharing controversies) have created lasting scepticism. Citizens may not distinguish between "safe, governed data sharing" and "surveillance". Media framing tends towards privacy alarmism.

**Trigger Events:**
- Media article: "Your council is sharing your data with Whitehall"
- Privacy campaign group targets GDS Local data sharing
- Citizen trust survey shows <40% confidence
- Social media backlash against data sharing pilot

**Consequences if Realized:**
- Citizen consent rates too low for consent-based sharing arrangements
- Political pressure to curtail or terminate data sharing programme
- Councils withdraw from data sharing pilots due to local political pressure
- ICO pressured to take stricter position

**Affected Stakeholders:**
- **Citizens** (SD-7): Trust in government data handling
- **MHCLG Digital Director** (SD-3): Data sharing ambition threatened
- **ICO** (SD-8): Increased scrutiny pressure

**Related Objectives:**
- Goal G-2 (Data sharing framework): Dependent on citizen trust
- Outcome O-2 (Joined-up support): Requires citizen cooperation

#### Inherent and Residual Risk Assessment

| Assessment | Inherent | Residual |
|------------|----------|----------|
| **Likelihood** | 3 - Possible | 2 - Unlikely |
| **Impact** | 4 - Major | 4 - Major |
| **Score** | **12** (Medium) | **8** (Medium) |

**Controls:** Citizen transparency — privacy notices explain exactly what is shared and why; citizen consent mechanisms where consent is the lawful basis; public beta with citizen usability testing; proactive communications showing citizen benefit stories; ICO endorsement as trust signal.

#### Risk Response: TREAT

---

### Risk R-017: GOV.UK OneLogin Not Ready for Local Authority Federation

**Category:** TECHNOLOGY
**Status:** Open
**Risk Owner:** GDS Director General (OneLogin is a GDS platform)
**Action Owner:** GDS OneLogin Team Lead

#### Risk Identification

**Risk Description:**
GOV.UK OneLogin platform does not reach sufficient maturity for local authority OIDC federation by Q3 2026 (Assumption A-1), blocking Goal G-1 (50 councils by Q4 2027). Research indicates OneLogin currently supports OIDC only (no SAML), is in "discovery phase" for local authorities, and may require feature development for council-specific use cases (identity assurance levels, council-branded login screens).

**Root Cause:**
OneLogin was designed for central government services. Local authority use cases (council-branded authentication, variable identity assurance levels per service, self-service council onboarding) may require platform features not yet developed. The platform is under active development with competing central government priorities.

**Trigger Events:**
- OneLogin team confirms local authority features not on roadmap for 2026
- OIDC federation testing reveals functional gaps for council use cases
- Council identity assurance requirements don't map to OneLogin's assurance model
- OneLogin major incident delays feature development

**Consequences if Realized:**
- G-1 timeline delayed by 6-12 months (50 councils pushes to Q2-Q4 2028)
- Pathfinder councils cannot integrate, damaging early momentum and peer advocacy
- Programme forced to consider interim federation solution (additional cost and complexity)
- Minister cannot announce OneLogin progress at planned milestones

**Affected Stakeholders:**
- **GDS Director General** (SD-2): Platform extension model challenged
- **LA Digital/IT Directors** (SD-5): Awaiting integration capability
- **DSIT Minister** (SD-1): Milestone not met

**Related Objectives:**
- Goal G-1 (OneLogin to 50 councils): Directly blocked
- Outcome O-1 (Single sign-on): Delayed

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | OneLogin is in active development for central government. Local authority features are additional scope that competes for platform team capacity. |
| **Impact** | 5 - Catastrophic | OneLogin extension is the most visible GDS Local deliverable. Failure blocks the headline goal and undermines the platform economy narrative. |
| **Inherent Risk Score** | **15** (High) | 3 x 5 = 15 |

#### Current Controls and Mitigations

1. **Early engagement with OneLogin team**: Programme Director engaging OneLogin product lead from Q1 2026
   - Effectiveness: **Adequate**
2. **OIDC-only approach**: Aligns with OneLogin's current capability (no SAML dependency)
   - Effectiveness: **Strong** — eliminates SAML compatibility risk identified in research
3. **Phased targets**: 5 pathfinder councils first, not 50 councils simultaneously
   - Effectiveness: **Strong** — early testing reveals issues before scale-up
4. **Standards-based federation**: OIDC is well-understood; integration pattern is standard
   - Effectiveness: **Adequate**

**Overall Control Effectiveness:** Strong (reduces risk from 15 to 8)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Early engagement and OIDC-only approach significantly reduce likelihood. |
| **Impact** | 4 - Major | Downgraded from Catastrophic because phased approach means a delay affects the 50-council target, not the entire programme. |
| **Residual Risk Score** | **8** (Medium) | 2 x 4 = 8 |

#### Risk Response: TREAT — Maintain close engagement with OneLogin team; validate federation capability in Q2 2026 with first pathfinder council.

---

### Risk R-018: Custom Data Sharing Platform Development Delays

**Category:** TECHNOLOGY
**Status:** Open
**Risk Owner:** GDS Local Programme Director
**Action Owner:** Programme Architect

#### Risk Identification

**Risk Description:**
The custom data sharing platform (FR-004) — identified in research as requiring 12-18 months development because no off-the-shelf solution meets requirements — is delayed, over-budget, or technically inadequate. This is the programme's most complex technology delivery.

**Root Cause:**
No COTS product combines UK GDPR cross-service data sharing with purpose limitation, DSA enforcement, audit trails, and multi-authority governance. Custom development is required, with all the attendant delivery risks (requirements uncertainty, architectural complexity, integration challenges with diverse council systems).

**Trigger Events:**
- Architecture design phase reveals greater complexity than anticipated
- ICO sandbox engagement requires architectural rework
- Integration testing with pilot council systems reveals unexpected technical challenges
- Key technical staff turnover during development

**Consequences if Realized:**
- Goal G-2 (3 pilot data sharing use cases by Q2 2027) delayed by 6-12 months
- Programme costs increase by £500K-1M for additional development
- MHCLG Digital Director frustrated — data sharing is their primary driver
- Councils participating in data sharing pilots face uncertainty

**Affected Stakeholders:**
- **MHCLG Digital Director** (SD-3): Data sharing ambition delayed
- **ICO** (SD-8): Regulatory sandbox engagement disrupted
- **LA Service Managers**: Frontline workers don't get cross-service data access

**Related Objectives:**
- Goal G-2 (Data sharing framework): Directly delayed
- Outcome O-2 (Joined-up support for vulnerable citizens): Delayed

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Custom platform development is inherently risky. 12-18 month estimate has significant uncertainty. Integration with diverse council systems adds complexity. |
| **Impact** | 4 - Major | Data sharing is one of GDS Local's three strategic priorities. Significant delay undermines MHCLG partnership. |
| **Inherent Risk Score** | **16** (High) | 4 x 4 = 16 |

#### Current Controls and Mitigations

1. **Agile delivery with 2-week sprints**: Continuous delivery reduces big-bang risk
   - Effectiveness: **Adequate**
2. **Pilot-first approach**: Build for 3 specific use cases, not generic platform
   - Effectiveness: **Strong** — constrains scope and enables rapid feedback
3. **Modular architecture**: Privacy gateway, audit service, consent management as independent components
   - Effectiveness: **Adequate** — reduces integration complexity
4. **ICO sandbox engagement**: Architectural guidance before major development investment
   - Effectiveness: **Strong** — reduces risk of regulatory rework

**Overall Control Effectiveness:** Adequate (reduces risk from 16 to 9)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Agile and pilot-first reduce risk but custom development complexity remains. |
| **Impact** | 3 - Moderate | Pilot-first means a delay affects 3 use cases, not the entire programme. Other workstreams continue. |
| **Residual Risk Score** | **9** (Medium) | 3 x 3 = 9 |

#### Risk Response: TREAT

---

### Risk R-019: Cyber Attack on Shared Components Affects Connected Councils

**Category:** TECHNOLOGY
**Status:** Open
**Risk Owner:** GDS Local Programme Director
**Action Owner:** Head of Security

#### Risk Identification

**Risk Description:**
A successful cyber attack against GDS Local shared components (OneLogin federation gateway, API gateway, data sharing platform) compromises the security of multiple connected councils simultaneously. Shared infrastructure creates a concentration of risk — one compromise has amplified blast radius.

**Root Cause:**
Local authorities have experienced significant cyber incidents (Hackney 2020, Redcar & Cleveland 2020). Extending shared components to councils expands the attack surface. Shared components become high-value targets because compromising them affects multiple organisations. Supply chain attacks could target shared dependencies.

**Trigger Events:**
- Ransomware attack targeting GDS Local infrastructure
- Zero-day vulnerability in shared component dependency
- Compromised council admin credentials used to access shared platform
- Supply chain attack on API gateway or identity provider
- Insider threat exploiting cross-authority data access

**Consequences if Realized:**
- Citizen personal data exposed across multiple authorities
- Council services disrupted simultaneously
- ICO enforcement and potential fines
- Media: "Centralised government IT hacked — data from dozens of councils exposed"
- Councils withdraw from shared platform, potentially permanently

**Affected Stakeholders:**
- **Citizens** (SD-7): Personal data compromised
- **NCSC** (SD-11): Government security posture weakened
- **LA Chief Executives** (SD-4): Liability and reputational damage
- **ICO** (SD-8): Data breach notification and enforcement

**Related Objectives:**
- All goals — security incident could be programme-ending

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Cyber attacks against UK public sector occur regularly. Shared platforms are high-value targets. |
| **Impact** | 5 - Catastrophic | Multi-authority data breach would be one of the largest government cyber incidents. |
| **Inherent Risk Score** | **15** (High) | 3 x 5 = 15 |

#### Current Controls and Mitigations

1. **Zero-trust architecture (NFR-SEC-001)**: No implicit trust; all requests authenticated
   - Effectiveness: **Strong**
2. **Tenant isolation (NFR-SEC-002)**: Council A cannot access Council B's data
   - Effectiveness: **Strong** — architecturally enforced
3. **NCSC Secure by Design review**: Security architecture reviewed by NCSC
   - Effectiveness: **Strong**
4. **Penetration testing by CHECK-certified provider**: Annual pen test + quarterly automated scans
   - Effectiveness: **Adequate**
5. **Vulnerability management SLA** (NFR-SEC-005): Critical 24h, High 7d
   - Effectiveness: **Strong**
6. **Encryption (NFR-SEC-003)**: TLS 1.2+ in transit, AES-256 at rest
   - Effectiveness: **Strong**

**Overall Control Effectiveness:** Strong (reduces risk from 15 to 8)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Comprehensive security controls significantly reduce likelihood. NCSC review provides expert assurance. |
| **Impact** | 4 - Major | Tenant isolation limits blast radius. Even a successful attack would not compromise all councils. |
| **Residual Risk Score** | **8** (Medium) | 2 x 4 = 8 |

#### Risk Response: TRANSFER (partial) + TREAT

**Rationale:** Treat through comprehensive security controls. Transfer residual risk element through cyber insurance for breach response costs. Government indemnity provisions may also apply.

---

### Risk R-020: Supplier Market Disruption

**Category:** TECHNOLOGY
**Status:** Open
**Risk Owner:** GDS Local Programme Director
**Action Owner:** Programme Comms Lead

#### Risk Identification

**Risk Description:**
Incumbent local government technology suppliers (Civica, Capita, NEC, Idox) actively resist GDS Local by lobbying councils against adoption, creating FUD (fear, uncertainty, doubt), refusing to support integration with shared components, or making contractual integration difficult.

**Root Cause:**
GDS Local shared components (identity, notifications, payments) could displace elements of existing supplier offerings. Suppliers have multi-year contracts with councils and significant revenue at risk. Supplier resistance is rational commercial behaviour — they are protecting their market position.

**Trigger Events:**
- Major supplier refuses to publish integration APIs for their council systems
- Supplier-funded "independent" report criticises GDS Local approach
- Supplier sales teams actively discourage councils from GDS Local adoption
- Supplier contract terms explicitly prevent council from using competing identity/notification services

**Consequences if Realized:**
- Council integration with shared components blocked by supplier non-cooperation
- Councils unable to adopt GDS Local components due to existing contract restrictions
- Market uncertainty delays council procurement decisions
- Programme team distracted by supplier relations management

**Affected Stakeholders:**
- **Technology Suppliers** (SD-10): Revenue at risk, market position threatened
- **LA Digital/IT Directors** (SD-5): Caught between GDS Local and existing suppliers
- **LA Chief Executives** (SD-4): Contractual and commercial complexity

**Related Objectives:**
- Goal G-1 (OneLogin adoption): Integration blocked
- Goal G-3 (Shared components): Adoption reduced

#### Inherent and Residual Risk Assessment

| Assessment | Inherent | Residual |
|------------|----------|----------|
| **Likelihood** | 3 - Possible | 2 - Unlikely |
| **Impact** | 3 - Moderate | 3 - Moderate |
| **Score** | **9** (Medium) | **6** (Medium) |

**Controls:** Early market engagement events; clear scope boundaries published (GDS Local builds horizontal capabilities, not vertical council systems); open APIs enabling integration rather than replacement; supplier integration guides; positioning suppliers as partners (integration services opportunity).

#### Risk Response: TOLERATE — Market dynamics cannot be fully controlled. Manage through engagement and positioning. Risk is within appetite.

---

## D. Risk Category Analysis

### STRATEGIC Risks

**Total STRATEGIC Risks:** 3
**Average Inherent Score:** 15.7 (High)
**Average Residual Score:** 10.3 (Medium)
**Control Effectiveness:** 34% reduction

**Risk List:**
- R-001: Insufficient local authority adoption — Residual: 12 (Medium)
- R-002: Ministerial direction or MoG change — Residual: 10 (Medium)
- R-003: "Whitehall imposing on councils" perception — Residual: 9 (Medium)

**Key Themes:**
- Council adoption is the programme's existential challenge — without sufficient council participation, shared components have no audience
- Political risks (ministerial change, central-local perception) are structural and difficult to mitigate through technical controls
- All three risks are interconnected: poor perception (R-003) reduces adoption (R-001), and political change (R-002) can disrupt both

**Category Risk Profile:** Concerning — Highest average residual score (10.3). Two risks exceed appetite. Active management required.

---

### OPERATIONAL Risks

**Total OPERATIONAL Risks:** 4
**Average Inherent Score:** 9.8 (Medium)
**Average Residual Score:** 6.3 (Medium)
**Control Effectiveness:** 36% reduction

**Risk List:**
- R-004: GDS platform team capacity — Residual: 9 (Medium)
- R-005: Skills gap in data sharing architecture — Residual: 6 (Medium)
- R-006: Community of practice critical mass — Residual: 4 (Low)
- R-007: GDS Service Assessment failure — Residual: 6 (Medium)

**Key Themes:**
- Capacity and skills risks dominate — the programme's delivery capability depends on people, not technology
- GDS platform team capacity (R-004) is the most significant operational risk and affects the headline OneLogin goal
- Community and assessment risks are well-controlled through LGA partnership and early engagement

**Category Risk Profile:** Acceptable — One risk exceeds appetite (R-004). Overall good control effectiveness.

---

### FINANCIAL Risks

**Total FINANCIAL Risks:** 3
**Average Inherent Score:** 12.0 (Medium)
**Average Residual Score:** 8.0 (Medium)
**Control Effectiveness:** 33% reduction

**Risk List:**
- R-008: Programme funding not sustained — Residual: 10 (Medium)
- R-009: Cloud infrastructure costs exceed projections — Residual: 6 (Medium)
- R-010: Savings target (£50M) not achieved — Residual: 8 (Medium)

**Key Themes:**
- Funding sustainability (R-008) is the highest financial risk and has catastrophic impact potential
- The £50M savings target (R-010) carries measurement and attribution challenges
- Cloud costs (R-009) are well-controlled through FinOps practices

**Category Risk Profile:** Concerning — One risk exceeds appetite (R-008). Funding sustainability requires GDS DG attention.

---

### COMPLIANCE/REGULATORY Risks

**Total COMPLIANCE Risks:** 3
**Average Inherent Score:** 11.7 (Medium)
**Average Residual Score:** 7.3 (Medium)
**Control Effectiveness:** 37% reduction

**Risk List:**
- R-011: Data sharing privacy breach — Residual: 10 (Medium)
- R-012: UK GDPR non-compliance in cross-authority data — Residual: 8 (Medium)
- R-013: Accessibility non-compliance — Residual: 4 (Low)

**Key Themes:**
- Data sharing compliance risks are the hardest to bring within appetite — both exceed the low compliance threshold
- The governance-first approach is the primary mitigation strategy
- Accessibility risk is well-controlled through GOV.UK Design System and automated testing

**Category Risk Profile:** Concerning — Both data sharing risks (R-011, R-012) exceed compliance appetite. These represent the programme's greatest compliance challenge.

---

### REPUTATIONAL Risks

**Total REPUTATIONAL Risks:** 3
**Average Inherent Score:** 12.0 (Medium)
**Average Residual Score:** 8.3 (Medium)
**Control Effectiveness:** 31% reduction

**Risk List:**
- R-014: High-profile service outage — Residual: 8 (Medium)
- R-015: Parliamentary scrutiny and media criticism — Residual: 9 (Medium)
- R-016: Citizen trust erosion — Residual: 8 (Medium)

**Key Themes:**
- Reputational risks have the lowest control effectiveness (31%) — reputation is difficult to protect proactively
- Parliamentary scrutiny (R-015) is inherent to government programmes and can only be managed, not eliminated
- Citizen trust (R-016) and service reliability (R-014) are closely linked — an outage could trigger trust concerns

**Category Risk Profile:** Concerning — One risk exceeds appetite (R-015). Proactive communications strategy essential.

---

### TECHNOLOGY Risks

**Total TECHNOLOGY Risks:** 4
**Average Inherent Score:** 13.8 (High)
**Average Residual Score:** 7.8 (Medium)
**Control Effectiveness:** 44% reduction

**Risk List:**
- R-017: GOV.UK OneLogin not ready — Residual: 8 (Medium)
- R-018: Custom data sharing platform delays — Residual: 9 (Medium)
- R-019: Cyber attack on shared components — Residual: 8 (Medium)
- R-020: Supplier market disruption — Residual: 6 (Medium)

**Key Themes:**
- Highest inherent risk category (13.8 average) but best control effectiveness (44%) — technology risks respond well to technical controls
- Custom data sharing platform (R-018) is the programme's most complex delivery challenge
- OneLogin readiness (R-017) is critical-path and depends on external GDS team
- Cyber security (R-019) has comprehensive controls but catastrophic impact potential

**Category Risk Profile:** Acceptable — All risks within technology appetite (≤12). Good control effectiveness.

---

## E. Risk Ownership Matrix

| Stakeholder | Role | Owned Risks | Exceeding Appetite | Total Residual Score | Concentration |
|-------------|------|-------------|-------------------|---------------------|---------------|
| GDS Director General | Programme Board Chair | R-002, R-004, R-008, R-015, R-017 | R-002, R-004, R-008, R-015 | 46 | HIGH |
| GDS Local Programme Director | Programme Delivery | R-003, R-005, R-007, R-009, R-013, R-014, R-018, R-019, R-020 | None | 65 | HIGH (volume) |
| MHCLG Digital Director | Data Sharing Co-lead | R-011, R-012, R-016 | R-011, R-012 | 26 | FOCUSED |
| LGA | Council Engagement | R-001, R-006, R-010 | R-001 | 24 | MODERATE |

**Risk Concentration Analysis:**
- **GDS Director General owns 5 risks with total score 46** — concentrated high-impact strategic and financial risks. Appropriate given seniority. 4 of 5 exceed appetite — requires Programme Board attention.
- **GDS Local Programme Director owns 9 risks with total score 65** — high volume but lower individual scores. No risks exceed appetite — good operational management position.
- **MHCLG Digital Director owns 3 risks with total score 26** — focused on data sharing compliance. Both data sharing risks exceed appetite — requires escalation to ICO and Programme Board.
- **LGA owns 3 risks with total score 24** — adoption and savings risks. R-001 exceeds appetite — LGA's convening power is the primary mitigation.

**Escalation Paths:**
- **Strategic/Financial Risks** (R-001, R-002, R-008): GDS DG -> Programme Board -> DSIT Senior Officials -> DSIT SoS
- **Compliance Risks** (R-011, R-012): MHCLG Digital Director -> Programme Board -> ICO
- **Technology Risks** (R-017, R-018, R-019): Programme Director -> Programme Board -> GDS DG
- **Reputational Risks** (R-014, R-015, R-016): Programme Director -> GDS DG -> DSIT Minister

---

## F. 4Ts Response Framework Summary

| Response | Count | % | Total Residual Score | Key Examples |
|----------|-------|---|---------------------|--------------|
| **TOLERATE** | 3 | 15% | 25 | R-002 (MoG change), R-015 (parliamentary scrutiny), R-020 (supplier dynamics) |
| **TREAT** | 16 | 80% | 127 | R-001, R-003, R-004, R-005, R-006, R-007, R-008, R-009, R-010, R-011, R-012, R-013, R-014, R-016, R-017, R-018 |
| **TRANSFER** | 1 | 5% | 8 | R-019 (cyber attack — partial transfer via insurance + treat) |
| **TERMINATE** | 0 | 0% | 0 | No activities should be terminated at this stage |
| **TOTAL** | 20 | 100% | 160 | |

**Response Breakdown by Category:**

| Category | Tolerate | Treat | Transfer | Terminate | Predominant |
|----------|----------|-------|----------|-----------|-------------|
| STRATEGIC | 1 | 2 | 0 | 0 | Treat (67%) |
| OPERATIONAL | 0 | 4 | 0 | 0 | Treat (100%) |
| FINANCIAL | 0 | 3 | 0 | 0 | Treat (100%) |
| COMPLIANCE | 0 | 3 | 0 | 0 | Treat (100%) |
| REPUTATIONAL | 1 | 2 | 0 | 0 | Treat (67%) |
| TECHNOLOGY | 1 | 2 | 1 | 0 | Treat (50%) |

**Key Insights:**
- **80% of risks require active treatment** — the programme is at an early stage where most risks can and should be actively mitigated
- **Only 15% tolerated** — these are genuine "act of God" risks (political change, parliamentary scrutiny, market dynamics) that cannot be controlled
- **One partial transfer** (cyber insurance) — most programme risks are internal and cannot be insured
- **No terminations** — all programme activities remain justified; termination would be considered only if risk profile becomes unacceptable

---

## G. Risk Appetite Compliance

**Programme Risk Appetite Thresholds:**

*Note: No organizational risk appetite statement found in `projects/000-global/policies/`. These thresholds are set for the GDS Local programme based on UK Government public sector context.*

| Category | Appetite Level | Threshold | Rationale |
|----------|---------------|-----------|-----------|
| STRATEGIC | Medium | ≤ 9 | Moderate tolerance for strategic risk in an innovation programme, but exceeding threatens programme viability |
| OPERATIONAL | Medium | ≤ 8 | Moderate tolerance for operational challenges during programme establishment |
| FINANCIAL | Low-Medium | ≤ 8 | Public money requires careful stewardship; NAO scrutiny expected |
| COMPLIANCE | Low | ≤ 6 | Low tolerance for compliance breaches — ICO enforcement, PSBAR 2018, GDS Service Standard |
| REPUTATIONAL | Low | ≤ 8 | Low tolerance for reputational damage — programme depends on trust |
| TECHNOLOGY | Medium | ≤ 12 | Willing to adopt new technology with controls; innovation is the programme's purpose |

**Compliance Summary:**

| Category | Appetite | Risks Within | Risks Exceeding | Avg Excess | Action Required |
|----------|----------|--------------|-----------------|------------|-----------------|
| STRATEGIC | ≤ 9 | 1 (R-003) | 2 (R-001, R-002) | +2.0 | Programme Board approval |
| OPERATIONAL | ≤ 8 | 3 (R-005, R-006, R-007) | 1 (R-004) | +1.0 | GDS DG approval |
| FINANCIAL | ≤ 8 | 1 (R-009) | 1 (R-008) | +2.0 | GDS DG / DSIT Finance approval |
| COMPLIANCE | ≤ 6 | 1 (R-013) | 2 (R-011, R-012) | +3.0 | MHCLG Digital Director / ICO escalation |
| REPUTATIONAL | ≤ 8 | 2 (R-014, R-016) | 1 (R-015) | +1.0 | GDS DG acceptance |
| TECHNOLOGY | ≤ 12 | 4 (all) | 0 | N/A | Compliant |

**Overall Appetite Compliance:** Concerning — 7 of 20 risks (35%) exceed appetite across 5 of 6 categories. Only TECHNOLOGY category is fully within appetite.

**Risks Significantly Exceeding Appetite (>50% over threshold):**

| Risk ID | Category | Appetite | Actual | Excess | % Over | Escalation |
|---------|----------|----------|--------|--------|--------|------------|
| R-011 | COMPLIANCE | 6 | 10 | +4 | 67% | MHCLG Digital Director + ICO engagement |
| R-001 | STRATEGIC | 9 | 12 | +3 | 33% | Programme Board |
| R-012 | COMPLIANCE | 6 | 8 | +2 | 33% | MHCLG Digital Director |
| R-008 | FINANCIAL | 8 | 10 | +2 | 25% | GDS DG / DSIT Finance |

**Recommendations:**
1. **URGENT**: MHCLG Digital Director to formally accept R-011 and R-012 compliance risks pending ICO sandbox engagement — governance-first approach is the primary mitigation
2. **HIGH PRIORITY**: Programme Board to approve R-001 strategic risk — LGA co-leadership and pathfinder approach are the mitigations
3. **MONITOR**: GDS DG to accept R-002, R-004, R-008, R-015 — these are structural risks inherent to the programme's operating context

---

## H. Prioritized Action Plan

### Priority 1: URGENT (Risks Exceeding Appetite — Compliance)

| # | Action | Risk(s) | Owner | Due Date | Expected Impact | Status |
|---|--------|---------|-------|----------|-----------------|--------|
| 1 | Complete ICO regulatory sandbox engagement for data sharing framework | R-011, R-012 | MHCLG Digital Director | 2026-06-30 | Reduce R-011 from 10 to 5; R-012 from 8 to 4 | Not Started |
| 2 | Develop joint incident response plan with ICO for data sharing breaches | R-011 | Data Protection Officer | 2026-05-31 | Reduce impact response time from days to hours | Not Started |
| 3 | Complete DPIAs for 3 pilot data sharing use cases | R-011, R-012 | DPO | 2026-07-31 | Legal compliance assurance | Not Started |

### Priority 2: HIGH (Risks Exceeding Appetite — Strategic/Financial)

| # | Action | Risk(s) | Owner | Due Date | Expected Impact | Status |
|---|--------|---------|-------|----------|-----------------|--------|
| 4 | Launch pathfinder council programme with 5 volunteer councils | R-001 | LGA | 2026-06-30 | Generate peer advocacy; validate onboarding | Not Started |
| 5 | Publish council savings calculator with projected ROI per council type | R-001, R-010 | Programme Director | 2026-05-31 | Strengthen adoption value proposition | Not Started |
| 6 | Fund dedicated council onboarding support team (5 FTEs) | R-001, R-004 | Programme Director | 2026-04-30 | Reduce onboarding friction | Not Started |
| 7 | Submit 3-year funding case to DSIT Finance with NAO-ready evidence | R-008 | GDS DG | 2026-04-30 | Secure sustained programme funding | Not Started |
| 8 | Validate OneLogin local authority federation capability with pathfinder council | R-017 | GDS OneLogin Team Lead | 2026-06-30 | Confirm technical readiness for council integration | Not Started |

### Priority 3: MEDIUM (High-Score Risks Within or Near Appetite)

| # | Action | Risk(s) | Owner | Due Date | Expected Impact | Status |
|---|--------|---------|-------|----------|-----------------|--------|
| 9 | Establish LGA joint communications protocol for all GDS Local announcements | R-003, R-015 | Programme Comms Lead | 2026-04-15 | Prevent "Whitehall imposing" narrative | Not Started |
| 10 | Commission NCSC security architecture review of data sharing platform design | R-019 | Head of Security | 2026-06-30 | NCSC assurance of security architecture | Not Started |
| 11 | Establish FinOps monitoring and monthly cost review for cloud infrastructure | R-009 | Technical Lead | 2026-05-31 | Early detection of cost overruns | Not Started |
| 12 | Begin recruitment of data sharing architecture specialists | R-005, R-018 | Programme Director | 2026-03-31 | Build specialist team for data sharing platform | Not Started |

**Overall Action Plan Summary:**
- **Total Actions:** 12
- **Total Investment:** Primarily staff time; funded onboarding team is the main new cost (5 FTEs ~ £400K/year)
- **Target Completion:** All actions by Q3 2026
- **Expected Risk Reduction:** 7 risks currently exceeding appetite targeted to come within appetite by Q3 2026

---

## I. Integration with SOBC

**How this Risk Register feeds into Strategic Outline Business Case (SOBC):**

### SOBC Strategic Case (Part A)
- **"Why Now?" section** uses strategic risks to demonstrate urgency:
  - R-001 (adoption): Without immediate action, councils will continue individual procurement and GDS Local loses momentum
  - R-002 (political change): Programme must deliver visible results before next political cycle to ensure continuity
  - R-017 (OneLogin readiness): Window of opportunity while OneLogin is being extended — alignment with platform roadmap

### SOBC Economic Case (Part B)
- **Risk-adjusted costs** use financial risks + HM Treasury optimism bias:
  - R-008 (funding): Phased investment model reduces annual commitment — £6-10M/year not £18-29M upfront
  - R-009 (cloud costs): Add 15% contingency for cloud cost uncertainty (~£450K/year)
  - R-018 (platform development): Add 20% contingency for custom development risk (~£200K)
  - **Total risk contingency:** ~£1M added to Economic Case costs

### SOBC Management Case (Part E - Risk Management)
- **Full risk register** included in Management Case Part E
- **Top 10 risks** highlighted with mitigation plans
- **Risk ownership matrix** demonstrates clear accountability from stakeholder RACI
- **Monitoring framework** shows ongoing risk management capability
- **Orange Book compliance** demonstrates methodological rigour

### SOBC Recommendation
- Programme risk profile is **Concerning but manageable** — no critical residual risks, but 7 exceeding appetite
- **Recommendation**: Proceed with phased approach, addressing urgent compliance risks before data sharing pilots
- **Key condition**: ICO regulatory sandbox endorsement before any cross-authority data sharing (R-011, R-012)

---

## J. Monitoring and Review Framework

### Review Schedule

| Risk Level | Review Frequency | Reviewed By | Escalated To | Report Format |
|------------|------------------|-------------|--------------|---------------|
| **Exceeding Appetite** | Bi-weekly | Risk Owner + Programme Director | Programme Board | Dashboard + narrative |
| **Medium (6-12)** | Monthly | Risk Owner | Programme Director | Dashboard |
| **Low (1-5)** | Quarterly | Action Owner | Risk Owner | Status update |

### Key Risk Indicators (KRIs)

**Leading Indicators** (predict future risk changes):
- Council registration rate (target: 10/month) — leading indicator for R-001
- GDS platform team sprint velocity on local gov features — leading indicator for R-004, R-017
- ICO sandbox engagement progress (milestones met vs. planned) — leading indicator for R-011, R-012
- Community of practice membership growth rate — leading indicator for R-006
- DSIT Spending Review signals and ministerial briefing outcomes — leading indicator for R-002, R-008

**Lagging Indicators** (confirm risk materialization):
- Actual vs. projected council adoption numbers — confirms R-001
- Data sharing audit anomalies detected — confirms R-011
- Monthly cloud spend vs. budget — confirms R-009
- GDS Service Assessment outcomes — confirms R-007
- Security incident count and severity — confirms R-019

### Escalation Criteria

**Automatic Escalation Triggers:**
1. Any risk increases by 5+ points between reviews
2. Any new High (13+) or Critical (20+) residual risk identified
3. Any risk exceeds appetite and no mitigation plan exists
4. Any mitigation action delayed > 1 month past due date
5. 3+ risks in same category exceed appetite simultaneously
6. Risk owner vacancy — risk unowned for > 2 weeks

### Reporting Requirements

**Bi-weekly** (Risks Exceeding Appetite):
- Dashboard to Programme Board showing all 7 appetite-exceeding risks
- Narrative update on action plan progress
- Any new escalation triggers

**Monthly** (All Risks):
- Full risk register to Programme Board
- Risk matrix visualization (inherent and residual)
- Risk appetite compliance summary
- Action plan status
- KRI trend analysis

**Quarterly** (Strategic Review):
- Risk trend analysis to DSIT Senior Officials
- Risk appetite threshold review
- Lessons learned from risk materialization (if any)
- Risk register process improvement review
- Update risk register version

### Risk Register Maintenance

**Risk Register Owner:** GDS Local Programme Director

**Update Process:**
1. Risk owners submit updates bi-weekly (appetite-exceeding) or monthly (within appetite)
2. Programme Director validates and updates register
3. PMO reviews for consistency and completeness
4. Programme Board approves material changes (new risks, score changes >3 points)

**Next Full Review Date:** 2026-03-17

---

## K. Orange Book Compliance Checklist

This risk register demonstrates compliance with HM Treasury Orange Book (2023):

### Part I — Risk Management Principles

- **A. Governance and Leadership**
  - Risk owners assigned from senior stakeholders (GDS DG, MHCLG Digital Director, Programme Director, LGA) via RACI matrix in ARC-001-STKE-v1.0
  - Escalation paths defined to Programme Board, DSIT Senior Officials, and DSIT Secretary of State
  - Programme risk appetite set across 6 categories with exceedance tracking

- **B. Integration**
  - Risks linked to strategic objectives (stakeholder goals G-1 through G-6 and outcomes O-1 through O-4)
  - Risks inform business case (SOBC Management Case Part E integration documented)
  - Risk management embedded in programme governance through monthly and quarterly review cycles

- **C. Collaboration and Best Information**
  - Risks sourced from stakeholder concerns and conflict analysis (ARC-001-STKE-v1.0 Section: Conflict Analysis)
  - Multiple perspectives considered: central government, local government, regulators, suppliers, citizens
  - Evidence-based assessment with likelihood and impact justified per risk

- **D. Risk Management Processes**
  - Systematic identification across 6 Orange Book categories (Strategic, Operational, Financial, Compliance, Reputational, Technology)
  - Consistent assessment methodology (5x5 matrix, Likelihood x Impact)
  - 4Ts response framework applied to all 20 risks
  - Inherent and residual risk tracked with control effectiveness measured

- **E. Continual Improvement**
  - Regular review schedule (bi-weekly for appetite-exceeding, monthly all risks, quarterly strategic)
  - Key Risk Indicators defined for leading and lagging measurement
  - Lessons learned process embedded in quarterly review
  - Risk register version control and maintenance process defined

### Part II — Risk Control Framework

- **4-Pillar "House" Structure**
  - Risk appetite and tolerance defined per category
  - Risk ownership and governance established via stakeholder RACI
  - Risk assessment methodology documented (Appendix A of template)
  - Control effectiveness measured: average 35% reduction from inherent to residual risk

---

## Appendix A: Stakeholder-Risk Linkage

**Traceability from Stakeholders to Risks:**

| Stakeholder | Driver (from ARC-001-STKE-v1.0) | Risk ID | Risk Title | Category | Residual |
|-------------|--------------------------------|---------|------------|----------|----------|
| DSIT Minister | SD-1: Demonstrate digital transformation | R-002 | Ministerial direction change | STRATEGIC | 10 |
| DSIT Minister | SD-1: Demonstrate digital transformation | R-015 | Parliamentary scrutiny | REPUTATIONAL | 9 |
| GDS Director General | SD-2: Platform economy extension | R-004 | Platform team capacity | OPERATIONAL | 9 |
| GDS Director General | SD-2: Platform economy extension | R-017 | OneLogin not ready | TECHNOLOGY | 8 |
| MHCLG Digital Director | SD-3: Local gov modernisation | R-011 | Data sharing privacy breach | COMPLIANCE | 10 |
| MHCLG Digital Director | SD-3: Local gov modernisation | R-018 | Data sharing platform delays | TECHNOLOGY | 9 |
| LA Chief Executives | SD-4: Services within constraints | R-001 | Insufficient adoption | STRATEGIC | 12 |
| LA Chief Executives | SD-4: Services within constraints | R-010 | £50M savings not achieved | FINANCIAL | 8 |
| LA Digital/IT Directors | SD-5: Practical technology | R-005 | Skills gap | OPERATIONAL | 6 |
| LA Digital/IT Directors | SD-5: Practical technology | R-020 | Supplier disruption | TECHNOLOGY | 6 |
| LGA | SD-6: Represent council interests | R-003 | "Whitehall imposing" perception | STRATEGIC | 9 |
| LGA | SD-6: Represent council interests | R-006 | Community critical mass | OPERATIONAL | 4 |
| Citizens | SD-7: Seamless services | R-014 | Service outage | REPUTATIONAL | 8 |
| Citizens | SD-7: Seamless services | R-016 | Citizen trust erosion | REPUTATIONAL | 8 |
| ICO | SD-8: Lawful data sharing | R-011 | Privacy breach | COMPLIANCE | 10 |
| ICO | SD-8: Lawful data sharing | R-012 | GDPR non-compliance | COMPLIANCE | 8 |
| NAO | SD-9: Value for money | R-008 | Funding not sustained | FINANCIAL | 10 |
| NAO | SD-9: Value for money | R-010 | Savings target not met | FINANCIAL | 8 |
| Technology Suppliers | SD-10: Market clarity | R-020 | Supplier disruption | TECHNOLOGY | 6 |
| NCSC | SD-11: Secure architecture | R-019 | Cyber attack | TECHNOLOGY | 8 |

**Stakeholder Conflicts Mapped to Risks:**

| Conflict (from ARC-001-STKE-v1.0) | Risk(s) Created | Mitigation |
|------------------------------------|-----------------|------------|
| Conflict 1: DSIT Minister (speed) vs LA Chief Execs (autonomy) | R-001, R-003 | Pathfinder approach; voluntary model; LGA co-lead |
| Conflict 2: GDS DG (platform extension) vs LA IT Directors (local fit) | R-004, R-017 | Co-design; OIDC standards-based; self-service onboarding |
| Conflict 3: MHCLG (data sharing ambition) vs ICO (governance rigour) | R-011, R-012 | Governance first; ICO sandbox; pilot-first |
| Conflict 4: GDS Local components vs Supplier market | R-020 | Clear scope; open APIs; partnership positioning |

---

## Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| **Risk Register Owner** (Programme Director) | | | |
| **Programme Sponsor** (GDS Director General) | | | |
| **Data Sharing Co-sponsor** (MHCLG Digital Director) | | | |
| **Council Partnership Lead** (LGA) | | | |

---

## Next Steps

1. **Immediate Actions** (This Week):
   - [ ] Circulate risk register to all risk owners for validation
   - [ ] Schedule Programme Board session to review and accept appetite-exceeding risks
   - [ ] MHCLG Digital Director to initiate ICO regulatory sandbox engagement for R-011/R-012
   - [ ] GDS DG to confirm 3-year funding case timeline for R-008

2. **Short-term Actions** (This Month):
   - [ ] Begin recruitment for data sharing architecture specialists (R-005, R-018)
   - [ ] Establish LGA joint communications protocol (R-003)
   - [ ] Set up FinOps monitoring for cloud infrastructure (R-009)
   - [ ] Fund and recruit council onboarding support team (R-001)

3. **Medium-term Actions** (This Quarter — by May 2026):
   - [ ] Launch pathfinder council programme with 5 councils (R-001)
   - [ ] Validate OneLogin federation with first pathfinder council (R-017)
   - [ ] Complete DPIAs for 3 pilot data sharing use cases (R-011, R-012)
   - [ ] Commission NCSC security architecture review (R-019)
   - [ ] First monthly risk review meeting with all risk owners
   - [ ] Integrate risk register into SOBC Management Case Part E

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-001-STKE-v1.0 | Stakeholder Analysis | ArcKit | 11 drivers, 6 goals, 4 conflicts, 5 stakeholder risks, RACI matrix for risk ownership | projects/001-gds-local/ARC-001-STKE-v1.0.md |
| ARC-001-REQ-v1.0 | Requirements | ArcKit | 6 BRs, 10 FRs, 18 NFRs, 5 dependencies, budget £18-29M | projects/001-gds-local/ARC-001-REQ-v1.0.md |
| ARC-000-PRIN-v1.1 | Architecture Principles | ArcKit | 25 principles, non-negotiable security (P5) and accessibility (P6) | projects/000-global/ARC-000-PRIN-v1.1.md |
| ARC-001-RSCH-v1.0 | Technology Research | ArcKit | Custom build needed for data sharing platform (12-18 months), OneLogin OIDC only, £1.2M 3-year TCO | projects/001-gds-local/ARC-001-RSCH-v1.0.md |
| HM Treasury Orange Book | Risk Management | HM Treasury | 5 principles, 4Ts framework, risk control framework | gov.uk |

---

**Generated by**: ArcKit `/arckit:risk` command
**Generated on**: 2026-02-17
**ArcKit Version**: 2.4.5
**Project**: GDS Local (Project 001)
**AI Model**: Claude Opus 4.6
