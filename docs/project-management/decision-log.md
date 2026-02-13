# Architecture Decision Records (ADR)

## Purpose
Document significant architectural and technical decisions made during the project, including context and consequences.

## What is an ADR?
An Architecture Decision Record (ADR) captures an important architectural decision made along with its context and consequences. ADRs create a log of decisions that helps teams understand:
- Why certain choices were made
- What alternatives were considered
- What trade-offs were accepted
- What the expected impact is

## When to Create an ADR
Create an ADR when making decisions about:
- Technology stack or framework selection
- Data architecture or storage solutions
- API design patterns
- Security or authentication approaches
- Deployment architecture
- Third-party integrations
- Significant refactoring approaches

**Not every decision needs an ADR** — focus on decisions that:
- Have long-term impact
- Are difficult or costly to reverse
- Affect multiple teams or systems
- Involve significant trade-offs

## ADR Location
- Store ADRs in `docs/project-management/adr/` directory
- Name files sequentially: `0001-decision-title.md`, `0002-decision-title.md`, etc.
- Use the template in `adr/0000-template.md`

## ADR Workflow

### 1. Draft the ADR
- Copy `0000-template.md` to a new file with the next number
- Fill in Status as "Proposed"
- Document the context, decision, and consequences

### 2. Review
- Share ADR with relevant stakeholders
- Discuss in team meeting or async
- Update based on feedback

### 3. Accept or Reject
- Update Status to "Accepted" or "Rejected"
- If accepted, implement the decision
- If rejected, document why and consider alternatives

### 4. Maintain
- ADRs are immutable once accepted (don't edit old decisions)
- If a decision is superseded, create a new ADR and link to the old one
- Update Status of old ADR to "Superseded by ADR-XXXX"

## ADR Index

| Number | Title | Status | Date |
|--------|-------|--------|------|
| [0000](adr/0000-template.md) | Template | Template | N/A |

*Add new ADRs to this index as they are created*

## Related Documentation
- [Process Overview](process-overview.md) — Overall workflow
- [Project Planning](../octoacme-project-planning.md) — Decision-making in planning phase
