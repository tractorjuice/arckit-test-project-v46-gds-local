# GDS Service Assessment Preparation Report

> **Template Status**: Beta | **Version**: 2.15.1 | **Command**: `/arckit.service-assessment`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SVCASS-v1.0 |
| **Document Type** | GDS Service Assessment Preparation Report |
| **Project** | GDS Local (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-02-28 |
| **Last Modified** | 2026-02-28 |
| **Review Cycle** | Monthly |
| **Next Review Date** | 2026-03-28 |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | GDS Local Programme Team, GDS Director General, MHCLG Digital, LGA, DSIT Finance |
| **Assessment Phase** | Alpha |
| **Assessment Date** | Not yet scheduled |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-28 | ArcKit AI | Initial creation from `/arckit.service-assessment` command | PENDING | PENDING |

---

## Executive Summary

**Overall Readiness**: 🟡 Amber (Nearly Ready)

**Readiness Score**: 5/14 points Green, 9/14 Amber, 0 Red

**Breakdown**:

- 🟢 Green: 5 points
- 🟡 Amber: 9 points
- 🔴 Red: 0 points

**Summary**:

The GDS Local programme has an exceptionally strong documentation foundation for an Alpha assessment. Comprehensive stakeholder analysis (ARC-001-STKE-v1.0) identifies 11 stakeholder drivers with detailed user groups, needs, and pain points. Requirements (ARC-001-REQ-v1.0) are well-structured with 6 business requirements, 10 functional requirements, 18 non-functional requirements, and 5 integration requirements, all traced to stakeholder goals. The Strategic Outline Business Case (ARC-001-SOBC-v1.0) follows HM Treasury Green Book methodology with a BCR of 2.8:1 on a £24M investment, and the Project Plan (ARC-001-PLAN-v1.0) defines a clear 68-week delivery timeline with GDS Agile Delivery phases.

The programme's greatest strength is its commitment to reusing and extending existing GDS common components (GOV.UK OneLogin, Notify, Pay) rather than building from scratch. Architecture Principles (ARC-000-PRIN-v1.1) explicitly mandate open standards, platform reuse, and privacy by design. The C4 System Context Diagram (ARC-001-DIAG-001-v1.0) demonstrates a well-thought-out integration architecture with requirements traceability.

The Amber ratings are primarily because the programme has not yet entered its formal Alpha phase (planned for weeks 13-32, June-October 2026). Key gaps include: no prototype usability testing yet conducted, no formal threat model (Secure by Design assessment), no DPIA despite processing citizen PII across services, no Architecture Decision Records (ADRs), and no explicit open source code strategy. These are all artefacts that would naturally be produced during Alpha — the team should prioritise their creation to convert Amber ratings to Green before booking the Alpha assessment.

**Critical Gaps** (Must address before assessment):

- Point 9: No Secure by Design (SECD) assessment or DPIA despite cross-service citizen data sharing
- Point 1: No prototype testing with real users yet documented
- Point 12: No explicit open source code strategy or repository approach

**Key Strengths**:

- Exceptional stakeholder analysis and user needs documentation (STKE, REQ)
- Strong commitment to GDS common components and open standards (PRIN, DIAG)
- Comprehensive business case with clear success metrics (SOBC)
- Well-structured project plan with GDS Agile Delivery phases (PLAN)
- Extensive business research providing market and policy context (RSCH v2.0)

**Recommended Timeline**:

- 6-8 weeks to address critical gaps (run `/arckit:secure`, `/arckit:dpia`, `/arckit:adr`)
- 4-6 weeks additional for prototype testing and iteration documentation
- **Recommended assessment booking**: After Alpha week 20 (approximately September 2026)

---

## Service Standard Assessment (14 Points)

### 1. Understand Users and Their Needs

**Status**: 🟡 Amber

**What This Point Means**:
You must understand your users and their needs through research. You should develop a deep understanding of what users need, how they behave, and what they experience when interacting with your service.

**Why It Matters**:
Services that don't start with user needs risk solving the wrong problem. Understanding users ensures public money is spent on services people actually need and can use.

**Evidence Required for Alpha**:

- User needs documented from research
- User groups and personas identified
- Prototype testing results with real users (critical)
- Evidence of research with diverse user groups
- Analytics data (optional for alpha)

**Evidence Found in ArcKit Artifacts**:

✅ **ARC-001-STKE-v1.0** (Stakeholder Drivers)

- 11 stakeholder drivers documented with detailed needs, pain points, and goals
- User groups comprehensively identified: Citizens (56M population), Council Officers (housing, social workers, service managers), Council IT Teams (digital service managers, developers), LGA, MHCLG, ICO
- RACI matrix mapping roles and responsibilities across all stakeholder groups
- Pain points documented per user group: Citizens face "form-filling fatigue" and "repeat verification"; Council Officers face "siloed data" and "manual workarounds"; Council IT Teams face "vendor lock-in" and "limited flexibility"

✅ **ARC-001-REQ-v1.0** (Requirements)

- 6 business requirements traced to stakeholder goals (BR-001 through BR-006)
- 10 functional requirements with acceptance criteria
- User stories embedded within requirements documentation
- Requirement BR-004: "Co-design with local government practitioners" explicitly commits to user-centred design

✅ **ARC-001-RSCH-v2.0** (Business Research)

- Research with over 300 local government digital professionals (January-April 2025)
- GOV.UK OneLogin discovery: 14 councils, 8 suppliers, 36 survey respondents
- Digital maturity data from 71 councils (Local Digital Fund survey)
- Key user finding: "cost savings and identity verification" are top council priorities; "digital exclusion and resident trust" are key barriers

⚠️ **Weak**: Research is secondary (desk-based market research and GDS engagement data) rather than primary user research conducted by the programme team

❌ **Missing**: Prototype testing results with real users — PLAN references prototype testing during Alpha phase (weeks 13-32) but this has not yet been conducted

❌ **Missing**: Primary user research conducted by the programme's own user researcher — current evidence is from GDS engagement activities and MHCLG discovery research

**Gap Analysis**:
The programme has strong foundational user needs documentation through the stakeholder analysis and requirements. The business research provides excellent secondary evidence about user groups and their challenges. However, the critical gap is primary user research: the programme has not yet conducted its own discovery research with citizens, council officers, or council IT teams. The prototype testing evidence required for Alpha assessment has not yet been produced. This is expected given the programme hasn't yet entered Alpha, but must be addressed before assessment.

**Readiness Rating**: 🟡 Amber

**Strengths**:

- Comprehensive stakeholder analysis with 11 drivers, detailed user groups, and RACI matrix
- Business research providing evidence from 300+ professionals, 14 councils, and sector-wide data
- Requirements explicitly traced to user needs and stakeholder goals

**Weaknesses**:

- No primary user research conducted by the programme team
- No prototype testing with real users (planned but not yet done)
- No user personas with demographic and accessibility characteristics

**Recommendations**:

1. **Critical**: Conduct primary user research with citizens, council officers, and council IT teams during Alpha Discovery/Sprint 1
   - Timeline: 4-6 weeks
   - Owner: Lead User Researcher
   - Evidence to create: User research findings report, user personas, user journey maps

2. **Critical**: Conduct prototype usability testing with at least 5 diverse users per user group
   - Timeline: Ongoing through Alpha (weeks 16-28)
   - Owner: Lead User Researcher
   - Evidence to create: Usability testing reports with findings and iteration decisions

3. **High**: Create detailed user personas including accessibility needs, digital confidence levels, and channel preferences
   - Timeline: 2 weeks
   - Owner: Lead User Researcher + Content Designer
   - Evidence to create: 4-6 user personas covering citizens, council officers, and IT teams

**Assessment Day Guidance**:

- **Prepare**: User research findings with quotes from real users; show research wall or synthesis board
- **Show**: User journey maps, prototype iterations based on feedback, research playback
- **Bring**: Lead User Researcher must attend and present
- **Materials**: Research findings, user personas, prototype screens, iteration log
- **Likely Questions**:
  - "How have you tested your prototype with real users, including those with access needs?"
  - "What did you learn from your research that surprised you or changed your approach?"

---

### 2. Solve a Whole Problem for Users

**Status**: 🟢 Green

**What This Point Means**:
Work towards creating a service that solves a whole problem for users, collaborating across organisational boundaries where necessary. The service should not force users to understand government structures to get what they need.

**Why It Matters**:
Users don't care about departmental boundaries. They need services that work end-to-end without requiring them to navigate between central and local government systems.

**Evidence Required for Alpha**:

- User journey maps showing end-to-end experience
- Problem definition beyond government touchpoints
- Understanding of user context before/after service interaction
- Identification of pain points in current experience

**Evidence Found in ArcKit Artifacts**:

✅ **ARC-001-REQ-v1.0** (Requirements)

- End-to-end functional requirements covering the complete user journey: identity federation (FR-001), onboarding (FR-002), component catalogue (FR-003), data sharing (FR-004), governance (FR-005), community (FR-006), procurement (FR-007), monitoring (FR-008), APIs (FR-009), consent (FR-010)
- Integration requirements showing cross-organisational data flows (INT-001 through INT-005)
- Business requirement BR-001: "Extend GDS platforms to local authorities" addresses the whole problem of fragmented central-local government services

✅ **ARC-001-STKE-v1.0** (Stakeholder Drivers)

- User goals documented: "Citizens expect seamless access across central and local government services"
- Pain points identify the whole problem: "333 councils individually procuring commodity technology", "no single sign-on across council services", "repeat verification"
- Measurable outcomes tied to solving the whole problem: "50 councils onboarded by Q4 2027"

✅ **ARC-001-DIAG-001-v1.0** (System Context Diagram)

- C4 System Context diagram showing the full service boundary and external integrations
- All 6 external systems mapped: GOV.UK OneLogin, Notify, Pay, Local Authority Systems, ICO, Crown Commercial Service
- Relationships show end-to-end data flows from citizen authentication through to data sharing and payments
- Architecture Decision 3 documents the voluntary pathfinder approach — solving for real councils, not theoretical users

✅ **ARC-001-RSCH-v2.0** (Business Research)

- Extensive analysis of user context: local authority landscape (317 authorities), financial crisis (8 Section 114 notices), digital maturity variation (4.9% digital spend vs 7% benchmark)
- Comparable programmes analysed: NHS Digital, Wales CDPS, Estonia X-Road, New Zealand RealMe
- Understanding of barriers beyond technology: "digital exclusion, resident trust, transitioning users from existing systems"

✅ **ARC-001-SOBC-v1.0** (Business Case)

- Problem definition spans fiscal crisis, digital maturity gaps, and citizen experience — well beyond government touchpoints
- Five-case model addresses strategic, economic, commercial, financial, and management dimensions

**Gap Analysis**:
This is one of the programme's strongest areas. The documentation comprehensively addresses the whole problem: from citizen identity fragmentation across 333 councils, through cross-service data sharing barriers, to procurement inefficiencies. The system context diagram shows clear service boundaries with justified rationale. The business research provides deep context about the local government landscape that informs the problem definition.

**Readiness Rating**: 🟢 Green

**Strengths**:

- Comprehensive problem definition spanning central and local government boundaries
- System context diagram with clear service boundaries and external system mapping
- Deep understanding of user context from extensive business research
- International comparisons (Estonia X-Road, NZ RealMe) showing awareness of best practice

**Weaknesses**:

- User journey maps not yet created as standalone artefacts (journey is implicit in requirements)
- Assisted digital provision for councils with low digital maturity not yet detailed

**Recommendations**:

1. **Medium**: Create standalone user journey maps for each primary user group (citizen, council officer, council IT team)
   - Timeline: 2 weeks
   - Owner: Service Designer
   - Evidence to create: 3 user journey maps showing end-to-end experience with pain points

**Assessment Day Guidance**:

- **Prepare**: Walk-through of end-to-end user journey showing how GDS Local solves the whole problem
- **Show**: System context diagram, user journey from citizen perspective crossing central-local boundary
- **Bring**: Product Manager and Service Designer
- **Materials**: ARC-001-DIAG-001-v1.0, user journey maps, RSCH v2.0 problem context
- **Likely Questions**:
  - "How does this service work for a citizen who needs both central and local government services?"
  - "What happens for councils that aren't part of the programme — how do citizens experience the transition?"

---

### 3. Provide a Joined Up Experience Across All Channels

**Status**: 🟡 Amber

**What This Point Means**:
Create a joined up experience across all channels — online, phone, paper, face-to-face — so that users get a consistent experience regardless of how they interact with the service.

**Why It Matters**:
Many users, particularly vulnerable citizens, interact with councils through non-digital channels. The service must work across all access methods.

**Evidence Required for Alpha**:

- Channels identified and mapped
- Integration strategy defined
- Consistent branding and messaging planned
- Understanding of user channel preferences

**Evidence Found in ArcKit Artifacts**:

✅ **ARC-001-DIAG-001-v1.0** (System Context Diagram)

- Digital channels mapped: citizen web interface (HTTPS), council officer interface (HTTPS), API gateway for system integration
- GOV.UK Notify integration covers email, SMS, and letters — multi-channel notifications

✅ **ARC-001-REQ-v1.0** (Requirements)

- FR-002: Self-service onboarding portal (digital channel)
- FR-006: Community of practice platform (digital channel)
- INT-003: GOV.UK Notify extension for email, SMS, and letters
- NFR accessibility requirements mandate WCAG 2.2 AA compliance

✅ **ARC-000-PRIN-v1.1** (Architecture Principles)

- P1: User-Centred Design — "Design for all users, including those with low digital confidence"
- P8: Central-Local Collaboration — consistent approach across central and local government
- GOV.UK Design System mandated for consistent branding

⚠️ **Weak**: No explicit channel strategy mapping all access methods (digital, phone, paper, face-to-face)

❌ **Missing**: Assisted digital strategy for users who cannot use the digital channel

❌ **Missing**: User channel preference data from research

**Gap Analysis**:
Digital channels are well-defined and GOV.UK Notify provides multi-channel notification (email, SMS, letters). However, the programme lacks an explicit channel strategy that maps all access methods including non-digital channels. For a platform serving 56 million citizens with variable digital confidence, an assisted digital strategy is important. This gap is typical for early Alpha and can be addressed through user research.

**Readiness Rating**: 🟡 Amber

**Strengths**:

- Digital channels well-defined with clear integration architecture
- GOV.UK Notify provides built-in multi-channel communication (email, SMS, letters)
- GOV.UK Design System ensures consistent branding

**Weaknesses**:

- No explicit channel strategy document
- Assisted digital provision not detailed
- No data on user channel preferences

**Recommendations**:

1. **High**: Document channel strategy covering digital, phone, paper, and face-to-face access methods
   - Timeline: 2 weeks
   - Owner: Service Designer
   - Evidence to create: Channel strategy document with user volumes and accessibility considerations

2. **Medium**: Define assisted digital approach for users with low digital confidence
   - Timeline: 2 weeks
   - Owner: Lead User Researcher + Service Designer
   - Evidence to create: Assisted digital plan referencing user research findings

**Assessment Day Guidance**:

- **Prepare**: Channel map showing all access methods and how they connect
- **Show**: GOV.UK Notify multi-channel capabilities, GOV.UK Design System consistency
- **Bring**: Service Designer and User Researcher
- **Materials**: Channel strategy, notification templates, accessibility approach
- **Likely Questions**:
  - "How does the service work for someone who can't use digital channels?"
  - "How do you ensure consistency between the digital service and phone/paper channels?"

---

### 4. Make the Service Simple to Use

**Status**: 🟡 Amber

**What This Point Means**:
Build a service that's simple to use so that people can succeed first time, without needing to contact the service for help. The service should use familiar patterns, simple language, and minimal steps.

**Why It Matters**:
Complex services waste public money on support costs and exclude users who can't navigate complexity.

**Evidence Required for Alpha**:

- Prototype usability testing conducted
- Design iterations based on user feedback
- Simple language and clear instructions
- Task completion rates in testing

**Evidence Found in ArcKit Artifacts**:

✅ **ARC-000-PRIN-v1.1** (Architecture Principles)

- P1: User-Centred Design — mandates user-centred approaches
- P2: Simplicity — "Favour simplicity and clarity in all design decisions"
- P4: Open Standards — familiar, widely-used standards reduce complexity

✅ **ARC-001-REQ-v1.0** (Requirements)

- FR-002: Self-service onboarding portal — designed for council IT teams to integrate without GDS support
- NFR usability targets referenced (though specific task completion rates not defined)
- Acceptance criteria for each functional requirement define "success" for key tasks

✅ **ARC-001-DIAG-001-v1.0** (System Context Diagram)

- Architecture Decision 4: "All integrations use open standards only" — reduces cognitive load on council developers
- API endpoints designed with clear, RESTful conventions

❌ **Missing**: Prototype usability testing results

❌ **Missing**: Design iterations based on user feedback

❌ **Missing**: Specific task completion rate targets

**Gap Analysis**:
Principles and requirements clearly commit to simplicity and user-centred design. The architecture favours open standards specifically to reduce complexity. However, no prototype testing has been conducted yet, so there is no evidence of design iterations based on user feedback or task completion rates. This is expected pre-Alpha.

**Readiness Rating**: 🟡 Amber

**Strengths**:

- Simplicity is a core architecture principle (P2)
- Self-service onboarding model reduces barriers for councils
- Open standards approach reduces integration complexity

**Weaknesses**:

- No prototype testing evidence
- No design iteration log
- No specific task completion rate targets

**Recommendations**:

1. **Critical**: Conduct prototype usability testing during Alpha sprints 3-8
   - Timeline: 6-8 weeks (within Alpha)
   - Owner: Lead User Researcher + Service Designer
   - Evidence to create: Usability testing reports with task completion rates

2. **High**: Define specific task completion rate targets (e.g., > 80% first-time completion for onboarding)
   - Timeline: 1 week
   - Owner: Product Manager
   - Evidence to create: Updated NFRs with measurable usability targets

**Assessment Day Guidance**:

- **Prepare**: Prototype demo showing simplicity of key user journeys
- **Show**: Before/after comparisons if design iterations have occurred
- **Bring**: Service Designer and User Researcher
- **Materials**: Prototype, usability test results, iteration log
- **Likely Questions**:
  - "Can you show us how you've simplified the service based on what users told you?"
  - "What's the first-time success rate for the key tasks in your service?"

---

### 5. Make Sure Everyone Can Use the Service

**Status**: 🟡 Amber

**What This Point Means**:
Make sure everyone can use the service, including disabled people, people with low digital literacy, and those who access services in different ways. The service must meet WCAG 2.1 AA as a minimum.

**Why It Matters**:
Public services must be accessible to everyone. Excluding disabled users is both a legal requirement (Equality Act 2010) and a service failure.

**Evidence Required for Alpha**:

- Accessibility considerations documented
- WCAG 2.1 AA compliance planned
- Testing with assistive technology planned
- Full accessibility audit not required at alpha

**Evidence Found in ArcKit Artifacts**:

✅ **ARC-001-REQ-v1.0** (Requirements)

- NFR accessibility requirements specify WCAG 2.2 AA compliance (exceeding the 2.1 AA minimum)
- GOV.UK Design System mandated — provides built-in accessibility
- Accessibility referenced as a non-functional requirement category

✅ **ARC-000-PRIN-v1.1** (Architecture Principles)

- P1: User-Centred Design — "Design for all users, including those with low digital confidence"
- P5: Accessibility — referenced in principles framework
- GOV.UK Design System is accessible by design

✅ **ARC-001-STKE-v1.0** (Stakeholder Drivers)

- Citizens identified as primary users with variable digital confidence
- Recognises diverse council populations including vulnerable citizens

⚠️ **Weak**: Accessibility is mentioned but lacks detailed testing plans for assistive technologies (screen readers, voice control, magnification)

❌ **Missing**: Assistive technology testing plan specifying which technologies and when

❌ **Missing**: Accessibility specialist role not explicitly identified in team structure

**Gap Analysis**:
Accessibility requirements are documented and the programme mandates WCAG 2.2 AA compliance (exceeding the minimum). The use of GOV.UK Design System provides strong accessibility foundations. However, there is no detailed plan for testing with assistive technologies or disabled users. An accessibility specialist is not explicitly identified in the team structure. These gaps are manageable for Alpha but must be addressed before Beta.

**Readiness Rating**: 🟡 Amber

**Strengths**:

- WCAG 2.2 AA compliance target exceeds minimum requirement (2.1 AA)
- GOV.UK Design System provides accessible-by-default components
- User-centred design principles acknowledge diverse user needs

**Weaknesses**:

- No specific assistive technology testing plan
- No accessibility specialist identified in team
- No user research planned with disabled users

**Recommendations**:

1. **High**: Include disabled users in Alpha user research (at least 2 participants using assistive technology)
   - Timeline: During Alpha user research (weeks 16-28)
   - Owner: Lead User Researcher
   - Evidence to create: Accessibility-specific user research findings

2. **High**: Identify or recruit accessibility specialist for the team
   - Timeline: 4 weeks
   - Owner: Delivery Manager
   - Evidence to create: Updated team structure with accessibility role

3. **Medium**: Create an accessibility testing plan specifying assistive technologies to test with
   - Timeline: 2 weeks
   - Owner: Accessibility Specialist (when appointed)
   - Evidence to create: Accessibility testing plan covering screen readers, voice control, and magnification

**Assessment Day Guidance**:

- **Prepare**: Explain accessibility approach: WCAG 2.2 AA target, GOV.UK Design System, testing plans
- **Show**: GOV.UK Design System components in prototype, any accessibility testing conducted
- **Bring**: Accessibility specialist (if appointed) or designer with accessibility knowledge
- **Materials**: Accessibility requirements from REQ, GOV.UK Design System usage evidence
- **Likely Questions**:
  - "How are you ensuring disabled users can access this service?"
  - "Have you tested with assistive technology? What did you find?"

---

### 6. Have a Multidisciplinary Team

**Status**: 🟢 Green

**What This Point Means**:
Put in place a sustainable multidisciplinary team that can design, build, and operate the service. The team should have or have access to the right skills, including user research, design, development, and content.

**Why It Matters**:
Services built by single-discipline teams (e.g., only developers) fail to meet user needs. A multidisciplinary team ensures all aspects of service design are considered.

**Evidence Required for Alpha**:

- Team composition documented
- Key roles filled: Product Manager, User Researcher, Tech Lead, Designer, Delivery Manager
- Skills audit showing capability coverage
- Team co-located or good remote working practices

**Evidence Found in ArcKit Artifacts**:

✅ **ARC-001-PLAN-v1.0** (Project Plan)

- Team structure documented with 35 FTE peak (Alpha: 30 FTE)
- Roles defined: Programme Director, Service Owner (Liz Adams), Technical Architect, User Research Lead, Service Designer, Delivery Manager, Business Analyst, Developers, Security Architect, Data Architect
- Phase-specific team scaling: Discovery (15 FTE), Alpha (30 FTE), Beta (35 FTE), Live (15 FTE)
- £38.2M TCO with team costs as largest component

✅ **ARC-001-STKE-v1.0** (Stakeholder Drivers)

- RACI matrix documenting responsibilities across all team members and external stakeholders
- Clear accountability model with named roles for each activity

✅ **ARC-001-SOBC-v1.0** (Business Case)

- Team funding secured through business case approval
- Sustainability plan documented — ongoing team funded through operational budget
- Skills requirements identified alongside cost model

✅ **ARC-001-RSCH-v2.0** (Business Research)

- Leadership identified: Service Owner Liz Adams, Local Government Champion Theo Blackwell
- GDS Local operating within DSIT/GDS — access to broader GDS capability and expertise

**Gap Analysis**:
Team composition is well-documented with clear roles, funding, and scaling plans. The RACI matrix shows good governance. Named leaders are identified. The key gap is that some roles (accessibility specialist, content designer) are not explicitly listed. However, the overall team structure is strong for Alpha.

**Readiness Rating**: 🟢 Green

**Strengths**:

- 30 FTE team planned for Alpha with clear role definitions
- Named leadership: Service Owner (Liz Adams), Local Government Champion (Theo Blackwell)
- RACI matrix showing clear accountability
- Funding secured via business case (£38.2M TCO)

**Weaknesses**:

- Accessibility specialist not explicitly listed in team
- Content designer role not explicitly documented

**Recommendations**:

1. **Medium**: Ensure accessibility specialist and content designer are included in Alpha team composition
   - Timeline: 2 weeks
   - Owner: Delivery Manager
   - Evidence to create: Updated team structure document

**Assessment Day Guidance**:

- **Prepare**: Team org chart showing all disciplines; explain how team accesses specialist skills
- **Show**: RACI matrix, team scaling plan across phases
- **Bring**: Delivery Manager to present team structure; have multiple team members present
- **Materials**: ARC-001-PLAN-v1.0 team section, RACI from STKE
- **Likely Questions**:
  - "Do you have all the skills you need? How do you fill gaps?"
  - "How does the team make decisions? Who has the authority to change direction?"

---

### 7. Use Agile Ways of Working

**Status**: 🟢 Green

**What This Point Means**:
Create the service using agile, iterative, user-centred methods. The team should work in short cycles, test ideas with users, and adapt based on evidence.

**Why It Matters**:
Waterfall approaches in government have a poor track record. Agile delivery reduces risk by validating assumptions early and delivering value incrementally.

**Evidence Required for Alpha**:

- Agile ceremonies established (standups, retros, planning)
- Sprint cadence defined (typically 1-2 weeks)
- User stories and backlog maintained
- Iterative approach to prototyping

**Evidence Found in ArcKit Artifacts**:

✅ **ARC-001-PLAN-v1.0** (Project Plan)

- GDS Agile Delivery phases explicitly adopted: Discovery (weeks 1-12), Alpha (13-32), Beta (33-68), Live (69+)
- 2-week sprint cadence documented
- Sprint ceremonies referenced: planning, standups, retrospectives, reviews
- Governance gates at phase transitions (Discovery → Alpha, Alpha → Beta, etc.)
- Gantt chart and workflow diagrams showing iterative delivery
- Risk management integrated into sprint reviews

✅ **ARC-001-SOBC-v1.0** (Business Case)

- Phased delivery approach documented with incremental value delivery
- Benefits realisation aligned to agile phases

✅ **ARC-001-RISK-v1.0** (Risk Register)

- Iterative risk management: risks reviewed at sprint boundaries
- Risk R-003 specifically addresses "Scope creep from expanding service catalogue" — evidence of backlog discipline

**Gap Analysis**:
Agile ways of working are well-documented with clear phase structure, sprint cadence, ceremonies, and governance gates. The programme follows GDS Agile Delivery methodology. Evidence of actual agile practice (sprint boards, velocity charts, retrospective outputs) will be generated during Alpha.

**Readiness Rating**: 🟢 Green

**Strengths**:

- GDS Agile Delivery methodology explicitly adopted
- 2-week sprint cadence with full ceremony set
- Governance gates at phase transitions
- Agile delivery experience within GDS organisation

**Weaknesses**:

- No evidence of actual agile practice yet (sprint boards, velocity, retro outputs) — expected pre-Alpha

**Recommendations**:

1. **Medium**: Document retrospective outcomes and iteration decisions during Alpha sprints
   - Timeline: Ongoing through Alpha
   - Owner: Delivery Manager
   - Evidence to create: Sprint retrospective log showing improvements made

**Assessment Day Guidance**:

- **Prepare**: Show sprint board (physical or digital), sprint cadence, ceremony schedule
- **Show**: Examples of how retrospectives led to improvements; show how user research feeds into sprint planning
- **Bring**: Delivery Manager to present; have team members confirm agile practices
- **Materials**: Sprint board screenshot, retrospective outputs, velocity chart (if available)
- **Likely Questions**:
  - "What does a typical sprint look like for your team?"
  - "Can you give an example of something you changed based on a retrospective?"

---

### 8. Iterate and Improve Frequently

**Status**: 🟡 Amber

**What This Point Means**:
Make sure you have the capacity, resources, and technical flexibility to iterate and improve the service frequently. The team should be able to release changes quickly and respond to user feedback.

**Why It Matters**:
Services that can't iterate become stale and fail to meet evolving user needs. Frequent iteration demonstrates a learning culture.

**Evidence Required for Alpha**:

- Prototype iterations documented
- Changes based on user feedback
- Multiple design options explored
- Learning log showing insights and pivots

**Evidence Found in ArcKit Artifacts**:

✅ **ARC-001-RSCH-v2.0** (Business Research)

- Version history shows iteration: v1.0 (technology-focused) was replaced by v2.0 (business-focused) — demonstrating willingness to pivot based on learning
- Research scope evolved from technology vendor analysis to comprehensive business intelligence

✅ **ARC-001-DIAG-001-v1.0** (System Context Diagram)

- Four architecture decisions documented with options analysis (Decision 1-4)
- Each decision shows context, decision, rationale, and consequences — evidence of structured design exploration

✅ **ARC-001-PLAN-v1.0** (Project Plan)

- Iteration cycles planned with review gates
- Alpha phase specifically allocated for prototyping and testing

⚠️ **Weak**: No formal design iteration log or learning log

❌ **Missing**: Prototype iterations with before/after comparisons

❌ **Missing**: Learning log showing insights and pivots during Alpha

**Gap Analysis**:
The programme demonstrates willingness to iterate (research document version change from technology to business focus). Architecture decisions show structured options exploration. However, no formal iteration or learning log exists, and prototype iterations haven't occurred yet. This is expected pre-Alpha but the team should establish a learning log early in Alpha.

**Readiness Rating**: 🟡 Amber

**Strengths**:

- Evidence of pivoting (RSCH v1.0 → v2.0 shows willingness to change direction)
- Structured options analysis in architecture decisions
- Iteration cycles planned in project schedule

**Weaknesses**:

- No formal learning log
- No prototype iteration evidence
- No documented design history

**Recommendations**:

1. **High**: Establish a learning log from Alpha Sprint 1, documenting insights, pivots, and decisions
   - Timeline: 1 day to set up, ongoing maintenance
   - Owner: Delivery Manager
   - Evidence to create: Learning log with dated entries showing insights and actions taken

2. **Medium**: Create a design history showing evolution of key design decisions
   - Timeline: Ongoing through Alpha
   - Owner: Service Designer
   - Evidence to create: Design history document with before/after comparisons

**Assessment Day Guidance**:

- **Prepare**: Learning log entries; show how research changed the programme's direction
- **Show**: RSCH v1.0 → v2.0 pivot as evidence of iteration; architecture decision options analysis
- **Bring**: Product Manager and Service Designer
- **Materials**: Learning log, design history, prototype iteration examples
- **Likely Questions**:
  - "What have you learned during Alpha that changed your approach?"
  - "How quickly can you make changes based on what you learn from users?"

---

### 9. Create a Secure Service Which Protects Users' Privacy

**Status**: 🟡 Amber

**What This Point Means**:
Evaluate what data the service will collect, store, and share. Understand how you'll protect it, and how you'll treat the risk of data loss. Put appropriate security measures in place.

**Why It Matters**:
GDS Local will process citizen PII across multiple councils and services. Cross-service data sharing creates significant privacy risks. Several councils have suffered major ransomware attacks in recent years.

**Evidence Required for Alpha**:

- Threat model created
- Security risks identified and assessed
- GDPR compliance approach defined
- Data protection impact assessment (if needed)
- Privacy considerations documented

**Evidence Found in ArcKit Artifacts**:

✅ **ARC-001-RISK-v1.0** (Risk Register)

- R-011: "Privacy breach through cross-service data sharing" — residual risk score 10 (High) with controls: purpose-limited API queries, audit trails, ICO regulatory sandbox
- R-012: "Data governance failure across 333 autonomous councils" — residual risk score 8
- R-017: "Cyber attack on shared platform affecting all connected councils" — controls: NCSC Cyber Essentials Plus, pen testing
- Security risks form a dedicated category in the risk register with specific mitigations

✅ **ARC-000-PRIN-v1.1** (Architecture Principles)

- P15: Secure by Design — "Security is not an afterthought; embed NCSC secure design principles"
- P16: Zero Trust Architecture — "Verify identity and authorisation at every service boundary"
- P17: Privacy by Design — "Embed UK GDPR compliance into all data processing"
- These three principles form a comprehensive security framework

✅ **ARC-001-REQ-v1.0** (Requirements)

- NFR-SEC-003: TLS 1.3 mandatory for all communications, AES-256 for data at rest
- NFR-C-001: Purpose-limited data sharing with full audit trail
- FR-010: Citizen consent management system
- FR-005: Data sharing governance dashboard
- All security NFRs traced to NCSC guidance

✅ **ARC-001-DIAG-001-v1.0** (System Context Diagram)

- Architecture Decision 2: "Governed data sharing via purpose-limited API queries, not bulk data transfer"
- ICO regulatory sandbox engagement planned
- OAuth 2.0 council-scoped authentication, mutual TLS for service providers
- Technology choices: TLS 1.3, AES-256, OIDC/SAML 2.0, OAuth 2.0

✅ **ARC-001-RSCH-v2.0** (Business Research)

- Section 5.6: Cyber security context — documents Hackney (£10M+), Redcar (£11.3M), and other council ransomware incidents
- Section 5.3: Data sharing legislation — Digital Economy Act 2017, UK GDPR, Data Protection Act 2018 legal basis analysis
- Identifies legislative gap: no general power for local authorities to share data between services

❌ **Missing**: Formal threat model / Secure by Design (SECD) assessment — run `/arckit:secure`

❌ **Missing**: Data Protection Impact Assessment (DPIA) — required given cross-service citizen PII processing; run `/arckit:dpia`

⚠️ **Weak**: No ICO engagement timeline or plan documented

**Gap Analysis**:
Security and privacy are well-considered across multiple artifacts. The risk register identifies specific privacy and cyber risks with controls. Architecture principles mandate Secure by Design, Zero Trust, and Privacy by Design. Requirements specify encryption standards and consent management. However, the programme lacks two critical artifacts: a formal Secure by Design assessment (threat model) and a DPIA. Given that GDS Local will process citizen PII across multiple councils, a DPIA is legally required under UK GDPR Article 35. These should be produced early in Alpha.

**Readiness Rating**: 🟡 Amber

**Strengths**:

- Three security-focused architecture principles (Secure by Design, Zero Trust, Privacy by Design)
- Comprehensive security risks in risk register with specific controls
- Purpose-limited data sharing approach with audit trails and ICO engagement
- Strong encryption and authentication standards (TLS 1.3, AES-256, OAuth 2.0)
- Legal basis analysis for data sharing in business research

**Weaknesses**:

- No formal Secure by Design assessment or threat model
- No DPIA despite processing citizen PII across services (legally required)
- No ICO engagement timeline

**Recommendations**:

1. **Critical**: Generate Secure by Design assessment using `/arckit:secure`
   - Timeline: 2 weeks
   - Owner: Security Architect
   - Evidence to create: ARC-001-SECD-v1.0.md with NCSC threat model, security controls, and residual risk assessment

2. **Critical**: Generate Data Protection Impact Assessment using `/arckit:dpia`
   - Timeline: 2 weeks
   - Owner: Data Protection Officer
   - Evidence to create: ARC-001-DPIA-v1.0.md with data flows, processing purposes, lawful basis, and ICO consultation plan

3. **High**: Plan ICO regulatory sandbox engagement with specific timeline and milestones
   - Timeline: 1 week
   - Owner: Data Protection Officer + Programme Director
   - Evidence to create: ICO engagement plan with dates

**Assessment Day Guidance**:

- **Prepare**: Security architecture overview, data sharing governance model, DPIA summary
- **Show**: Purpose-limited data sharing approach, consent management, audit trail design
- **Bring**: Security Architect and Data Protection Officer
- **Materials**: Risk register security section, SECD assessment, DPIA, architecture decisions
- **Likely Questions**:
  - "How do you protect citizen data when sharing across council boundaries?"
  - "Have you completed a DPIA? What did it find?"
  - "How do you handle a data breach affecting multiple councils?"

---

### 10. Define What Success Looks Like and Publish Performance Data

**Status**: 🟡 Amber

**What This Point Means**:
Work out what success looks like for your service and identify metrics to tell you how it's performing. Collect data and use it to improve your service.

**Why It Matters**:
Without clear success metrics, services drift without accountability. Performance data drives evidence-based improvement and demonstrates value to stakeholders.

**Evidence Required for Alpha**:

- Success metrics defined (user satisfaction, completion rates, cost per transaction)
- Baseline measurements identified
- Data collection approach planned
- KPIs aligned to user needs

**Evidence Found in ArcKit Artifacts**:

✅ **ARC-001-SOBC-v1.0** (Business Case)

- BCR 2.8:1 on £24M investment — clear quantified success measure
- Benefits realisation framework with specific targets: £67M net benefits over 10 years
- Phase-specific milestones: 5 pathfinder councils (Phase 1), 20 councils (Phase 2), 50 councils (Phase 3)
- Cost per transaction targets implicit in savings model

✅ **ARC-001-REQ-v1.0** (Requirements)

- NFR performance targets: 99.9% uptime, < 2 seconds query response, < 500ms authentication
- Business requirement BR-003: "Deliver measurable cost savings" — success explicitly requires measurement
- FR-008: Platform health and status dashboard — technical monitoring built into requirements

✅ **ARC-001-PLAN-v1.0** (Project Plan)

- Phase milestones with measurable success criteria at each governance gate
- Phase success criteria defined for Discovery, Alpha, Beta, Live transitions

✅ **ARC-001-STKE-v1.0** (Stakeholder Drivers)

- Measurable outcomes per stakeholder group: "50 councils onboarded by Q4 2027", "30% reduction in procurement costs"
- User satisfaction measures implicit in stakeholder outcome targets

⚠️ **Weak**: No specific data collection plan for the 4 mandatory KPIs (cost per transaction, user satisfaction, completion rate, digital take-up)

❌ **Missing**: Baseline measurements for current council performance (how long do transactions take today? What is current user satisfaction?)

**Gap Analysis**:
Success is well-defined at the programme level through the business case and project plan. Quantified targets exist for benefits, adoption, and technical performance. However, the programme lacks specific plans for collecting the 4 mandatory GDS KPIs and has not established baseline measurements. For Alpha, this is acceptable but should be addressed to strengthen the case.

**Readiness Rating**: 🟡 Amber

**Strengths**:

- Clear quantified success metrics: BCR 2.8:1, 50 councils, £67M net benefits
- Performance NFRs with specific targets (99.9% uptime, < 2s response)
- Phase-specific milestones with governance gates
- Platform monitoring dashboard in requirements (FR-008)

**Weaknesses**:

- No plan for collecting mandatory GDS KPIs (cost per transaction, user satisfaction, completion rate, digital take-up)
- No baseline measurements for current council performance

**Recommendations**:

1. **High**: Define data collection approach for the 4 mandatory GDS KPIs
   - Timeline: 2 weeks
   - Owner: Performance Analyst
   - Evidence to create: KPI measurement plan specifying data sources, collection frequency, and baselines

2. **Medium**: Establish baseline measurements by surveying pathfinder councils on current performance
   - Timeline: 4 weeks
   - Owner: User Researcher + Performance Analyst
   - Evidence to create: Baseline performance report from pathfinder councils

**Assessment Day Guidance**:

- **Prepare**: Show KPI framework, targets, and how you'll measure success
- **Show**: Benefits model from SOBC, phase milestones from PLAN, monitoring dashboard design
- **Bring**: Product Manager and Performance Analyst
- **Materials**: SOBC benefits section, PLAN milestones, KPI measurement plan
- **Likely Questions**:
  - "What does success look like at the end of Alpha?"
  - "How will you measure cost per transaction and user satisfaction?"

---

### 11. Choose the Right Tools and Technology

**Status**: 🟢 Green

**What This Point Means**:
Choose tools and technology that let you create a high quality service in a cost effective way. Minimise the cost of changing direction, and avoid getting locked in to contracts or technology choices.

**Why It Matters**:
Poor technology choices waste money, create vendor lock-in, and constrain future development. Government services must use technology that enables rapid iteration.

**Evidence Required for Alpha**:

- Technology options explored
- Build vs buy analysis completed
- Technology spikes/proof of concepts conducted
- Technology choices justified against requirements
- Cost analysis for technology options

**Evidence Found in ArcKit Artifacts**:

✅ **ARC-001-DIAG-001-v1.0** (System Context Diagram)

- Technology choices documented with rationale: OIDC/SAML 2.0, REST APIs (OpenAPI), OAuth 2.0, TLS 1.3, AES-256, GOV.UK Design System
- Evolution stage analysis for each component (Genesis/Custom/Product/Commodity)
- Build/Buy/Reuse decisions: BUILD for core platform, REUSE for GOV.UK services (OneLogin, Notify, Pay)
- Component inventory with 7 components, technology, and responsibilities mapped
- Architecture Decision 1: "Extend existing GOV.UK platforms rather than building new equivalents" — clear build vs buy rationale

✅ **ARC-001-RSCH-v2.0** (Business Research)

- Market analysis: key suppliers identified (Civica, Capita, NEC, Idox, Access Group)
- Comparable programmes analysed for technology approach: NHS Digital, Wales CDPS, Estonia X-Road
- Market dynamics documented including vendor lock-in risks and switching costs

✅ **ARC-000-PRIN-v1.1** (Architecture Principles)

- P4: Open Standards — mandates open, vendor-neutral technology choices
- P13: Reuse GDS Platforms — "use existing government platforms before building new"
- P14: Cloud-First — "cloud-native architectures for scalability and cost efficiency"
- P16: Zero Trust Architecture — technology constraint requiring specific patterns

✅ **ARC-001-SOBC-v1.0** (Business Case)

- Cost analysis across options (Do Nothing, Do Minimum, Preferred Option, Do Maximum)
- TCO analysis: £38.2M over programme lifecycle
- Technology costs broken down by phase

✅ **ARC-001-REQ-v1.0** (Requirements)

- All technology choices traced to specific requirements
- Open standards mandated as technical constraints (TC-1, TC-2)

**Gap Analysis**:
Technology choices are exceptionally well-justified. The architecture diagram provides a clear component inventory with evolution stages and build/buy/reuse decisions. Architecture principles mandate open standards and platform reuse. The business case provides cost analysis across options. The only gap is the absence of formal Architecture Decision Records (ADRs) documenting each technology choice individually, though the decisions are well-captured in the diagram's architecture decisions section.

**Readiness Rating**: 🟢 Green

**Strengths**:

- Clear build vs buy analysis with REUSE strategy for GDS platforms
- Technology choices justified against requirements with full traceability
- Evolution stage analysis showing commodity vs custom technology
- Cost analysis across 4 options in business case
- Open standards mandate prevents vendor lock-in

**Weaknesses**:

- No formal Architecture Decision Records (ADRs) — decisions are captured in diagram but not as standalone documents
- No evidence of technology spikes/POCs yet (planned for Alpha)

**Recommendations**:

1. **Medium**: Generate formal Architecture Decision Records using `/arckit:adr` for key technology decisions
   - Timeline: 2 weeks
   - Owner: Technical Architect
   - Evidence to create: ARC-001-ADR-001 through ARC-001-ADR-004 covering the 4 key decisions from the diagram

2. **Medium**: Conduct technology spikes/POCs during Alpha for OneLogin federation and data sharing API
   - Timeline: 4-6 weeks (Alpha sprints 1-4)
   - Owner: Technical Architect + Lead Developer
   - Evidence to create: POC evaluation reports

**Assessment Day Guidance**:

- **Prepare**: Technology choices presentation with build vs buy rationale
- **Show**: Component evolution stage analysis, cost comparison from SOBC options
- **Bring**: Technical Architect
- **Materials**: ARC-001-DIAG-001-v1.0, architecture decisions, SOBC cost analysis
- **Likely Questions**:
  - "Why did you choose to build vs buy for the core platform?"
  - "How will you avoid vendor lock-in?"
  - "What happens if GOV.UK OneLogin timeline slips further?"

---

### 12. Make New Source Code Open

**Status**: 🟡 Amber

**What This Point Means**:
Make all new source code open and reusable, and publish it under appropriate licences. Make source code available so people outside your team can benefit from it, learn from it, or contribute to it.

**Why It Matters**:
Open source code enables transparency, collaboration, and reuse. It builds trust and allows other public sector organisations to benefit from government investment.

**Evidence Required for Alpha**:

- Open source approach decided
- Security and IP considerations addressed
- Code repository approach defined
- Code may not be public yet at alpha

**Evidence Found in ArcKit Artifacts**:

✅ **ARC-000-PRIN-v1.1** (Architecture Principles)

- P4: Open Standards — "Use open, vendor-neutral standards to maximise interoperability"
- Open approach is embedded in principles but doesn't explicitly cover source code

✅ **ARC-001-DIAG-001-v1.0** (System Context Diagram)

- Architecture Decision 4: "All integrations use open standards only" — supports open approach
- Technology choices are all based on open protocols (OIDC, REST, OAuth 2.0)

⚠️ **Weak**: Open standards are well-documented but open source code is not the same as open standards — the programme has not explicitly committed to open sourcing its code

❌ **Missing**: Open source policy statement (license choice, repository location, contribution model)

❌ **Missing**: Code repository approach (GitHub organisation, repository structure)

❌ **Missing**: Process for reviewing code for secrets before publication

**Gap Analysis**:
The programme is strongly committed to open standards and open protocols, but has not explicitly addressed open source code. There is no policy on licensing, repository location, or contribution. This is a common gap in early programmes and is straightforward to address. For Alpha, the panel will want to see a clear decision on the open source approach, even if code is not yet public.

**Readiness Rating**: 🟡 Amber

**Strengths**:

- Strong commitment to open standards and open protocols
- Technology choices are all based on open ecosystems
- GDS organisational culture strongly supports open source

**Weaknesses**:

- No explicit open source code policy
- No repository approach defined
- No contribution model or licence chosen

**Recommendations**:

1. **High**: Define open source policy: license choice (MIT or Apache 2.0 recommended), GitHub organisation, contribution guidelines
   - Timeline: 1 week
   - Owner: Technical Architect
   - Evidence to create: Open source policy document covering license, repository approach, and contribution model

2. **Medium**: Set up code repository (likely GitHub under GDS/DSIT organisation) during Alpha
   - Timeline: 2 weeks
   - Owner: Lead Developer
   - Evidence to create: GitHub repository with README, LICENSE, and CONTRIBUTING.md

**Assessment Day Guidance**:

- **Prepare**: Explain open source approach, license choice, repository plans
- **Show**: GitHub repository (if created), README with project purpose
- **Bring**: Technical Architect or Lead Developer
- **Materials**: Open source policy, GitHub repo link
- **Likely Questions**:
  - "Will your code be open? Under what licence?"
  - "How will you ensure secrets don't end up in public repositories?"

---

### 13. Use and Contribute to Open Standards, Common Components and Patterns

**Status**: 🟢 Green

**What This Point Means**:
Build on open standards and common components and patterns from inside and outside government. If you develop a new pattern or component, share it so others can use it.

**Why It Matters**:
Using common components saves money and time, and provides users with a consistent experience across government services.

**Evidence Required for Alpha**:

- GOV.UK Design System usage planned
- Common components identified (GOV.UK Notify, Pay, etc.)
- API standards considered (RESTful, OpenAPI)
- Data standards identified (if applicable)

**Evidence Found in ArcKit Artifacts**:

✅ **ARC-001-DIAG-001-v1.0** (System Context Diagram)

- GOV.UK OneLogin: REUSE — identity federation (OIDC/SAML)
- GOV.UK Notify: REUSE — multi-channel notifications (email, SMS, letters)
- GOV.UK Pay: REUSE — payment processing (REST API)
- GOV.UK Design System: specified for citizen-facing UI
- API standards: REST (OpenAPI), OAuth 2.0, mutual TLS
- Architecture Decision 1: "Extend existing GOV.UK platforms rather than building new equivalents"

✅ **ARC-000-PRIN-v1.1** (Architecture Principles)

- P4: Open Standards — "Use open, vendor-neutral standards to maximise interoperability"
- P13: Reuse GDS Platforms — "Evaluate and use existing GDS platforms (Notify, Pay, OneLogin, Forms) before building custom alternatives"
- These principles make common component usage a governance requirement

✅ **ARC-001-REQ-v1.0** (Requirements)

- TC-2: "Use open standards for all data exchange and API interfaces"
- INT-001 through INT-005: Integration requirements specifying open standard protocols
- FR-003: Shared component catalogue — the programme itself creates a new common component for councils

✅ **ARC-001-RSCH-v2.0** (Business Research)

- Section 3: Documents existing GOV.UK platform adoption in local government
- GOV.UK Notify: "More than half of all councils in the UK now use GOV.UK Notify"
- GOV.UK Pay: Open to local authorities for council tax, planning fees, parking permits
- TCoP Point 8 (Share and Reuse) referenced as governance driver

**Gap Analysis**:
This is the programme's strongest area. The entire GDS Local programme is fundamentally about extending and reusing common components. GOV.UK OneLogin, Notify, and Pay are core to the architecture. The programme also creates new common components (shared component catalogue, data sharing platform) that other councils can use. Open standards are mandated at the principles level.

**Readiness Rating**: 🟢 Green

**Strengths**:

- Programme is fundamentally built on reusing GDS common components
- Three GOV.UK platforms integrated: OneLogin, Notify, Pay
- Open standards mandated as architecture principle and technical constraint
- Programme creates new common components for local government reuse
- API standards follow government API design guidelines (REST, OpenAPI)

**Weaknesses**:

- GOV.UK Forms not yet included in the component set (potential opportunity)

**Recommendations**:

1. **Medium**: Consider including GOV.UK Forms in the shared component catalogue for council form building
   - Timeline: 2 weeks
   - Owner: Product Manager
   - Evidence to create: Assessment of GOV.UK Forms suitability for local government

**Assessment Day Guidance**:

- **Prepare**: Map of all GDS common components used and how they integrate
- **Show**: System context diagram showing GOV.UK platform integrations; explain how the programme itself creates new shared components
- **Bring**: Technical Architect
- **Materials**: ARC-001-DIAG-001-v1.0, principles P4 and P13, GOV.UK platform adoption data from RSCH
- **Likely Questions**:
  - "Which GDS common components are you using? Are there others you should consider?"
  - "How will you share what you build with other teams?"

---

### 14. Operate a Reliable Service

**Status**: 🟡 Amber

**What This Point Means**:
Minimise service downtime and have a plan to deal with it when it does happen. Use data from monitoring to inform improvements.

**Why It Matters**:
GDS Local is a shared platform — downtime affects all connected councils simultaneously. Platform reliability directly impacts citizen access to council services.

**Evidence Required for Alpha**:

- Reliability requirements defined
- Uptime targets set
- High-level resilience approach planned
- Full operational procedures not needed at alpha

**Evidence Found in ArcKit Artifacts**:

✅ **ARC-001-REQ-v1.0** (Requirements)

- 99.9% availability target (equates to < 8.76 hours downtime/year)
- < 2 seconds response time for data sharing queries
- < 500ms authentication flow via OneLogin
- FR-008: Platform health and status dashboard — monitoring built into requirements
- FR-009: API gateway with rate limiting — prevents cascading failures

✅ **ARC-001-DIAG-001-v1.0** (System Context Diagram)

- SLA table for external systems: OneLogin 99.9%, Notify 99.95%, Pay 99.9%
- Platform adds < 100ms latency on council data responses
- Architecture shows clear separation between internal platform and external dependencies

✅ **ARC-001-RISK-v1.0** (Risk Register)

- R-017: "Cyber attack on shared platform affecting all connected councils" — controls identified
- R-014: Platform scalability risks documented
- Operational risks form a dedicated category with mitigations

❌ **Missing**: DevOps strategy (CI/CD pipeline, infrastructure as code, monitoring approach) — run `/arckit:devops`

❌ **Missing**: Operational readiness documentation (incident response, on-call, DR/BCP)

❌ **Missing**: Load testing plan

**Gap Analysis**:
Reliability requirements are well-defined with specific uptime and performance targets. The risk register addresses operational risks. However, no DevOps strategy, operational procedures, or incident response plan exists. For Alpha, this is acceptable — the panel primarily wants to see reliability requirements and a high-level approach. These operational artifacts should be produced during Beta.

**Readiness Rating**: 🟡 Amber

**Strengths**:

- Clear reliability targets: 99.9% availability, < 2s response, < 500ms auth
- Monitoring dashboard built into requirements (FR-008)
- API gateway with rate limiting prevents cascading failures (FR-009)
- Operational risks identified in risk register

**Weaknesses**:

- No DevOps strategy or CI/CD approach
- No incident response plan
- No disaster recovery / business continuity plan

**Recommendations**:

1. **Medium**: Document high-level resilience approach for Alpha assessment (detailed operational docs can wait for Beta)
   - Timeline: 2 weeks
   - Owner: Technical Architect
   - Evidence to create: Resilience approach document covering cloud architecture, failover strategy, and monitoring

2. **Medium**: Generate DevOps strategy using `/arckit:devops` during Alpha
   - Timeline: 3 weeks
   - Owner: DevOps Engineer
   - Evidence to create: ARC-001-DEVOPS-v1.0.md with CI/CD, IaC, and monitoring approach

**Assessment Day Guidance**:

- **Prepare**: Reliability requirements and high-level approach to resilience
- **Show**: NFR targets, monitoring dashboard design, API gateway rate limiting
- **Bring**: Technical Architect
- **Materials**: REQ NFRs, DIAG SLA table, resilience approach document
- **Likely Questions**:
  - "What happens when the platform goes down? How does it affect connected councils?"
  - "What's your uptime target and how will you achieve it?"

---

## Evidence Inventory

**Complete Traceability**: Service Standard Point → ArcKit Artifacts

| Service Standard Point | ArcKit Artifacts | Status | Critical Gaps |
|------------------------|------------------|--------|---------------|
| 1. Understand users | ARC-001-STKE-v1.0, ARC-001-REQ-v1.0, ARC-001-RSCH-v2.0 | 🟡 Amber | Primary user research, prototype testing with real users |
| 2. Solve whole problem | ARC-001-REQ-v1.0, ARC-001-STKE-v1.0, ARC-001-DIAG-001-v1.0, ARC-001-RSCH-v2.0, ARC-001-SOBC-v1.0 | 🟢 Green | None critical |
| 3. Joined up experience | ARC-001-DIAG-001-v1.0, ARC-001-REQ-v1.0, ARC-000-PRIN-v1.1 | 🟡 Amber | Channel strategy, assisted digital plan |
| 4. Simple to use | ARC-000-PRIN-v1.1, ARC-001-REQ-v1.0, ARC-001-DIAG-001-v1.0 | 🟡 Amber | Prototype usability testing, task completion rates |
| 5. Everyone can use | ARC-001-REQ-v1.0, ARC-000-PRIN-v1.1, ARC-001-STKE-v1.0 | 🟡 Amber | Assistive technology testing plan, accessibility specialist |
| 6. Multidisciplinary team | ARC-001-PLAN-v1.0, ARC-001-STKE-v1.0, ARC-001-SOBC-v1.0, ARC-001-RSCH-v2.0 | 🟢 Green | None critical |
| 7. Agile ways of working | ARC-001-PLAN-v1.0, ARC-001-SOBC-v1.0, ARC-001-RISK-v1.0 | 🟢 Green | None critical |
| 8. Iterate frequently | ARC-001-RSCH-v2.0, ARC-001-DIAG-001-v1.0, ARC-001-PLAN-v1.0 | 🟡 Amber | Learning log, prototype iteration evidence |
| 9. Secure and private | ARC-001-RISK-v1.0, ARC-000-PRIN-v1.1, ARC-001-REQ-v1.0, ARC-001-DIAG-001-v1.0, ARC-001-RSCH-v2.0 | 🟡 Amber | Secure by Design (SECD), DPIA |
| 10. Success metrics | ARC-001-SOBC-v1.0, ARC-001-REQ-v1.0, ARC-001-PLAN-v1.0, ARC-001-STKE-v1.0 | 🟡 Amber | GDS KPI collection plan, baseline measurements |
| 11. Right tools | ARC-001-DIAG-001-v1.0, ARC-001-RSCH-v2.0, ARC-000-PRIN-v1.1, ARC-001-SOBC-v1.0, ARC-001-REQ-v1.0 | 🟢 Green | None critical |
| 12. Open source | ARC-000-PRIN-v1.1, ARC-001-DIAG-001-v1.0 | 🟡 Amber | Open source policy, code repository approach |
| 13. Open standards | ARC-001-DIAG-001-v1.0, ARC-000-PRIN-v1.1, ARC-001-REQ-v1.0, ARC-001-RSCH-v2.0 | 🟢 Green | None critical |
| 14. Reliable service | ARC-001-REQ-v1.0, ARC-001-DIAG-001-v1.0, ARC-001-RISK-v1.0 | 🟡 Amber | DevOps strategy, incident response plan |

**Summary**:

- ✅ Strong evidence: Points 2 (whole problem), 6 (team), 7 (agile), 11 (technology), 13 (open standards)
- ⚠️ Adequate but needs strengthening: Points 1 (users), 3 (channels), 4 (simplicity), 5 (accessibility), 8 (iteration), 10 (metrics), 12 (open source), 14 (reliability)
- ❌ Critical gaps requiring specific artifacts: Point 9 (SECD + DPIA missing)

---

## Assessment Preparation Checklist

### Critical Actions (Complete within 2 weeks)

Priority: Complete these before booking assessment — they address the most significant gaps

- [ ] **Generate Secure by Design assessment**: Run `/arckit:secure` to produce ARC-001-SECD-v1.0.md with threat model and security controls
  - Point: 9 (Secure service)
  - Timeline: 5 days
  - Owner: Security Architect
  - Outcome: Formal threat model with NCSC-aligned controls mapped to data sharing risks

- [ ] **Generate Data Protection Impact Assessment**: Run `/arckit:dpia` to produce ARC-001-DPIA-v1.0.md with data flows, lawful basis, and ICO consultation plan
  - Point: 9 (Secure service)
  - Timeline: 5 days
  - Owner: Data Protection Officer
  - Outcome: UK GDPR Article 35 DPIA covering cross-service citizen PII processing

- [ ] **Define open source code policy**: Document license choice, GitHub organisation, contribution model, and secret scanning
  - Point: 12 (Open source)
  - Timeline: 3 days
  - Owner: Technical Architect
  - Outcome: Open source policy statement ready for assessment presentation

### High Priority Actions (Complete within 4 weeks)

Priority: Should complete to strengthen Amber points to Green

- [ ] **Conduct primary user research**: Research with citizens, council officers, and council IT teams during Alpha Discovery
  - Point: 1 (Understand users)
  - Timeline: 4-6 weeks
  - Owner: Lead User Researcher
  - Outcome: User research findings, personas, and journey maps

- [ ] **Create channel strategy**: Document all access methods (digital, phone, paper, face-to-face) with assisted digital approach
  - Point: 3 (Joined up experience)
  - Timeline: 2 weeks
  - Owner: Service Designer
  - Outcome: Channel strategy document with user volumes and accessibility considerations

- [ ] **Define GDS KPI measurement plan**: Specify how cost per transaction, user satisfaction, completion rate, and digital take-up will be collected
  - Point: 10 (Success metrics)
  - Timeline: 2 weeks
  - Owner: Performance Analyst
  - Outcome: KPI measurement plan with data sources and collection frequency

- [ ] **Establish learning log**: Set up structured learning log from Alpha Sprint 1
  - Point: 8 (Iterate frequently)
  - Timeline: 1 day setup, ongoing
  - Owner: Delivery Manager
  - Outcome: Dated learning log showing insights, pivots, and actions

- [ ] **Recruit accessibility specialist**: Ensure accessibility expertise available within or supporting the team
  - Point: 5 (Everyone can use)
  - Timeline: 4 weeks
  - Owner: Delivery Manager
  - Outcome: Accessibility specialist role filled or contracted

- [ ] **Generate Architecture Decision Records**: Run `/arckit:adr` for 4 key technology decisions from diagram
  - Point: 11 (Right tools)
  - Timeline: 2 weeks
  - Owner: Technical Architect
  - Outcome: ARC-001-ADR-001 through ARC-001-ADR-004

### Medium Priority Actions (Nice to Have)

Priority: Strengthens overall case but not blocking

- [ ] **Create user personas**: Develop 4-6 detailed user personas with accessibility needs and digital confidence levels
  - Point: 1 (Understand users)
  - Timeline: 2 weeks
  - Owner: Lead User Researcher + Content Designer
  - Outcome: User persona documents

- [ ] **Create standalone user journey maps**: Map end-to-end journeys for citizen, council officer, and council IT team
  - Point: 2 (Whole problem)
  - Timeline: 2 weeks
  - Owner: Service Designer
  - Outcome: 3 user journey maps

- [ ] **Define task completion rate targets**: Set specific measurable usability targets for key tasks
  - Point: 4 (Simple to use)
  - Timeline: 1 week
  - Owner: Product Manager
  - Outcome: Updated NFRs with usability targets

- [ ] **Document high-level resilience approach**: Cloud architecture, failover strategy, monitoring for Alpha presentation
  - Point: 14 (Reliable service)
  - Timeline: 2 weeks
  - Owner: Technical Architect
  - Outcome: Resilience approach document

- [ ] **Generate DevOps strategy**: Run `/arckit:devops` for CI/CD, infrastructure as code, and monitoring
  - Point: 14 (Reliable service)
  - Timeline: 3 weeks
  - Owner: DevOps Engineer
  - Outcome: ARC-001-DEVOPS-v1.0.md

---

## Assessment Day Preparation

### Timeline and Booking

**Current Readiness**:
The programme is not yet ready to book an Alpha assessment. The most critical gaps (SECD, DPIA, primary user research, prototype testing) must be addressed during the Alpha phase. The documentation foundation is strong, but Alpha assessment requires evidence of actual prototyping and user testing.

**Recommended Booking Timeline**:

- Complete critical actions (SECD, DPIA, open source policy): 2 weeks
- Complete high priority actions (user research, channel strategy, KPIs): 4-6 weeks
- Prototype testing and iteration evidence: 6-8 weeks into Alpha
- Buffer for preparation: 1 week
- **Ready to book after**: Alpha week 20 (approximately September 2026)

**How to Book**:

1. Contact GDS Central Digital & Data Office assessment team
2. Book 5 weeks in advance minimum
3. Assessments typically on Tuesday, Wednesday, or Thursday
4. Duration: 4 hours
5. Provide: Service name (GDS Local), department (DSIT), phase (Alpha), preferred dates

### Documentation to Share with Panel

**Send 1 week before assessment**:

Required documentation:

- [ ] Project overview (1-2 pages) — extract from ARC-001-PLAN-v1.0 executive summary
- [ ] User research repository or summary — from primary user research findings
- [ ] Service architecture diagrams — ARC-001-DIAG-001-v1.0 system context diagram
- [ ] Prototype/demo environment URL

Recommended documentation:

- [ ] Key ArcKit artifacts:
  - ARC-001-STKE-v1.0 — Stakeholder analysis and user needs
  - ARC-001-REQ-v1.0 — Requirements and user stories
  - ARC-000-PRIN-v1.1 — Architecture principles
  - ARC-001-RISK-v1.0 — Risk register
  - ARC-001-SECD-v1.0 — Secure by Design assessment (when created)
  - ARC-001-DPIA-v1.0 — Data Protection Impact Assessment (when created)

Optional supplementary:

- [ ] ARC-001-RSCH-v2.0 — Business research context
- [ ] ARC-001-SOBC-v1.0 — Business case and benefits model
- [ ] ARC-001-PLAN-v1.0 — Project plan with team structure
- [ ] Research findings (videos, playback slides)

### Who Should Attend

**Core Team** (required):

- ✅ **Service Owner (Liz Adams)** — Overall service vision, programme strategy, decision-making authority
- ✅ **Lead User Researcher** — User needs, research findings, prototype testing results
- ✅ **Technical Architect** — Technology choices, architecture decisions, security approach
- ✅ **Delivery Manager** — Agile practices, team dynamics, iteration approach

**Phase-Specific Additions (Alpha)**:

- ✅ **Lead Designer** — Prototype design, user interface, GOV.UK Design System usage
- ✅ **Business Analyst** — Requirements, user stories, stakeholder analysis

**Optional Attendees**:

- Senior Responsible Owner (Programme Director — for context, may not attend full session)
- Local Government Champion (Theo Blackwell — if available, demonstrates partnership model)
- Data Protection Officer (given data sharing focus)

### Show and Tell Structure

**4-Hour Assessment Timeline**:

**0:00-0:15 — Introductions and Context**

- Team introductions (name, role, experience)
- GDS Local overview: extending GDS platforms to 333 local authorities (2 minutes)
- Programme context: fiscal crisis, digital maturity gap, policy drivers

**0:15-1:00 — User Research and Needs (Points 1, 2, 3, 4)**

- Lead User Researcher presents:
  - Primary research methodology and findings
  - User groups: citizens (56M), council officers, council IT teams
  - Evidence from 300+ local government professionals and OneLogin discovery
  - Prototype testing results and design iterations
- Show: User personas, journey maps, research playback highlights

**1:00-1:45 — Service Demonstration (Points 2, 3, 4, 5)**

- Lead Designer presents:
  - End-to-end prototype walkthrough: citizen authentication → council service access → data sharing
  - Council onboarding journey: self-service portal for IT teams
  - GOV.UK Design System usage and accessibility features
  - Multi-channel approach: digital, GOV.UK Notify (email/SMS/letters)
- Show: Working prototype with realistic test data

**1:45-2:30 — Technical Architecture and Security (Points 9, 11, 12, 13, 14)**

- Technical Architect presents:
  - C4 System Context diagram and integration architecture
  - Technology choices: OIDC, REST, OAuth 2.0 (all open standards)
  - GOV.UK platform reuse: OneLogin, Notify, Pay
  - Security: threat model, purpose-limited data sharing, ICO engagement
  - Open source approach and repository plans
- Show: Architecture diagram, technology decision rationale, SECD assessment

**2:30-3:00 — Team and Ways of Working (Points 6, 7, 8, 10)**

- Delivery Manager presents:
  - Team composition: 30 FTE, multidisciplinary, named leadership
  - Agile practices: 2-week sprints, GDS Delivery phases, governance gates
  - Iteration evidence: learning log, research pivot (v1.0 → v2.0)
  - Success metrics: BCR 2.8:1, 50 councils target, GDS KPIs
- Show: Sprint board, retrospective outputs, learning log

**3:00-3:45 — Open Q&A**

- Panel asks questions across all 14 Service Standard points
- Team responds with evidence and examples from ArcKit artifacts
- Opportunity to address panel concerns on data sharing privacy, council adoption, and platform reliability

**3:45-4:00 — Panel Deliberation**

- Team steps out
- Panel discusses and decides on RAG ratings per point
- Panel may call team back for clarifications

### Tips for Success

**Do**:

- ✅ Show real work, not polished presentations (max 10 slides if any)
- ✅ Have people who did the work present it — User Researcher presents research, not the Service Owner
- ✅ Be honest about what you don't know yet — Alpha is about learning
- ✅ Explain your problem-solving approach, especially around data sharing privacy
- ✅ Demonstrate iteration based on learning — show the RSCH v1.0 → v2.0 pivot
- ✅ Show enthusiasm for user needs and the GDS Local mission
- ✅ Provide evidence for claims — reference ArcKit artifacts by document ID
- ✅ Emphasise the voluntary adoption model and co-design approach

**Don't**:

- ❌ Over-prepare presentations — panel wants to see artifacts, not decks
- ❌ Hide the OneLogin timeline risk or the challenge of 333 autonomous councils
- ❌ Use jargon or assume panel knows local government context
- ❌ Let senior leaders (Service Owner, Programme Director) dominate — panel wants to hear from doers
- ❌ Argue with panel feedback — take it as learning for Beta
- ❌ Rush through the data sharing privacy model — this will be scrutinised

**Materials to Have Ready**:

- Prototype or working service with test data loaded (citizen journey, council onboarding)
- Laptops for team members to show their work
- Backup plan if demo breaks (screenshots, prototype recording)
- Links to ArcKit artifacts (docs site if deployed via `/arckit:pages`)
- User research videos or clips (if appropriate and participants consented)
- Architecture diagrams printed large or on screen (system context, data flow)

---

## After the Assessment

### If You Pass (Green)

**Immediate Actions**:

- [ ] Celebrate with the team
- [ ] Share assessment report with stakeholders (DSIT, MHCLG, LGA)
- [ ] Plan for Beta phase (weeks 33-68 per ARC-001-PLAN-v1.0)
- [ ] Book Beta assessment (target: Beta week 20, approximately Q2 2027)
- [ ] Begin pathfinder council onboarding (5 councils in Phase 1)

**Continuous Improvement**:

- [ ] Act on any panel feedback and recommendations
- [ ] Continue user research with pathfinder councils
- [ ] Update ArcKit artifacts as service evolves
- [ ] Generate outstanding artifacts: DEVOPS, TRAC, TCOP, HLDR, DLDR

### If You Get Amber

**Understanding Amber**:

- Service can proceed to Beta phase
- Must fix amber issues within 3 months
- Progress tracked in "tracking amber evidence" document
- GDS assessment team will monitor progress

**Immediate Actions**:

- [ ] Create "tracking amber evidence" document listing each amber point and required actions
- [ ] Assign owners to each amber point from the team
- [ ] Set deadlines for addressing amber issues (within 3 months — by December 2026)
- [ ] Schedule regular check-ins with GDS assessment team (fortnightly)

**Tracking Amber Evidence**:

Create a public document (visible to assessment team) showing:

- Each amber point and the specific concern raised by panel
- Actions taken to address the concern
- Evidence created (with links/dates)
- Status (not started, in progress, complete)
- Next assessment milestone

### If You Fail (Red)

**Understanding Red**:

- Service cannot proceed to Beta phase
- Must address red issues before reassessment
- Team remains in Alpha phase
- Requires another full Alpha assessment

**Immediate Actions**:

- [ ] Review assessment report carefully with team and Programme Director
- [ ] Identify root causes of red ratings — are they evidence gaps or fundamental approach issues?
- [ ] Create action plan to address each red point with specific artifacts and activities
- [ ] Re-run `/arckit:service-assessment PHASE=alpha` weekly to track progress against checklist
- [ ] Book reassessment once red issues resolved (typically 3-6 months — Q1 2027)

---

## Next Steps

### This Week

**Immediate actions** (within 7 days):

1. Run `/arckit:secure` to generate Secure by Design assessment (SECD) — most critical gap
2. Run `/arckit:dpia` to generate Data Protection Impact Assessment — legally required
3. Draft open source code policy (license, repository, contribution model)

**Quick wins** (can complete in 1-2 days):

- Establish learning log template and create first entry
- Define GDS KPI collection approach (1-page outline)

### Next 2 Weeks

**Priority actions** (complete before booking):

1. Complete SECD and DPIA generation and review
2. Begin primary user research planning for Alpha
3. Create channel strategy document
4. Set up code repository with README, LICENSE, and CONTRIBUTING.md

### Next 4 Weeks

**Strengthening actions** (improve Amber to Green):

1. Conduct first round of primary user research (weeks 1-4 of Alpha)
2. Create user personas from research findings
3. Generate Architecture Decision Records using `/arckit:adr`
4. Begin prototype development for usability testing
5. Recruit or contract accessibility specialist

### Continuous Improvement

**Weekly**:

- [ ] Re-run `/arckit:service-assessment PHASE=alpha` to track progress against this checklist
- [ ] Update this report as evidence is gathered (mark checklist items complete)
- [ ] Review sprint backlog includes Service Standard prep tasks
- [ ] Learning log updated with insights from the week

**Fortnightly**:

- [ ] Team review of assessment readiness (15-minute standup)
- [ ] Practice show-and-tell with colleagues or stakeholders
- [ ] Gather feedback on presentation approach from GDS colleagues

**Before Booking**:

- [ ] All critical actions complete (SECD, DPIA, open source policy)
- [ ] Primary user research conducted with at least 3 user groups
- [ ] Prototype tested with real users (at least 5 per user group)
- [ ] At least 12/14 points rated Green or Amber
- [ ] Team confident and prepared
- [ ] Documentation ready to share with panel
- [ ] Demo environment tested and working

---

## Resources

### GDS Service Standard Resources

**Official Guidance**:

- [Service Standard](https://www.gov.uk/service-manual/service-standard) — All 14 points explained
- [What happens at a service assessment](https://www.gov.uk/service-manual/service-assessments/how-service-assessments-work) — Assessment process
- [Book a service assessment](https://www.gov.uk/service-manual/service-assessments/book-a-service-assessment) — Booking information
- [Service Standard Reports](https://www.gov.uk/service-standard-reports) — Browse 450+ published assessment reports

**Phase-Specific Guidance**:

- [Alpha phase](https://www.gov.uk/service-manual/agile-delivery/how-the-alpha-phase-works) — What to do in alpha
- [Beta phase](https://www.gov.uk/service-manual/agile-delivery/how-the-beta-phase-works) — What to do in beta
- [Live phase](https://www.gov.uk/service-manual/agile-delivery/how-the-live-phase-works) — What to do when live

**Deep Dives by Service Standard Point**:

- [Point 1: Understand users](https://www.gov.uk/service-manual/service-standard/point-1-understand-user-needs)
- [Point 2: Solve a whole problem](https://www.gov.uk/service-manual/service-standard/point-2-solve-a-whole-problem)
- [Point 3: Joined up experience](https://www.gov.uk/service-manual/service-standard/point-3-join-up-across-channels)
- [Point 4: Simple to use](https://www.gov.uk/service-manual/service-standard/point-4-make-the-service-simple-to-use)
- [Point 5: Everyone can use](https://www.gov.uk/service-manual/service-standard/point-5-make-sure-everyone-can-use-the-service)
- [Point 6: Multidisciplinary team](https://www.gov.uk/service-manual/service-standard/point-6-have-a-multidisciplinary-team)
- [Point 7: Agile ways of working](https://www.gov.uk/service-manual/service-standard/point-7-use-agile-ways-of-working)
- [Point 8: Iterate frequently](https://www.gov.uk/service-manual/service-standard/point-8-iterate-and-improve-frequently)
- [Point 9: Secure and private](https://www.gov.uk/service-manual/service-standard/point-9-create-a-secure-service)
- [Point 10: Success metrics](https://www.gov.uk/service-manual/service-standard/point-10-define-success-publish-performance-data)
- [Point 11: Right tools](https://www.gov.uk/service-manual/service-standard/point-11-choose-the-right-tools-and-technology)
- [Point 12: Open source](https://www.gov.uk/service-manual/service-standard/point-12-make-new-source-code-open)
- [Point 13: Open standards](https://www.gov.uk/service-manual/service-standard/point-13-use-common-components-and-patterns)
- [Point 14: Reliable service](https://www.gov.uk/service-manual/service-standard/point-14-operate-a-reliable-service)

### Related ArcKit Commands

**Complementary Analysis**:

- `/arckit:analyze` — Comprehensive governance quality analysis across all artifacts
- `/arckit:traceability` — Requirements traceability matrix showing evidence chains

**Overlap with TCoP**:

- `/arckit:tcop` — Technology Code of Practice assessment (points 11, 13 overlap with Service Standard)

**Generate Missing Evidence**:

- `/arckit:secure` — Generate Secure by Design assessment (Point 9 — **critical gap**)
- `/arckit:dpia` — Generate Data Protection Impact Assessment (Point 9 — **critical gap**)
- `/arckit:adr` — Generate Architecture Decision Records (Point 11 — strengthens case)
- `/arckit:devops` — Generate DevOps strategy (Point 14 — strengthens case)
- `/arckit:diagram` — Generate additional architecture diagrams (container, component levels)
- `/arckit:hld-review` — Review High-Level Design when HLD is available
- `/arckit:traceability` — Generate traceability matrix linking all evidence

### Community Resources

**Blog Posts and Lessons Learned**:

- [Preparing for a GDS assessment](https://www.iterate.org.uk/10-things-to-remember-when-preparing-for-a-service-standard-assessment/)
- [What I learned as a user researcher](https://dwpdigital.blog.gov.uk/2020/08/17/what-ive-learned-about-gds-assessments-as-a-user-researcher/)
- [Service assessments: not Dragon's Den](https://medium.com/deloitte-uk-design-blog/service-assessments-no-longer-dragons-den-909b56c43593)

**Supplier Support** (G-Cloud):

- Search Digital Marketplace for "GDS assessment preparation" support services
- Many suppliers offer assessment prep workshops and mock assessments

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| *None provided* | — | — | — | — |

---

**Generated by**: ArcKit `/arckit.service-assessment` command
**Generated on**: 2026-02-28
**ArcKit Version**: 2.15.1
**Project**: GDS Local (Project 001)
**Model**: Claude Opus 4.6

**Next Actions**:

1. Review this report with your team
2. Prioritize critical actions in sprint planning: `/arckit:secure` and `/arckit:dpia`
3. Re-run `/arckit:service-assessment PHASE=alpha` weekly to track progress
4. Use checklist to track completion of preparation tasks

---

*Good luck with your assessment! Show your work, explain your thinking, and be open to feedback.*
