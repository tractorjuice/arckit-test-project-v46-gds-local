# GDS Local Enterprise Architecture Principles

> **Template Status**: Live | **Version**: 2.4.5 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.1 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | GDS Local (Project 000) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.1 |
| **Created Date** | 2026-02-16 |
| **Last Modified** | 2026-02-16 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-05-16 |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Architecture Team, Development Teams, Senior Leadership, Local Authority Partners |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-16 | ArcKit AI | Initial creation from `/arckit:principles` command | PENDING | PENDING |
| 1.1 | 2026-02-16 | ArcKit AI | Enriched with GDS Local programme context from gov.uk/guidance/gds-local. Added principles for Central-Local Collaboration (P8), Cross-Service Data Sharing (P9), Federated Identity (P10). Enhanced existing principles with GDS Local-specific implications for shared technology components, integrated purchasing, and GOV.UK platform extension to local authorities. Total principles: 25 (up from 22). | PENDING | PENDING |

---

## Executive Summary

This document establishes the architecture principles governing all technology decisions for the **GDS Local** programme. GDS Local is a unit within the Government Digital Service (GDS), directed by the Department for Science, Innovation and Technology (DSIT), established to **strengthen collaboration between central and local government**, share learning and innovation, and improve digital services for citizens and communities across the UK.

The programme has three strategic focus areas:
1. **Local Government Technology Vision** — Developing shared technology products and components with MHCLG, LGA, and practitioners, with an integrated purchasing approach
2. **Data Access Improvement** — Dismantling barriers to cross-service data sharing (e.g., housing departments accessing health and social care data to support vulnerable populations while maintaining privacy)
3. **GDS Product Availability** — Extending GDS platforms (GOV.UK App, GOV.UK OneLogin) to local authorities for single sign-on and identity verification across central and local government

These principles align with the **GDS Service Standard** (14 points), the **Technology Code of Practice (TCoP)**, and the **UK Government Digital, Data and Technology (DDaT) profession framework**. They incorporate UK-specific requirements including the **Public Sector Bodies Accessibility Regulations 2018**, **UK GDPR**, and **NCSC Cyber Security guidance**.

**Scope**: All technology projects, systems, and initiatives within GDS Local and partner local authorities
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the documented exception process

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

---

## I. Strategic Principles

### 1. User Needs First

**Principle Statement**:
All systems MUST be designed around validated user needs, not organisational structures, technology preferences, or assumptions. User needs span both central and local government contexts.

**Rationale**:
The GDS Service Standard requires understanding user needs (Point 1). GDS Local serves multiple user groups: citizens accessing local services, local authority officers delivering services, and central government teams coordinating policy. Services that do not meet real user needs waste public money and erode trust in government digital services.

**GDS Service Standard Alignment**: Point 1 — Understand users and their needs

**GDS Local Context**:
- User research must cover citizens in diverse local authority areas with varying needs
- Local authority officers have different workflows, systems, and constraints to central government
- Architecture must support the "whole problem" across organisational boundaries (Point 2)
- Citizens should not need to understand whether a service is provided by central or local government

**Implications**:
- User research informs all architecture decisions across both governance tiers
- Services are designed around user journeys, not back-office or organisational boundaries
- Accessibility is a core architectural requirement, not an afterthought
- Performance budgets are set based on user expectations and device capabilities
- Architecture supports iterative delivery based on user feedback
- Research includes users from councils of different sizes and geographies (metropolitan, rural, unitary, county/district)

**Validation Gates**:
- [ ] User research conducted with citizens AND local authority officers
- [ ] Architecture supports the identified user journeys across central-local boundaries
- [ ] Performance meets user expectations across all supported devices
- [ ] Feedback mechanisms built into the service for continuous improvement
- [ ] Architecture supports A/B testing and iterative improvement
- [ ] Research covers diverse council types and demographics

---

### 2. Scalability and Elasticity

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on load across 300+ local authorities.

**Rationale**:
GDS Local services will serve citizens across hundreds of local authorities. Demand patterns vary by council size, geography, and time (e.g., council tax deadlines, planning consultation periods, seasonal services). Systems must handle these variations without manual intervention or degraded user experience.

**GDS Local Context**:
- Services must scale to support all 333 councils in England (plus devolved administrations if applicable)
- Demand is not uniform — metropolitan councils have vastly different load profiles to rural districts
- Onboarding new councils must not require architectural changes
- Shared components must handle aggregate load from all participating authorities

**Implications**:
- Design for stateless components that can be replicated
- Avoid hard-coded limits or fixed capacity assumptions
- Plan for distributed deployment across multiple compute nodes
- Use load balancing to distribute traffic across instances
- Implement auto-scaling based on demand metrics
- Design for cost-efficient scaling — public money must be spent wisely
- Multi-tenancy architecture to efficiently serve many authorities from shared infrastructure

**Validation Gates**:
- [ ] System can scale horizontally (add more instances)
- [ ] No single points of failure that limit scaling
- [ ] Load testing demonstrates capacity growth with added resources
- [ ] Scaling metrics and triggers defined
- [ ] Cost model accounts for variable capacity
- [ ] Tested with representative load across multiple simulated authorities

---

### 3. Resilience and Fault Tolerance

**Principle Statement**:
All systems MUST gracefully degrade when dependencies fail and recover automatically without data loss or manual intervention.

**Rationale**:
Failures are inevitable in distributed systems. Government services are relied upon by citizens and must be available when needed. The architecture must assume failures will occur and design for resilience rather than perfect reliability.

**GDS Local Context**:
- Failure in a shared component must not cascade to affect all participating local authorities
- Local authorities have varying levels of technical capability to respond to outages
- Integration points between central and local systems are additional failure surfaces

**Implications**:
- Implement circuit breakers for external dependencies
- Use timeouts on all network calls
- Retry with exponential backoff for transient failures
- Graceful degradation when non-critical services fail
- Automated health checks and recovery
- Avoid cascading failures through bulkhead isolation
- Maintain offline or alternative service channels where appropriate
- Tenant-level isolation to prevent noisy-neighbour effects

**Validation Gates**:
- [ ] Failure modes identified and mitigated
- [ ] Chaos engineering or fault injection testing performed
- [ ] Recovery Time Objective (RTO) and Recovery Point Objective (RPO) defined
- [ ] Automated failover tested
- [ ] Degraded mode behaviour documented
- [ ] Cross-authority blast radius assessed and contained

---

### 4. Interoperability and Open Standards

**Principle Statement**:
All systems MUST expose functionality through well-defined, versioned interfaces using open standards. Proprietary protocols and direct database access across system boundaries are prohibited. Central-local government integration MUST use published, open APIs.

**Rationale**:
The Technology Code of Practice requires use of open standards. GDS Local's core mission is interoperability between central and local government. Loose coupling through standard interfaces enables independent evolution, avoids vendor lock-in, and makes shared components genuinely reusable across diverse local authority technology estates.

**GDS Service Standard Alignment**: TCoP Point 6 — Make things accessible and use open standards

**GDS Local Context**:
- Local authorities use a wide diversity of technology stacks, suppliers, and platforms
- Shared components must integrate with this diversity via open standards — not mandate specific technology
- The integrated purchasing approach requires vendor-neutral, standards-based interfaces
- Data exchange between central and local government must follow published schemas
- GOV.UK OneLogin integration requires standards-based identity federation

**Implications**:
- Use open, standardised protocols (HTTP, REST, GraphQL, message queuing, event streaming)
- Version all interfaces with backward compatibility strategy
- Publish interface specifications (API contracts, event schemas)
- No direct database access across system boundaries
- Asynchronous communication for non-real-time interactions
- Prefer open data formats (JSON, CSV, ODF) over proprietary formats
- APIs designed for consumption by councils with varying technical maturity
- Self-service API documentation with sandbox environments for local authority developers

**Validation Gates**:
- [ ] Interface specifications published (OpenAPI, AsyncAPI, GraphQL schema)
- [ ] Open standards used — proprietary protocols justified if used
- [ ] Versioning strategy defined
- [ ] Authentication and authorisation model documented
- [ ] Error handling and retry behaviour specified
- [ ] No direct database coupling across systems
- [ ] API sandbox available for local authority integration testing

---

### 5. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles aligned to NCSC guidance. Security is NOT a feature to be added later — it is a foundational requirement. Cross-organisational data sharing MUST implement appropriate access controls and audit trails.

**Rationale**:
Government systems handle citizen data and provide essential services. GDS Local introduces additional security considerations: data flows cross organisational boundaries between central and local government, shared components create shared attack surfaces, and federated identity spans governance tiers.

**GDS Service Standard Alignment**: Point 9 — Create a secure service which protects users' privacy

**GDS Local Context**:
- Cross-organisational data sharing (e.g., housing accessing health data) requires strong access controls, purpose limitation, and audit trails
- Shared components serve multiple authorities — compromise of one must not expose others
- GOV.UK OneLogin integration requires secure identity federation across governance tiers
- Local authorities have varying security maturity — shared platforms must enforce a baseline

**Zero Trust Pillars**:
1. **Identity-Based Access**: No network-based trust; every request authenticated
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible
3. **Encryption Everywhere**: Data encrypted in transit and at rest
4. **Continuous Verification**: Monitor, log, and analyse all access patterns

**Mandatory Controls**:
- [ ] Multi-factor authentication for all human access
- [ ] Service-to-service authentication (mutual TLS, signed tokens, or equivalent)
- [ ] Secrets management via secure vault (never in code or config files)
- [ ] Network segmentation with minimal trust zones
- [ ] Encryption at rest for all data stores
- [ ] Encrypted transport for all network communication
- [ ] Structured logging of all authentication/authorisation events
- [ ] Regular security testing (penetration testing, vulnerability scanning)
- [ ] NCSC Secure by Design principles applied throughout
- [ ] Tenant isolation enforced — authority A cannot access authority B's data
- [ ] Cross-organisational data access logged with purpose and legal basis

**Compliance Frameworks**:
- NCSC Cyber Assessment Framework (CAF)
- NCSC 10 Steps to Cyber Security
- ISO 27001
- UK GDPR (data protection controls)
- Cyber Essentials Plus (minimum baseline for all participating organisations)

**Exceptions**:
- NONE. Security principles are non-negotiable.
- Specific control implementations may vary with compensating controls approved by the SIRO.

**Validation Gates**:
- [ ] Threat model completed and reviewed (including cross-authority threats)
- [ ] Security controls mapped to requirements
- [ ] Security testing plan defined
- [ ] Incident response runbook created (including cross-authority incident coordination)
- [ ] NCSC Secure by Design checklist completed
- [ ] Tenant isolation verified through security testing

---

### 6. Accessibility by Default (NON-NEGOTIABLE)

**Principle Statement**:
All user-facing systems MUST meet WCAG 2.2 AA standards and comply with the Public Sector Bodies Accessibility Regulations 2018. Accessibility is a legal requirement, not an enhancement.

**Rationale**:
The Public Sector Bodies (Websites and Mobile Applications) Accessibility Regulations 2018 require public sector digital services to be accessible. The GDS Service Standard (Point 5) mandates accessibility. Approximately 1 in 5 people in the UK have a disability. GDS Local services reach citizens across all communities including those with higher proportions of disabled and elderly residents.

**GDS Service Standard Alignment**: Point 5 — Make sure everyone can use the service

**GDS Local Context**:
- Local authority services often serve populations with higher accessibility needs (elderly, disabled, low digital literacy)
- Shared components must be accessible by default — local authorities should not need to add accessibility after integration
- GOV.UK Design System patterns provide tested, accessible components
- Assisted digital channels must be supported for users who cannot use digital services independently

**Mandatory Requirements**:
- WCAG 2.2 Level AA compliance for all user-facing interfaces
- Accessibility statements published and maintained
- Regular accessibility audits (automated and manual)
- Assistive technology testing (screen readers, voice recognition, switch access)
- Progressive enhancement — core functionality works without JavaScript
- GOV.UK Design System patterns used where applicable

**Implications**:
- Architecture supports progressive enhancement
- Content delivery is not dependent on specific client capabilities
- APIs return structured data that can be rendered accessibly
- Performance budgets account for assistive technology overhead
- Multi-channel access supported (web, mobile, assisted digital)

**Exceptions**:
- NONE. Accessibility is a legal requirement.
- Exemptions only as defined in the Accessibility Regulations (pre-September 2018 content, live audio/video, third-party content not funded/controlled)

**Validation Gates**:
- [ ] WCAG 2.2 AA compliance tested (automated and manual)
- [ ] Accessibility statement published
- [ ] Assistive technology testing completed
- [ ] Progressive enhancement implemented
- [ ] Accessibility audit scheduled in release cycle
- [ ] GOV.UK Design System patterns used where applicable

---

### 7. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning across the shared platform and individual authority contexts.

**Rationale**:
We cannot operate what we cannot observe. GDS Local shared components serve multiple authorities — operational visibility must span the platform while respecting data boundaries. Local authorities need visibility into their own service performance.

**GDS Service Standard Alignment**: Point 14 — Operate a reliable service

**GDS Local Context**:
- Platform-level observability for shared component health
- Per-authority dashboards showing service performance for each council
- Cross-authority aggregated metrics for programme-level reporting
- Performance data published in line with Point 10 of the Service Standard
- Anomaly detection across authorities (one council experiencing issues may indicate broader problems)

**Telemetry Requirements**:
- **Logging**: Structured logs with correlation IDs and authority context (ensure no PII in logs)
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates — per authority and aggregate
- **Tracing**: Distributed trace context for request flows across central-local boundaries
- **Alerting**: Service Level Objective (SLO)-based alerting with actionable runbooks

**Required Instrumentation**:
- Request volume, latency distribution, error rate (per authority and aggregate)
- Resource utilisation (CPU, memory, I/O, network)
- Business metrics (transactions, service completions, user drop-off points)
- Security events (auth failures, policy violations, suspicious patterns)
- Cross-authority adoption and usage metrics

**Log Retention**:
- **Security/audit logs**: 7 years (aligned with UK regulatory requirements)
- **Application logs**: 90 days minimum
- **Metrics**: 2 years with aggregation for trend analysis

**Validation Gates**:
- [ ] Logging, metrics, tracing instrumented
- [ ] Dashboards and alerts configured (platform and per-authority)
- [ ] Service Level Objectives (SLOs) and Service Level Indicators (SLIs) defined
- [ ] Runbooks created for common failure scenarios
- [ ] Capacity planning metrics tracked
- [ ] No PII present in log outputs
- [ ] Performance data publishable for Service Standard Point 10

---

## II. Central-Local Collaboration Principles

### 8. Central-Local Government Collaboration by Design

**Principle Statement**:
All shared technology products and components MUST be co-designed with local government practitioners, the Local Government Association (LGA), and MHCLG. Architecture MUST support collaboration across governance tiers without mandating uniformity.

**Rationale**:
GDS Local exists to strengthen partnerships between central and local government. Technology designed centrally without local input fails to account for the diversity of local authority needs, existing systems, and operational contexts. Co-design ensures shared components are genuinely useful across the 333 councils in England.

**GDS Local Programme Alignment**: Strategic Focus Area 1 — Local Government Technology Vision

**Implications**:
- Architecture decisions informed by practitioner input from diverse council types
- Shared components must be configurable to local authority contexts without forking
- Standards are unified across sectors but implementation flexibility is preserved
- Design for "adopt and adapt" — councils can integrate shared components into existing systems
- Innovation pathways allow councils to contribute back improvements and learning
- Community of practice infrastructure supports knowledge sharing between authorities

**Validation Gates**:
- [ ] Local authority practitioners involved in requirements and design
- [ ] Architecture tested with councils of different sizes and technical maturity
- [ ] Configuration supports local authority customisation without code changes
- [ ] Contribution and feedback mechanisms available to participating councils
- [ ] Learning and innovation sharing infrastructure in place

---

### 9. Cross-Service Data Sharing with Privacy Protection

**Principle Statement**:
Architecture MUST enable cross-service data sharing to improve citizen outcomes while maintaining strict privacy protections, purpose limitation, and transparency. Data sharing MUST have a lawful basis, clear governance, and citizen trust at its core.

**Rationale**:
GDS Local's second strategic priority is dismantling obstacles preventing information sharing across services. For example, housing departments need access to health and social care information to support vulnerable populations. However, this data sharing must maintain privacy protections and citizen trust. The architecture must make safe data sharing easy and unsafe data sharing hard.

**GDS Local Programme Alignment**: Strategic Focus Area 2 — Data Access Improvement

**Implications**:
- Data sharing agreements defined and enforced architecturally (not just by policy)
- Purpose limitation enforced technically — data accessed only for authorised purposes
- Consent management where consent is the lawful basis for processing
- Fine-grained access controls: authority A's housing team can access relevant health data, but not all health data for all purposes
- Audit trail of all cross-service data access (who, what, when, why, lawful basis)
- Data minimisation — share only what is necessary, not entire datasets
- Privacy-enhancing technologies evaluated (differential privacy, secure computation, data clean rooms)
- Citizens can understand and, where applicable, control how their data is shared

**Data Sharing Governance**:
- Data Sharing Agreements (DSAs) required for all cross-organisational flows
- Data Protection Impact Assessments (DPIAs) mandatory for new sharing arrangements
- Information Asset Owners identified for each data domain
- Regular review of sharing arrangements for continued necessity and proportionality

**Validation Gates**:
- [ ] Lawful basis documented for each data sharing arrangement
- [ ] Data Sharing Agreements in place before technical integration
- [ ] DPIA completed for cross-service data flows
- [ ] Purpose limitation enforced technically (not just by policy)
- [ ] Access audit trail captures who, what, when, why, and lawful basis
- [ ] Data minimisation applied — only necessary data shared
- [ ] Citizen transparency: privacy notices explain cross-service sharing

---

### 10. Federated Identity and Single Sign-On

**Principle Statement**:
Architecture MUST support federated identity enabling citizens to use a single verified identity across central and local government services. Identity federation MUST use open standards and not mandate a single technology.

**Rationale**:
GDS Local's third strategic priority is making GDS platforms (GOV.UK App, GOV.UK OneLogin) accessible to local authorities. Citizens should be able to use single sign-on and identity verification across both governance levels. This requires federated identity architecture that respects local authority autonomy while providing a seamless citizen experience.

**GDS Local Programme Alignment**: Strategic Focus Area 3 — GDS Product Availability

**Implications**:
- Identity federation using open standards (SAML, OpenID Connect, OAuth 2.0)
- Local authorities can integrate with GOV.UK OneLogin without replacing existing identity systems
- Identity assurance levels (low, medium, high) supported based on service risk
- Citizen identity verified once, reused across services (with consent)
- Local authorities retain control over authorisation (who can access their services) while delegating authentication
- Architecture supports phased adoption — councils can integrate at their own pace
- Fallback mechanisms for councils not yet integrated with federated identity

**Validation Gates**:
- [ ] Identity federation uses open standards (SAML, OIDC, OAuth 2.0)
- [ ] GOV.UK OneLogin integration path documented
- [ ] Identity assurance levels mapped to service risk
- [ ] Local authority authorisation independence preserved
- [ ] Phased adoption supported — services work for both federated and non-federated councils
- [ ] Fallback authentication for authorities not yet onboarded

---

## III. Data Principles

### 11. Data Sovereignty and UK GDPR Compliance

**Principle Statement**:
Data classification, residency, retention, and access controls MUST comply with UK GDPR, the Data Protection Act 2018, and the UK Government Security Classifications policy.

**Rationale**:
Government holds sensitive citizen data. GDS Local's cross-service data sharing ambition makes data governance even more critical. The UK GDPR and Data Protection Act 2018 impose strict requirements on data processing. The UK Government Security Classifications policy (OFFICIAL, SECRET, TOP SECRET) governs information handling.

**UK Government Security Classifications**:
1. **OFFICIAL**: The majority of government information — routine business, public services
2. **OFFICIAL-SENSITIVE**: OFFICIAL information requiring additional handling controls
3. **SECRET**: Sensitive information requiring enhanced protection
4. **TOP SECRET**: The most sensitive information requiring the highest levels of protection

**GDS Local Context**:
- Cross-authority data sharing introduces data controller/processor relationships that must be clearly defined
- Joint controllership may apply where central and local government jointly determine processing purposes
- Each local authority remains a data controller for their own citizen data
- Shared platforms must support multiple data controllers with independent data governance

**Data Residency**:
- Personal data of UK citizens MUST be processed and stored in jurisdictions with UK adequacy decisions
- OFFICIAL data SHOULD be stored within UK sovereign data centres where practical
- Cross-border data transfers require legal basis (UK adequacy decisions, International Data Transfer Agreements)
- Data sovereignty requirements documented for each data store

**Data Retention**:
- Automatic deletion after defined retention period
- Legal hold process for litigation/investigation
- Backup retention aligned with compliance and recovery requirements
- Data minimisation — only collect and retain data that is necessary

**Validation Gates**:
- [ ] Data classification performed using UK Government Security Classifications
- [ ] Residency requirements mapped to infrastructure
- [ ] Retention policies configured with automated deletion
- [ ] Access controls enforce least privilege and need-to-know
- [ ] Data Protection Impact Assessment (DPIA) completed for high-risk processing
- [ ] Lawful basis for processing documented for each data type
- [ ] Data controller/processor relationships defined for shared components

---

### 12. Data Quality and Lineage

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability and troubleshooting.

**Rationale**:
Government decisions and services depend on accurate data. GDS Local's cross-service data sharing means that poor data quality in one authority's system can affect service delivery in another. Data lineage is essential for understanding where data came from and how it was transformed.

**Quality Standards**:
- **Completeness**: No unexpected nulls in required fields
- **Consistency**: Cross-system data reconciliation
- **Accuracy**: Validation rules and constraints enforced at source
- **Timeliness**: Freshness Service Level Agreements (SLAs) defined and monitored

**GDS Local Context**:
- Data quality standards must be agreed across participating authorities
- Source authority data quality directly affects consuming authority's service quality
- Data quality metrics published per sharing arrangement
- Remediation responsibilities clearly assigned (source authority fixes quality issues)

**Lineage Requirements**:
- Source-to-target mapping documented for all data flows
- Transformation logic version-controlled and reviewable
- Data quality metrics tracked per pipeline
- Impact analysis capability for schema changes

**Validation Gates**:
- [ ] Data quality rules defined and automated
- [ ] Lineage metadata captured and queryable
- [ ] Data contracts between producers and consumers
- [ ] Schema evolution strategy documented
- [ ] Cross-authority data quality responsibilities assigned

---

### 13. Single Source of Truth

**Principle Statement**:
Every data domain MUST have a single authoritative source. Derived copies must be clearly labelled and synchronised. In cross-authority sharing, the originating authority remains the authoritative source.

**Rationale**:
Multiple authoritative sources create inconsistency, reconciliation overhead, and data integrity issues. GDS Local's data sharing model must be clear about which authority owns which data — consuming authorities receive derived copies, not co-ownership.

**Implications**:
- Identify the system of record for each data domain
- Derived/cached copies are read-only and clearly labelled as such
- Synchronisation strategy defined for all derived copies
- Avoid bidirectional synchronisation (creates split-brain scenarios)
- Use government registers as authoritative sources where they exist
- Cross-authority data access should query the source where possible rather than replicating

**Validation Gates**:
- [ ] System of record identified for each data entity
- [ ] Derived copies documented with sync frequency
- [ ] No bidirectional sync without conflict resolution strategy
- [ ] Master data management (MDM) strategy for shared reference data
- [ ] Cross-authority data flows clearly identify source authority as authoritative

---

## IV. Integration Principles

### 14. Loose Coupling

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, avoiding shared databases, file systems, or tight runtime dependencies. This is especially critical for central-local government integration where systems evolve independently.

**Rationale**:
Loose coupling enables independent deployment, technology diversity, team autonomy, and system evolution without breaking dependencies. Local authorities must be able to update their systems without breaking integration with shared GDS Local components, and vice versa.

**GDS Service Standard Alignment**: Point 11 — Choose the right tools and technology

**GDS Local Context**:
- Local authorities have diverse technology estates — shared components cannot assume specific technology stacks
- Central platform changes must not break local authority integrations
- Local authority system upgrades must not break central platform integration
- Versioned APIs with backward compatibility are essential across governance boundaries

**Implications**:
- Communicate through published APIs or asynchronous events
- No direct database access across system boundaries
- Each system manages its own data lifecycle
- Shared libraries kept minimal (favour duplication over coupling)
- Avoid distributed transactions across systems
- Services can be replaced independently without affecting the wider ecosystem
- API versioning with deprecation notices and migration support

**Validation Gates**:
- [ ] Systems communicate via APIs or events, not databases
- [ ] No shared mutable state
- [ ] Each system has independent data store
- [ ] Deployment of one system does not require deployment of another
- [ ] Interface changes versioned with backward compatibility
- [ ] API deprecation policy defined with migration support period

---

### 15. Asynchronous Communication

**Principle Statement**:
Systems SHOULD use asynchronous communication for non-real-time interactions to improve resilience and decoupling.

**Rationale**:
Asynchronous patterns reduce temporal coupling, improve fault tolerance, and enable better scalability. This is particularly important for GDS Local where integration spans organisational boundaries and local authority systems have varying availability and responsiveness.

**When to Use Async**:
- Non-real-time business processes (application processing, batch jobs)
- Event notification and pub/sub patterns
- Long-running operations that do not require immediate response
- Integration with unreliable or slow external systems
- Cross-authority data synchronisation and notification

**When Synchronous is Acceptable**:
- Real-time user interactions requiring immediate feedback
- Query operations (read-only, idempotent)
- Transactions requiring immediate consistency

**Validation Gates**:
- [ ] Async patterns used for non-real-time flows
- [ ] Message durability and delivery guarantees defined
- [ ] Event schemas versioned and published
- [ ] Dead letter queues and error handling configured

---

### 16. Reuse Government Platforms and Shared Components

**Principle Statement**:
Systems MUST evaluate and reuse existing GDS platforms and GDS Local shared components before building bespoke solutions. Local authorities SHOULD adopt shared technology products developed through the GDS Local programme.

**Rationale**:
The Technology Code of Practice requires government to reuse and share technology. GDS Local specifically develops shared technology products and components for central-local reuse. Using shared components reduces cost, improves quality, and creates consistency across government.

**GDS Service Standard Alignment**: TCoP Point 4 — Make use of open standards and common platforms

**GDS Local Context**:
- GOV.UK App and GOV.UK OneLogin are being extended to local authorities — adopt where applicable
- Shared components developed through GDS Local are designed for central-local reuse
- The integrated purchasing approach means shared procurement for common needs
- Local authorities contribute requirements and feedback to improve shared components

**GDS Platforms to Evaluate**:
- **GOV.UK OneLogin**: Federated identity and single sign-on for citizens across central and local government
- **GOV.UK App**: Citizen-facing application for accessing government services
- **GOV.UK Notify**: Notifications (email, SMS, letters) — already available to local authorities
- **GOV.UK Pay**: Payment processing for government services
- **GOV.UK Forms**: Form building for service teams
- **GOV.UK Design System**: Accessible design patterns and components

**GDS Local Shared Components** (as developed):
- Shared data exchange components for cross-service data sharing
- Common integration adapters for local authority systems
- Reusable service patterns for common local government processes

**Validation Gates**:
- [ ] GDS platform options evaluated and documented
- [ ] GDS Local shared components evaluated
- [ ] Justification provided if government platform or shared component not used
- [ ] Integration with government platforms uses published APIs
- [ ] New capabilities assessed for reuse potential across authorities
- [ ] Contribution to shared component library where improvements identified

---

## V. Quality Attributes

### 17. Performance and Efficiency

**Principle Statement**:
All systems MUST meet defined performance targets under expected load with efficient use of computational resources. Public money must not be wasted on over-provisioned or inefficient infrastructure.

**Rationale**:
GDS Local services serve citizens across hundreds of local authorities. Poor performance erodes trust and excludes users on slower connections or older devices. Shared components must perform well under aggregate load from all participating authorities.

**Performance Targets** (define for each system):
- **Response Time**: p50, p95, p99 latency targets
- **Throughput**: Requests per second, transactions per minute
- **Concurrency**: Simultaneous user/request capacity
- **Resource Efficiency**: CPU/memory utilisation targets
- **Page Weight**: Frontend payload budgets for inclusive performance

**Implications**:
- Performance requirements defined before implementation
- Load testing performed before production deployment
- Performance monitoring continuous, not just point-in-time
- Optimise hot paths identified through profiling
- Caching strategies for expensive operations
- Consider users on slow connections and older devices
- Multi-authority aggregate load testing

**Validation Gates**:
- [ ] Performance requirements defined with measurable targets
- [ ] Load testing performed at expected capacity (including multi-authority aggregate)
- [ ] Performance metrics monitored in production
- [ ] Capacity planning model defined

---

### 18. Availability and Reliability

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss.

**Rationale**:
Government services are relied upon by citizens and businesses. GDS Local shared components have amplified availability impact — an outage affects services across all participating authorities simultaneously.

**GDS Service Standard Alignment**: Point 14 — Operate a reliable service

**Availability Targets** (define for each system):
- **Uptime SLA**: e.g., 99.9% (43.8 min downtime/month), 99.95%, 99.99%
- **Recovery Time Objective (RTO)**: Maximum acceptable downtime
- **Recovery Point Objective (RPO)**: Maximum acceptable data loss

**High Availability Patterns**:
- Redundancy across availability zones / data centres
- Automated health checks and failover
- Active-active or active-passive configurations
- Regular disaster recovery testing

**Validation Gates**:
- [ ] Availability SLA defined
- [ ] RTO and RPO requirements documented
- [ ] Redundancy strategy implemented
- [ ] Failover tested regularly
- [ ] Backup and restore procedures validated

---

### 19. Maintainability and Evolvability

**Principle Statement**:
All systems MUST be designed for change, with clear separation of concerns, modular architecture, and comprehensive documentation.

**Rationale**:
Government policy changes frequently. GDS Local's collaborative model means shared components must evolve based on input from multiple authorities. Design decisions should optimise for understandability and modifiability, enabling rapid response to policy changes and community needs.

**Implications**:
- Modular architecture with clear boundaries
- Separation of concerns (business logic, data access, presentation)
- Code is self-documenting with meaningful names
- Architecture Decision Records (ADRs) for significant choices
- Automated testing to enable confident refactoring
- Consider long-term supportability — avoid niche technologies that may lack future support
- Configuration-driven behaviour to support local authority customisation

**Validation Gates**:
- [ ] Architecture documentation exists and is current
- [ ] Module boundaries clear with defined responsibilities
- [ ] Automated test coverage enables safe refactoring
- [ ] Architecture Decision Records (ADRs) document key choices

---

## VI. Development Practices

### 20. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines.

**Rationale**:
Manual infrastructure changes create drift, inconsistency, and undocumented state. Infrastructure as Code (IaC) enables repeatability, auditability, and disaster recovery. It also supports rapid provisioning for new local authority environments.

**Implications**:
- All infrastructure defined in declarative code
- Infrastructure changes go through code review
- Environments are reproducible from code
- No manual changes to production infrastructure
- Infrastructure versioned alongside application code

**Validation Gates**:
- [ ] Infrastructure defined as code
- [ ] Infrastructure code version-controlled
- [ ] Automated deployment pipeline for infrastructure
- [ ] No manual infrastructure changes in production

---

### 21. Automated Testing

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment to production.

**Rationale**:
Government services must be reliable. GDS Local shared components have amplified impact — a defect affects all participating authorities. Automated testing provides confidence in changes and enables the rapid, iterative delivery approach required by the GDS Service Standard.

**Test Pyramid**:
- **Unit Tests**: Fast, isolated, high coverage (70-80% of tests)
- **Integration Tests**: Test component interactions (15-20% of tests)
- **End-to-End Tests**: Critical user journeys (5-10% of tests)

**Required Test Types**:
- Functional tests (does it work?)
- Performance tests (is it fast enough?)
- Security tests (is it secure?)
- Accessibility tests (is it accessible?)
- Resilience tests (does it handle failures?)
- Multi-tenancy tests (does authority isolation work?)

**Validation Gates**:
- [ ] Automated tests exist and pass before merge
- [ ] Test coverage meets defined thresholds
- [ ] Critical paths have end-to-end tests
- [ ] Accessibility tests included in CI pipeline
- [ ] Performance tests run regularly
- [ ] Tenant isolation tested

---

### 22. Continuous Integration and Deployment

**Principle Statement**:
All code changes MUST go through automated build, test, and deployment pipelines with quality gates at each stage.

**Rationale**:
The GDS Service Standard requires frequent, iterative releases. Automated pipelines reduce risk, improve quality, and enable rapid response to user needs and security vulnerabilities.

**GDS Service Standard Alignment**: Point 8 — Iterate and improve frequently

**Pipeline Stages**:
1. **Source Control**: All changes committed to version control (open source by default)
2. **Build**: Automated compilation and packaging
3. **Test**: Automated test execution (including accessibility and tenant isolation)
4. **Security Scan**: Dependency and code vulnerability scanning
5. **Deployment**: Automated deployment to environments

**Quality Gates**:
- All tests must pass (functional, accessibility, security, tenant isolation)
- No critical security vulnerabilities
- Code review approval required
- Deployment requires production readiness checklist

**Validation Gates**:
- [ ] Automated CI/CD pipeline exists
- [ ] Pipeline includes security scanning
- [ ] Pipeline includes accessibility testing
- [ ] Deployment is automated and repeatable
- [ ] Rollback capability tested

---

### 23. Open Source by Default

**Principle Statement**:
All new source code SHOULD be made open unless there is a clear, documented reason not to. Existing open source solutions SHOULD be evaluated before building bespoke. GDS Local shared components SHOULD be published as open source to enable adoption and contribution by local authorities.

**Rationale**:
The GDS Service Standard and Technology Code of Practice require government code to be open by default. Open source enables transparency, collaboration, and reuse across government. GDS Local's collaborative model is strengthened when shared components are openly available.

**GDS Service Standard Alignment**: Point 12 — Make new source code open

**GDS Local Context**:
- Open source shared components allow local authorities to inspect, understand, and contribute
- Transparency builds trust in the central-local collaboration
- Open source licensing enables councils to adopt without procurement barriers
- Community contributions from councils improve shared components

**Implications**:
- New repositories are public by default
- Secrets, keys, and credentials never committed to source control
- Open source licensing selected appropriate to the use case
- Dependencies assessed for security, maintenance, and licence compatibility
- Contributions back to upstream projects encouraged
- Contribution guidelines published for local authority developers

**Exceptions** (code MAY be kept closed):
- Code relating to security-sensitive functions
- Code containing keys, credentials, or secrets
- Code that would reveal fraud detection algorithms
- Code subject to specific policy restrictions

**Validation Gates**:
- [ ] Repository is public unless exception documented
- [ ] No secrets or credentials in source code
- [ ] Open source licence applied
- [ ] Dependency licences compatible and reviewed
- [ ] Contribution guidelines published

---

## VII. UK Government Specific Principles

### 24. GDS Service Standard Compliance

**Principle Statement**:
All public-facing digital services MUST meet the 14 points of the GDS Service Standard and pass service assessments at alpha, beta, and live stages.

**Rationale**:
The GDS Service Standard is mandatory for government services. GDS Local extends this expectation to shared components used by local authorities — ensuring consistent quality across government tiers.

**The 14 Points** (architecture must support):
1. Understand users and their needs
2. Solve a whole problem for users
3. Provide a joined up experience across all channels
4. Make the service simple to use
5. Make sure everyone can use the service
6. Have a multidisciplinary team
7. Use agile ways of working
8. Iterate and improve frequently
9. Create a secure service which protects users' privacy
10. Define what success looks like and publish performance data
11. Choose the right tools and technology
12. Make new source code open
13. Use and contribute to open standards, common components and patterns
14. Operate a reliable service

**GDS Local Context**:
- Point 2 (Solve a whole problem) is central — GDS Local bridges the central-local boundary
- Point 3 (Joined up experience) directly served by shared components and OneLogin
- Point 13 (Open standards, common components) is the core GDS Local mission

**Validation Gates**:
- [ ] Service mapped against all 14 points
- [ ] Architecture supports each applicable point
- [ ] Service assessment evidence documented
- [ ] Performance metrics published on GOV.UK Performance Platform

---

### 25. Spend Controls, Integrated Purchasing, and Value for Money

**Principle Statement**:
All technology spend MUST demonstrate value for public money and comply with Cabinet Office spend controls where applicable. GDS Local's integrated purchasing approach SHOULD be used for shared technology needs across central and local government.

**Rationale**:
Public money must be spent wisely. GDS Local establishes an integrated purchasing approach aligned with modern digital government objectives. Shared procurement reduces cost, avoids duplicated effort, and increases collective buying power across 300+ authorities.

**GDS Local Programme Alignment**: Strategic Focus Area 1 — Integrated purchasing approach

**Implications**:
- Total Cost of Ownership (TCO) assessed over appropriate lifecycle (typically 3-5 years)
- Avoid vendor lock-in through portable architectures and open standards
- Use government frameworks (G-Cloud, Digital Outcomes and Specialists) for procurement
- Evaluate GDS Local integrated purchasing options before independent procurement
- Consider aggregate value across participating authorities, not just individual council costs
- Consider operational cost alongside capital cost
- Design for cost-efficient scaling
- Regular review of running costs against value delivered

**Validation Gates**:
- [ ] TCO analysis completed
- [ ] Lock-in risks identified and mitigated
- [ ] GDS Local integrated purchasing options evaluated
- [ ] Procurement via appropriate government framework
- [ ] Running costs monitored and reviewed quarterly
- [ ] Value for money assessment documented
- [ ] Aggregate cross-authority value considered

---

## VIII. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Enterprise Architecture Review Board.

**Valid Exception Reasons**:
- Technical constraints that prevent compliance
- Regulatory or legal requirements
- Transitional state during migration (with defined end date)
- Pilot/proof-of-concept with defined end date
- Legacy system integration with remediation plan
- Local authority-specific constraint not addressable by shared component configuration

**Exception Request Requirements**:
- [ ] Justification with business/technical rationale
- [ ] Alternative approach and compensating controls
- [ ] Risk assessment and mitigation plan
- [ ] Expiration date (exceptions are time-bound, maximum 12 months)
- [ ] Remediation plan to achieve compliance

**Approval Process**:
1. Submit exception request to Enterprise Architecture team
2. Review by architecture review board
3. SIRO/SRO approval for exceptions to security or data principles
4. Document exception in project architecture documentation
5. Regular review of exceptions (quarterly)

---

## IX. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key milestones, aligned with the GDS Service Standard assessment process:

**Discovery/Alpha**:
- [ ] Architecture principles understood
- [ ] High-level approach aligns with principles
- [ ] No obvious principle violations
- [ ] User needs validated and informing architecture (central and local users)
- [ ] Government platform and GDS Local shared component options evaluated

**Beta/Design**:
- [ ] Detailed architecture documented
- [ ] Compliance with each principle validated
- [ ] Exceptions requested and approved
- [ ] Security and data principles validated (including cross-authority concerns)
- [ ] Accessibility approach confirmed
- [ ] GDS Service Standard self-assessment completed
- [ ] Local authority integration approach validated

**Pre-Production/Live**:
- [ ] Implementation matches approved architecture
- [ ] All validation gates passed
- [ ] Operational readiness verified
- [ ] Security testing completed (including tenant isolation)
- [ ] Accessibility audit passed
- [ ] Performance testing completed (including multi-authority load)

### Enforcement

- Architecture reviews are **mandatory** for all projects
- Principle violations must be remediated before production deployment
- Approved exceptions are time-bound (maximum 12 months) and reviewed quarterly
- Retrospective reviews for compliance on live systems
- Non-compliance escalated to the SRO/SIRO

---

## X. Appendix

### Principle Summary Checklist

| # | Principle | Category | Criticality | Validation |
|---|-----------|----------|-------------|------------|
| 1 | User Needs First | Strategic | CRITICAL | User research (central + local), journey mapping |
| 2 | Scalability and Elasticity | Strategic | HIGH | Load testing, multi-authority scaling |
| 3 | Resilience and Fault Tolerance | Strategic | CRITICAL | Chaos testing, RTO/RPO, blast radius |
| 4 | Interoperability and Open Standards | Strategic | HIGH | API specs, open standards, sandbox |
| 5 | Security by Design | Strategic | CRITICAL | Threat model, pen testing, tenant isolation |
| 6 | Accessibility by Default | Strategic | CRITICAL | WCAG 2.2 AA, accessibility audit |
| 7 | Observability | Strategic | HIGH | Metrics, logs, traces (per-authority) |
| 8 | Central-Local Collaboration | Collaboration | CRITICAL | Co-design, practitioner input |
| 9 | Cross-Service Data Sharing | Collaboration | CRITICAL | DPIA, purpose limitation, audit trail |
| 10 | Federated Identity | Collaboration | HIGH | OneLogin integration, open standards |
| 11 | Data Sovereignty and UK GDPR | Data | CRITICAL | DPIA, compliance audit, controller roles |
| 12 | Data Quality | Data | MEDIUM | Quality metrics, cross-authority responsibility |
| 13 | Single Source of Truth | Data | HIGH | Data lineage, source authority |
| 14 | Loose Coupling | Integration | HIGH | Deployment independence, API versioning |
| 15 | Asynchronous Communication | Integration | MEDIUM | Async patterns used |
| 16 | Reuse Government Platforms | Integration | HIGH | GDS + GDS Local component assessment |
| 17 | Performance and Efficiency | Quality | HIGH | Load testing, multi-authority aggregate |
| 18 | Availability and Reliability | Quality | CRITICAL | SLA monitoring |
| 19 | Maintainability and Evolvability | Quality | MEDIUM | Documentation, tests, configurability |
| 20 | Infrastructure as Code | DevOps | HIGH | IaC coverage |
| 21 | Automated Testing | DevOps | HIGH | Test coverage, tenant isolation tests |
| 22 | CI/CD | DevOps | HIGH | Pipeline exists |
| 23 | Open Source by Default | DevOps | HIGH | Public repos, contribution guidelines |
| 24 | GDS Service Standard Compliance | UK Gov | CRITICAL | 14-point assessment |
| 25 | Spend Controls and Integrated Purchasing | UK Gov | HIGH | TCO analysis, GDS Local procurement |

### Criticality Levels

| Level | Meaning | Exception Process |
|-------|---------|-------------------|
| **CRITICAL** | Non-negotiable. Legal, security, accessibility, or programme-critical requirement. | Requires SIRO/SRO approval. Compensating controls mandatory. |
| **HIGH** | Strong expectation of compliance. Deviations carry significant risk. | Architecture Review Board approval. Remediation plan required. |
| **MEDIUM** | Best practice. Compliance expected but flexibility permitted. | Team lead approval with documented justification. |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| GDS Local Guidance | Programme | GOV.UK | Programme purpose, three strategic focus areas, co-design approach | gov.uk/guidance/gds-local |
| GDS Service Standard | Standard | GOV.UK | 14-point assessment criteria | gov.uk/service-manual/service-standard |
| Technology Code of Practice | Policy | Cabinet Office | Technology decision guidance | gov.uk/guidance/the-technology-code-of-practice |
| NCSC 10 Steps to Cyber Security | Guidance | NCSC | Security baseline | ncsc.gov.uk |
| UK GDPR | Regulation | ICO | Data protection requirements | ico.org.uk |
| Public Sector Bodies Accessibility Regulations 2018 | Regulation | UK Parliament | Accessibility requirements | legislation.gov.uk |
| UK Government Security Classifications | Policy | Cabinet Office | OFFICIAL, SECRET, TOP SECRET | gov.uk |

---

**Generated by**: ArcKit `/arckit:principles` command
**Generated on**: 2026-02-16
**ArcKit Version**: 2.4.5
**Project**: GDS Local (Project 000)
**AI Model**: Claude Opus 4.6
