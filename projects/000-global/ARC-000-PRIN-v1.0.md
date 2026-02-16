# GDS Local Enterprise Architecture Principles

> **Template Status**: Live | **Version**: 2.4.5 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | GDS Local (Project 000) |
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
| **Distribution** | Architecture Team, Development Teams, Senior Leadership |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-16 | ArcKit AI | Initial creation from `/arckit:principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the architecture principles governing all technology decisions for GDS Local. These principles ensure consistency, security, scalability, and alignment with UK Government standards across all projects and initiatives.

These principles are designed to align with the **GDS Service Standard** (14 points), the **Technology Code of Practice (TCoP)**, and the **UK Government Digital, Data and Technology (DDaT) profession framework**. They incorporate UK-specific requirements including the **Public Sector Bodies Accessibility Regulations 2018**, **UK GDPR**, and **NCSC Cyber Security guidance**.

**Scope**: All technology projects, systems, and initiatives within GDS Local
**Authority**: Enterprise Architecture Review Board
**Compliance**: Mandatory unless exception approved through the documented exception process

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles.

---

## I. Strategic Principles

### 1. User Needs First

**Principle Statement**:
All systems MUST be designed around validated user needs, not organisational structures, technology preferences, or assumptions.

**Rationale**:
The GDS Service Standard requires understanding user needs (Point 1). Services that do not meet real user needs waste public money and erode trust in government digital services.

**GDS Service Standard Alignment**: Point 1 — Understand users and their needs

**Implications**:
- User research informs all architecture decisions
- Services are designed around user journeys, not back-office processes
- Accessibility is a core architectural requirement, not an afterthought
- Performance budgets are set based on user expectations and device capabilities
- Architecture supports iterative delivery based on user feedback

**Validation Gates**:
- [ ] User research conducted and documented before design decisions
- [ ] Architecture supports the identified user journeys
- [ ] Performance meets user expectations across all supported devices
- [ ] Feedback mechanisms built into the service for continuous improvement
- [ ] Architecture supports A/B testing and iterative improvement

---

### 2. Scalability and Elasticity

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet demand, with the ability to dynamically adjust capacity based on load.

**Rationale**:
Government services experience variable demand — from steady-state to peaks driven by policy announcements, deadlines, or seasonal patterns. Systems must handle these variations without manual intervention or degraded user experience.

**Implications**:
- Design for stateless components that can be replicated
- Avoid hard-coded limits or fixed capacity assumptions
- Plan for distributed deployment across multiple compute nodes
- Use load balancing to distribute traffic across instances
- Implement auto-scaling based on demand metrics
- Design for cost-efficient scaling — public money must be spent wisely

**Validation Gates**:
- [ ] System can scale horizontally (add more instances)
- [ ] No single points of failure that limit scaling
- [ ] Load testing demonstrates capacity growth with added resources
- [ ] Scaling metrics and triggers defined
- [ ] Cost model accounts for variable capacity

---

### 3. Resilience and Fault Tolerance

**Principle Statement**:
All systems MUST gracefully degrade when dependencies fail and recover automatically without data loss or manual intervention.

**Rationale**:
Failures are inevitable in distributed systems. Government services are relied upon by citizens and must be available when needed. The architecture must assume failures will occur and design for resilience rather than perfect reliability.

**Implications**:
- Implement circuit breakers for external dependencies
- Use timeouts on all network calls
- Retry with exponential backoff for transient failures
- Graceful degradation when non-critical services fail
- Automated health checks and recovery
- Avoid cascading failures through bulkhead isolation
- Maintain offline or alternative service channels where appropriate

**Validation Gates**:
- [ ] Failure modes identified and mitigated
- [ ] Chaos engineering or fault injection testing performed
- [ ] Recovery Time Objective (RTO) and Recovery Point Objective (RPO) defined
- [ ] Automated failover tested
- [ ] Degraded mode behaviour documented

---

### 4. Interoperability and Open Standards

**Principle Statement**:
All systems MUST expose functionality through well-defined, versioned interfaces using open standards. Proprietary protocols and direct database access across system boundaries are prohibited.

**Rationale**:
The Technology Code of Practice requires use of open standards. Loose coupling through standard interfaces enables independent evolution, avoids vendor lock-in, and supports government's commitment to interoperability.

**GDS Service Standard Alignment**: TCoP Point 6 — Make things accessible and use open standards

**Implications**:
- Use open, standardised protocols (HTTP, REST, GraphQL, message queuing, event streaming)
- Version all interfaces with backward compatibility strategy
- Publish interface specifications (API contracts, event schemas)
- No direct database access across system boundaries
- Asynchronous communication for non-real-time interactions
- Prefer open data formats (JSON, CSV, ODF) over proprietary formats

**Validation Gates**:
- [ ] Interface specifications published (OpenAPI, AsyncAPI, GraphQL schema)
- [ ] Open standards used — proprietary protocols justified if used
- [ ] Versioning strategy defined
- [ ] Authentication and authorisation model documented
- [ ] Error handling and retry behaviour specified
- [ ] No direct database coupling across systems

---

### 5. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles aligned to NCSC guidance. Security is NOT a feature to be added later — it is a foundational requirement.

**Rationale**:
Government systems handle citizen data and provide essential services. The threat landscape requires assuming breach, eliminating implicit trust, and continuously verifying all access requests. NCSC's 10 Steps to Cyber Security and Secure by Design principles are mandatory.

**GDS Service Standard Alignment**: Point 9 — Create a secure service which protects users' privacy

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

**Compliance Frameworks**:
- NCSC Cyber Assessment Framework (CAF)
- NCSC 10 Steps to Cyber Security
- ISO 27001
- UK GDPR (data protection controls)
- Cyber Essentials Plus (minimum baseline)

**Exceptions**:
- NONE. Security principles are non-negotiable.
- Specific control implementations may vary with compensating controls approved by the SIRO.

**Validation Gates**:
- [ ] Threat model completed and reviewed
- [ ] Security controls mapped to requirements
- [ ] Security testing plan defined
- [ ] Incident response runbook created
- [ ] NCSC Secure by Design checklist completed

---

### 6. Accessibility by Default (NON-NEGOTIABLE)

**Principle Statement**:
All user-facing systems MUST meet WCAG 2.2 AA standards and comply with the Public Sector Bodies Accessibility Regulations 2018. Accessibility is a legal requirement, not an enhancement.

**Rationale**:
The Public Sector Bodies (Websites and Mobile Applications) Accessibility Regulations 2018 require public sector digital services to be accessible. The GDS Service Standard (Point 5) mandates accessibility. Approximately 1 in 5 people in the UK have a disability.

**GDS Service Standard Alignment**: Point 5 — Make sure everyone can use the service

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

---

### 7. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting, and capacity planning.

**Rationale**:
We cannot operate what we cannot observe. Government services must meet availability commitments and be diagnosable when issues arise. Instrumentation is a first-class architectural requirement, not an afterthought.

**GDS Service Standard Alignment**: Point 14 — Operate a reliable service

**Telemetry Requirements**:
- **Logging**: Structured logs with correlation IDs (ensure no PII in logs)
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates
- **Tracing**: Distributed trace context for request flows
- **Alerting**: Service Level Objective (SLO)-based alerting with actionable runbooks

**Required Instrumentation**:
- Request volume, latency distribution, error rate
- Resource utilisation (CPU, memory, I/O, network)
- Business metrics (transactions, service completions, user drop-off points)
- Security events (auth failures, policy violations, suspicious patterns)

**Log Retention**:
- **Security/audit logs**: 7 years (aligned with UK regulatory requirements)
- **Application logs**: 90 days minimum
- **Metrics**: 2 years with aggregation for trend analysis

**Validation Gates**:
- [ ] Logging, metrics, tracing instrumented
- [ ] Dashboards and alerts configured
- [ ] Service Level Objectives (SLOs) and Service Level Indicators (SLIs) defined
- [ ] Runbooks created for common failure scenarios
- [ ] Capacity planning metrics tracked
- [ ] No PII present in log outputs

---

## II. Data Principles

### 8. Data Sovereignty and UK GDPR Compliance

**Principle Statement**:
Data classification, residency, retention, and access controls MUST comply with UK GDPR, the Data Protection Act 2018, and the UK Government Security Classifications policy.

**Rationale**:
Government holds sensitive citizen data. The UK GDPR and Data Protection Act 2018 impose strict requirements on data processing. The UK Government Security Classifications policy (OFFICIAL, SECRET, TOP SECRET) governs information handling.

**UK Government Security Classifications**:
1. **OFFICIAL**: The majority of government information — routine business, public services
2. **OFFICIAL-SENSITIVE**: OFFICIAL information requiring additional handling controls
3. **SECRET**: Sensitive information requiring enhanced protection
4. **TOP SECRET**: The most sensitive information requiring the highest levels of protection

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

---

### 9. Data Quality and Lineage

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability and troubleshooting.

**Rationale**:
Government decisions and services depend on accurate data. Poor data quality leads to incorrect policy decisions, failed service delivery, and erosion of public trust.

**Quality Standards**:
- **Completeness**: No unexpected nulls in required fields
- **Consistency**: Cross-system data reconciliation
- **Accuracy**: Validation rules and constraints enforced at source
- **Timeliness**: Freshness Service Level Agreements (SLAs) defined and monitored

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

---

### 10. Single Source of Truth

**Principle Statement**:
Every data domain MUST have a single authoritative source. Derived copies must be clearly labelled and synchronised.

**Rationale**:
Multiple authoritative sources create inconsistency, reconciliation overhead, and data integrity issues. Government registers and authoritative datasets must have clear ownership.

**Implications**:
- Identify the system of record for each data domain
- Derived/cached copies are read-only and clearly labelled as such
- Synchronisation strategy defined for all derived copies
- Avoid bidirectional synchronisation (creates split-brain scenarios)
- Use government registers as authoritative sources where they exist

**Validation Gates**:
- [ ] System of record identified for each data entity
- [ ] Derived copies documented with sync frequency
- [ ] No bidirectional sync without conflict resolution strategy
- [ ] Master data management (MDM) strategy for shared reference data

---

## III. Integration Principles

### 11. Loose Coupling

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces, avoiding shared databases, file systems, or tight runtime dependencies.

**Rationale**:
Loose coupling enables independent deployment, technology diversity, team autonomy, and system evolution without breaking dependencies. This aligns with the GDS approach to building small, focused services.

**GDS Service Standard Alignment**: Point 11 — Choose the right tools and technology

**Implications**:
- Communicate through published APIs or asynchronous events
- No direct database access across system boundaries
- Each system manages its own data lifecycle
- Shared libraries kept minimal (favour duplication over coupling)
- Avoid distributed transactions across systems
- Services can be replaced independently without affecting the wider ecosystem

**Validation Gates**:
- [ ] Systems communicate via APIs or events, not databases
- [ ] No shared mutable state
- [ ] Each system has independent data store
- [ ] Deployment of one system does not require deployment of another
- [ ] Interface changes versioned with backward compatibility

---

### 12. Asynchronous Communication

**Principle Statement**:
Systems SHOULD use asynchronous communication for non-real-time interactions to improve resilience and decoupling.

**Rationale**:
Asynchronous patterns reduce temporal coupling, improve fault tolerance, and enable better scalability. This is particularly important for government services that integrate with multiple legacy systems.

**When to Use Async**:
- Non-real-time business processes (application processing, batch jobs)
- Event notification and pub/sub patterns
- Long-running operations that do not require immediate response
- Integration with unreliable or slow external systems

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

### 13. Reuse Government Platforms

**Principle Statement**:
Systems SHOULD reuse existing government platforms and shared services before building bespoke solutions.

**Rationale**:
The Technology Code of Practice requires government to reuse and share technology. Government platforms (GOV.UK Notify, GOV.UK Pay, GOV.UK Verify) have been built and assured for government use, reducing cost and risk.

**GDS Service Standard Alignment**: TCoP Point 4 — Make use of open standards and common platforms

**Implications**:
- Evaluate government shared platforms before procuring or building alternatives
- Architecture must integrate with government platforms via their published APIs
- Where no government platform exists, design services as potentially reusable
- Contribute back to shared platforms where improvements are identified
- Register services on the government API catalogue

**Government Platforms to Evaluate**:
- Notifications (email, SMS, letters)
- Payment processing
- Identity verification
- Content publishing
- Forms and submissions
- Hosting platforms

**Validation Gates**:
- [ ] Government platform options evaluated and documented
- [ ] Justification provided if government platform not used
- [ ] Integration with government platforms uses published APIs
- [ ] New capabilities assessed for reuse potential

---

## IV. Quality Attributes

### 14. Performance and Efficiency

**Principle Statement**:
All systems MUST meet defined performance targets under expected load with efficient use of computational resources. Public money must not be wasted on over-provisioned or inefficient infrastructure.

**Rationale**:
Government services serve millions of citizens. Poor performance erodes trust and excludes users on slower connections or older devices.

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

**Validation Gates**:
- [ ] Performance requirements defined with measurable targets
- [ ] Load testing performed at expected capacity
- [ ] Performance metrics monitored in production
- [ ] Capacity planning model defined

---

### 15. Availability and Reliability

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss.

**Rationale**:
Government services are relied upon by citizens and businesses. Downtime has direct impact on people's lives and the functioning of government.

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

### 16. Maintainability and Evolvability

**Principle Statement**:
All systems MUST be designed for change, with clear separation of concerns, modular architecture, and comprehensive documentation.

**Rationale**:
Government policy changes frequently. Software spends most of its lifetime in maintenance. Design decisions should optimise for understandability and modifiability, enabling rapid response to policy changes.

**Implications**:
- Modular architecture with clear boundaries
- Separation of concerns (business logic, data access, presentation)
- Code is self-documenting with meaningful names
- Architecture Decision Records (ADRs) for significant choices
- Automated testing to enable confident refactoring
- Consider long-term supportability — avoid niche technologies that may lack future support

**Validation Gates**:
- [ ] Architecture documentation exists and is current
- [ ] Module boundaries clear with defined responsibilities
- [ ] Automated test coverage enables safe refactoring
- [ ] Architecture Decision Records (ADRs) document key choices

---

## V. Development Practices

### 17. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled, and deployed through automated pipelines.

**Rationale**:
Manual infrastructure changes create drift, inconsistency, and undocumented state. Infrastructure as Code (IaC) enables repeatability, auditability, and disaster recovery. It also supports the GDS Service Standard requirement for reproducible deployments.

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

### 18. Automated Testing

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment to production.

**Rationale**:
Government services must be reliable. Automated testing provides confidence in changes and enables the rapid, iterative delivery approach required by the GDS Service Standard.

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

**Validation Gates**:
- [ ] Automated tests exist and pass before merge
- [ ] Test coverage meets defined thresholds
- [ ] Critical paths have end-to-end tests
- [ ] Accessibility tests included in CI pipeline
- [ ] Performance tests run regularly

---

### 19. Continuous Integration and Deployment

**Principle Statement**:
All code changes MUST go through automated build, test, and deployment pipelines with quality gates at each stage.

**Rationale**:
The GDS Service Standard requires frequent, iterative releases. Automated pipelines reduce risk, improve quality, and enable rapid response to user needs and security vulnerabilities.

**GDS Service Standard Alignment**: Point 8 — Iterate and improve frequently

**Pipeline Stages**:
1. **Source Control**: All changes committed to version control (open source by default)
2. **Build**: Automated compilation and packaging
3. **Test**: Automated test execution (including accessibility)
4. **Security Scan**: Dependency and code vulnerability scanning
5. **Deployment**: Automated deployment to environments

**Quality Gates**:
- All tests must pass (functional, accessibility, security)
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

### 20. Open Source by Default

**Principle Statement**:
All new source code SHOULD be made open unless there is a clear, documented reason not to. Existing open source solutions SHOULD be evaluated before building bespoke.

**Rationale**:
The GDS Service Standard and Technology Code of Practice require government code to be open by default. Open source enables transparency, collaboration, and reuse across government.

**GDS Service Standard Alignment**: Point 12 — Make new source code open

**Implications**:
- New repositories are public by default
- Secrets, keys, and credentials never committed to source control
- Open source licensing selected appropriate to the use case
- Dependencies assessed for security, maintenance, and licence compatibility
- Contributions back to upstream projects encouraged

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

## VI. UK Government Specific Principles

### 21. GDS Service Standard Compliance

**Principle Statement**:
All public-facing digital services MUST meet the 14 points of the GDS Service Standard and pass service assessments at alpha, beta, and live stages.

**Rationale**:
The GDS Service Standard is mandatory for government services. Architecture decisions directly impact the ability to meet assessment criteria.

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

**Validation Gates**:
- [ ] Service mapped against all 14 points
- [ ] Architecture supports each applicable point
- [ ] Service assessment evidence documented
- [ ] Performance metrics published on GOV.UK Performance Platform

---

### 22. Spend Controls and Value for Money

**Principle Statement**:
All technology spend MUST demonstrate value for public money and comply with Cabinet Office spend controls where applicable.

**Rationale**:
Public money must be spent wisely. The Technology Code of Practice requires government to consider total cost of ownership, avoid lock-in, and ensure competitive procurement.

**Implications**:
- Total Cost of Ownership (TCO) assessed over appropriate lifecycle (typically 3-5 years)
- Avoid vendor lock-in through portable architectures and open standards
- Use government frameworks (G-Cloud, Digital Outcomes and Specialists) for procurement
- Consider operational cost alongside capital cost
- Design for cost-efficient scaling
- Regular review of running costs against value delivered

**Validation Gates**:
- [ ] TCO analysis completed
- [ ] Lock-in risks identified and mitigated
- [ ] Procurement via appropriate government framework
- [ ] Running costs monitored and reviewed quarterly
- [ ] Value for money assessment documented

---

## VII. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Enterprise Architecture Review Board.

**Valid Exception Reasons**:
- Technical constraints that prevent compliance
- Regulatory or legal requirements
- Transitional state during migration (with defined end date)
- Pilot/proof-of-concept with defined end date
- Legacy system integration with remediation plan

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

## VIII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key milestones, aligned with the GDS Service Standard assessment process:

**Discovery/Alpha**:
- [ ] Architecture principles understood
- [ ] High-level approach aligns with principles
- [ ] No obvious principle violations
- [ ] User needs validated and informing architecture
- [ ] Government platform options evaluated

**Beta/Design**:
- [ ] Detailed architecture documented
- [ ] Compliance with each principle validated
- [ ] Exceptions requested and approved
- [ ] Security and data principles validated
- [ ] Accessibility approach confirmed
- [ ] GDS Service Standard self-assessment completed

**Pre-Production/Live**:
- [ ] Implementation matches approved architecture
- [ ] All validation gates passed
- [ ] Operational readiness verified
- [ ] Security testing completed
- [ ] Accessibility audit passed
- [ ] Performance testing completed

### Enforcement

- Architecture reviews are **mandatory** for all projects
- Principle violations must be remediated before production deployment
- Approved exceptions are time-bound (maximum 12 months) and reviewed quarterly
- Retrospective reviews for compliance on live systems
- Non-compliance escalated to the SRO/SIRO

---

## IX. Appendix

### Principle Summary Checklist

| # | Principle | Category | Criticality | Validation |
|---|-----------|----------|-------------|------------|
| 1 | User Needs First | Strategic | CRITICAL | User research, journey mapping |
| 2 | Scalability and Elasticity | Strategic | HIGH | Load testing, scaling metrics |
| 3 | Resilience and Fault Tolerance | Strategic | CRITICAL | Chaos testing, RTO/RPO |
| 4 | Interoperability and Open Standards | Strategic | HIGH | API specs, open standards audit |
| 5 | Security by Design | Strategic | CRITICAL | Threat model, pen testing, NCSC |
| 6 | Accessibility by Default | Strategic | CRITICAL | WCAG 2.2 AA, accessibility audit |
| 7 | Observability | Strategic | HIGH | Metrics, logs, traces |
| 8 | Data Sovereignty and UK GDPR | Data | CRITICAL | DPIA, compliance audit |
| 9 | Data Quality | Data | MEDIUM | Quality metrics |
| 10 | Single Source of Truth | Data | HIGH | Data lineage |
| 11 | Loose Coupling | Integration | HIGH | Deployment independence |
| 12 | Asynchronous Communication | Integration | MEDIUM | Async patterns used |
| 13 | Reuse Government Platforms | Integration | HIGH | Platform assessment |
| 14 | Performance and Efficiency | Quality | HIGH | Load testing |
| 15 | Availability and Reliability | Quality | CRITICAL | SLA monitoring |
| 16 | Maintainability and Evolvability | Quality | MEDIUM | Documentation, tests |
| 17 | Infrastructure as Code | DevOps | HIGH | IaC coverage |
| 18 | Automated Testing | DevOps | HIGH | Test coverage |
| 19 | CI/CD | DevOps | HIGH | Pipeline exists |
| 20 | Open Source by Default | DevOps | HIGH | Public repos, licence review |
| 21 | GDS Service Standard Compliance | UK Gov | CRITICAL | 14-point assessment |
| 22 | Spend Controls and Value for Money | UK Gov | HIGH | TCO analysis |

### Criticality Levels

| Level | Meaning | Exception Process |
|-------|---------|-------------------|
| **CRITICAL** | Non-negotiable. Legal, security, or accessibility requirement. | Requires SIRO/SRO approval. Compensating controls mandatory. |
| **HIGH** | Strong expectation of compliance. Deviations carry significant risk. | Architecture Review Board approval. Remediation plan required. |
| **MEDIUM** | Best practice. Compliance expected but flexibility permitted. | Team lead approval with documented justification. |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
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
