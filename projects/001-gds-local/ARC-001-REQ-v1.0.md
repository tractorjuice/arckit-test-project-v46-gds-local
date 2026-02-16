# Project Requirements: GDS Local

> **Template Status**: Live | **Version**: 2.4.5 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Business and Technical Requirements |
| **Project** | GDS Local (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-02-16 |
| **Last Modified** | 2026-02-16 |
| **Review Cycle** | Monthly |
| **Next Review Date** | 2026-03-18 |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | [PENDING] |
| **Approved By** | [PENDING] |
| **Distribution** | GDS Local Programme Team, Architecture Team, MHCLG Digital, LGA, Pilot Council Representatives |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-16 | ArcKit AI | Initial creation from `/arckit:requirements` command | [PENDING] | [PENDING] |

## Document Purpose

This document defines the comprehensive business, functional, non-functional, integration, and data requirements for the GDS Local programme. It will be used for architecture design, vendor RFPs (via G-Cloud and DOS frameworks), service assessments, and acceptance testing. Requirements are traced to stakeholder goals (ARC-001-STKE-v1.0) and aligned with architecture principles (ARC-000-PRIN-v1.1).

---

## Executive Summary

### Business Context
GDS Local is a unit within the Government Digital Service (GDS), directed by DSIT, established to strengthen collaboration between central and local government. The programme addresses three problems: (1) local authorities spend over £5 billion annually on technology with limited sharing and duplicated procurement, (2) data silos between services prevent joined-up support for vulnerable citizens, and (3) GDS platforms (OneLogin, Notify, Pay) serve only central government while local authorities manage bespoke equivalents.

The programme will deliver shared technology products and components co-designed with MHCLG, LGA, and council practitioners; a cross-service data sharing framework with robust privacy protections; and extension of GOV.UK platforms (OneLogin, App) to local authorities.

### Objectives
- Extend GOV.UK OneLogin to 50 local authorities by Q4 2027 (Goal G-1)
- Establish cross-service data sharing framework with 3 pilot use cases by Q2 2027 (Goal G-2)
- Launch shared technology component catalogue with 5 reusable components by Q3 2027 (Goal G-3)
- Establish integrated purchasing framework saving councils £50M over 3 years (Goal G-4)
- Achieve GDS Service Standard pass for all public-facing components (Goal G-5)
- Build community of practice with 100+ active councils by Q4 2026 (Goal G-6)

### Expected Outcomes
- O-1: Citizens can access central and local services with a single login (40% of digital interactions by Q4 2028)
- O-2: Vulnerable citizens receive better joined-up support through safe data sharing (coordination time reduced from 15 to 5 days)
- O-3: Councils save £50M over 3 years through shared components and integrated purchasing
- O-4: Unified standards improve consistency without reducing local autonomy (50% of participating councils using shared patterns by Q4 2028)

### Project Scope

**In Scope**:
- GOV.UK OneLogin extension to local authorities via standards-based identity federation
- Cross-service data sharing platform with governance framework for 3 pilot use cases (housing-health, social care-benefits, planning-transport)
- Shared technology component catalogue (5 new components for common council needs)
- Integrated purchasing framework for common technology needs
- Community of practice platform and programme
- API gateway and developer portal for local authority integration
- Extension of GOV.UK Notify, Pay, and Design System to local authority contexts

**Out of Scope**:
- Replacement of existing council line-of-business systems (housing management, social care, planning)
- Devolved administration services (Scotland, Wales, Northern Ireland) — future phase
- Non-digital service delivery channels (phone, face-to-face)
- Council internal IT infrastructure (networks, endpoints, email)
- Training of council staff on existing council systems

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| DSIT Minister | Executive Sponsor | DSIT | Strategic direction, ministerial accountability |
| GDS Director General | Programme Board Chair | GDS | Strategic governance, budget approval |
| GDS Local Programme Director | Programme Delivery Lead | GDS | Requirements ownership, day-to-day decisions |
| MHCLG Digital Director | Co-delivery Partner | MHCLG | Data sharing governance, policy alignment |
| LGA Digital Lead | Co-delivery Partner | LGA | Council engagement, integrated purchasing |
| LA Digital/IT Directors | Co-designers/Implementers | Various councils | Requirements validation, integration testing |
| LA Service Managers | End Users | Various councils | User research, acceptance testing |
| Citizens | Beneficiaries | Public | Usability testing, satisfaction surveys |
| ICO | Regulator | ICO | Data sharing framework approval |
| NCSC | Security Advisor | NCSC | Security architecture review |
| GDS Platform Teams | Platform Providers | GDS | OneLogin/Notify/Pay extension |

---

## Business Requirements

### BR-001: Extend GDS Platforms to Local Authorities

**Description**: The programme MUST extend GOV.UK platforms (OneLogin, Notify, Pay, Forms, Design System) to local authorities, enabling councils to adopt shared platforms that are free at point of use and reduce duplicated technology spend.

**Rationale**: 333 councils individually procure and manage commodity technology (identity, notifications, payments). GDS platforms are proven, assured, and free — extending them to local government reduces cost and improves quality. Addresses stakeholder goals G-1 (OneLogin), G-3 (shared components).

**Success Criteria**:
- 50 local authorities live with at least one GDS platform by Q4 2027
- Platforms accessible via open standards (OIDC, REST APIs) with self-service onboarding
- No charge to local authorities for platform usage

**Priority**: MUST_HAVE

**Stakeholder**: GDS DG (SD-2), DSIT Minister (SD-1), LA Chief Executives (SD-4)

**Principle Alignment**: P4 (Interoperability), P13 (Reuse Government Platforms), P16 (Reuse Government Platforms)

---

### BR-002: Enable Cross-Service Data Sharing with Privacy Protections

**Description**: The programme MUST establish a cross-service data sharing framework that enables local authority services (housing, social care, planning) to share relevant citizen data across organisational boundaries while maintaining strict privacy protections, purpose limitation, and citizen transparency.

**Rationale**: Vulnerable citizens interact with multiple services (housing, health, social care, benefits) but data silos mean frontline workers cannot access information needed to provide joined-up support. Currently takes 15 working days to coordinate multi-service support. Addresses stakeholder goal G-2.

**Success Criteria**:
- 3 pilot data sharing use cases operational across 10 councils by Q2 2027
- ICO endorsement of data sharing framework
- Each sharing arrangement has approved DPIA, Data Sharing Agreement, and documented lawful basis
- Citizen trust survey shows >60% confidence in cross-service data handling

**Priority**: MUST_HAVE

**Stakeholder**: MHCLG Digital (SD-3), Citizens (SD-7), ICO (SD-8)

**Principle Alignment**: P9 (Cross-Service Data Sharing), P11 (Data Sovereignty), P5 (Security by Design)

---

### BR-003: Deliver Measurable Cost Savings for Local Authorities

**Description**: The programme MUST deliver measurable cost savings to participating councils through integrated purchasing and shared component adoption, with cumulative savings of £50M over 3 years independently verifiable.

**Rationale**: Local authorities face severe budget pressures. Cost savings are the most tangible value proposition and the primary driver for council adoption. The NAO will audit value for money. Addresses stakeholder goals G-3, G-4.

**Success Criteria**:
- £50M cumulative savings over 3 years independently verified
- 100+ councils participating in integrated purchasing by Year 2
- Individual council savings calculable and reportable
- NAO audit-ready benefits tracking from inception

**Priority**: MUST_HAVE

**Stakeholder**: LA Chief Executives (SD-4), NAO (SD-9), DSIT Minister (SD-1)

**Principle Alignment**: P25 (Spend Controls and Value for Money)

---

### BR-004: Co-design with Local Government Practitioners

**Description**: All shared technology products and components MUST be co-designed with local government practitioners from diverse council types (metropolitan, rural, unitary, county/district, large, small).

**Rationale**: Central government initiatives that do not involve local practitioners fail to account for council diversity and create adoption resistance. The LGA and council chief executives require genuine co-design, not consultation on pre-decided solutions. Addresses stakeholder goals G-3, G-6.

**Success Criteria**:
- Community of practice with 100+ active council participants by Q4 2026
- Each shared component has documented co-design process with council input
- Component roadmap influenced by council practitioner feedback
- Councils of varying sizes and types represented in co-design

**Priority**: MUST_HAVE

**Stakeholder**: LGA (SD-6), LA Digital/IT Directors (SD-5), MHCLG (SD-3)

**Principle Alignment**: P1 (User Needs First), P8 (Central-Local Collaboration)

---

### BR-005: Meet GDS Service Standard for All Public-Facing Components

**Description**: All public-facing GDS Local components and services MUST pass GDS Service Standard assessment at alpha and beta stages.

**Rationale**: Service Standard compliance ensures quality, accessibility, security, and operational reliability. It provides assurance to ministers, the NAO, and citizens. Addresses stakeholder goal G-5.

**Success Criteria**:
- 100% pass rate at alpha and beta assessments
- WCAG 2.2 AA compliance verified for all citizen-facing interfaces
- Security assessments completed with NCSC engagement
- Performance data published on GOV.UK

**Priority**: MUST_HAVE

**Stakeholder**: DSIT Minister (SD-1), Citizens (SD-7), NCSC (SD-11)

**Principle Alignment**: P6 (Accessibility), P5 (Security), P24 (GDS Service Standard)

---

### BR-006: Voluntary Adoption Model

**Description**: The programme MUST operate on a voluntary adoption model — no council should be mandated to adopt GDS Local components. Adoption must be driven by demonstrated value, not obligation.

**Rationale**: Local authorities are independent democratic bodies. Mandating technology creates political resistance and undermines the partnership model. The LGA and council chief executives have made voluntary adoption a condition of engagement. Addresses stakeholder driver SD-6.

**Success Criteria**:
- No requirement for councils to adopt any GDS Local component
- Adoption driven by demonstrated value (cost savings, quality improvement)
- Councils can partially adopt (e.g., use Notify but not OneLogin)
- Exit strategy documented for councils that wish to discontinue use

**Priority**: MUST_HAVE

**Stakeholder**: LGA (SD-6), LA Chief Executives (SD-4)

---

## Functional Requirements

### User Personas

#### Persona 1: Sarah — Council Digital Service Manager
- **Role**: Manages digital services for a mid-sized unitary council (250k population)
- **Goals**: Improve citizen-facing services while reducing operational burden on her small team (15 staff)
- **Pain Points**: Managing bespoke identity system, maintaining separate notification service, duplicated procurement for commodity technology
- **Technical Proficiency**: High

#### Persona 2: Marcus — Council Housing Officer
- **Role**: Frontline housing officer in a metropolitan borough
- **Goals**: Support vulnerable tenants by coordinating with health and social care services
- **Pain Points**: Cannot access health/social care data; spends days chasing information by phone/email; citizens repeat their story to every service
- **Technical Proficiency**: Medium

#### Persona 3: Priya — Citizen
- **Role**: Single parent using council services (housing, council tax, school admissions) and central services (benefits, tax)
- **Goals**: Access all government services quickly and easily without multiple accounts
- **Pain Points**: 7 different logins for different government services; repeating personal information to each; confusing which service is central vs. local
- **Technical Proficiency**: Low-Medium

#### Persona 4: James — Small District Council IT Manager
- **Role**: IT manager for a small district council (80k population, 5-person IT team)
- **Goals**: Reduce time spent on commodity technology so team can focus on service innovation
- **Pain Points**: Maintaining identity, hosting, and notification infrastructure with minimal staff; cannot attract specialist talent; vendor lock-in on expensive contracts
- **Technical Proficiency**: High (but resource-constrained)

#### Persona 5: Aisha — GDS Platform Engineer
- **Role**: Engineer on the GOV.UK OneLogin platform team
- **Goals**: Extend OneLogin to local authorities without breaking central government service reliability
- **Pain Points**: Diverse council technical estates; unclear local authority use cases; additional support burden
- **Technical Proficiency**: Very High

---

### Use Cases

#### UC-1: Citizen Authenticates to Council Service via OneLogin

**Actor**: Priya (Citizen)

**Preconditions**:
- Citizen has a GOV.UK OneLogin account (from central government use)
- Council service supports OneLogin federation
- Council has signed data processing agreement with GDS

**Main Flow**:
1. Citizen navigates to council service (e.g., council tax account)
2. Council service presents "Sign in with GOV.UK OneLogin" option alongside existing council login
3. Citizen selects GOV.UK OneLogin
4. System redirects to GOV.UK OneLogin authentication
5. Citizen authenticates (password + MFA)
6. OneLogin returns identity assertion to council service
7. Council service creates/matches local account and grants access
8. Citizen accesses council service with pre-populated name and address

**Postconditions**:
- Citizen authenticated with verified identity
- Council service has user identity token (no password stored locally)
- Authentication event logged in OneLogin analytics

**Alternative Flows**:
- **Alt 1a**: Citizen does not have OneLogin account — offered option to create one or use existing council login
- **Alt 2a**: Council service requires higher identity assurance — citizen prompted for additional verification

**Exception Flows**:
- **Ex 1**: OneLogin service unavailable — citizen redirected to council's fallback authentication

**Business Rules**:
- Council MUST maintain fallback authentication during transition period
- Citizen MUST NOT be forced to use OneLogin — existing council login remains available
- Identity data shared MUST be limited to what the council service needs

**Priority**: CRITICAL

---

#### UC-2: Housing Officer Accesses Cross-Service Data

**Actor**: Marcus (Housing Officer)

**Preconditions**:
- Housing officer authenticated and authorised for cross-service data access
- Data Sharing Agreement in place between housing and health/social care
- DPIA approved for this use case
- Citizen record exists in housing system

**Main Flow**:
1. Housing officer opens vulnerable tenant case in housing management system
2. Officer selects "View cross-service information" for the tenant
3. System queries data sharing platform with tenant identifier and purpose code
4. Data sharing platform verifies officer's authorisation, purpose limitation, and DSA validity
5. Platform returns relevant health/social care flags (e.g., "active social care case", "known to mental health services")
6. Housing officer sees summary information alongside housing record
7. Officer records that cross-service data was viewed and the decision it informed

**Postconditions**:
- Officer has relevant cross-service context for decision-making
- Full audit trail recorded (who, what, when, purpose, lawful basis)
- No bulk data transferred — only relevant summary for specific citizen

**Alternative Flows**:
- **Alt 1a**: No cross-service data exists for this citizen — system shows "No records found"
- **Alt 2a**: Officer's role does not have authorisation for this data type — access denied with explanation

**Exception Flows**:
- **Ex 1**: Data sharing platform unavailable — officer shown "Service temporarily unavailable, try again later"
- **Ex 2**: DSA expired — access denied, system notifies data sharing administrator

**Business Rules**:
- Access MUST be purpose-limited — only data relevant to the housing case
- Access MUST be logged with full audit trail
- Data MUST NOT be downloaded or copied in bulk
- DSA MUST be valid and current for data access to proceed

**Priority**: CRITICAL

---

#### UC-3: Council IT Team Integrates Shared Component

**Actor**: Sarah (Council Digital Service Manager)

**Preconditions**:
- Council has registered with GDS Local programme
- Shared component published in catalogue with documentation
- Sandbox environment available

**Main Flow**:
1. Sarah browses GDS Local shared component catalogue
2. Sarah selects component and reads documentation, API specs, and integration guide
3. Sarah creates sandbox environment for testing
4. Sarah's team develops integration using published APIs and SDKs
5. Team tests integration in sandbox against representative scenarios
6. Sarah requests production access via self-service portal
7. GDS Local team reviews and approves production integration
8. Council deploys integration to production

**Postconditions**:
- Council service integrated with shared component
- Usage analytics tracking enabled
- Council added to component notification list for updates

**Alternative Flows**:
- **Alt 1a**: Component does not fit council use case — Sarah submits feature request via community
- **Alt 2a**: Integration requires customisation — documentation covers extension points

**Business Rules**:
- Self-service onboarding SHOULD complete within 5 working days
- Sandbox environment MUST mirror production behaviour
- Breaking API changes MUST have 6-month deprecation notice

**Priority**: HIGH

---

### Functional Requirements Detail

#### FR-001: GOV.UK OneLogin Federation Gateway

**Description**: The system MUST provide an identity federation gateway enabling local authority services to authenticate citizens via GOV.UK OneLogin using open standards (OpenID Connect and SAML 2.0).

**Relates To**: BR-001, UC-1, Goal G-1

**Acceptance Criteria**:
- [ ] Given a council service registered for OneLogin, when a citizen selects "Sign in with GOV.UK OneLogin", then the citizen is redirected to OneLogin and returned with a valid identity assertion
- [ ] Given a citizen authenticated via OneLogin, when the identity assertion is received by the council service, then it contains only the attributes the council has registered to receive
- [ ] Given a council service where OneLogin is unavailable, when a citizen attempts to sign in, then the council's fallback authentication is offered within 5 seconds

**Data Requirements**:
- **Inputs**: OIDC/SAML authentication request from council service
- **Outputs**: Identity assertion (name, email, verified address where applicable)
- **Validations**: Token signature verification, audience validation, replay protection

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: GOV.UK OneLogin platform readiness; council service OIDC/SAML capability

---

#### FR-002: Local Authority Self-Service Onboarding Portal

**Description**: The system MUST provide a self-service portal where local authority IT teams can register, configure, and manage their integration with GDS Local platforms and shared components.

**Relates To**: BR-001, UC-3, Goal G-1, G-3

**Acceptance Criteria**:
- [ ] Given a council IT team, when they register on the portal, then they can access sandbox environments within 1 working day
- [ ] Given a registered council, when they request production access, then approval completes within 5 working days
- [ ] Given a council with production access, when they need to rotate API credentials, then they can do so via self-service without contacting GDS

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: Identity management for council admin users; API key management infrastructure

---

#### FR-003: Shared Component Catalogue

**Description**: The system MUST provide a searchable catalogue of shared technology components with documentation, API specifications, integration guides, and sandbox environments.

**Relates To**: BR-001, UC-3, Goal G-3

**Acceptance Criteria**:
- [ ] Given a council developer, when they browse the catalogue, then each component shows description, API docs (OpenAPI), integration guide, status, and SLA
- [ ] Given a component in the catalogue, when a developer requests a sandbox, then a functional sandbox is provisioned within 4 hours
- [ ] Given a component, when API specifications are updated, then the catalogue reflects changes within 1 hour

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-004: Cross-Service Data Sharing Platform

**Description**: The system MUST provide a platform enabling authorised cross-service data queries between local authority systems (housing, social care, health, planning, transport) with purpose limitation, audit trails, and governance enforcement.

**Relates To**: BR-002, UC-2, Goal G-2

**Acceptance Criteria**:
- [ ] Given an authorised user with a valid purpose code, when they query cross-service data for a specific citizen, then only data permitted by the active DSA is returned
- [ ] Given a data query, when it is executed, then a complete audit record is created (who, what, when, purpose, lawful basis, result)
- [ ] Given an expired or revoked DSA, when a query is attempted against that sharing arrangement, then access is denied and the data sharing administrator is notified
- [ ] Given a data query, when the source system is unavailable, then a meaningful error is returned within 10 seconds and the query is not partially fulfilled

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: Council systems capable of API-based data exchange; signed DSAs; approved DPIAs

---

#### FR-005: Data Sharing Governance Dashboard

**Description**: The system MUST provide a governance dashboard showing all active Data Sharing Agreements, their status, DPIA status, access volumes, and audit summaries.

**Relates To**: BR-002, Goal G-2

**Acceptance Criteria**:
- [ ] Given a data sharing administrator, when they access the dashboard, then they see all DSAs with status (active/expired/pending), DPIA status, and access volume for the last 30 days
- [ ] Given a DSA approaching expiry (30 days), when the administrator views the dashboard, then a renewal alert is prominently displayed
- [ ] Given a query for audit data, when the administrator requests it, then a complete audit report can be generated for any DSA within any time period

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-006: Community of Practice Platform

**Description**: The system MUST provide a collaboration platform for the GDS Local community of practice, supporting discussion forums, event management, resource sharing, and contribution tracking.

**Relates To**: BR-004, Goal G-6

**Acceptance Criteria**:
- [ ] Given a council participant, when they join the community, then they can access discussion forums, upcoming events, and shared resources
- [ ] Given a community member, when they submit a feature request or bug report for a shared component, then it is tracked and visible to the community
- [ ] Given the programme team, when they need engagement metrics, then dashboard shows active members, posts, events attended, and contributions per council

**Priority**: SHOULD_HAVE

**Complexity**: LOW

---

#### FR-007: Integrated Purchasing Portal

**Description**: The system MUST provide a portal where councils can access collective procurement frameworks, view aggregated demand, and participate in integrated purchasing for common technology needs.

**Relates To**: BR-003, Goal G-4

**Acceptance Criteria**:
- [ ] Given a council procurement officer, when they access the portal, then they see available frameworks, current aggregate demand, and estimated savings vs. individual procurement
- [ ] Given a procurement framework, when a council commits to participate, then their demand is added to the aggregate and savings estimate is updated
- [ ] Given a completed procurement, when savings are calculated, then individual council savings and programme-wide totals are reported

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

**Dependencies**: Legal framework for collective procurement; Crown Commercial Service alignment

---

#### FR-008: Platform Health and Status Dashboard

**Description**: The system MUST provide a public-facing status page showing the real-time health of all GDS Local shared components and platforms, with per-authority status where applicable.

**Relates To**: BR-005, Goal G-5

**Acceptance Criteria**:
- [ ] Given any user, when they access the status page, then they see real-time status of all shared components (operational, degraded, outage)
- [ ] Given a council IT team, when they access their authority-specific view, then they see component status, recent incidents, and upcoming maintenance relevant to their integrations
- [ ] Given an incident, when it is declared, then the status page updates within 5 minutes with impact description and estimated resolution

**Priority**: MUST_HAVE

**Complexity**: LOW

---

#### FR-009: API Gateway with Rate Limiting and Analytics

**Description**: The system MUST provide a central API gateway for all GDS Local APIs, with authentication, rate limiting, versioning, and per-council usage analytics.

**Relates To**: BR-001, Goal G-3

**Acceptance Criteria**:
- [ ] Given a council integration, when it calls an API, then the request is authenticated, rate-limited, and logged with council identifier
- [ ] Given an API version, when a new version is released, then the previous version continues to work for at least 6 months with deprecation warnings
- [ ] Given a council IT team, when they request usage analytics, then they can see their API call volumes, error rates, and latency by endpoint

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-010: Citizen Consent Management

**Description**: Where consent is the lawful basis for cross-service data sharing, the system MUST provide mechanisms for citizens to grant, review, and withdraw consent for specific data sharing arrangements.

**Relates To**: BR-002, Goal G-2

**Acceptance Criteria**:
- [ ] Given a citizen, when consent is required for a data sharing arrangement, then they are presented with clear, plain-English explanation of what data will be shared, with whom, and for what purpose
- [ ] Given a citizen who has granted consent, when they wish to review their consents, then they can see all active consents and withdraw any at any time
- [ ] Given a citizen who withdraws consent, when the withdrawal is processed, then data sharing for that arrangement ceases within 24 hours

**Priority**: MUST_HAVE (where consent is the lawful basis)

**Complexity**: HIGH

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-001: API Response Time

**Requirement**: All GDS Local platform APIs MUST respond within defined latency targets:
- Identity federation (OneLogin): < 500ms for authentication flow (95th percentile)
- Data sharing queries: < 2 seconds for single-citizen queries (95th percentile)
- Component catalogue and portal: < 1 second page load (95th percentile)
- API gateway: < 50ms added latency (99th percentile)

**Measurement Method**: Application Performance Monitoring (APM) with real-time dashboards; synthetic monitoring from multiple UK locations

**Load Conditions**:
- Peak authentication: 10,000 concurrent OneLogin sessions across all councils
- Peak data sharing: 500 queries per second across all pilot councils
- Portal: 1,000 concurrent admin users

**Priority**: MUST_HAVE

**Principle Alignment**: P17 (Performance and Efficiency)

---

#### NFR-P-002: Throughput and Capacity

**Requirement**: The system MUST handle the aggregate load from 50 councils in Phase 1, scaling to 333 councils at full adoption:
- Phase 1 (50 councils): 50,000 OneLogin authentications/day; 5,000 data sharing queries/day
- Phase 2 (150 councils): 200,000 OneLogin authentications/day; 20,000 data sharing queries/day
- Full scale (333 councils): 500,000 OneLogin authentications/day; 50,000 data sharing queries/day

**Scalability**: Must scale horizontally without architectural changes

**Priority**: MUST_HAVE

**Principle Alignment**: P2 (Scalability and Elasticity)

---

### Availability and Resilience Requirements

#### NFR-A-001: Platform Availability

**Requirement**: GDS Local shared platforms MUST achieve 99.9% availability (43.8 minutes unplanned downtime per month maximum):
- OneLogin federation gateway: 99.9%
- Data sharing platform: 99.9%
- API gateway: 99.95%
- Community platform: 99.5%
- Purchasing portal: 99.5%

**Maintenance Windows**: Planned maintenance SHOULD occur between 22:00-06:00 GMT on Sundays with 7 days notice to councils

**Priority**: MUST_HAVE

**Principle Alignment**: P18 (Availability and Reliability)

---

#### NFR-A-002: Disaster Recovery

**RPO (Recovery Point Objective)**: Maximum 15 minutes data loss for transactional systems (data sharing audit logs, OneLogin sessions); 4 hours for non-transactional (community platform, catalogue)

**RTO (Recovery Time Objective)**: Maximum 1 hour for critical systems (OneLogin, data sharing); 4 hours for supporting systems

**Backup Requirements**:
- Continuous replication for critical databases
- Daily backups for all data stores
- Backup retention: 90 days for operational; 7 years for audit/compliance
- Geographic backup in separate UK data centre

**Failover Requirements**:
- Automatic failover to secondary availability zone: YES
- Failover time: < 5 minutes for critical systems

**Priority**: MUST_HAVE

**Principle Alignment**: P3 (Resilience and Fault Tolerance)

---

#### NFR-A-003: Fault Tolerance and Graceful Degradation

**Requirement**: System MUST gracefully degrade when components or council systems fail, without cascading failures across authorities:

**Resilience Patterns Required**:
- [ ] Circuit breaker for all external council system integrations
- [ ] Retry with exponential backoff for transient failures
- [ ] Timeout on all network calls (default 10s, configurable)
- [ ] Bulkhead isolation — one council's integration failure MUST NOT affect other councils
- [ ] Graceful degradation — if data sharing platform is down, council services continue operating with local data only
- [ ] OneLogin unavailability MUST trigger fallback to council's own authentication

**Priority**: MUST_HAVE

**Principle Alignment**: P3 (Resilience), P14 (Loose Coupling)

---

### Scalability Requirements

#### NFR-S-001: Horizontal Scaling for Multi-Authority Platform

**Requirement**: The system MUST scale horizontally to serve 333 councils without architectural changes:

**Growth Projections**:
- Year 1 (2026-27): 50 councils, 15M citizens, 50K auth/day
- Year 2 (2027-28): 150 councils, 30M citizens, 200K auth/day
- Year 3 (2028-29): 333 councils, 56M citizens, 500K auth/day

**Multi-tenancy**: Platform MUST support efficient multi-tenancy — onboarding a new council MUST NOT require infrastructure changes

**Priority**: MUST_HAVE

**Principle Alignment**: P2 (Scalability), P8 (Central-Local Collaboration)

---

### Security Requirements

#### NFR-SEC-001: Zero-Trust Authentication

**Requirement**: All system access MUST follow zero-trust principles — no implicit trust based on network location. All requests authenticated and authorised.

**Multi-Factor Authentication (MFA)**:
- Required for: All admin access, all data sharing platform access, privileged API operations
- Citizens: MFA required for OneLogin (managed by OneLogin platform)
- Council staff: MFA required via council identity provider or GOV.UK OneLogin

**Session Management**:
- Session timeout: 30 minutes inactivity for admin interfaces
- Absolute session timeout: 12 hours
- Re-authentication for: data sharing queries, configuration changes, credential rotation

**Priority**: MUST_HAVE

**Principle Alignment**: P5 (Security by Design)

---

#### NFR-SEC-002: Tenant Isolation

**Requirement**: Council data MUST be strictly isolated — Council A MUST NOT be able to access Council B's data, configuration, or operational telemetry except where explicitly permitted by a Data Sharing Agreement.

**Isolation Requirements**:
- Logical data isolation at minimum; physical isolation for OFFICIAL-SENSITIVE data
- API keys and credentials scoped to individual councils
- Cross-council data access ONLY via governed data sharing platform with DSA enforcement
- Security testing MUST include tenant isolation verification

**Priority**: MUST_HAVE

**Principle Alignment**: P5 (Security), P9 (Cross-Service Data Sharing)

---

#### NFR-SEC-003: Encryption

**Requirement**:
- Data in transit: TLS 1.2+ (TLS 1.3 preferred) with strong cipher suites for all communications
- Data at rest: AES-256 encryption for all data stores
- Key management: Managed key service with automatic rotation

**Encryption Scope**:
- [ ] All databases encrypted at rest
- [ ] All backups encrypted
- [ ] All API communications encrypted in transit
- [ ] Cross-service data sharing payloads encrypted end-to-end
- [ ] Audit logs encrypted at rest with tamper-evident storage

**Priority**: MUST_HAVE

**Principle Alignment**: P5 (Security by Design)

---

#### NFR-SEC-004: Audit Logging and Forensics

**Requirement**: Comprehensive, tamper-evident audit trail for all security-relevant and data-sharing events.

**Audit Log Contents**:
- Who: User/service identity (council, role, individual)
- What: Action performed (authentication, data query, configuration change)
- When: Timestamp (UTC, millisecond precision)
- Where: System component, API endpoint
- Why: Purpose code, DSA reference (for data sharing)
- Result: Success/failure with error details

**Log Retention**: 7 years for compliance/audit logs (immutable storage)

**Log Integrity**: Tamper-evident logging with cryptographic chaining

**Priority**: MUST_HAVE

**Principle Alignment**: P7 (Observability), P5 (Security)

---

#### NFR-SEC-005: Vulnerability Management

**Requirement**:
- Dependency scanning in CI/CD pipeline (zero critical/high vulnerabilities in production)
- Static application security testing (SAST) on all code changes
- Dynamic application security testing (DAST) on deployed environments
- Penetration testing: Annually by CHECK-certified provider; quarterly automated scans
- NCSC Secure by Design review at architecture and design stages

**Remediation SLA**:
- Critical vulnerabilities: 24 hours
- High vulnerabilities: 7 days
- Medium vulnerabilities: 30 days

**Priority**: MUST_HAVE

**Principle Alignment**: P5 (Security by Design)

---

### Compliance and Regulatory Requirements

#### NFR-C-001: UK GDPR and Data Protection Act 2018

**Requirement**: All data processing MUST comply with UK GDPR and the Data Protection Act 2018.

**Compliance Requirements**:
- [ ] Lawful basis documented for every data processing activity
- [ ] Data Protection Impact Assessments (DPIAs) completed for all cross-service data sharing
- [ ] Data subject rights supported (access, rectification, erasure, portability, restriction, objection)
- [ ] Data breach notification to ICO within 72 hours
- [ ] Privacy notices published explaining cross-service data sharing
- [ ] Data minimisation enforced — only necessary data collected and shared
- [ ] Data controller/processor relationships documented for all shared components

**Data Residency**: All citizen personal data processed and stored within UK jurisdiction

**Priority**: MUST_HAVE

**Principle Alignment**: P11 (Data Sovereignty and UK GDPR)

---

#### NFR-C-002: Public Sector Bodies Accessibility Regulations 2018

**Requirement**: All citizen-facing interfaces MUST comply with WCAG 2.2 Level AA and the Public Sector Bodies Accessibility Regulations 2018.

**Accessibility Features**:
- [ ] Keyboard navigation for all functions
- [ ] Screen reader compatibility (tested with JAWS, NVDA, VoiceOver)
- [ ] GOV.UK Design System patterns used for all citizen-facing interfaces
- [ ] Progressive enhancement — core functionality works without JavaScript
- [ ] Accessibility statement published and maintained
- [ ] Regular automated and manual accessibility audits

**Priority**: MUST_HAVE

**Principle Alignment**: P6 (Accessibility by Default)

---

#### NFR-C-003: GDS Service Standard

**Requirement**: All public-facing GDS Local services MUST meet the 14 points of the GDS Service Standard and pass assessment at alpha and beta stages.

**Priority**: MUST_HAVE

**Principle Alignment**: P24 (GDS Service Standard)

---

#### NFR-C-004: NCSC Security Standards

**Requirement**: All GDS Local components MUST meet NCSC security guidance including Secure by Design principles, Cyber Assessment Framework, and Cyber Essentials Plus baseline.

**Priority**: MUST_HAVE

**Principle Alignment**: P5 (Security by Design)

---

### Usability Requirements

#### NFR-U-001: GOV.UK Design System Compliance

**Requirement**: All citizen-facing interfaces MUST use GOV.UK Design System components and patterns. Council-facing admin interfaces SHOULD use GOV.UK Design System with appropriate extensions for professional users.

**Browser Support**: Last 2 versions of Chrome, Firefox, Safari, Edge; IE11 not required

**Priority**: MUST_HAVE

---

#### NFR-U-002: Self-Service Council Onboarding

**Requirement**: Council IT teams MUST be able to self-service onboard to GDS Local platforms using published documentation, without requiring direct GDS support for standard integration patterns.

**Target**: 80% of council integrations completed via self-service within 10 working days

**Priority**: SHOULD_HAVE

---

### Maintainability Requirements

#### NFR-M-001: Observability

**Requirement**: Comprehensive instrumentation for monitoring and troubleshooting, with both platform-wide and per-council visibility.

**Telemetry Requirements**:
- **Logging**: Structured JSON logs with correlation IDs and council context; no PII in logs
- **Metrics**: Request volume, latency (p50/p95/p99), error rates — per council and aggregate
- **Tracing**: Distributed tracing across central-local boundaries
- **Dashboards**: Platform health dashboard (public); per-council dashboard (authenticated)
- **Alerts**: SLO-based alerting with actionable runbooks

**Priority**: MUST_HAVE

**Principle Alignment**: P7 (Observability)

---

#### NFR-M-002: API Versioning and Backward Compatibility

**Requirement**: All APIs MUST be versioned. Breaking changes MUST have a minimum 6-month deprecation period with migration documentation. Councils MUST NOT be forced to upgrade during active service delivery.

**Priority**: MUST_HAVE

**Principle Alignment**: P4 (Interoperability), P14 (Loose Coupling)

---

#### NFR-M-003: Open Source Publication

**Requirement**: All GDS Local source code SHOULD be published as open source unless a documented exception applies (security-sensitive code, credentials).

**Priority**: SHOULD_HAVE

**Principle Alignment**: P23 (Open Source by Default)

---

## Integration Requirements

### INT-001: GOV.UK OneLogin Platform Integration

**Purpose**: Extend GOV.UK OneLogin to support local authority service provider registration and citizen authentication across council services.

**Integration Type**: Real-time API (OIDC/SAML federation)

**Data Exchanged**:
- **From OneLogin to Council**: Identity assertion (name, email, verified address — attribute set configurable per council)
- **From Council to OneLogin**: Authentication request, service provider metadata

**Authentication**: Mutual TLS for service provider registration; OIDC/SAML for citizen authentication

**Error Handling**: Automatic fallback to council authentication within 5 seconds if OneLogin unavailable

**SLA**: 99.9% availability; < 500ms authentication flow

**Owner**: GDS OneLogin Team

**Priority**: MUST_HAVE

---

### INT-002: Local Authority Line-of-Business Systems

**Purpose**: Enable council housing, social care, planning, and other systems to participate in cross-service data sharing and consume shared components.

**Integration Type**: REST APIs via API gateway; event-driven notifications for async updates

**Data Exchanged**:
- **From Council Systems to Data Sharing Platform**: Citizen data responses to authorised queries
- **From Data Sharing Platform to Council Systems**: Authorised data queries with purpose codes

**Authentication**: OAuth 2.0 client credentials with council-scoped API keys

**Error Handling**: Circuit breaker per council system; retry with backoff; graceful degradation to local data only

**SLA**: Best-effort (depends on council system capability); platform adds < 100ms latency

**Owner**: Individual councils (their systems); GDS Local (platform and gateway)

**Priority**: MUST_HAVE

---

### INT-003: GOV.UK Notify Extension

**Purpose**: Extend GOV.UK Notify for local authority service notifications (email, SMS, letters) with council-branded templates.

**Integration Type**: REST API

**Data Exchanged**:
- **From Council to Notify**: Notification requests (recipient, template, personalisation data)
- **From Notify to Council**: Delivery status callbacks

**Authentication**: API key per council

**SLA**: 99.95% availability (existing Notify SLA)

**Owner**: GDS Notify Team

**Priority**: SHOULD_HAVE

---

### INT-004: GOV.UK Pay Extension

**Purpose**: Extend GOV.UK Pay for local authority payment processing (council tax, planning fees, parking permits).

**Integration Type**: REST API + redirect-based payment flow

**Data Exchanged**:
- **From Council to Pay**: Payment request (amount, reference, description)
- **From Pay to Council**: Payment outcome callback (success, failure, reference)

**Authentication**: API key per council; PCI-DSS compliance maintained by Pay platform

**SLA**: 99.9% availability

**Owner**: GDS Pay Team

**Priority**: SHOULD_HAVE

---

### INT-005: ICO Regulatory Interface

**Purpose**: Support ICO oversight of cross-service data sharing including DPIA submission, audit report generation, and breach notification.

**Integration Type**: Report generation and manual submission (no real-time API integration with ICO expected in Phase 1)

**Data Exchanged**:
- **From Platform to ICO**: DPIA documents, audit reports, breach notifications
- **From ICO to Platform**: DPIA feedback, regulatory guidance

**Priority**: SHOULD_HAVE

---

## Data Requirements

### DR-001: Council Registration Data

**Description**: Data about local authorities registered with GDS Local, their integrations, API credentials, and configuration.

**Data Classification**: OFFICIAL

**Data Retention**: Active while council is participating; archived 2 years after departure

**Estimated Volume**: 333 council records with up to 50 integrations each

---

### DR-002: Identity Federation Data

**Description**: Service provider metadata, authentication event logs, and session data for OneLogin federation.

**Data Classification**: OFFICIAL (metadata); OFFICIAL-SENSITIVE (authentication events)

**Data Retention**: Session data 90 days; authentication event logs 7 years

**Estimated Volume**: 500,000 authentication events/day at full scale

---

### DR-003: Data Sharing Audit Logs

**Description**: Complete audit trail of all cross-service data queries including who, what, when, purpose, lawful basis, and result.

**Data Classification**: OFFICIAL-SENSITIVE

**Data Retention**: 7 years (regulatory requirement)

**Data Integrity**: Tamper-evident storage with cryptographic chaining

**Estimated Volume**: 50,000 audit records/day at full scale; ~18M records/year

---

### DR-004: Data Sharing Agreements

**Description**: Digital records of Data Sharing Agreements between participating organisations, including parties, data types, purposes, lawful basis, expiry dates, and approval chain.

**Data Classification**: OFFICIAL

**Data Retention**: Active agreements plus 7 years after expiry

---

### DR-005: Community and Engagement Data

**Description**: Community of practice membership, event participation, contribution tracking, and engagement metrics.

**Data Classification**: OFFICIAL

**Data Retention**: Active while member is participating; anonymised for long-term analytics after departure

---

### Data Quality Requirements

**Data Accuracy**: Council registration data validated at entry; identity assertions validated cryptographically; audit logs verified for completeness

**Data Completeness**: All mandatory fields enforced at API level; audit logs MUST have zero gaps

**Data Consistency**: Cross-system reconciliation for council registration across platforms

**Data Timeliness**: Authentication events logged in real-time; audit logs queryable within 5 minutes of event

**Data Lineage**: Source authority clearly identified in all cross-service data responses

---

### Data Migration Requirements

**Migration Scope**: No legacy data migration required — GDS Local is a new programme. Councils migrating from existing identity systems will need to link existing accounts to OneLogin identities.

**Account Linking Strategy**: Progressive linking — citizens link accounts when they first use OneLogin on a council service; no bulk migration of citizen accounts.

---

## Constraints and Assumptions

### Technical Constraints

**TC-1**: GOV.UK OneLogin platform must support local authority use cases without architectural changes to the core platform — local authority extensions are additive only.

**TC-2**: Council systems are diverse (hundreds of different technology stacks across 333 councils) — all integrations must use open standards (REST, OIDC, SAML) with no assumptions about council technology.

**TC-3**: Data sharing platform must work with councils that have limited API capability — batch/file-based integration must be supported as a fallback.

**TC-4**: All infrastructure must be hosted in UK sovereign data centres (UK GDPR data residency requirement).

---

### Business Constraints

**BC-1**: Voluntary adoption — no council can be mandated to participate. Adoption driven by demonstrated value.

**BC-2**: GDS platform teams have limited capacity — local authority extensions must be efficient and not degrade central government service quality.

**BC-3**: Cabinet Office spend controls apply to all technology procurement above thresholds.

**BC-4**: LGA must be a visible co-partner in governance — not sidelined or presented as endorsing a pre-decided approach.

---

### Assumptions

**A-1**: GOV.UK OneLogin will reach sufficient maturity for local authority federation by Q3 2026.

**A-2**: At least 5 councils will volunteer as pathfinders for Phase 1 integration.

**A-3**: ICO will engage constructively with the data sharing regulatory sandbox approach.

**A-4**: Existing GDS platform APIs (Notify, Pay) will require minimal modification for local authority use.

**A-5**: DSIT will provide sustained programme funding for at least 3 years.

**Validation Plan**: Assumptions validated through early engagement with OneLogin team (A-1), LGA pathfinder recruitment (A-2), ICO pre-engagement (A-3), GDS platform technical review (A-4), and DSIT spending review submission (A-5).

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Councils using GDS Local platforms | 0 | 50 | Q4 2027 | Platform adoption tracker |
| Cross-service data sharing pilots | 0 | 3 use cases, 10 councils | Q2 2027 | Data sharing platform analytics |
| Cumulative council savings | £0 | £50M | 3 years | Independent savings audit |
| Community of practice members | 0 | 100+ councils | Q4 2026 | Community platform analytics |
| Citizen OneLogin authentications on council services | 0 | 200K/day | Q4 2028 | OneLogin analytics |

### Technical Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| Platform availability | 99.9% | Uptime monitoring |
| API response time (p95) | < 500ms (auth), < 2s (data sharing) | APM tooling |
| Error rate | < 0.1% | Log aggregation |
| Time to onboard new council | < 10 working days (self-service) | Onboarding tracker |
| Mean time to recovery (MTTR) | < 1 hour (critical systems) | Incident tracking |

### User Adoption Metrics

| Metric | Target | Timeline | Measurement Method |
|--------|--------|----------|-------------------|
| Council developer satisfaction | >4/5 | Ongoing | Developer survey |
| Citizen satisfaction with OneLogin on council services | >80% | Q4 2027 | GOV.UK satisfaction survey |
| Self-service onboarding success rate | >80% | Ongoing | Onboarding analytics |

---

## Dependencies and Risks

### Dependencies

| Dependency | Description | Owner | Target Date | Status | Impact if Delayed |
|------------|-------------|-------|-------------|--------|-------------------|
| GOV.UK OneLogin readiness | OneLogin platform ready for local authority federation | GDS OneLogin Team | Q3 2026 | On Track | HIGH — blocks G-1 |
| ICO sandbox engagement | ICO agrees to regulatory sandbox for data sharing pilots | GDS Local + ICO | Q2 2026 | On Track | HIGH — blocks G-2 |
| Pathfinder councils recruited | 5+ councils volunteer for Phase 1 | LGA + GDS Local | Q2 2026 | On Track | HIGH — blocks all goals |
| DSIT programme funding | 3-year funding confirmed | DSIT Finance | Q1 2026 | At Risk | CRITICAL — blocks programme |
| Crown Commercial Service alignment | CCS agrees to integrated purchasing framework | LGA + CCS | Q3 2026 | On Track | MEDIUM — blocks G-4 |

### Risks

| Risk ID | Description | Probability | Impact | Mitigation Strategy | Owner |
|---------|-------------|-------------|--------|---------------------|-------|
| R-1 | Insufficient council adoption | MEDIUM | HIGH | Pathfinder approach; demonstrate value early; funded onboarding support | GDS Local Programme Director |
| R-2 | Data sharing privacy incident | LOW | CRITICAL | Governance before technology; ICO sandbox; DPIAs; audit trails | MHCLG Digital Director |
| R-3 | GDS platform team capacity | HIGH | MEDIUM | Dedicated local gov capacity; prioritise OneLogin; open source contributions | GDS Director General |
| R-4 | "Whitehall imposing on councils" perception | MEDIUM | HIGH | LGA co-lead; council co-design; voluntary model; joint communications | LGA + GDS Local |
| R-5 | Supplier market disruption | MEDIUM | MEDIUM | Early market engagement; clear scope; open APIs; partnership positioning | GDS Local Programme Director |

---

## Requirement Conflicts & Resolutions

### Conflict C-1: Speed of Delivery vs. Council Autonomy

**Conflicting Requirements**:
- **BR-001**: Extend GDS platforms to 50 councils by Q4 2027 (MUST_HAVE)
- **BR-006**: Voluntary adoption model — no mandates (MUST_HAVE)

**Stakeholders Involved**:
- **DSIT Minister (SD-1)**: Wants visible progress — 50 councils is the commitment
- **LA Chief Executives (SD-4)**: Will not be mandated; adoption must be voluntary

**Nature of Conflict**: Achieving 50 council adoptions by Q4 2027 on a purely voluntary basis requires that shared platforms are compellingly better than alternatives. If value is not demonstrated quickly, the timeline may slip.

**Trade-off Analysis**:

| Option | Pros | Cons | Impact |
|--------|------|------|--------|
| **Option 1**: Set mandatory adoption | Fast adoption numbers | Destroys partnership model; LGA withdraws | Minister happy short-term; programme fails long-term |
| **Option 2**: Accept slower voluntary adoption | Trust maintained; sustainable | May miss Q4 2027 target | Minister frustrated; programme sustainable |
| **Option 3**: Pathfinder approach with funded support | Quick wins with willing councils; builds evidence | Higher cost; smaller initial numbers | Both partially satisfied |

**Resolution Strategy**: PHASE

**Decision**: Option 3 — Pathfinder councils with funded onboarding support. Start with 5 enthusiastic councils in Q2-Q3 2026, scale to 20 by end 2026, then use peer advocacy and demonstrated savings to reach 50 by Q4 2027.

**Decision Authority**: Programme Board (GDS DG + MHCLG Digital Director + LGA)

**Impact on Requirements**: BR-001 success criteria refined to include phased targets (5 → 20 → 50). FR-002 (onboarding portal) prioritised for funded onboarding workflow.

**Stakeholder Management**: Minister briefed on phased approach with pathfinder success stories as early evidence. LGA and councils reassured that voluntary model is maintained.

---

### Conflict C-2: Data Sharing Ambition vs. Privacy Governance

**Conflicting Requirements**:
- **FR-004**: Cross-service data sharing platform (MUST_HAVE)
- **NFR-C-001**: UK GDPR compliance with full DPIAs (MUST_HAVE)

**Stakeholders Involved**:
- **MHCLG (SD-3)**: Wants ambitious data sharing to improve citizen outcomes
- **ICO (SD-8)**: Requires robust governance before any data sharing proceeds

**Nature of Conflict**: Comprehensive data sharing governance (DPIAs, DSAs, ICO sandbox) takes time. MHCLG wants to demonstrate citizen benefit quickly. Rushing governance risks ICO enforcement.

**Resolution Strategy**: PHASE

**Decision**: Governance first, technology second. Q1-Q2 2026 focused on framework design with ICO sandbox. Pilot data sharing in Q3 2026 with 3 tightly scoped use cases. Scale only after ICO endorsement.

**Decision Authority**: MHCLG Digital Director with ICO advisory input

**Impact on Requirements**: FR-004 acceptance criteria include ICO endorsement as a gate. FR-005 (governance dashboard) elevated to MUST_HAVE.

---

### Conflict C-3: GDS Platform Standardisation vs. Council Diversity

**Conflicting Requirements**:
- **FR-001**: OneLogin federation via OIDC/SAML (MUST_HAVE)
- **INT-002**: Integration with diverse council systems (MUST_HAVE)

**Stakeholders Involved**:
- **GDS DG (SD-2)**: Wants councils to adopt standard GDS platform patterns
- **LA Digital/IT Directors (SD-5)**: Need integration with diverse existing systems; cannot replace everything

**Nature of Conflict**: GDS platforms are designed for a specific pattern. Council systems are diverse. Expecting councils to conform entirely to GDS patterns is unrealistic; fully adapting GDS platforms for every council system is unscalable.

**Resolution Strategy**: COMPROMISE

**Decision**: GDS Local provides standard integration patterns (OIDC, REST) with well-documented extension points. A "reference integration" is provided for 3-5 common council system types. Councils with non-standard systems receive community support via the community of practice.

**Decision Authority**: GDS Local Programme Director with council practitioner input

**Impact on Requirements**: FR-002 and FR-003 include "reference integrations" for common council platforms. NFR-U-002 (self-service onboarding) target adjusted to 80% (accepting 20% will need support).

---

### Conflict C-4: Shared Component Scope vs. Supplier Market

**Conflicting Requirements**:
- **BR-001**: Build shared components for common council needs (MUST_HAVE)
- Supplier ecosystem stability and council choice (implicit requirement from SD-10)

**Stakeholders Involved**:
- **GDS DG (SD-2)**: Wants to build shared components that displace duplicated supplier solutions
- **Technology Suppliers (SD-10)**: Want to protect existing revenue and contracts

**Resolution Strategy**: INNOVATE

**Decision**: GDS Local builds horizontal commodity capabilities (identity, notifications, payments, forms) and provides open APIs. Suppliers retain domain-specific solutions (housing management, social care, planning) and are encouraged to integrate with GDS Local via open APIs. Integration guides published for major council system suppliers.

**Decision Authority**: Programme Board

**Impact on Requirements**: FR-009 (API gateway) explicitly supports supplier integration. Market engagement requirements added to BR-004 process.

---

## Timeline and Milestones

### High-Level Milestones

| Milestone | Description | Target Date | Dependencies |
|-----------|-------------|-------------|--------------|
| Requirements Approval | Stakeholder sign-off on this document | Q1 2026 | This document |
| Community of Practice Launch | 100+ councils participating | Q4 2026 | LGA engagement |
| Pathfinder Councils Live | 5 councils integrated with OneLogin | Q3 2026 | OneLogin readiness |
| Data Sharing Framework Approved | ICO endorsement of governance framework | Q2 2027 | ICO sandbox |
| 50 Councils on GDS Local | OneLogin and/or shared components | Q4 2027 | Phased rollout |
| £50M Savings Milestone | Cumulative verified savings | Q4 2028 | Integrated purchasing |

---

## Budget

### Cost Estimate (Indicative — Subject to Spending Review)

| Category | Estimated Cost | Notes |
|----------|----------------|-------|
| Programme team (3 years) | £8-12M | 30-40 FTEs including secondees |
| Platform development | £5-8M | API gateway, data sharing platform, portals |
| Council onboarding support | £3-5M | Pathfinder funding, integration support |
| Community of practice | £1-2M | Platform, events, community management |
| Security and compliance | £1-2M | Pen testing, DPIA consultancy, NCSC reviews |
| **Total (3-year programme)** | **£18-29M** | |

### Ongoing Operational Costs

| Category | Annual Cost | Notes |
|----------|-------------|-------|
| Platform hosting and operations | £2-3M/year | Cloud infrastructure, monitoring, support |
| GDS platform usage (Notify, Pay, OneLogin) | Included in GDS budget | Free to councils |
| Community management | £0.5M/year | Dedicated community team |
| **Total** | **£2.5-3.5M/year** | |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| GDS Local Programme Director | Programme Delivery Lead | [ ] Approved | | |
| MHCLG Digital Director | Co-delivery Partner | [ ] Approved | | |
| LGA Digital Lead | Council Representative | [ ] Approved | | |
| GDS Platform Leads | Technical Feasibility | [ ] Approved | | |
| ICO Representative | Data Sharing Governance | [ ] Approved | | |
| NCSC Representative | Security Requirements | [ ] Approved | | |
| Pilot Council Representatives | End User Validation | [ ] Approved | | |

### Sign-Off

| Stakeholder | Signature | Date |
|-------------|-----------|------|
| GDS Director General (Programme Sponsor) | _________ | |
| MHCLG Digital Director (Co-sponsor) | _________ | |
| LGA Digital Lead (Partnership Lead) | _________ | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| DSIT | Department for Science, Innovation and Technology |
| GDS | Government Digital Service |
| MHCLG | Ministry of Housing, Communities and Local Government |
| LGA | Local Government Association |
| OneLogin | GOV.UK One Login — government single sign-on platform |
| DSA | Data Sharing Agreement |
| DPIA | Data Protection Impact Assessment |
| OIDC | OpenID Connect — identity federation standard |
| SAML | Security Assertion Markup Language — identity federation standard |
| ICO | Information Commissioner's Office |
| NCSC | National Cyber Security Centre |
| NAO | National Audit Office |
| TCoP | Technology Code of Practice |
| WCAG | Web Content Accessibility Guidelines |
| SLO | Service Level Objective |
| SLI | Service Level Indicator |

### Appendix B: Reference Documents

| Document | Document ID | Path |
|----------|------------|------|
| Architecture Principles (GDS Local) | ARC-000-PRIN-v1.1 | projects/000-global/ARC-000-PRIN-v1.1.md |
| Stakeholder Drivers & Goals | ARC-001-STKE-v1.0 | projects/001-gds-local/ARC-001-STKE-v1.0.md |
| GDS Local Guidance | — | gov.uk/guidance/gds-local |
| GDS Service Standard | — | gov.uk/service-manual/service-standard |
| Technology Code of Practice | — | gov.uk/guidance/the-technology-code-of-practice |

### Appendix C: Requirements Traceability to Stakeholder Goals

| Requirement | Stakeholder Goal | Stakeholder Driver |
|-------------|-----------------|-------------------|
| BR-001 | G-1 (OneLogin 50 councils), G-3 (Shared components) | SD-1, SD-2, SD-4, SD-5 |
| BR-002 | G-2 (Data sharing framework) | SD-3, SD-7, SD-8 |
| BR-003 | G-4 (£50M savings) | SD-4, SD-9 |
| BR-004 | G-6 (Community of practice), G-3 | SD-5, SD-6 |
| BR-005 | G-5 (Service Standard) | SD-1, SD-7, SD-11 |
| BR-006 | G-6 (Community) | SD-4, SD-6 |
| FR-001 | G-1 (OneLogin) | SD-2, SD-7 |
| FR-004 | G-2 (Data sharing) | SD-3, SD-8 |
| FR-007 | G-4 (Savings) | SD-4, SD-9 |
| NFR-SEC-002 | G-2 (Data sharing — secure) | SD-8, SD-11 |
| NFR-C-001 | G-2 (Data sharing — lawful) | SD-8 |
| NFR-C-002 | G-5 (Accessibility) | SD-7 |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-000-PRIN-v1.1 | Architecture Principles | ArcKit | 25 principles including GDS Local collaboration, data sharing, federated identity | projects/000-global/ARC-000-PRIN-v1.1.md |
| ARC-001-STKE-v1.0 | Stakeholder Analysis | ArcKit | 11 drivers, 6 goals, 4 outcomes, 4 conflicts, 5 risks | projects/001-gds-local/ARC-001-STKE-v1.0.md |
| GDS Local Guidance | Programme | GOV.UK | Programme purpose, 3 strategic focus areas | gov.uk/guidance/gds-local |

---

**Generated by**: ArcKit `/arckit:requirements` command
**Generated on**: 2026-02-16
**ArcKit Version**: 2.4.5
**Project**: GDS Local (Project 001)
**AI Model**: Claude Opus 4.6
**Generation Context**: Requirements derived from ARC-001-STKE-v1.0 (stakeholder analysis) and ARC-000-PRIN-v1.1 (architecture principles), informed by GDS Local programme context from gov.uk/guidance/gds-local.
