# Onboarding & Handoff Checklist

## Purpose
Ensure smooth onboarding of new team members and effective knowledge transfer during team transitions.

---

## Part 1: New Team Member Onboarding

**Use this checklist when someone joins the project team**

### Pre-Start (Before Day 1)

**Team Lead / PM:**
- [ ] Send welcome email with start date, time, and meeting link
- [ ] Add to team communication channels (Slack, Teams, email lists)
- [ ] Grant access to project tools (GitHub, Jira, docs, etc.)
- [ ] Assign onboarding buddy
- [ ] Schedule 1:1 with manager for Day 1
- [ ] Share project overview doc and key links

### Week 1: Orientation

**New Team Member:**
- [ ] Complete company-wide onboarding
- [ ] Read [Project Management Overview](../octoacme-project-management-overview.md)
- [ ] Review [Project Charter / One-pager](#) (link to your project doc)
- [ ] Review [RACI Matrix](ownership-raci-template.md) — understand your role
- [ ] Set up development environment (follow repo README)
- [ ] Clone repo and run tests successfully
- [ ] Join all relevant meetings (standups, sprint planning, retros)
- [ ] Meet 1:1 with each team member (5-10 min intros)

**Onboarding Buddy:**
- [ ] Walk through codebase structure
- [ ] Explain team workflow (PR process, branching, etc.)
- [ ] Review [Definition of Done](definition-of-done.md)
- [ ] Show where to find docs and how to navigate them
- [ ] Answer questions and provide context

**Manager / Team Lead:**
- [ ] 1:1 on Day 1: Welcome, expectations, and initial goals
- [ ] Introduce to stakeholders
- [ ] Assign first "onboarding task" (small, well-defined)

### Week 2-4: Ramp Up

**New Team Member:**
- [ ] Complete first task and submit PR
- [ ] Participate in code reviews (review others' code)
- [ ] Attend sprint planning and contribute ideas
- [ ] Shadow on-call or incident response (if applicable)
- [ ] Review recent retrospective notes to understand team improvements
- [ ] Ask questions in team channel (don't stay blocked!)

**Onboarding Buddy:**
- [ ] Review first PR and provide constructive feedback
- [ ] Check in 2x/week to answer questions
- [ ] Gradually reduce support as confidence grows

**Manager / Team Lead:**
- [ ] Weekly 1:1s to discuss progress and blockers
- [ ] Adjust workload based on ramp-up speed
- [ ] Collect feedback on onboarding experience

### End of Month 1: Self-Sufficient

**New Team Member:**
- [ ] Can complete tasks independently
- [ ] Comfortable with PR workflow and code review process
- [ ] Understands team rituals and cadences
- [ ] Knows who to ask for different types of help
- [ ] Contributing in standups and planning

**Manager / Team Lead:**
- [ ] 30-day check-in: How's it going? What support is needed?
- [ ] Gather feedback: What worked well? What could improve in onboarding?
- [ ] Set goals for next 60-90 days

---

## Part 2: Project Handoff Checklist

**Use this checklist when transitioning project ownership or when a team member is leaving**

### Handoff Timeline: 2-4 Weeks Recommended

### Week 1-2: Knowledge Transfer

**Outgoing Team Member:**
- [ ] Schedule handoff meetings with incoming person (or team)
- [ ] Create/update project README with:
  - [ ] Project purpose and goals
  - [ ] Key stakeholders and contacts
  - [ ] Important dates and milestones
  - [ ] Known issues and workarounds
- [ ] Document critical workflows and processes
- [ ] Share credentials (via secure method) and access instructions
- [ ] Review open issues and PRs together
- [ ] Explain current priorities and in-flight work
- [ ] Share tribal knowledge (quirks, gotchas, common issues)

**Incoming Team Member:**
- [ ] Attend all handoff sessions
- [ ] Take notes and ask clarifying questions
- [ ] Review all documentation provided
- [ ] Shadow on day-to-day tasks
- [ ] Start participating in team meetings

### Week 2-3: Shadowing & Pairing

**Outgoing Team Member:**
- [ ] Pair on 2-3 tasks (outgoing drives, incoming observes)
- [ ] Reverse pair on 1-2 tasks (incoming drives, outgoing guides)
- [ ] Review ongoing initiatives and roadmap
- [ ] Introduce incoming person to stakeholders
- [ ] Share context on past decisions (review ADRs if available)
- [ ] Explain escalation paths and who to contact for what

**Incoming Team Member:**
- [ ] Complete 1-2 small tasks with guidance
- [ ] Ask about historical context and rationale
- [ ] Build relationships with stakeholders
- [ ] Review past retrospectives for team insights

### Week 3-4: Transition Period

**Outgoing Team Member:**
- [ ] Incoming person takes the lead; you provide backup
- [ ] Hand over active work items
- [ ] Update team on transition status
- [ ] Share final handoff notes document
- [ ] Set up async communication for questions after departure

**Incoming Team Member:**
- [ ] Take ownership of daily responsibilities
- [ ] Lead team meetings (with outgoing person present)
- [ ] Complete tasks independently
- [ ] Identify gaps and ask questions while outgoing person is still available

### Final Week / Last Day

**Outgoing Team Member:**
- [ ] Transfer ownership of all issues/tickets
- [ ] Remove yourself from active rotations (on-call, etc.)
- [ ] Share final status update with team and stakeholders
- [ ] Provide contact info for urgent questions (if comfortable)
- [ ] Complete exit interview or feedback survey

**Incoming Team Member:**
- [ ] Confirm you have access to all systems
- [ ] Assume full ownership of responsibilities
- [ ] Schedule follow-up with manager to discuss progress

**Manager / Team Lead:**
- [ ] Announce transition to broader team and stakeholders
- [ ] Update RACI matrix and team docs
- [ ] Monitor incoming person for first few weeks
- [ ] Schedule 1:1s to ensure smooth transition

---

## Part 3: Institutional Knowledge Capture

**Critical information that should always be documented:**

### Technical Knowledge
- [ ] Architecture diagrams and design decisions (see [ADR process](decision-log.md))
- [ ] How to build, test, and deploy
- [ ] Common troubleshooting steps
- [ ] Dependencies and integrations
- [ ] Configuration and environment details

### Process Knowledge
- [ ] Team workflows and rituals
- [ ] Escalation procedures
- [ ] On-call responsibilities
- [ ] Release process specifics

### Relationship Knowledge
- [ ] Key stakeholders and their priorities
- [ ] Vendor/partner contacts
- [ ] Cross-team dependencies
- [ ] Customer insights and feedback channels

### Historical Context
- [ ] Why certain decisions were made
- [ ] Past incidents and lessons learned
- [ ] Evolution of the product/project
- [ ] Known limitations and future plans

**Where to Document:**
- **Code:** Inline comments, README files
- **Architecture:** ADRs in `docs/project-management/adr/`
- **Process:** This folder (`docs/project-management/`)
- **Runbooks:** Wiki or internal docs
- **Decisions:** Meeting notes, ADRs, retrospective notes

---

## Emergency Handoff

**When someone leaves unexpectedly (emergency, sudden departure):**

**Immediate (Day 1):**
- [ ] Assess impact: What was this person working on?
- [ ] Identify most critical tasks and re-assign
- [ ] Check for access issues (credentials, permissions)
- [ ] Review open PRs and issues

**Week 1:**
- [ ] Team brainstorm: What knowledge might be missing?
- [ ] Mine Slack/email for context on current work
- [ ] Review code commits and comments for insights
- [ ] Identify "bus factor" risks in other areas

**Week 2-4:**
- [ ] Document discovered knowledge gaps
- [ ] Create missing documentation
- [ ] Distribute responsibilities to reduce single points of failure
- [ ] Update [RACI](ownership-raci-template.md) and team structure

---

## Self-Assessment Questions

**For outgoing team members:**
- What would you want to know if you were inheriting this project?
- What questions do new team members always ask?
- What took you the longest to learn?
- What mistakes did you make that others should avoid?

**For incoming team members:**
- Do you know who to ask when you're stuck?
- Can you complete a typical task end-to-end?
- Do you understand the current priorities?
- Are there gaps in the documentation you've received?

---

## Continuous Improvement

After each onboarding or handoff:
- [ ] Gather feedback on the process
- [ ] Update this checklist with lessons learned
- [ ] Improve documentation based on gaps discovered
- [ ] Share insights in retrospective

---

## Related Documentation
- [Process Overview](process-overview.md) — How work flows through the project
- [RACI Template](ownership-raci-template.md) — Understand roles and responsibilities
- [Roles & Personas](../octoacme-roles-and-personas.md) — Detailed role descriptions
- [Meeting Notes Template](meeting-notes-template.md) — Capture tribal knowledge in meetings
- [Decision Log / ADRs](decision-log.md) — Document important decisions
