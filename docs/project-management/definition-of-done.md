# Definition of Done

## Purpose
Establish clear, consistent criteria that all work items must meet before being considered complete.

## General Definition of Done
All work items must meet these criteria before moving to "Done":

### Code Quality
- [ ] Code follows project style guide and conventions
- [ ] Code is peer-reviewed and approved
- [ ] No linter errors or warnings
- [ ] Code is self-documenting with clear variable/function names
- [ ] Complex logic includes explanatory comments

### Testing
- [ ] Unit tests written and passing (minimum 80% coverage for new code)
- [ ] Integration tests added where applicable
- [ ] All existing tests still pass
- [ ] Manual testing completed for UI changes
- [ ] Edge cases and error conditions tested

### Security
- [ ] Security scan passed (no high/critical vulnerabilities)
- [ ] Input validation implemented where needed
- [ ] Authentication/authorization properly enforced
- [ ] Sensitive data properly protected (no hardcoded secrets)

### Documentation
- [ ] User-facing documentation updated (if applicable)
- [ ] API documentation updated (if applicable)
- [ ] README or setup instructions updated (if applicable)
- [ ] Release notes drafted

### Acceptance Criteria
- [ ] All acceptance criteria from the issue/story met
- [ ] Stakeholder/Product Manager review completed
- [ ] Demo to team completed (if applicable)

### Deployment Readiness
- [ ] Feature flags configured (if applicable)
- [ ] Configuration changes documented
- [ ] Deployment/rollback plan documented
- [ ] Monitoring and alerting configured (if applicable)

### Review & Approval
- [ ] PR approved by at least one reviewer
- [ ] All review comments addressed or resolved
- [ ] Merge conflicts resolved
- [ ] CI/CD pipeline green

## Story-Specific DoD
For certain work item types, add these additional criteria:

### Features
- [ ] Validated against user stories/requirements
- [ ] Accessibility standards met (WCAG 2.1 AA)
- [ ] Performance benchmarks met
- [ ] Analytics/tracking implemented (if applicable)

### Bug Fixes
- [ ] Root cause identified and documented
- [ ] Fix validated in affected environments
- [ ] Regression test added to prevent recurrence

### Technical Debt / Refactoring
- [ ] Refactoring scope clearly defined and limited
- [ ] No functional behavior changes (or clearly documented)
- [ ] Performance impact assessed

### Documentation
- [ ] Accuracy verified by subject matter expert
- [ ] Examples tested and working
- [ ] Peer reviewed for clarity

## Environment-Specific DoD

### Before merging to main/trunk
- [ ] All general DoD criteria met
- [ ] Feature branch up to date with main
- [ ] No breaking changes (or migration plan documented)

### Before deploying to staging
- [ ] Smoke tests defined
- [ ] Test data prepared (if needed)

### Before deploying to production
- [ ] Staging validation completed
- [ ] Release checklist completed
- [ ] Stakeholders notified
- [ ] Rollback plan ready

## Exceptions
Exceptions to the DoD require:
- Written justification
- Product Manager approval
- Documentation in PR/issue

Common valid exceptions:
- Hotfixes for critical production issues (streamlined DoD)
- Experimental features behind feature flags
- Documentation-only changes (subset of DoD)

## Related Documentation
- [Process Overview](process-overview.md) — Overall workflow
- [Execution & Tracking](../octoacme-execution-and-tracking.md) — Daily workflows and quality standards
- [Release Checklist](release-checklist.md) — Production deployment criteria
