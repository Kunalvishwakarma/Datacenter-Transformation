# Cutover and Rollback Runbook Template

> This is a generic template, not an approved production procedure. Adapt it through the organization's change, security and service governance processes. All examples must remain synthetic in this public repository.

## 1. Change information

| Field | Value |
|---|---|
| Change reference | CHG-XXXX |
| Service / scope | Synthetic service name |
| Source and target | Approved project references |
| Change owner | Role / team |
| Technical lead | Role / team |
| Business approver | Service owner role |
| Planned window | YYYY-MM-DD HH:MM to HH:MM |
| Communication channel | Approved project channel |
| Runbook version | 1.0 |
| Go / no-go authority | Named role in controlled change record |

## 2. Entry criteria

- [ ] Change approved and stakeholders notified
- [ ] Scope, sequence and owners confirmed
- [ ] Dependency map reviewed
- [ ] Target capacity and connectivity validated
- [ ] Firewall, routing, DNS and identity changes approved
- [ ] Backup completed and restore evidence verified
- [ ] Monitoring, logging and alert routing tested
- [ ] Functional and non-functional test plans ready
- [ ] Rollback method rehearsed and feasible within the window
- [ ] Support teams and decision-makers available
- [ ] Business impact and outage communication agreed

If any critical entry criterion is not met, pause and escalate to the change authority.

## 3. Execution log

| Step | Action | Responsible role | Planned time | Actual time | Evidence / result |
|---|---|---|---|---|---|
| 1 | Open bridge and confirm attendance | Change lead | T-30 min | | |
| 2 | Confirm go / no-go and record decision | Change authority | T-15 min | | |
| 3 | Confirm latest backup / restore point | Backup lead | T-10 min | | |
| 4 | Freeze agreed changes and confirm baseline | Technical lead | T0 | | |
| 5 | Execute approved migration sequence | Platform team | | | |
| 6 | Apply approved network / DNS transition | Network team | | | |
| 7 | Run technical smoke tests | Application team | | | |
| 8 | Run business validation | Service owner | | | |
| 9 | Confirm monitoring and support handover | Operations | | | |
| 10 | Record complete / rollback decision | Change authority | | | |

## 4. Validation checklist

- [ ] Application starts and remains healthy
- [ ] User authentication and authorization work
- [ ] Critical business transactions complete
- [ ] Database and data consistency checks pass
- [ ] Required integrations respond
- [ ] DNS and network paths behave as expected
- [ ] Performance is within agreed thresholds
- [ ] Security logging and monitoring are operational
- [ ] Backup jobs and recovery controls are active
- [ ] Service owner accepts the outcome

Use measurable, service-specific thresholds agreed before the change. Do not invent thresholds during the cutover.

## 5. Rollback decision

Examples of potential rollback triggers (define exact thresholds for each service before approval):
- Critical business transaction fails and cannot be restored within the agreed decision window.
- Data integrity cannot be confirmed.
- A critical dependency is unavailable.
- Security control or access boundary is materially broken.
- Service health remains outside the agreed threshold after the permitted remediation period.
- Remaining change window is insufficient to complete safe validation.

The change authority and service owner must understand who can call rollback and how the decision is recorded.

## 6. Rollback procedure outline

1. Announce rollback decision and freeze further forward changes.
2. Confirm rollback owner and bridge participants.
3. Execute the pre-approved reversal sequence.
4. Restore routing, DNS, configuration or workload placement as documented.
5. Validate service operation on the source environment.
6. Verify data consistency and reconcile any transactions as required.
7. Confirm monitoring, access and support coverage.
8. Obtain service-owner confirmation.
9. Record outcome, timestamps, evidence and follow-up actions.

Never improvise destructive data actions. Follow the service-specific, approved recovery procedure.

## 7. Closure and hypercare

- [ ] Final status communicated to stakeholders
- [ ] Change record updated with evidence and actual timings
- [ ] Known issues and workarounds documented
- [ ] Hypercare owner and exit criteria confirmed
- [ ] Configuration and asset records updated
- [ ] Backup and monitoring ownership confirmed
- [ ] Lessons learned and corrective actions assigned

## 8. Approval record

| Decision | Name / role | Decision | Timestamp | Reference |
|---|---|---|---|---|
| Go / no-go | Change authority | Pending | | |
| Technical readiness | Technical lead | Pending | | |
| Business acceptance | Service owner | Pending | | |
| Rollback completion (if used) | Recovery lead | N/A | | |
