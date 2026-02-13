# RACI Matrix Template

## Purpose
Clarify roles and responsibilities using RACI (Responsible, Accountable, Consulted, Informed) framework to avoid confusion and ensure accountability.

---

## What is RACI?

**R - Responsible:** Does the work; executes the task  
**A - Accountable:** Ultimately answerable; approves completion (only ONE per task)  
**C - Consulted:** Provides input; two-way communication  
**I - Informed:** Kept up-to-date; one-way communication

### Key Rules
- Every task must have exactly **one A (Accountable)**
- A task can have multiple R's (Responsible) working together
- Avoid too many C's — consult only those who truly need to provide input
- Don't over-inform; only include people who genuinely need to know

---

## Project RACI Template

**Project Name:** [Your Project]  
**Date Created:** YYYY-MM-DD  
**Version:** 1.0

### Team Roster

| Role | Name | Initials |
|------|------|----------|
| Product Manager | [Name] | [XX] |
| Project Manager | [Name] | [XX] |
| Engineering Lead | [Name] | [XX] |
| Developer 1 | [Name] | [XX] |
| Developer 2 | [Name] | [XX] |
| QA Engineer | [Name] | [XX] |
| Designer | [Name] | [XX] |
| DevOps Engineer | [Name] | [XX] |

---

## RACI Matrix

### Project Initiation & Planning

| Activity | PdM | PM | Eng Lead | Dev | QA | Designer | DevOps |
|----------|-----|----|----|-----|----|----|--------|
| Define project goals & success metrics | **A** | C | C | I | I | C | I |
| Create project charter | C | **A** | C | I | I | I | I |
| Scope definition & acceptance criteria | **A** | C | C | I | I | C | I |
| Estimate effort & timeline | C | **A** | R | R | C | I | I |
| Identify risks & dependencies | C | **A** | R | R | R | I | R |
| Create sprint/milestone plan | C | **A** | R | I | I | I | I |

### Design & Development

| Activity | PdM | PM | Eng Lead | Dev | QA | Designer | DevOps |
|----------|-----|----|----|-----|----|----|--------|
| UI/UX design | C | I | I | I | I | **A/R** | I |
| Technical design & architecture | C | I | **A** | R | I | I | C |
| Code implementation | I | I | C | **A/R** | I | I | I |
| Code review | I | I | **A** | R | I | I | I |
| Unit testing | I | I | C | **A/R** | I | I | I |
| Documentation (technical) | I | I | C | **A/R** | I | I | I |

### Quality Assurance & Testing

| Activity | PdM | PM | Eng Lead | Dev | QA | Designer | DevOps |
|----------|-----|----|----|-----|----|----|--------|
| Test plan creation | C | I | C | C | **A/R** | I | I |
| Manual QA testing | I | I | I | C | **A/R** | I | I |
| Integration testing | I | I | C | R | **A** | I | C |
| Performance testing | I | I | C | C | **A/R** | I | R |
| Security testing | I | I | C | C | **A/R** | I | C |
| Bug triage & prioritization | C | C | **A** | I | R | I | I |

### Deployment & Release

| Activity | PdM | PM | Eng Lead | Dev | QA | Designer | DevOps |
|----------|-----|----|----|-----|----|----|--------|
| Infrastructure setup | I | I | C | I | I | I | **A/R** |
| Deployment automation | I | I | C | R | I | I | **A** |
| Pre-release smoke testing | C | I | C | C | **A/R** | I | R |
| Production deployment | I | C | C | R | I | I | **A** |
| Post-deployment monitoring | I | C | C | R | R | I | **A** |
| Release notes | **A** | R | C | C | I | I | I |
| Release communication | **A** | R | I | I | I | I | I |

### Project Management & Operations

| Activity | PdM | PM | Eng Lead | Dev | QA | Designer | DevOps |
|----------|-----|----|----|-----|----|----|--------|
| Daily standup facilitation | I | **A/R** | C | R | R | R | I |
| Sprint planning | C | **A** | R | R | R | C | C |
| Backlog prioritization | **A** | R | C | I | I | C | I |
| Stakeholder updates | **A** | R | C | I | I | I | I |
| Risk management | C | **A** | R | R | R | I | R |
| Issue/blocker escalation | I | **A** | R | R | R | I | R |
| Sprint retrospective | C | **A** | R | R | R | R | R |

---

## Decision-Making Authority

### Strategic Decisions
**Accountable:** Product Manager  
**Examples:** Product direction, feature prioritization, go-to-market timing

### Delivery Decisions
**Accountable:** Project Manager  
**Examples:** Timeline adjustments, resource allocation, process improvements

### Technical Decisions
**Accountable:** Engineering Lead  
**Examples:** Architecture choices, technology stack, technical trade-offs

### Quality Decisions
**Accountable:** QA Engineer (with Eng Lead approval for significant risks)  
**Examples:** Release readiness, acceptable bug threshold, test coverage requirements

---

## Escalation & Exceptions

When roles conflict or clarity is needed:

1. **Team-level:** Discuss in standup or team sync
2. **Management-level:** Escalate to Project Manager + Engineering Lead
3. **Executive-level:** Escalate to Product Lead or VP Engineering

---

## Customization Guide

**To use this template:**

1. Copy this template for your project
2. Update the Team Roster with actual names
3. Modify the RACI matrix based on:
   - Your team structure (add/remove columns)
   - Your project activities (add/remove rows)
   - Your organizational practices
4. Review and validate with the team
5. Update as the project evolves or team changes

**Common Variations:**

- **Small team:** One person may fill multiple roles (e.g., PM+PdM, Dev+QA)
- **Large team:** Split Dev into Frontend/Backend, or multiple squads
- **Different methodologies:** Adjust for Kanban vs Scrum vs Waterfall

---

## Tips for Success

✅ **Do:**
- Review RACI at project kickoff
- Update when team or scope changes
- Use during onboarding for new team members
- Reference during role confusion
- Keep it simple — don't RACI every tiny task

❌ **Don't:**
- Have multiple A's for one task (decision paralysis)
- Make everyone C or I (RACI overload)
- Set-and-forget (keep it current)
- Use as a weapon ("That's not my job per RACI")

---

## Related Documentation
- [Roles & Personas](../octoacme-roles-and-personas.md) — Detailed role descriptions
- [Process Overview](process-overview.md) — How work flows through the project
- [Onboarding Checklist](onboarding-handoff-checklist.md) — Help new team members understand their role
