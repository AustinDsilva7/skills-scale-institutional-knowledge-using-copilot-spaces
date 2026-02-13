# Triage Playbook

## Purpose
Provide a consistent framework for prioritizing, labeling, and responding to issues and incidents.

---

## Severity Levels

### 🔴 Critical (P0)
**Definition:** Production is down or severely impacted for all/most users

**Examples:**
- Complete service outage
- Data loss or corruption
- Security breach or vulnerability actively exploited
- Payment processing failure

**Response SLA:**
- **Acknowledgment:** Immediate (< 15 minutes)
- **Initial Response:** < 30 minutes
- **Resolution Target:** < 4 hours
- **Team Involvement:** All hands, page on-call immediately

**Escalation:**
- Immediately notify: Engineering Lead, Product Lead, On-call engineer
- Create incident channel and start incident log
- Consider external communication (status page)

---

### 🟠 High (P1)
**Definition:** Major functionality broken or severely degraded for many users

**Examples:**
- Key feature completely unavailable
- Significant performance degradation (>50% slower)
- Critical workflow blocked for subset of users
- Data inconsistency affecting operations

**Response SLA:**
- **Acknowledgment:** < 1 hour
- **Initial Response:** < 2 hours
- **Resolution Target:** < 24 hours
- **Team Involvement:** Assigned developer + on-call backup

**Escalation:**
- Notify: Engineering Lead, Product Manager
- Daily updates required until resolved
- Consider workaround communication

---

### 🟡 Medium (P2)
**Definition:** Moderate impact on functionality; workaround available

**Examples:**
- Non-critical feature broken
- Moderate performance issue
- Cosmetic UI bugs affecting usability
- Intermittent errors affecting small user segment

**Response SLA:**
- **Acknowledgment:** < 4 hours (business hours)
- **Initial Response:** < 1 business day
- **Resolution Target:** < 1 week
- **Team Involvement:** Assigned to sprint backlog

**Escalation:**
- Notify: Team lead
- Weekly updates if not resolved within target

---

### 🟢 Low (P3)
**Definition:** Minor issue with minimal impact; nice-to-have improvements

**Examples:**
- Minor UI inconsistencies
- Feature request or enhancement
- Documentation gaps
- Low-impact bugs with easy workarounds

**Response SLA:**
- **Acknowledgment:** < 2 business days
- **Initial Response:** < 1 week
- **Resolution Target:** Backlog prioritization
- **Team Involvement:** Scheduled in future sprint

**Escalation:**
- None required unless aging beyond 30 days

---

## Issue Labels

### Severity Labels
- `severity:critical` — P0 issues
- `severity:high` — P1 issues
- `severity:medium` — P2 issues
- `severity:low` — P3 issues

### Type Labels
- `type:bug` — Something broken
- `type:feature` — New functionality
- `type:enhancement` — Improvement to existing feature
- `type:documentation` — Docs-only changes
- `type:security` — Security-related
- `type:performance` — Performance issue
- `type:technical-debt` — Refactoring or cleanup

### Status Labels
- `status:triage` — Needs initial review
- `status:accepted` — Confirmed and prioritized
- `status:blocked` — Cannot progress (note blocker in comments)
- `status:in-progress` — Actively being worked
- `status:needs-review` — Awaiting feedback
- `status:ready-to-close` — Resolved, pending verification

### Area Labels
- `area:frontend` — UI/client-side
- `area:backend` — Server/API
- `area:database` — Data layer
- `area:infrastructure` — DevOps/deployment
- `area:testing` — QA/testing
- `area:docs` — Documentation

---

## Triage Process

### Daily Triage (for new issues)
**Who:** Rotating team member or dedicated triage lead  
**When:** Daily standup or dedicated triage time  
**Duration:** 15-30 minutes

#### Steps:
1. **Review all `status:triage` issues**
2. **Assess severity** — Apply severity label (P0-P3)
3. **Categorize** — Add type and area labels
4. **Validate** 
   - Is this a duplicate? Link and close if yes
   - Is there enough information? Request clarification if no
   - Can it be reproduced? Verify and document steps
5. **Prioritize** — Move to appropriate backlog/sprint
6. **Assign ownership** (or leave unassigned for backlog)
7. **Update status** — Change to `status:accepted` or close if not valid

### Weekly Backlog Review
**Who:** Product Manager + Engineering Lead  
**When:** Weekly planning meeting  
**Duration:** 30-60 minutes

#### Steps:
1. Review all open P1 and P2 issues
2. Re-assess priority if business context changed
3. Identify issues blocked > 5 days — escalate or close
4. Groom P3 issues — close stale items (>60 days, no activity)
5. Plan upcoming sprint capacity for bug fixes vs features

---

## Escalation Paths

### Level 1: Team Triage
**When:** Daily standup or immediate for P0/P1  
**Who Handles:** Engineering team, Team Lead  
**Action:** 
- Assess and assign
- Begin work or identify blocker
- Create action plan

### Level 2: Management Escalation
**When:** 
- P0 not resolved in 4 hours
- P1 not resolved in 24 hours
- Issue blocked with no clear path forward
- Cross-team dependency blocking progress

**Who Handles:** Engineering Lead + Product Manager  
**Action:**
- Unblock dependencies
- Reallocate resources
- Adjust priorities
- Communicate to stakeholders

### Level 3: Executive Escalation
**When:**
- P0 extending beyond initial estimates
- Customer escalation or PR risk
- Legal, compliance, or contract implications
- Multi-team coordination required

**Who Handles:** VP Engineering, Product Lead, Executive Sponsor  
**Action:**
- Company-level coordination
- Customer communication
- External vendor engagement
- Risk mitigation decisions

---

## Incident Response (for Critical Issues)

### When to Declare an Incident
- Any P0 issue
- Multiple P1 issues with common cause
- Widespread customer impact
- Security event

### Incident Workflow
1. **Declare incident** — Create incident channel (e.g., `#incident-YYYY-MM-DD`)
2. **Assign roles:**
   - **Incident Commander:** Coordinates response
   - **Technical Lead:** Drives technical resolution
   - **Communications Lead:** Handles stakeholder updates
3. **Investigate & mitigate:** Focus on stopping the bleeding first
4. **Communicate:** Regular updates (every 30 min for P0)
5. **Resolve:** Implement fix and verify
6. **Close incident:** Update status page, notify stakeholders
7. **Post-mortem:** Schedule within 48 hours (see template below)

### Incident Post-Mortem Template
- **Incident Summary:** What happened?
- **Timeline:** Key events with timestamps
- **Root Cause:** Why did it happen?
- **Resolution:** How was it fixed?
- **Impact:** Customer/business impact
- **Action Items:** Preventative measures (owner + due date)
- **Lessons Learned:** What went well, what to improve

---

## Stale Issue Policy

**30 days:** Issues with no activity get `status:needs-info` label and comment requesting update  
**60 days:** P3 issues with no activity are closed with note "Closing due to inactivity"  
**90 days:** P2 issues reviewed for re-prioritization or closure  
**P0/P1:** Never auto-close; require explicit resolution

---

## Communication Templates

### Initial Response (P0/P1)
```
Thank you for reporting this. We've triaged this as [P0/P1] and are actively investigating.

**Current Status:** [Brief description]
**Assigned To:** [Name]
**Next Update:** [Time]

We'll provide updates every [frequency] until resolved.
```

### Resolution Notification
```
This issue has been resolved in [PR link / release version].

**Resolution:** [Brief explanation]
**Available:** [Now / After next deployment / Release date]
**Verification:** [How to verify fix]

Please confirm the fix works for you. Closing this issue but happy to reopen if needed.
```

---

## Related Documentation
- [Process Overview](process-overview.md) — Overall workflow
- [Execution & Tracking](../octoacme-execution-and-tracking.md) — Blocker escalation details
- [Definition of Done](definition-of-done.md) — Quality standards to prevent issues
- [Release Checklist](release-checklist.md) — Pre-release validation to catch issues early
