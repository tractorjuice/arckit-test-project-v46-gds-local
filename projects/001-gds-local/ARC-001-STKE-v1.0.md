# Stakeholder Drivers & Goals Analysis: GDS Local

> **Template Status**: Live | **Version**: 2.4.5 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | GDS Local (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-02-16 |
| **Last Modified** | 2026-02-16 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-05-16 |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | GDS Local Programme Team, DSIT Leadership, MHCLG Digital, LGA, Local Authority Partners |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-16 | ArcKit AI | Initial creation from `/arckit:stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose
This document identifies the key stakeholders of the GDS Local programme, their underlying drivers (motivations, concerns, needs), how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. GDS Local is a unit within GDS/DSIT established to strengthen collaboration between central and local government through shared technology products, cross-service data sharing, and extending GDS platforms to local authorities.

### Key Findings
The programme operates at the intersection of central and local government, creating a complex stakeholder landscape with strong alignment on citizen outcomes but significant tensions around speed of delivery vs. local authority autonomy, data sharing ambition vs. privacy concerns, and standardisation vs. the diversity of 333 councils. The strongest driver across all stakeholders is **improving citizen outcomes through better joined-up services** — this shared purpose provides a foundation for resolving conflicts. The greatest risk is insufficient local authority engagement due to competing priorities and change fatigue.

### Critical Success Factors
- Local authority practitioner engagement from day one (co-design, not top-down)
- Early demonstrable value through pilot councils before scaling
- Robust data sharing governance that builds trust before enabling technology
- GOV.UK OneLogin integration that works alongside (not replaces) existing council identity systems
- Sustainable funding model that does not depend on individual council budgets

### Stakeholder Alignment Score
**Overall Alignment**: MEDIUM

Strong alignment on end goals (better citizen services) but significant tensions on approach (pace, autonomy, standardisation). The central-local government dynamic introduces inherent friction that must be actively managed through co-design and partnership rather than directive governance.

---

## Stakeholder Identification

### Internal Stakeholders (Central Government)

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| DSIT Secretary of State / Minister for AI & Digital | Ministerial accountability | HIGH | HIGH | Quarterly briefings, PQ preparation |
| GDS Director General | GDS strategic direction | HIGH | HIGH | Monthly steering, programme board |
| GDS Local Programme Director | Programme delivery lead | HIGH | HIGH | Weekly programme meetings |
| MHCLG Digital Director | Local government digital policy | HIGH | HIGH | Fortnightly co-design sessions |
| GDS Platform Teams (OneLogin, Notify, Pay) | Platform extension to local gov | MEDIUM | HIGH | Sprint-level integration planning |
| DSIT Finance | Programme budget and spend controls | HIGH | MEDIUM | Monthly budget reviews |
| Cabinet Office Spend Controls | Technology spend approval | HIGH | LOW | Major spend gate approvals |
| GDS Service Standard Assessors | Quality assurance | MEDIUM | MEDIUM | Service assessment gates |
| CDDO (Central Digital & Data Office) | Cross-government digital strategy | HIGH | MEDIUM | Quarterly strategy alignment |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|-------------|--------------|-----------|----------|
| Local Authority Chief Executives | 333 councils | Partners / adopters | HIGH | MEDIUM |
| Local Authority Digital/IT Directors | Council technology teams | Implementers / co-designers | MEDIUM | HIGH |
| Local Authority Service Managers | Housing, social care, planning etc. | End users of shared components | LOW | HIGH |
| Local Government Association (LGA) | Representative body | Convener, advocate | HIGH | HIGH |
| Society of IT Management (Socitm) | Professional body | Influencer, community | MEDIUM | HIGH |
| Citizens | Public | Beneficiaries | LOW | HIGH |
| Local Authority Frontline Staff | Council workers | Day-to-day users | LOW | HIGH |
| ICO (Information Commissioner) | Regulator | Data protection oversight | HIGH | MEDIUM |
| NAO (National Audit Office) | Auditor | Value for money scrutiny | HIGH | LOW |
| NCSC (National Cyber Security Centre) | Advisor | Security assurance | HIGH | MEDIUM |
| Technology Suppliers | Incumbent council system vendors | Commercial interest | MEDIUM | HIGH |
| Devolved Administrations | Scotland, Wales, NI | Potential future partners | LOW | LOW |

### Stakeholder Power-Interest Grid

```
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • Cabinet Office   │  • DSIT Minister    │
        │    Spend Controls   │  • GDS Director Gen │
        │  • NAO              │  • GDS Local Prog   │
        │  • DSIT Finance     │    Director         │
        │  • NCSC             │  • MHCLG Digital    │
 P      │  • ICO              │  • LGA              │
 O      │  • CDDO             │  • LA Chief Execs   │
 W      │                     │                     │
 E      ├─────────────────────┼─────────────────────┤
 R      │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
        │                     │                     │
   Low  │  • Devolved Admins  │  • LA Digital/IT    │
        │                     │    Directors        │
        │                     │  • LA Service Mgrs  │
        │                     │  • GDS Platform     │
        │                     │    Teams            │
        │                     │  • Citizens         │
        │                     │  • Socitm           │
        │                     │  • LA Frontline     │
        │                     │    Staff            │
        │                     │  • Tech Suppliers   │
        └─────────────────────┴─────────────────────┘
```

| Stakeholder | Power | Interest | Quadrant | Engagement Strategy |
|-------------|-------|----------|----------|---------------------|
| DSIT Minister | HIGH | HIGH | Manage Closely | Quarterly briefings, PQ support, progress dashboards |
| GDS Director General | HIGH | HIGH | Manage Closely | Monthly steering, programme board chair |
| GDS Local Programme Director | HIGH | HIGH | Manage Closely | Weekly programme delivery, daily standups |
| MHCLG Digital Director | HIGH | HIGH | Manage Closely | Fortnightly co-design, joint governance |
| LGA | HIGH | HIGH | Manage Closely | Strategic partnership, co-convening councils |
| LA Chief Executives | HIGH | MEDIUM | Manage Closely | Chief Executive briefings via LGA |
| CDDO | HIGH | MEDIUM | Keep Satisfied | Quarterly alignment, cross-gov strategy input |
| ICO | HIGH | MEDIUM | Keep Satisfied | DPIA reviews, data sharing framework approval |
| NCSC | HIGH | MEDIUM | Keep Satisfied | Security reviews at design gates |
| DSIT Finance | HIGH | MEDIUM | Keep Satisfied | Monthly budget reviews |
| Cabinet Office Spend Controls | HIGH | LOW | Keep Satisfied | Spend gate submissions |
| NAO | HIGH | LOW | Keep Satisfied | Annual audit preparation, VfM evidence |
| LA Digital/IT Directors | MEDIUM | HIGH | Keep Informed | Community of practice, co-design workshops |
| GDS Platform Teams | MEDIUM | HIGH | Keep Informed | Sprint planning, integration standups |
| Socitm | MEDIUM | HIGH | Keep Informed | Conference presentations, research partnerships |
| Technology Suppliers | MEDIUM | HIGH | Keep Informed | Market engagement, standards publication |
| LA Service Managers | LOW | HIGH | Keep Informed | User research sessions, demos, newsletters |
| Citizens | LOW | HIGH | Keep Informed | Usability testing, public beta, GOV.UK blog |
| LA Frontline Staff | LOW | HIGH | Keep Informed | Training, demos, feedback channels |
| Devolved Administrations | LOW | LOW | Monitor | Annual briefings, watching brief |

**Quadrant Interpretation:**
- **Manage Closely** (High Power, High Interest): Key decision-makers requiring active engagement and co-ownership
- **Keep Satisfied** (High Power, Low Interest): Influential stakeholders needing periodic updates and assurance
- **Keep Informed** (Low Power, High Interest): Engaged stakeholders needing regular communication and participation opportunities
- **Monitor** (Low Power, Low Interest): Minimal engagement required, watch for changes in interest

---

## Stakeholder Drivers Analysis

### SD-1: DSIT Minister — Demonstrable Digital Transformation

**Stakeholder**: Secretary of State for Science, Innovation and Technology / Minister for AI and Digital Government

**Driver Category**: STRATEGIC / POLITICAL

**Driver Statement**: Demonstrate visible progress on government digital transformation by extending proven GDS platforms to local government, enabling joined-up citizen services and responding positively to parliamentary scrutiny about the quality of local public services.

**Context & Background**:
GDS Local was announced in November 2025 as a strategic initiative under DSIT. Ministers face parliamentary questions about digital service quality in local government, council technology failures, and citizen frustration with fragmented government services. The programme must deliver visible, communicable progress that demonstrates government is actively improving local digital services.

**Driver Intensity**: CRITICAL

**Enablers**:
- Quick wins from extending existing GDS platforms (Notify, Pay) already proven at central level
- Strong narrative: "one login for all government services"
- LGA support providing political cover for central-local collaboration
- Cross-party appeal of improving local services

**Blockers**:
- Slow adoption if councils resist or lack capacity
- Data sharing controversy if privacy incidents occur
- Negative media coverage of "Whitehall telling councils what to do"
- Competing ministerial priorities and machinery of government changes

**Related Stakeholders**: GDS Director General (aligned), LA Chief Executives (potential tension on autonomy), NAO (scrutiny), MHCLG (co-delivery)

---

### SD-2: GDS Director General — Platform Economy Extension

**Stakeholder**: GDS Director General

**Driver Category**: STRATEGIC

**Driver Statement**: Extend the GDS platform model to local government, creating a "platform economy" where shared components (OneLogin, Notify, Pay, App) serve the entire public sector rather than just central government. This increases platform value, justifies continued investment, and positions GDS as the digital backbone of government.

**Context & Background**:
GDS has built successful platforms for central government but adoption plateaus without new markets. Local government represents 333 potential new "customers" for GDS platforms. Extending to local government strengthens the business case for continued platform investment and demonstrates GDS's relevance across the whole public sector.

**Driver Intensity**: HIGH

**Enablers**:
- Proven platforms with established APIs and documentation
- GOV.UK OneLogin already in development with cross-government ambition
- Cost savings for councils adopting shared platforms
- MHCLG partnership providing routes to local government

**Blockers**:
- GDS platform teams already stretched with central government commitments
- Local authority technical estates are diverse and complex
- Platforms designed for central government may not fit council use cases without adaptation
- Funding model unclear — who pays for local authority platform usage

**Related Stakeholders**: GDS Platform Teams (delivery), DSIT Finance (funding), LA Digital/IT Directors (adoption), Technology Suppliers (competitive displacement)

---

### SD-3: MHCLG Digital Director — Local Government Technology Modernisation

**Stakeholder**: MHCLG Director of Digital

**Driver Category**: STRATEGIC / OPERATIONAL

**Driver Statement**: Accelerate local government technology modernisation through shared products and standards, reducing the technology gap between the most and least digitally mature councils, and enabling better data-driven policy making in housing, planning, social care, and other MHCLG policy areas.

**Context & Background**:
MHCLG is the policy department for local government. It sees councils spending over £5 billion annually on technology with limited sharing, duplicated procurement, and significant variation in digital maturity. MHCLG needs better data flows from councils to inform policy (e.g., housing data, planning decisions, social care outcomes) but current fragmentation makes this difficult.

**Driver Intensity**: HIGH

**Enablers**:
- Existing MHCLG initiatives (planning data, housing standards) provide integration points
- LGA relationship provides convening power
- GDS Local partnership provides technology capability MHCLG lacks internally
- Council appetite for help with digital transformation

**Blockers**:
- Local authority autonomy — councils are independent bodies, not MHCLG subordinates
- 333 councils with different priorities, budgets, and political leadership
- Legacy system lock-in with incumbent suppliers
- Change fatigue in local government following COVID, funding pressures, and multiple central initiatives

**Related Stakeholders**: LGA (aligned but protective of council autonomy), LA Chief Executives (mixed reception), ICO (data flows require governance)

---

### SD-4: Local Authority Chief Executives — Improved Services Within Constraints

**Stakeholder**: Local Authority Chief Executives (collectively representing 333 councils)

**Driver Category**: OPERATIONAL / FINANCIAL / RISK

**Driver Statement**: Improve the quality and efficiency of local public services while managing severe budget pressures, workforce shortages, and growing demand. Any central initiative must reduce burden on councils, not add to it, and must respect local democratic accountability.

**Context & Background**:
Local authorities face a sustained funding crisis — real-terms budget reductions since 2010, growing demand (particularly in social care and housing), workforce recruitment challenges, and ageing technology infrastructure. Chief executives are pragmatic: they welcome help that genuinely reduces cost or improves services, but are wary of central government initiatives that create unfunded mandates, impose inappropriate standards, or fail to account for local context.

**Driver Intensity**: CRITICAL

**Enablers**:
- Free or low-cost access to shared platforms (GOV.UK Notify already free for councils)
- Reduced procurement cost through integrated purchasing
- Peer learning from digitally mature councils
- Central funding or capacity support for adoption

**Blockers**:
- Unfunded mandates — costs of adoption fall on already-stretched council budgets
- "One size fits all" approach that ignores council diversity (metropolitan vs. rural, large vs. small)
- Central government initiative fatigue
- Loss of local control over technology decisions
- Incumbent supplier contracts with years remaining

**Related Stakeholders**: DSIT Minister (tension on pace vs. autonomy), LGA (advocate for council interests), LA Digital/IT Directors (implementation capacity), DSIT Finance (funding model)

---

### SD-5: Local Authority Digital/IT Directors — Practical Technology That Works

**Stakeholder**: Local Authority Digital and IT Directors (via Socitm and direct engagement)

**Driver Category**: OPERATIONAL / PERSONAL

**Driver Statement**: Access proven, well-supported shared components that solve real technology problems (identity, notifications, payments), integrate with existing council systems without requiring wholesale replacement, and reduce the team's operational burden on commodity technology so they can focus on service-specific innovation.

**Context & Background**:
Council IT teams are typically small (10-50 staff for smaller councils) and manage diverse technology estates with limited specialist capability. They spend disproportionate time on commodity functions (email, identity, hosting) rather than service innovation. They want practical help but have been burned by central initiatives that under-deliver, over-promise, or create dependency on unsupported platforms.

**Driver Intensity**: HIGH

**Enablers**:
- Well-documented APIs and integration guides
- Sandbox environments for testing before commitment
- Migration support and onboarding assistance
- Community of practice for peer support
- Open source components they can inspect and understand

**Blockers**:
- Poor documentation or unclear integration paths
- Breaking API changes without migration support
- Inadequate support for council-specific use cases
- Platform availability that doesn't meet council SLA needs
- No clear exit strategy if shared components are discontinued

**Related Stakeholders**: GDS Platform Teams (delivery quality), Technology Suppliers (competitive/complementary), GDS Local Programme Director (partnership approach)

---

### SD-6: LGA — Representing and Protecting Council Interests

**Stakeholder**: Local Government Association

**Driver Category**: STRATEGIC / RISK

**Driver Statement**: Ensure GDS Local genuinely benefits local government through co-design and partnership rather than top-down imposition. Protect council autonomy and democratic accountability while enabling the benefits of collaboration. Position LGA as the essential bridge between central and local government on digital matters.

**Context & Background**:
The LGA represents all councils in England. It has a strategic interest in digital transformation but is constitutionally committed to protecting local authority autonomy. The LGA wants to be seen as a credible partner that shapes central initiatives rather than having them imposed. It has its own digital programmes and capabilities that could complement or compete with GDS Local.

**Driver Intensity**: HIGH

**Enablers**:
- Formal partnership role in GDS Local governance
- LGA convening power to bring councils to the table
- LGA digital programmes providing complementary capability
- Joint communications presenting a united central-local front

**Blockers**:
- Perception that LGA is rubber-stamping a central government agenda
- GDS moving too fast without adequate consultation
- Councils reporting negative experiences with GDS Local components
- LGA being sidelined in favour of direct GDS-council relationships

**Related Stakeholders**: LA Chief Executives (LGA constituency), MHCLG (policy partner), GDS Local Programme Director (delivery partner)

---

### SD-7: Citizens — Seamless, Accessible Public Services

**Stakeholder**: UK Citizens interacting with local government services

**Driver Category**: CUSTOMER

**Driver Statement**: Access local government services easily, quickly, and seamlessly without needing to understand the boundary between central and local government. Have confidence that personal data is handled safely when shared across services to improve outcomes.

**Context & Background**:
Citizens interact with local government for housing, planning, council tax, social care, waste, libraries, and dozens of other services. Currently, each council has its own website, login system, and user experience. Citizens moving between areas or interacting with both central and local services face fragmented experiences. Vulnerable citizens (those needing housing AND social care AND benefits) are most affected by service fragmentation.

**Driver Intensity**: CRITICAL

**Enablers**:
- Single sign-on across central and local government (OneLogin)
- Consistent service patterns using GOV.UK Design System
- Data sharing that prevents citizens repeating information
- Accessible services meeting WCAG 2.2 AA

**Blockers**:
- Poor adoption leaving patchy experience across councils
- Privacy concerns reducing trust in data sharing
- Digital exclusion for citizens without internet access
- Complexity of local government services resisting simplification

**Related Stakeholders**: ICO (data protection), LA Service Managers (service delivery), GDS Local Programme Director (platform delivery)

---

### SD-8: ICO — Lawful and Transparent Data Sharing

**Stakeholder**: Information Commissioner's Office

**Driver Category**: COMPLIANCE / RISK

**Driver Statement**: Ensure cross-service data sharing enabled by GDS Local has a clear lawful basis under UK GDPR, is proportionate, transparent to citizens, and supported by robust Data Protection Impact Assessments. The ICO supports innovation in data sharing but requires proper governance.

**Context & Background**:
GDS Local's data access improvement priority directly involves sharing personal data across organisational boundaries (e.g., housing departments accessing health data). The ICO has regulatory enforcement powers including fines. Government data sharing has been controversial (e.g., care.data, National Pupil Database). The ICO wants to be a constructive enabler of responsible data sharing, not a blocker, but requires demonstrable compliance.

**Driver Intensity**: HIGH

**Enablers**:
- Early engagement with ICO regulatory sandbox for data sharing pilots
- Published data sharing codes of practice
- Privacy-by-design embedded in architecture
- DPIAs completed before data sharing begins
- Transparent citizen communication about data sharing

**Blockers**:
- Data sharing proceeding without adequate governance
- Scope creep — data collected for one purpose repurposed without consent
- Security incident involving cross-authority data
- Lack of transparency with citizens about how data is shared

**Related Stakeholders**: LA Chief Executives (data controllers), GDS Local Programme Director (architecture), NCSC (security controls)

---

### SD-9: NAO — Value for Money and Effective Delivery

**Stakeholder**: National Audit Office

**Driver Category**: COMPLIANCE / FINANCIAL

**Driver Statement**: GDS Local must demonstrate value for money, effective programme delivery, and measurable outcomes for citizens. The programme must avoid the pitfalls of previous government digital programmes that over-promised and under-delivered.

**Context & Background**:
The NAO regularly audits government digital programmes and has published critical reports on digital transformation, government platforms, and central-local government relationships. The NAO will assess whether GDS Local delivers its stated outcomes, whether spending is controlled, and whether lessons from previous programmes were learned.

**Driver Intensity**: MEDIUM

**Enablers**:
- Clear programme business case with measurable outcomes
- Benefits tracking from inception
- Regular programme reporting and transparency
- Learning from previous GDS programme audits

**Blockers**:
- Unclear or shifting programme scope
- Benefits that cannot be measured or attributed
- Cost overruns or uncontrolled spend
- Lack of adoption metrics showing real council usage

**Related Stakeholders**: DSIT Finance (budget controls), DSIT Minister (ministerial accountability), GDS Local Programme Director (delivery)

---

### SD-10: Technology Suppliers — Market Impact and Opportunity

**Stakeholder**: Incumbent local government technology suppliers (civica, Capita, NEC, Idox, and others)

**Driver Category**: FINANCIAL / RISK

**Driver Statement**: Understand the competitive implications of GDS Local shared components and position to either integrate with or complement them. Protect existing revenue from council contracts while identifying new opportunities in the GDS Local ecosystem.

**Context & Background**:
Local government technology is a multi-billion pound market served by established suppliers. GDS Local shared components (especially identity, notifications, payments) could displace elements of existing supplier offerings. Suppliers want clarity on GDS Local's scope to plan their strategy — compete, complement, or integrate. Some suppliers also see opportunity in providing the integration services councils will need.

**Driver Intensity**: HIGH

**Enablers**:
- Clear scope definition of what GDS Local will and will not provide
- Open APIs enabling integration with existing council systems
- Market engagement and standards consultation
- Opportunity to provide integration and migration services

**Blockers**:
- Ambiguous scope creating market uncertainty
- Closed or poorly documented APIs
- Aggressive displacement of existing solutions without transition support
- Lack of engagement with supplier community

**Related Stakeholders**: LA Digital/IT Directors (procurement decisions), GDS Local Programme Director (scope definition), Cabinet Office Spend Controls (procurement policy)

---

### SD-11: NCSC — Secure Cross-Government Architecture

**Stakeholder**: National Cyber Security Centre

**Driver Category**: COMPLIANCE / RISK

**Driver Statement**: Ensure GDS Local's shared components and cross-authority data sharing architecture meets NCSC security guidance, including Secure by Design principles, Cyber Assessment Framework, and zero-trust architecture patterns. Cross-authority integration must not create new attack surfaces or weaken the government's overall security posture.

**Context & Background**:
Extending GDS platforms to local government expands the attack surface. Local authorities have varying security maturity — some councils have experienced significant cyber incidents (e.g., Hackney, Redcar & Cleveland ransomware attacks). Shared components create shared risk: a compromise of a central component could affect all connected councils. NCSC wants to ensure the architecture strengthens rather than weakens the security picture.

**Driver Intensity**: HIGH

**Enablers**:
- Security architecture review at design stage
- Threat modelling for cross-authority integration patterns
- Shared security operations and incident response
- Security baseline requirements for participating councils

**Blockers**:
- Rapid delivery pressure bypassing security reviews
- Local authority security maturity gaps
- Shared components becoming single points of compromise
- Inadequate incident response coordination across authorities

**Related Stakeholders**: GDS Platform Teams (security implementation), LA Digital/IT Directors (local security), ICO (data breach notification)

---

## Driver-to-Goal Mapping

### Goal G-1: Extend GOV.UK OneLogin to 50 Local Authorities by Q4 2027

**Derived From Drivers**: SD-1 (Minister — visible progress), SD-2 (GDS DG — platform extension), SD-5 (LA IT Directors — practical identity), SD-7 (Citizens — single sign-on)

**Goal Owner**: GDS Local Programme Director

**Goal Statement**: Enable 50 local authorities representing at least 15 million citizens to offer GOV.UK OneLogin as an authentication option for council services by Q4 2027, with citizens able to access both central and local services using a single verified identity.

**Why This Matters**: OneLogin extension is the most visible deliverable of GDS Local. It directly addresses citizen frustration with multiple logins, provides ministerial "wins" for parliamentary questions, and demonstrates the GDS platform economy model. For councils, it removes the burden of managing bespoke identity systems.

**Success Metrics**:
- **Primary Metric**: Number of local authorities live with OneLogin integration
- **Secondary Metrics**:
  - Number of citizen authentications via OneLogin on council services per month
  - Citizen satisfaction with sign-on experience (GOV.UK survey)
  - Reduction in council identity management operational cost

**Baseline**: 0 councils using OneLogin (Feb 2026)

**Target**: 50 councils live by Q4 2027; 150 by Q4 2028

**Measurement Method**: OneLogin platform analytics (integrations live, authentication events); council adoption tracker; citizen satisfaction surveys

**Dependencies**:
- GOV.UK OneLogin platform readiness for local authority use cases
- Open standards-based federation (OIDC/SAML) confirmed
- Councils with services ready for integration
- Clear data processing agreements between GDS and councils

**Risks to Achievement**:
- OneLogin platform capacity constraints from central government demand
- Council services not technically ready for federation
- Citizen confusion during transition period
- Identity assurance levels not matching council service risk profiles

---

### Goal G-2: Establish Cross-Service Data Sharing Framework with 3 Pilot Use Cases by Q2 2027

**Derived From Drivers**: SD-3 (MHCLG — data-driven policy), SD-7 (Citizens — joined-up services), SD-8 (ICO — lawful sharing), SD-4 (LA Chief Execs — improved services)

**Goal Owner**: MHCLG Digital Director (jointly with GDS Local Programme Director)

**Goal Statement**: Design and implement a cross-service data sharing framework with ICO endorsement, and deliver 3 pilot use cases (housing-health, social care-benefits, planning-transport) across 10 participating councils by Q2 2027.

**Why This Matters**: Cross-service data sharing is GDS Local's highest-impact ambition but also its highest-risk. Early pilots with proper governance demonstrate that data sharing can be done safely and deliver citizen benefit. ICO endorsement provides legitimacy. Starting with 3 defined use cases avoids scope creep.

**Success Metrics**:
- **Primary Metric**: Number of pilot data sharing use cases operational with ICO endorsement
- **Secondary Metrics**:
  - Time saved per citizen interaction where data is pre-populated
  - Number of DPIAs completed and approved
  - Citizen trust survey results on cross-service data use
  - Volume of cross-service data queries processed

**Baseline**: No structured cross-service data sharing between central and local government (Feb 2026)

**Target**: 3 pilot use cases live across 10 councils by Q2 2027

**Measurement Method**: Data sharing platform analytics; DPIA completion tracker; citizen surveys; pilot council feedback; ICO formal assessment

**Dependencies**:
- ICO regulatory sandbox engagement
- Data Sharing Agreements signed between participating organisations
- Technical architecture for privacy-preserving data exchange
- Council systems capable of API-based data exchange
- Citizen consent mechanisms (where consent is the lawful basis)

**Risks to Achievement**:
- ICO concerns delaying or blocking specific use cases
- Privacy incident in pilot eroding citizen trust
- Council legal teams risk-averse on data sharing
- Technical complexity of integrating diverse council systems
- Political sensitivity of health-housing data sharing

---

### Goal G-3: Launch Shared Technology Component Catalogue with 5 Reusable Components by Q3 2027

**Derived From Drivers**: SD-2 (GDS DG — platform economy), SD-3 (MHCLG — modernisation), SD-5 (LA IT Directors — practical tools), SD-6 (LGA — co-designed solutions)

**Goal Owner**: GDS Local Programme Director

**Goal Statement**: Co-design and publish a catalogue of 5 shared technology components (in addition to existing GDS platforms) specifically addressing common local government needs, with at least 20 councils actively using at least one component by Q3 2027.

**Why This Matters**: Shared components reduce duplicated effort across 333 councils. Co-design with councils ensures components meet real needs. The component catalogue demonstrates the "build once, use many" principle that justifies the GDS Local investment.

**Success Metrics**:
- **Primary Metric**: Number of shared components published and in active use
- **Secondary Metrics**:
  - Number of councils actively using shared components
  - Estimated procurement savings across adopting councils
  - Component reliability (uptime, incident rate)
  - Developer satisfaction with component documentation and APIs

**Baseline**: 0 GDS Local-specific shared components (Feb 2026); existing GDS platforms (Notify, Pay) already available

**Target**: 5 new shared components; 20+ council adopters by Q3 2027

**Measurement Method**: Component catalogue platform; usage analytics per council; procurement savings calculator; developer survey; component health dashboards

**Dependencies**:
- Co-design process with diverse council representatives
- Funding for component development and long-term support
- Open source publication and contribution guidelines
- Integration testing across representative council technology estates

**Risks to Achievement**:
- Components not meeting diverse council needs
- Insufficient long-term funding for support and maintenance
- Low adoption due to integration complexity
- GDS platform teams lacking capacity for local government extensions

---

### Goal G-4: Establish Integrated Purchasing Framework Saving Councils £50M Over 3 Years

**Derived From Drivers**: SD-4 (LA Chief Execs — cost savings), SD-9 (NAO — value for money), SD-1 (Minister — transformation narrative), SD-10 (Suppliers — market clarity)

**Goal Owner**: LGA (jointly with GDS Local Programme Director)

**Goal Statement**: Establish an integrated purchasing framework for common local government technology needs, enabling collective procurement that saves participating councils a cumulative £50M over 3 years compared to individual procurement.

**Why This Matters**: Collective purchasing is one of the most tangible value propositions for councils. It addresses the financial driver head-on and demonstrates GDS Local's practical impact on council budgets. It also provides the NAO with clear, measurable value-for-money evidence.

**Success Metrics**:
- **Primary Metric**: Cumulative savings across participating councils (£)
- **Secondary Metrics**:
  - Number of councils using integrated purchasing
  - Procurement cycle time reduction
  - Supplier diversity in framework
  - Council satisfaction with procurement experience

**Baseline**: Councils procure individually; estimated average 20% price premium vs. collective purchase

**Target**: £50M cumulative savings over 3 years; 100+ councils participating

**Measurement Method**: Procurement savings calculator (before/after comparison); council finance reporting; Crown Commercial Service data; annual savings audit

**Dependencies**:
- LGA convening councils for demand aggregation
- Legal framework for collective procurement
- Crown Commercial Service alignment (G-Cloud, DOS)
- Supplier willingness to participate in framework
- Clear scope definition to avoid market distortion

**Risks to Achievement**:
- Insufficient council participation for volume discounts
- Supplier resistance to reduced margins
- Legal challenges to collective procurement approach
- Savings difficult to attribute (counterfactual problem)

---

### Goal G-5: Achieve GDS Service Standard Pass for All Public-Facing Components by Beta Stage

**Derived From Drivers**: SD-1 (Minister — quality assurance), SD-7 (Citizens — accessible services), SD-11 (NCSC — security), SD-8 (ICO — privacy)

**Goal Owner**: GDS Local Programme Director

**Goal Statement**: All public-facing GDS Local components and services must pass GDS Service Standard assessment at alpha and beta stages, with particular focus on Points 5 (accessibility), 9 (security/privacy), and 13 (open standards/common components).

**Why This Matters**: Service Standard compliance ensures quality, accessibility, and security. It also provides assurance to ministers, the NAO, and the public that GDS Local components meet the standard expected of government services.

**Success Metrics**:
- **Primary Metric**: Service assessment pass rate at each stage
- **Secondary Metrics**:
  - WCAG 2.2 AA compliance score
  - Security assessment completion rate
  - Number of open source repositories published
  - Performance metrics published on GOV.UK

**Baseline**: No GDS Local services yet assessed

**Target**: 100% pass rate at alpha and beta for all public-facing components

**Measurement Method**: GDS service assessment records; accessibility audit results; NCSC security review outcomes; GOV.UK performance platform

**Dependencies**:
- GDS assessment team capacity for GDS Local assessments
- Accessibility expertise within the programme
- NCSC engagement for security assessments
- Service Standard adapted/interpreted for shared component context

**Risks to Achievement**:
- Assessment bottleneck due to capacity constraints
- Accessibility gaps requiring rework
- Security findings requiring architectural changes
- Shared components may not map neatly to standard service assessment model

---

### Goal G-6: Build Community of Practice with Active Participation from 100+ Councils by Q4 2026

**Derived From Drivers**: SD-3 (MHCLG — share learning), SD-5 (LA IT Directors — peer support), SD-6 (LGA — convening), SD-4 (LA Chief Execs — practical help)

**Goal Owner**: LGA (jointly with GDS Local Programme Director)

**Goal Statement**: Establish and sustain a GDS Local community of practice with active participation from 100+ councils, enabling peer learning, innovation sharing, and co-design of shared components.

**Why This Matters**: GDS Local's success depends on local authority engagement. A thriving community creates the feedback loops, co-design input, and adoption momentum that the programme needs. It also scales learning and innovation beyond what the central programme team can deliver directly.

**Success Metrics**:
- **Primary Metric**: Number of councils with at least one active participant
- **Secondary Metrics**:
  - Community event attendance
  - Contributions to shared components (issues, PRs, feedback)
  - Peer-to-peer mentoring partnerships
  - Case studies published

**Baseline**: GDS Local announced Nov 2025; early interest registration via email

**Target**: 100+ active council participants by Q4 2026; 200+ by Q4 2027

**Measurement Method**: Community platform membership and activity analytics; event attendance records; contribution metrics; quarterly community survey

**Dependencies**:
- Community platform stood up (likely cross-government Slack + forum)
- LGA convening first cohort through existing networks
- Dedicated community management resource
- Incentives for council participation (funded time, recognition)

**Risks to Achievement**:
- Council staff too busy to participate alongside day jobs
- Community becomes "broadcast" channel not genuine collaboration
- Participation skewed to large/digitally mature councils
- Community management under-resourced

---

## Goal-to-Outcome Mapping

### Outcome O-1: Citizens Can Access Central and Local Services with a Single Login

**Supported Goals**: G-1 (OneLogin extension), G-5 (Service Standard compliance)

**Outcome Statement**: Citizens in participating council areas can authenticate once using GOV.UK OneLogin and access both central government services (tax, benefits, driving) and local council services (council tax, housing, planning) without creating separate accounts.

**Measurement Details**:
- **KPI**: Percentage of citizen digital interactions using single sign-on
- **Current Value**: 0% (separate logins for each council and central service)
- **Target Value**: 40% of digital interactions in participating councils via OneLogin by Q4 2028
- **Measurement Frequency**: Monthly
- **Data Source**: GOV.UK OneLogin analytics; participating council service analytics
- **Report Owner**: GDS Platform Team (OneLogin)

**Business Value**:
- **Financial Impact**: Estimated £2-5 per citizen interaction saved through reduced account management overhead
- **Strategic Impact**: Foundational capability for joined-up government services
- **Operational Impact**: Councils no longer managing bespoke identity infrastructure
- **Customer Impact**: Reduced friction; estimated 15% reduction in service abandonment at login

**Timeline**:
- **Phase 1 (Q1-Q2 2026)**: Technical integration patterns developed, 5 pilot councils onboarded
- **Phase 2 (Q3-Q4 2026)**: 20 councils live with OneLogin option
- **Phase 3 (2027)**: 50+ councils live; citizen awareness campaign
- **Sustainment (2028+)**: OneLogin becomes default authentication for council digital services

**Stakeholder Benefits**:
- **Citizens**: One account for all government services
- **LA IT Directors**: Reduced identity management burden
- **DSIT Minister**: Visible citizen-facing improvement
- **GDS DG**: Platform economy validated

**Leading Indicators** (early signals of success):
- Number of councils completing technical integration
- Citizen login success rate on first attempt
- Council IT team satisfaction with integration experience

**Lagging Indicators** (final proof of success):
- Citizen satisfaction with sign-on experience
- Reduction in council identity management costs
- Sustained monthly active users via OneLogin on council services

---

### Outcome O-2: Vulnerable Citizens Receive Better Joined-Up Support Through Safe Data Sharing

**Supported Goals**: G-2 (Data sharing framework), G-5 (Service Standard — privacy)

**Outcome Statement**: Vulnerable citizens (e.g., those in temporary housing needing health support, or elderly residents needing social care and benefits) receive faster, more appropriate support because frontline workers can access relevant information across services with proper governance, reducing the need for citizens to repeat their story.

**Measurement Details**:
- **KPI**: Reduction in time to coordinate multi-service support for vulnerable citizens
- **Current Value**: Average 15 working days to coordinate housing-health-social care support (estimated from pilot councils)
- **Target Value**: Average 5 working days by Q4 2027 in pilot councils
- **Measurement Frequency**: Quarterly
- **Data Source**: Pilot council case management systems; citizen experience surveys
- **Report Owner**: MHCLG Digital Director

**Business Value**:
- **Financial Impact**: Estimated £500-1,000 per case saved through reduced duplication and faster resolution
- **Strategic Impact**: Demonstrates cross-government data sharing can work safely
- **Operational Impact**: Frontline workers spend less time chasing information, more time supporting citizens
- **Customer Impact**: Vulnerable citizens receive support faster; reduced "falling through the cracks"

**Timeline**:
- **Phase 1 (Q1-Q2 2026)**: Data sharing framework designed; ICO sandbox engagement
- **Phase 2 (Q3 2026-Q1 2027)**: 3 pilot use cases live in 10 councils
- **Phase 3 (Q2-Q4 2027)**: Evaluation, refinement, scaling to 50+ councils
- **Sustainment (2028+)**: Standard data sharing patterns available as reusable components

**Stakeholder Benefits**:
- **Citizens**: Faster support, less repetition of personal information
- **LA Service Managers**: Better information for decisions, reduced administrative burden
- **MHCLG**: Data-driven policy insights from cross-service data
- **ICO**: Demonstrable model of responsible data sharing

**Leading Indicators**:
- DPIAs completed and approved for pilot use cases
- Number of cross-service data queries processed per week
- Frontline worker satisfaction with data access

**Lagging Indicators**:
- Reduction in multi-service coordination time
- Citizen satisfaction with joined-up support
- Zero data protection breaches in pilot sharing arrangements

---

### Outcome O-3: Councils Save Time and Money Through Shared Components and Integrated Purchasing

**Supported Goals**: G-3 (Shared components), G-4 (Integrated purchasing)

**Outcome Statement**: Participating councils demonstrably save money through integrated purchasing and reduce development effort through shared component adoption, freeing resources for service-specific innovation rather than commodity technology.

**Measurement Details**:
- **KPI**: Cumulative savings (procurement + development effort)
- **Current Value**: Baseline individual procurement costs (to be established in Q1 2026)
- **Target Value**: £50M cumulative savings over 3 years
- **Measurement Frequency**: Quarterly
- **Data Source**: Procurement savings tracker; council time/cost reporting; component usage analytics
- **Report Owner**: LGA (procurement savings); GDS Local Programme Director (component adoption)

**Business Value**:
- **Financial Impact**: £50M cumulative savings across participating councils
- **Strategic Impact**: Proven model for public sector technology collaboration
- **Operational Impact**: Council IT teams redirect from commodity to service innovation
- **Customer Impact**: Faster service improvements as councils have more capacity for innovation

**Timeline**:
- **Phase 1 (2026)**: First shared components available; integrated purchasing framework launched
- **Phase 2 (2027)**: 100+ councils participating; measurable savings reported
- **Phase 3 (2028)**: Full-year savings data; model refinement; expanded component catalogue
- **Sustainment (2029+)**: Self-sustaining model with community contributions

**Stakeholder Benefits**:
- **LA Chief Executives**: Budget relief, improved efficiency
- **NAO**: Clear value-for-money evidence
- **DSIT Minister**: "Saving councils £X through digital collaboration" narrative
- **Technology Suppliers**: New market opportunities in integration and specialised services

**Leading Indicators**:
- Number of councils registered for integrated purchasing
- Shared component downloads/integrations per month
- Developer engagement metrics (API calls, sandbox usage)

**Lagging Indicators**:
- Independently verified procurement savings
- Council technology budget reallocation (from commodity to innovation)
- Council satisfaction with shared components (annual survey)

---

### Outcome O-4: Unified Standards Improve Consistency Without Reducing Local Autonomy

**Supported Goals**: G-5 (Service Standard), G-6 (Community of practice), G-3 (Shared components)

**Outcome Statement**: The digital experience of interacting with local government becomes more consistent across councils through voluntary adoption of unified standards and shared patterns, while councils retain autonomy to tailor services to local needs.

**Measurement Details**:
- **KPI**: Percentage of participating councils using GOV.UK Design System and shared patterns
- **Current Value**: Estimated <10% of councils use GOV.UK Design System
- **Target Value**: 50% of participating councils using shared patterns by Q4 2028
- **Measurement Frequency**: Biannually
- **Data Source**: Community of practice survey; automated design system usage detection; council digital service audits
- **Report Owner**: GDS Local Programme Director

**Business Value**:
- **Financial Impact**: Reduced design/development costs through pattern reuse
- **Strategic Impact**: Consistent government digital experience across tiers
- **Operational Impact**: Faster service delivery using proven patterns
- **Customer Impact**: Citizens experience familiar, tested interaction patterns across councils

**Timeline**:
- **Phase 1 (2026)**: Standards published; community feedback collected; early adopters
- **Phase 2 (2027)**: Adoption grows through community of practice and shared component usage
- **Phase 3 (2028)**: Standards refined based on adoption experience; mainstream adoption
- **Sustainment (2029+)**: Standards become "the way things are done" through network effects

**Stakeholder Benefits**:
- **Citizens**: More consistent experience across councils
- **LA Digital/IT Directors**: Proven patterns reduce design risk
- **LGA**: Demonstrated sector improvement without mandates
- **GDS DG**: GDS standards extending across government

**Leading Indicators**:
- Community of practice participation and activity
- Standards document downloads and consultation responses
- Pilot council design review pass rates

**Lagging Indicators**:
- Independent assessment of cross-council digital consistency
- Citizen satisfaction with council digital services (national survey)
- Council design team productivity (services delivered per year)

---

## Complete Traceability Matrix

### Stakeholder → Driver → Goal → Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| DSIT Minister | SD-1 | Demonstrate digital transformation | G-1 | OneLogin to 50 councils | O-1 | Single sign-on for citizens |
| DSIT Minister | SD-1 | Demonstrate digital transformation | G-4 | £50M savings | O-3 | Council savings |
| DSIT Minister | SD-1 | Demonstrate digital transformation | G-5 | Service Standard pass | O-4 | Unified standards |
| GDS Director General | SD-2 | Platform economy extension | G-1 | OneLogin to 50 councils | O-1 | Single sign-on for citizens |
| GDS Director General | SD-2 | Platform economy extension | G-3 | 5 shared components | O-3 | Council savings |
| MHCLG Digital | SD-3 | Local gov modernisation | G-2 | Data sharing framework | O-2 | Joined-up vulnerable support |
| MHCLG Digital | SD-3 | Local gov modernisation | G-3 | 5 shared components | O-3 | Council savings |
| MHCLG Digital | SD-3 | Local gov modernisation | G-6 | Community of practice | O-4 | Unified standards |
| LA Chief Executives | SD-4 | Services within constraints | G-4 | £50M savings | O-3 | Council savings |
| LA Chief Executives | SD-4 | Services within constraints | G-2 | Data sharing framework | O-2 | Joined-up vulnerable support |
| LA Digital/IT Directors | SD-5 | Practical technology | G-3 | 5 shared components | O-3 | Council savings |
| LA Digital/IT Directors | SD-5 | Practical technology | G-1 | OneLogin to 50 councils | O-1 | Single sign-on for citizens |
| LA Digital/IT Directors | SD-5 | Practical technology | G-6 | Community of practice | O-4 | Unified standards |
| LGA | SD-6 | Represent council interests | G-6 | Community of practice | O-4 | Unified standards |
| LGA | SD-6 | Represent council interests | G-4 | £50M savings | O-3 | Council savings |
| Citizens | SD-7 | Seamless services | G-1 | OneLogin to 50 councils | O-1 | Single sign-on for citizens |
| Citizens | SD-7 | Seamless services | G-2 | Data sharing framework | O-2 | Joined-up vulnerable support |
| ICO | SD-8 | Lawful data sharing | G-2 | Data sharing framework | O-2 | Joined-up vulnerable support |
| NAO | SD-9 | Value for money | G-4 | £50M savings | O-3 | Council savings |
| NAO | SD-9 | Value for money | G-5 | Service Standard pass | O-4 | Unified standards |
| Tech Suppliers | SD-10 | Market clarity | G-3 | 5 shared components | O-3 | Council savings |
| NCSC | SD-11 | Secure architecture | G-5 | Service Standard pass | O-1 | Single sign-on (security) |
| NCSC | SD-11 | Secure architecture | G-2 | Data sharing framework | O-2 | Joined-up support (security) |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: **DSIT Minister (SD-1)** wants **fast visible progress** but **LA Chief Executives (SD-4)** want **careful adoption that respects local autonomy** and doesn't add burden.
  - **Resolution Strategy**: Phased rollout starting with enthusiastic "pathfinder" councils who volunteer. Demonstrate value with early adopters before asking sceptical councils to engage. Avoid mandates — make adoption compelling through quality and cost savings, not obligation.

- **Conflict 2**: **GDS DG (SD-2)** wants to **extend GDS platforms quickly** but **LA Digital/IT Directors (SD-5)** want platforms that **genuinely fit council use cases**, which may require adaptation.
  - **Resolution Strategy**: Co-design process with council practitioners before platform extension. Allocate dedicated GDS platform team capacity for local government adaptations. Accept that some central platform features may need modification for council contexts.

- **Conflict 3**: **MHCLG (SD-3)** wants **ambitious cross-service data sharing** but **ICO (SD-8)** requires **robust governance** and **LA Chief Executives (SD-4)** are wary of **risk and resource implications**.
  - **Resolution Strategy**: Start with 3 tightly scoped pilot use cases with ICO regulatory sandbox engagement. Build governance framework first, technology second. Demonstrate citizen benefit and safety before scaling. Central funding for council participation in pilots.

- **Conflict 4**: **Technology Suppliers (SD-10)** want to **protect existing revenue** while GDS Local shared components could **displace elements of their offerings**.
  - **Resolution Strategy**: Clear scope definition published early. Market engagement events explaining what GDS Local will and will not build. Open APIs enabling integration rather than replacement. Position shared components as addressing gaps, not competing with comprehensive council management systems.

**Synergies**:

- **Synergy 1**: **Citizens (SD-7)** and **DSIT Minister (SD-1)** share a driver for visible improvement in citizen-facing services — achieving G-1 (OneLogin) satisfies both simultaneously.
- **Synergy 2**: **LA Chief Executives (SD-4)** and **NAO (SD-9)** both want demonstrable value for money — G-4 (integrated purchasing savings) satisfies both.
- **Synergy 3**: **MHCLG (SD-3)**, **LGA (SD-6)**, and **LA Digital/IT Directors (SD-5)** all want co-designed, practical shared components — G-6 (community of practice) creates the mechanism to align all three.
- **Synergy 4**: **ICO (SD-8)** and **NCSC (SD-11)** both want robust governance and security — G-5 (Service Standard) and G-2 (data sharing framework) address both through design.

---

## Communication & Engagement Plan

### DSIT Minister

**Primary Message**: "GDS Local is delivering tangible results: X councils now offering single sign-on, £Xm saved through integrated purchasing, and citizens receiving faster joined-up support through safe data sharing."

**Key Talking Points**:
- Headline metrics suitable for parliamentary questions and media
- Citizen stories demonstrating real-world impact
- Comparison with international government digital programmes

**Communication Frequency**: Quarterly (with ad hoc PQ briefings)

**Preferred Channel**: Ministerial submission with dashboard; PQ briefing packs

**Success Story**: "A mother in [council area] was able to access housing support, health services, and benefits through a single login — receiving the help she needed in 5 days rather than 15."

---

### Local Authority Chief Executives

**Primary Message**: "GDS Local gives your council access to proven, free platforms, saves money through collective purchasing, and provides practical help — without mandating how you run your services."

**Key Talking Points**:
- Concrete cost savings from integrated purchasing and shared components
- Free access to GOV.UK platforms (Notify, Pay, OneLogin)
- Council autonomy preserved — adopt what works for you
- Peer council success stories

**Communication Frequency**: Quarterly (via LGA Chief Executives' Briefing)

**Preferred Channel**: LGA Chief Executives' network; annual LGA conference; CEO briefing packs

**Success Story**: "[Council name] saved £X per year by adopting GOV.UK Notify and shared components, freeing up budget for [local priority]."

---

### Local Authority Digital/IT Directors

**Primary Message**: "Here are well-documented, open-source, API-first components that solve problems you face every day. We built them with councils like yours. Try them in our sandbox."

**Key Talking Points**:
- Technical documentation and sandbox environments available
- Open source — inspect and contribute
- Integration support available
- Community of practice for peer problem-solving

**Communication Frequency**: Monthly (community meetings, newsletter)

**Preferred Channel**: Community of practice (Slack/forum); monthly virtual meetup; Socitm events

**Success Story**: "[Council IT Director] integrated GOV.UK OneLogin in 3 weeks using our documentation and sandbox. Their team now focuses on [service innovation] instead of identity management."

---

### ICO

**Primary Message**: "We are building data sharing governance before technology. Every cross-service data flow has a DPIA, a lawful basis, purpose limitation, and a full audit trail. We welcome your scrutiny."

**Key Talking Points**:
- ICO regulatory sandbox engagement for pilot use cases
- Privacy-by-design in architecture (Principle 9 from ARC-000-PRIN-v1.1)
- DPIAs completed before any data sharing begins
- Citizen transparency and control mechanisms

**Communication Frequency**: Bi-monthly (quarterly formal; interim working level)

**Preferred Channel**: Formal regulatory engagement; ICO sandbox sessions; DPIA review meetings

**Success Story**: "Our housing-health data sharing pilot was endorsed by the ICO as an exemplar of responsible data sharing, with full governance, audit trails, and citizen transparency."

---

### Technology Suppliers

**Primary Message**: "GDS Local builds shared components for common government needs. We publish clear scope, open APIs, and integration specifications. We see suppliers as partners in delivering council digital transformation, not competitors."

**Key Talking Points**:
- Clear scope: what GDS Local builds vs. what remains supplier territory
- Open APIs and integration specifications
- Market engagement and consultation opportunities
- Integration and migration services as new revenue opportunities

**Communication Frequency**: Quarterly (market engagement events)

**Preferred Channel**: Market engagement events; published roadmap; API documentation portal

**Success Story**: "[Supplier name] integrated GOV.UK OneLogin into their council management platform, offering customers a better authentication experience while growing their service offering."

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| LA Digital/IT Directors | Manage bespoke identity, notifications, payments | Adopt shared components, manage integration | HIGH | MEDIUM | Sandbox environments, community support, migration help |
| LA Service Managers | Siloed data, manual cross-referencing | Cross-service data access via governed APIs | HIGH | LOW | Training, clear processes, visible citizen benefit |
| LA Frontline Staff | Separate logins per system, manual data gathering | Federated access, pre-populated citizen data | MEDIUM | LOW | Training, demonstration of time savings |
| Citizens | Separate accounts per council and central service | Single sign-on, less repetition of information | MEDIUM | LOW | Clear communication, gradual transition, assisted digital support |
| GDS Platform Teams | Serve central government only | Extend platforms to 333 councils | HIGH | MEDIUM | Dedicated local gov capacity, clear prioritisation |
| Technology Suppliers | Direct council relationships | Coexistence with shared components | HIGH | HIGH | Early scope clarity, open APIs, partnership approach |
| Council Finance Teams | Individual procurement processes | Integrated purchasing via GDS Local/LGA | MEDIUM | LOW | Clear savings evidence, simple adoption process |

### Change Readiness

**Champions** (Enthusiastic supporters):
- **GDS Local Programme Director** — Leading the programme, personal commitment to success
- **Digitally mature councils** (e.g., those already using GOV.UK Notify) — Ready for deeper GDS integration, eager to shape shared components
- **LGA Digital team** — Strategic interest in demonstrating local government digital leadership
- **MHCLG Digital Director** — Policy ambition for data-driven local government

**Fence-sitters** (Neutral, need convincing):
- **Mid-maturity councils** — Interested but need proof of value and assurance of support before committing resources
- **GDS Platform Teams** — Supportive in principle but concerned about capacity and scope creep
- **Cabinet Office Spend Controls** — Will support if business case is strong but scrutinise rigorously

**Resisters** (Opposed or sceptical):
- **Councils with recent large-scale system procurement** — Contractually and practically locked into existing solutions for years; resistance is rational, not obstructive. Strategy: include them in community of practice; target adoption after current contracts expire
- **Incumbent technology suppliers** — Revenue at risk from shared components. Strategy: early market engagement; position as partners not competitors; open APIs for integration
- **Risk-averse council legal teams** — Concerned about data sharing liability. Strategy: ICO-endorsed framework; template Data Sharing Agreements; legal guidance co-developed with LGA

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Insufficient Local Authority Adoption

**Related Stakeholders**: LA Chief Executives (SD-4), LA Digital/IT Directors (SD-5), LGA (SD-6)

**Risk Description**: Councils do not adopt GDS Local shared components in sufficient numbers, resulting in the programme failing to achieve critical mass and demonstrable outcomes. This could occur due to competing priorities, insufficient council IT capacity, or perception that components don't meet local needs.

**Impact on Goals**: G-1 (OneLogin adoption), G-3 (shared components), G-4 (purchasing savings), G-6 (community)

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Start with pathfinder councils who volunteer and are motivated. Ensure early components deliver genuine value. Provide onboarding support and integration assistance. Fund dedicated council capacity for adoption. Build momentum through peer advocacy.

**Contingency Plan**: If adoption is below targets at 12-month review, refocus on fewer, higher-impact components based on council feedback. Consider offering funded integration services.

---

### Risk R-2: Data Sharing Privacy Incident

**Related Stakeholders**: ICO (SD-8), Citizens (SD-7), DSIT Minister (SD-1), LA Chief Executives (SD-4)

**Risk Description**: A privacy breach or misuse of cross-service data sharing erodes citizen trust and triggers ICO enforcement, derailing the data sharing programme and causing reputational damage to GDS Local.

**Impact on Goals**: G-2 (data sharing framework)

**Probability**: LOW (with proper governance) / MEDIUM (if governance is rushed)

**Impact**: CRITICAL

**Mitigation Strategy**: Governance before technology — Data Sharing Agreements, DPIAs, and ICO sandbox engagement before any data flows. Purpose limitation enforced technically. Comprehensive audit trails. Incident response plan co-developed with ICO. Start with low-risk use cases.

**Contingency Plan**: If incident occurs: immediate ICO notification, transparent public communication, temporary suspension of affected sharing arrangement, independent review before resumption.

---

### Risk R-3: GDS Platform Team Capacity Constraints

**Related Stakeholders**: GDS DG (SD-2), GDS Platform Teams, LA Digital/IT Directors (SD-5)

**Risk Description**: GDS platform teams (OneLogin, Notify, Pay) are already stretched meeting central government commitments. Extending to local government may result in poor quality, slow onboarding, or neglect of central government users.

**Impact on Goals**: G-1 (OneLogin extension), G-3 (shared components)

**Probability**: HIGH

**Impact**: MEDIUM

**Mitigation Strategy**: Dedicated GDS Local capacity within platform teams (not shared with central government priorities). Clear prioritisation framework. Local government extensions designed as incremental additions, not architectural changes. Open source contributions from councils.

**Contingency Plan**: If platform team capacity is insufficient, prioritise OneLogin extension (highest impact) and defer other platform extensions. Consider commercial support contracts for council onboarding.

---

### Risk R-4: "Whitehall Telling Councils What to Do" Perception

**Related Stakeholders**: LA Chief Executives (SD-4), LGA (SD-6), DSIT Minister (SD-1)

**Risk Description**: GDS Local is perceived by councils as another top-down central government initiative that doesn't understand local government. This perception could be fuelled by media coverage, council leader political positioning, or genuine programme missteps (e.g., launching components without council input).

**Impact on Goals**: All goals — undermines the partnership model that GDS Local depends on

**Probability**: MEDIUM

**Impact**: HIGH

**Mitigation Strategy**: Co-design with councils from day one. LGA as visible co-lead. Council practitioners in programme governance. "Nothing about us without us" principle. Voluntary adoption — no mandates. Joint communications with LGA and councils. Celebrate council contributions.

**Contingency Plan**: If perception takes hold: pause and re-engage through LGA. Commission independent council feedback survey. Adjust programme governance to increase council representation. Consider rebranding if necessary.

---

### Risk R-5: Supplier Market Disruption

**Related Stakeholders**: Technology Suppliers (SD-10), LA Chief Executives (SD-4)

**Risk Description**: Technology suppliers actively resist or undermine GDS Local by lobbying councils against adoption, creating FUD (fear, uncertainty, doubt), or refusing to support integration with shared components.

**Impact on Goals**: G-1 (OneLogin), G-3 (shared components), G-4 (purchasing)

**Probability**: MEDIUM

**Impact**: MEDIUM

**Mitigation Strategy**: Early and transparent market engagement. Publish clear scope boundaries. Open APIs that enable integration. Position suppliers as partners (integration services, migration support). Avoid competing with comprehensive council management systems — focus on horizontal commodity capabilities.

**Contingency Plan**: If supplier resistance is significant: escalate through Crown Commercial Service. Use competitive procurement to ensure market alternatives. Publish integration case studies showing coexistence.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Programme strategy and scope | GDS Local Programme Director | GDS Director General | MHCLG Digital, LGA, CDDO | All stakeholders |
| Budget allocation | DSIT Finance | GDS Director General | Programme Director, MHCLG | NAO, Cabinet Office |
| Shared component prioritisation | Programme Director | GDS DG | LA Digital/IT Directors (via CoP), LGA | Suppliers, MHCLG |
| Data sharing governance framework | Programme Director | MHCLG Digital Director | ICO, LA Chief Executives, NCSC | Citizens (via transparency) |
| Technology architecture decisions | Programme Architect | Programme Director | GDS Platform Teams, NCSC, LA technical reps | Socitm, Suppliers |
| Council onboarding prioritisation | Programme Director | LGA | LA Chief Executives | DSIT Minister |
| Service Standard assessment | GDS Assessment Team | GDS DG | Programme Director | All stakeholders |
| Integrated purchasing framework | LGA | LGA Chair | Programme Director, CCS, LA Finance | Suppliers, NAO |
| Communication and stakeholder engagement | Programme Comms Lead | Programme Director | LGA Comms, DSIT Comms | All |

### Escalation Path

1. **Level 1**: GDS Local Programme Director — day-to-day decisions, delivery issues, technical choices
2. **Level 2**: GDS Local Programme Board (GDS DG, MHCLG Digital Director, LGA representative) — scope changes, budget variances >10%, stakeholder conflicts
3. **Level 3**: DSIT/MHCLG Senior Officials — strategic direction, cross-departmental issues, ministerial implications
4. **Level 4**: DSIT Secretary of State — major policy decisions, significant reputational risks

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| GDS Local Programme Director | PENDING | | PENDING |
| MHCLG Digital Director | PENDING | | PENDING |
| LGA Digital Lead | PENDING | | PENDING |
| DSIT Finance | PENDING | | PENDING |
| Council representative(s) | PENDING | | PENDING |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme Sponsor (GDS DG) | | | |
| MHCLG Co-sponsor | | | |
| LGA Partnership Lead | | | |

---

## Appendices

### Appendix A: Stakeholder Interview Summaries

*Note: This document was generated from programme context and publicly available information. Stakeholder interviews should be conducted to validate and refine the analysis.*

#### Recommended Interviews

| Priority | Stakeholder | Purpose | Timing |
|----------|-------------|---------|--------|
| 1 | 5-10 LA Digital/IT Directors (diverse council types) | Validate drivers, test component priorities | Q1 2026 |
| 2 | 3-5 LA Chief Executives (via LGA) | Validate engagement approach, test messaging | Q1 2026 |
| 3 | ICO Data Sharing team | Validate data sharing framework approach | Q1 2026 |
| 4 | GDS Platform Team leads (OneLogin, Notify, Pay) | Validate capacity and extension approach | Q1 2026 |
| 5 | 3-5 Technology Suppliers | Validate market engagement approach | Q1 2026 |

---

### Appendix B: GDS Local Programme Context

**Source**: gov.uk/guidance/gds-local (published November 2025)

**Three Strategic Focus Areas**:
1. Local Government Technology Vision — shared technology products and components with MHCLG, LGA, and practitioners; integrated purchasing approach
2. Data Access Improvement — dismantling data sharing barriers (e.g., housing accessing health and social care data)
3. GDS Product Availability — extending GOV.UK App and GOV.UK OneLogin to local authorities

**Contact**: GDSlocal-info@dsit.gov.uk

---

### Appendix C: References

- ARC-000-PRIN-v1.1 — Enterprise Architecture Principles (GDS Local specific)
- GOV.UK Guidance: GDS Local (gov.uk/guidance/gds-local)
- GDS Service Standard (gov.uk/service-manual/service-standard)
- Technology Code of Practice (gov.uk/guidance/the-technology-code-of-practice)
- UK GDPR and Data Protection Act 2018
- NCSC Secure by Design principles

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GDS Local Guidance | Programme | GOV.UK | Programme purpose, 3 focus areas, co-design approach | gov.uk/guidance/gds-local |
| ARC-000-PRIN-v1.1 | Architecture Principles | ArcKit | 25 principles including GDS Local-specific collaboration, data sharing, federated identity | projects/000-global/ARC-000-PRIN-v1.1.md |

---

**Generated by**: ArcKit `/arckit:stakeholders` command
**Generated on**: 2026-02-16
**ArcKit Version**: 2.4.5
**Project**: GDS Local (Project 001)
**AI Model**: Claude Opus 4.6
