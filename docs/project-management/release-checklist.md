# Release Checklist

## Purpose
Ensure all critical steps are completed before and after deploying to production.

---

## Pre-Release Checklist

### Code Quality & Testing
- [ ] All acceptance criteria met for included features
- [ ] All PRs merged to release branch
- [ ] No open blockers or critical bugs
- [ ] Code review completed and approved
- [ ] All automated tests passing (unit, integration, E2E)
- [ ] Manual QA completed for critical paths
- [ ] Regression testing completed
- [ ] Performance testing completed (if applicable)
- [ ] Load/stress testing completed (for major releases)
- [ ] Security scan passed (no high/critical vulnerabilities)
- [ ] Dependency vulnerabilities addressed

### Documentation
- [ ] Release notes drafted and reviewed
- [ ] User-facing documentation updated
- [ ] API documentation updated (if applicable)
- [ ] Internal runbook/troubleshooting guide updated
- [ ] Configuration changes documented
- [ ] Migration steps documented (if applicable)

### Infrastructure & Configuration
- [ ] Infrastructure changes tested in staging
- [ ] Database migrations tested and reversible
- [ ] Environment variables/configs reviewed
- [ ] Feature flags configured (if using)
- [ ] Third-party integrations tested
- [ ] SSL certificates valid (if applicable)
- [ ] DNS changes scheduled (if applicable)

### Monitoring & Alerting
- [ ] Production monitoring configured
- [ ] Error tracking/logging verified
- [ ] Performance metrics/dashboards ready
- [ ] Alerts configured for critical errors
- [ ] On-call schedule confirmed

### Deployment Preparation
- [ ] Deployment window scheduled and communicated
- [ ] Stakeholders notified of release timing
- [ ] Rollback plan documented and tested
- [ ] Backup/snapshot completed (if applicable)
- [ ] Deployment runbook reviewed
- [ ] Team availability confirmed for deployment window

### Staging Validation
- [ ] Deployed to staging environment
- [ ] Smoke tests passed in staging
- [ ] Stakeholder demo/acceptance in staging
- [ ] Performance validated in staging
- [ ] Data migration tested in staging (if applicable)

### Approvals
- [ ] Product Manager approval
- [ ] Technical Lead approval
- [ ] Security team approval (if required)
- [ ] Go/No-go decision documented

---

## Deployment Checklist

### Pre-Deployment
- [ ] Final verification: all pre-release items complete
- [ ] Team assembled and ready (deployer + on-call)
- [ ] Communication channel open (Slack, Teams, etc.)
- [ ] Status page updated (if applicable): "Maintenance scheduled"

### Deployment Steps
- [ ] Database backup completed
- [ ] Announce deployment start to stakeholders
- [ ] Put application in maintenance mode (if applicable)
- [ ] Run database migrations
- [ ] Deploy application code
- [ ] Verify configuration applied correctly
- [ ] Restart services as needed
- [ ] Exit maintenance mode

### Post-Deployment Verification
- [ ] Application starts successfully
- [ ] Health check endpoints responding
- [ ] Smoke tests passed in production
- [ ] Critical user flows tested manually
- [ ] No errors in logs (or only expected errors)
- [ ] Performance metrics normal
- [ ] Database migrations completed successfully
- [ ] Third-party integrations working

---

## Post-Release Checklist

### Monitoring & Validation
- [ ] Monitor error rates for 1-4 hours post-deployment
- [ ] Monitor performance metrics (latency, throughput)
- [ ] Verify success metrics/analytics tracking
- [ ] Check for customer-reported issues
- [ ] Review support ticket queue

### Communication
- [ ] Announce successful deployment to stakeholders
- [ ] Publish release notes
- [ ] Update status page to "Operational"
- [ ] Notify customer support team
- [ ] Post in team channel/announce to company (if major release)

### Documentation & Cleanup
- [ ] Tag release in version control
- [ ] Update version number in docs/package files
- [ ] Archive deployment notes/logs
- [ ] Close related issues/tickets
- [ ] Update project status

### Follow-Up
- [ ] Schedule post-release retrospective (within 1 week)
- [ ] Track adoption/usage metrics
- [ ] Monitor for bugs in first week
- [ ] Collect customer feedback

---

## Rollback Checklist

**Use if deployment fails or critical issues are discovered**

- [ ] Declare rollback decision and notify team
- [ ] Stop current deployment (if in progress)
- [ ] Restore database from backup (if needed)
- [ ] Revert to previous application version
- [ ] Verify rollback successful (run smoke tests)
- [ ] Monitor for stability
- [ ] Update status page and notify stakeholders
- [ ] Create incident post-mortem issue
- [ ] Document root cause and lessons learned

---

## Release Types

### Hotfix (Critical Production Issue)
**Accelerated process for urgent fixes**
- Minimum viable testing (focus on fix validation)
- Required: code review, staging test, rollback plan
- Post-deploy: immediate monitoring, incident report

### Patch Release (Minor fixes, no new features)
- Standard checklist
- Can be expedited if low-risk
- May skip stakeholder demo if no user-facing changes

### Minor Release (New features, non-breaking changes)
- Full checklist
- Stakeholder demo required
- Marketing/announcement coordination

### Major Release (Breaking changes, significant features)
- Full checklist + extended validation
- Additional stakeholder approvals
- Customer migration support plan
- Extended monitoring period (24-48 hours)

---

## Related Documentation
- [Process Overview](process-overview.md) — Overall workflow including release phase
- [Release & Deployment Guide](../octoacme-release-and-deployment.md) — Detailed release guidance
- [Definition of Done](definition-of-done.md) — Quality criteria before release
- [Triage Playbook](triage-playbook.md) — How to handle issues found post-release
