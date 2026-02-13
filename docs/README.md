# OctoAcme Project Management Documentation

Welcome to the OctoAcme project management documentation. This guide serves as your entry point to understanding how OctoAcme runs cross-functional projects that deliver product features, services, and integrations.

## Overview

OctoAcme's project management approach is built on five core principles: customer-first delivery, iterative increments, clear ownership, data-informed decisions, and psychological safety. Every project follows a structured lifecycle from **Initiation** through **Planning**, **Execution**, **Release**, and concludes with a **Retrospective** to capture learnings and drive continuous improvement.

Projects are led collaboratively by a **Project Manager** (PM) who coordinates delivery, schedules, and risk management, and a **Product Manager** (PdM) who defines outcomes and prioritizes work. Development teams work in sprints or iterations, using a project board with columns (Backlog → Ready → In Progress → In Review → QA → Done) to track progress. Quality is ensured through comprehensive testing practices including unit tests, integration tests, end-to-end smoke tests, and security scanning integrated into CI pipelines.

Communication follows a regular cadence: weekly syncs between PM and PdM, twice-weekly team standups, and monthly stakeholder updates ensure alignment and transparency. When blockers arise, they are escalated through three levels—team triage in standups (Level 1), PM escalation to Product Lead (Level 2), and sponsor-level escalation for business-impacting issues (Level 3). Pull requests are kept small (≤400 lines when possible), include issue links and acceptance criteria, and require at least one approval before merging.

Throughout the project lifecycle, teams maintain key artifacts including the Project Charter, Roadmap, Risk Register, and Retrospective notes. The goal is to deliver measurable customer value through small, testable increments while maintaining high quality standards and continuous learning.

## Documentation Index

### Core Process Guides

Explore the complete OctoAcme project management documentation:

- **[Project Management Overview](octoacme-project-management-overview.md)** — Introduction to OctoAcme's approach, principles, roles, and lifecycle
- **[Project Initiation](octoacme-project-initiation.md)** — How to validate ideas, align stakeholders, and create a lightweight project plan
- **[Project Planning](octoacme-project-planning.md)** — Breaking work into shippable increments, estimating, and defining success criteria
- **[Execution & Tracking](octoacme-execution-and-tracking.md)** — Day-to-day workflows, PR practices, quality standards, and blocker escalation
- **[Risk Management & Communication](octoacme-risks-and-communication.md)** — Managing risks, dependencies, and stakeholder communication
- **[Release & Deployment](octoacme-release-and-deployment.md)** — Release types, deployment checklists, and rollback procedures
- **[Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md)** — Capturing learnings and converting them into actionable improvements
- **[Roles & Personas](octoacme-roles-and-personas.md)** — Detailed responsibilities and goals for Developers, Product Managers, and Project Managers

### Templates & Checklists

Practical templates and checklists for day-to-day project management:

- **[Process Overview](project-management/process-overview.md)** — End-to-end workflow from intake through release
- **[Definition of Done](project-management/definition-of-done.md)** — Quality criteria for completed work
- **[Decision Log / ADRs](project-management/decision-log.md)** — Architecture Decision Records process and template
- **[Meeting Notes Template](project-management/meeting-notes-template.md)** — Structured format for capturing meeting outcomes
- **[Status Update Template](project-management/status-update-template.md)** — Weekly/monthly project status reporting
- **[Release Checklist](project-management/release-checklist.md)** — Pre-release, deployment, and post-release validation
- **[Triage Playbook](project-management/triage-playbook.md)** — Issue prioritization, severity levels, and escalation paths
- **[RACI Template](project-management/ownership-raci-template.md)** — Clarify roles and responsibilities
- **[Onboarding & Handoff Checklist](project-management/onboarding-handoff-checklist.md)** — Team member onboarding and knowledge transfer

## Quick Start

**New to a project?** Start with the [Project Management Overview](octoacme-project-management-overview.md) to understand our approach, then review [Roles & Personas](octoacme-roles-and-personas.md) to clarify responsibilities. Use the [Onboarding Checklist](project-management/onboarding-handoff-checklist.md) to track your ramp-up.

**Starting a new project?** Follow the [Project Initiation](octoacme-project-initiation.md) guide to create your one-pager and stakeholder alignment, then move to [Project Planning](octoacme-project-planning.md) to build your backlog. Set up your [RACI matrix](project-management/ownership-raci-template.md) to clarify ownership.

**In active delivery?** Refer to [Execution & Tracking](octoacme-execution-and-tracking.md) for workflows and quality standards, and [Risk Management & Communication](octoacme-risks-and-communication.md) for stakeholder updates. Use the [Definition of Done](project-management/definition-of-done.md) and [Status Update Template](project-management/status-update-template.md).

**Preparing for release?** Check the [Release & Deployment](octoacme-release-and-deployment.md) guide for pre-release requirements and the detailed [Release Checklist](project-management/release-checklist.md).

**After a milestone or sprint?** Use the [Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md) guide to capture learnings and action items.

**Managing issues?** Follow the [Triage Playbook](project-management/triage-playbook.md) for prioritization and escalation.

---

For questions or suggestions about these processes, reach out to your Project Manager or Product Lead.
