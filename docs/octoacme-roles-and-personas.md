# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

---

## Additional recommended personas (new)

Below are proposed additions to the personas document to improve clarity, accountability, and cross-functional handoffs. Each entry includes a concise role summary, responsibilities, and how the persona interacts with existing roles.

### Technical Lead

Role Summary
- Owns the technical approach and architecture for a project or major feature area. Ensures technical decisions align with long-term system goals.

Responsibilities
- Define and propose technical designs and trade-offs
- Review architecture- and design-level PRs
- Identify technical risks and recommend mitigations
- Coordinate cross-team technical dependencies
- Ensure adherence to coding and design standards

Interactions with existing roles
- Developers: mentor and guide implementation; perform design reviews
- Project Manager / PM: communicate technical risks that may affect timelines
- Product Manager (PdM): advise on feasibility and cost of technical options
- Engineering Manager: align on staffing, hiring needs, and technical priorities

Example handoff
- During planning, the Technical Lead reviews proposed stories for technical gaps and flags required infrastructure work before development begins.

---

### Engineering Manager (EM)

Role Summary
- Responsible for people management, team capacity, and removing organizational impediments to delivery.

Responsibilities
- Support performance and career development of engineers
- Lead capacity planning and team staffing decisions
- Remove organizational blockers and escalate resource constraints
- Help with hiring and cross-team coordination

Interactions with existing roles
- Project Manager: align on resourcing and sprint capacity
- Technical Lead: balance technical priorities with team capacity
- Product Manager: communicate impact of staffing on delivery timelines

Example handoff
- During sprint planning, the EM confirms available capacity and raises foreseeable training or hiring needs.

---

### Release Engineer / Platform Engineer

Role Summary
- Maintains the CI/CD pipeline, release automation, and operational constraints to ensure safe and repeatable releases.

Responsibilities
- Build and maintain deployment pipelines and automation
- Define release readiness checks and rollback procedures
- Support release rehearsals and staging verification
- Collaborate on deployment safety and platform changes

Interactions with existing roles
- Developers & QA: ensure builds/tests are reliable and reproducible
- Project Manager: coordinate release windows and communications
- Support / SRE: align on runbooks and on-call impacts
- Security: ensure deployment changes meet security requirements

Example handoff
- Before a release, the Release Engineer verifies pipeline health and confirms rollback steps with the team.

---

### Security Owner / Security Engineer

Role Summary
- Ensures security and compliance considerations are integrated into design, development, and release processes.

Responsibilities
- Conduct threat modeling and security reviews
- Require and verify security checklists are satisfied for releases
- Triage vulnerabilities and recommend remediations
- Coordinate with compliance and privacy teams as needed

Interactions with existing roles
- Developers / Technical Lead: provide security guidance on designs and PRs
- Project Manager / PM: communicate risk and remediation timelines
- Release Engineer: sign off on production changes that affect security posture

Example handoff
- Security review provides a checklist that must be completed prior to merging features that modify sensitive components.

---

### UX Researcher / Designer

Role Summary
- Defines and validates user experience through research and design artifacts; ensures usability is considered throughout delivery.

Responsibilities
- Run user research and usability testing
- Provide designs, interaction patterns, and assets
- Define UX acceptance criteria and accessibility requirements
- Validate implemented flows before release

Interactions with existing roles
- Product Manager: collaborate on outcomes and acceptance criteria
- Developers & QA: hand off design artifacts and clarify expected behaviors
- Stakeholder Liaison: surface user-facing concerns or feedback

Example handoff
- During backlog grooming, the UX Researcher provides designs and acceptance criteria for stories that affect user flows.

---

### Data Analyst / Data Owner

Role Summary
- Owns product instrumentation, metrics definition, and post-release analysis to measure outcomes.

Responsibilities
- Define success metrics and instrumentation requirements
- Validate data quality and dashboards
- Analyze release impact and produce insights
- Advise on data-related risks and compliance concerns

Interactions with existing roles
- Product Manager: set and refine success metrics
- Developers: define and validate telemetry and data contracts
- Project Manager & Stakeholders: provide dashboards and findings that inform decisions

Example handoff
- Prior to release, Data Owner confirms instrumentation is in place and test events are flowing to analytics.

---

### Stakeholder Liaison / Business Owner

Role Summary
- Represents business unit stakeholders (e.g., Sales, Customer Success) and owns business acceptance for work with customer or revenue impact.

Responsibilities
- Prioritize business requests and validate business impact
- Approve go/no-go decisions for business-critical releases
- Provide subject matter context and stakeholder communications

Interactions with existing roles
- Product Manager: negotiate priority and acceptance criteria based on business impact
- Project Manager: coordinate milestone reviews and stakeholder updates
- Support: align on customer-facing communications and handoffs

Example handoff
- For releases impacting customers, the Stakeholder Liaison signs off on release communications and business acceptance.

---

### Support / SRE Representative

Role Summary
- Ensures production readiness, monitoring, and runbook accuracy; represents operations and on-call perspectives in planning and releases.

Responsibilities
- Maintain runbooks and incident response playbooks
- Validate observability and alerting for new features
- Participate in on-call rotations or advise on on-call impacts
- Triage production issues and drive remediation

Interactions with existing roles
- Release Engineer: coordinate deployment safety and rollback plans
- Developers: advise on instrumentation and resolvability of incidents
- Project Manager: escalate operational risks that affect delivery

Example handoff
- Before launch, SRE confirms alerts, dashboards, and runbooks are prepared and that support knows expected behaviors.

---

## Implementation notes for documenting personas

- Add a short "How this persona interacts with others" subsection for each role (as above) to make handoffs explicit.
- For each persona include:
  - Role summary (1–2 lines)
  - Responsibilities (bulleted)
  - Interactions / handoffs (who they work with, and when)
  - Example scenarios or checklist items (e.g., "security sign-off before release", "data instrumentation required before launch")
- Cross-reference existing core roles (PM, PdM, Developers, QA, Project Manager) to maintain consistency in language.
- Keep persona entries concise—prefer checklists and examples over long prose so the doc stays actionable.

---
