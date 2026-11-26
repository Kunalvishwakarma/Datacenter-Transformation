# Synthetic Case Study: Hybrid Datacenter Migration

> **Portfolio demonstration only.** This scenario, organization, locations, systems, volumes, dates and outcomes are fictional. It is not a description of any employer or customer engagement.

## 1. Scenario

A fictional organization operates two legacy datacenter sites and wants to consolidate workloads into a modern colocation facility while moving selected services to Azure. The goals are to reduce operational complexity, improve recoverability, standardize security controls and retire aging infrastructure.

### Illustrative scope

| Domain | Synthetic baseline |
|---|---|
| Sites | DC-NORTH and DC-SOUTH |
| Workloads | 42 fictional application/service groups |
| Platforms | Virtualized compute, physical appliances and shared services |
| Connectivity | Dual WAN, site-to-site VPN and private cloud connectivity |
| Shared services | DNS, directory, NTP, backup, monitoring |
| Target | Consolidated colocation plus Azure landing zone |

These figures are deliberately illustrative and must not be presented as actual delivery metrics.

## 2. Outcomes and success criteria

- Every in-scope service has an accountable owner and documented dependencies.
- Target architecture and security controls are approved before migration.
- Each migration wave has entry criteria, a cutover sequence and a tested rollback path.
- Business and technical validation is recorded after each move.
- Legacy assets are retired only after service-owner approval and dependency clearance.

## 3. Delivery approach

### Phase A — Mobilize and discover
1. Confirm scope, stakeholders, governance and decision rights.
2. Build an inventory of applications, infrastructure, interfaces and support contracts.
3. Identify service criticality, data classification and recovery requirements.
4. Map upstream/downstream dependencies, including DNS, identity, certificates and network paths.
5. Validate discovery findings with service owners.

**Exit gate:** inventory completeness and ownership accepted; material unknowns have owners and due dates.

### Phase B — Assess and design
1. Classify workloads by business criticality, technical complexity and migration suitability.
2. Define target compute, storage, network, identity, backup and monitoring patterns.
3. Design segmentation, privileged access, logging and secure administration.
4. Confirm connectivity, IP/DNS strategy, certificates and external integrations.
5. Define resilience, recovery objectives and operational support.

**Exit gate:** target design, security review and service transition approach approved.

### Phase C — Plan migration waves
Group services by dependency, business calendar, technical risk and recovery complexity. Move low-risk representative services first to validate patterns. Keep tightly coupled services together where separation would create avoidable risk.

**Exit gate:** each wave has named owners, prerequisites, test evidence, approved window and rollback decision points.

### Phase D — Prepare and execute
1. Complete pre-migration backups and verify restore evidence.
2. Confirm capacity, connectivity, firewall rules, DNS, identity and monitoring.
3. Conduct a readiness review and stakeholder briefing.
4. Execute the approved runbook with timestamped checkpoints.
5. Validate service health and business transactions.
6. Invoke rollback if agreed thresholds are breached.

**Exit gate:** service owner accepts the migrated service or rollback is completed and incident governance takes over.

### Phase E — Stabilize and decommission
1. Monitor service performance during hypercare.
2. Resolve defects and transfer support ownership.
3. Confirm backup, monitoring, asset and configuration records.
4. Obtain explicit decommission authorization.
5. Sanitize data and retire access, circuits and assets under approved controls.

## 4. Example migration wave model

| Wave | Example scope | Strategy | Key control |
|---|---|---|---|
| W0 | Shared platform pilot | Prove connectivity and operational patterns | Rollback rehearsal |
| W1 | Low-criticality services | Rehost or rebuild based on assessment | Service-owner validation |
| W2 | Standard business services | Group by dependency | End-to-end testing |
| W3 | Critical / tightly coupled services | Coordinated migration | Business-led go/no-go |
| W4 | Residual legacy services | Exception-led disposition | Formal decommission approval |

## 5. Governance and decision points

- **Design authority:** approves target patterns and exceptions.
- **Change authority:** approves production change windows and risk.
- **Service owner:** accepts business functionality and service impact.
- **Technical lead:** confirms technical readiness and execution evidence.
- **Incident manager:** coordinates response if service restoration is required.

A go/no-go decision should consider readiness evidence, open high risks, backup/restore status, stakeholder availability, business calendar and rollback feasibility—not schedule pressure alone.

## 6. Illustrative measures

Track measures consistently and define the denominator before reporting:
- Inventory coverage: discovered in-scope items with validated owners and attributes.
- Dependency coverage: services with reviewed dependency maps.
- Wave readiness: planned wave items meeting all entry criteria.
- Change success: changes completed without unplanned service-impacting rollback.
- Validation completion: services with signed technical and business checks.
- Decommission closure: assets with complete approval and evidence.

Do not invent achieved percentages or claim these illustrative measures as personal project results.

## 7. Lessons to test in a real engagement

- Discovery quality determines migration predictability.
- Shared services and identity dependencies often create cross-wave risk.
- DNS TTL, certificates, firewall policy and monitoring need explicit ownership.
- Rollback must be technically feasible and time-bounded.
- Decommissioning needs its own plan, approvals and evidence.
- Operational acceptance should be designed before the first migration wave.

## 8. Related templates

- [Discovery inventory](../templates/DISCOVERY-INVENTORY.md)
- [Dependency mapping](../templates/DEPENDENCY-MAPPING.md)
- [Migration wave tracker](../templates/MIGRATION-WAVE-TRACKER.csv)
- [Cutover and rollback runbook](../runbooks/CUTOVER-ROLLBACK-RUNBOOK.md)
- [Risk register](../templates/RISK-REGISTER.csv)
