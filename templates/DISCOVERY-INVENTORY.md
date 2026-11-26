# Infrastructure Discovery Inventory Template

Use this template to structure discovery workshops and record validated findings. Copy the table into an approved project workbook or CMDB process when needed.

> Use synthetic values in this public repository. Never publish real hostnames, IP addresses, diagrams, owners, vulnerabilities, asset IDs or customer information.

## Inventory fields

| Field | Description / guidance | Example (synthetic) |
|---|---|---|
| Record ID | Unique project tracking identifier | ASSET-001 |
| Service ID | Service or application identifier | SVC-PORTAL |
| Service name | Business-facing service name | Example Portal |
| Environment | Production, test, development, etc. | Production |
| Site / region | Current hosting location | DC-NORTH |
| Business owner | Role or approved project contact | Service Owner |
| Technical owner | Responsible technical team | Platform Team |
| Criticality | Agreed business impact tier | High |
| Data classification | Approved classification | Confidential |
| Platform | Physical, virtual, cloud, appliance | Virtual machine |
| OS / version | Operating system and supported release | Linux (example) |
| Compute | CPU and memory allocation / utilization | 4 vCPU / 16 GB |
| Storage | Capacity, performance and growth | 500 GB |
| Network zone | Approved segment / security zone | APP-ZONE |
| IP / DNS | Store in controlled project records, not public examples | REDACTED |
| Dependencies | Related service IDs | SVC-DNS; SVC-ID |
| Interfaces | APIs, ports, protocols, external endpoints | Document securely |
| Backup | Policy, last restore test, owner | Daily; restore evidence pending |
| Recovery objectives | Approved RTO / RPO | Confirm with owner |
| Monitoring | Tooling, alert coverage and escalation | Standard platform monitoring |
| Migration disposition | Rehost, replatform, refactor, retain, retire | Rehost |
| Target | Approved target platform / site | Target Cloud |
| Constraints | Licensing, latency, vendor, compliance | Vendor compatibility review |
| Evidence reference | Link to controlled source record | PROJECT-REF-001 |
| Validation status | Unverified, in review, validated | In review |
| Last reviewed | Date and reviewer role | YYYY-MM-DD / Architect |

## Discovery validation checklist

- [ ] Scope and source systems agreed
- [ ] Business and technical owners identified
- [ ] Service criticality and data classification confirmed
- [ ] Compute, storage and network facts validated
- [ ] Upstream and downstream dependencies reviewed
- [ ] External integrations and certificates identified
- [ ] Backup and restore evidence checked
- [ ] Monitoring and operational support understood
- [ ] Recovery objectives approved by service owner
- [ ] Migration disposition and target agreed
- [ ] Unknowns recorded with owner and due date

## Handling unknowns

Record unknowns as actions rather than silently assuming values. Include an accountable role, due date, impact if unresolved and the decision gate affected.

## Data handling

Keep sensitive discovery data in the organization's approved systems with access controls and retention rules. This template is generic and is not a substitute for formal security, privacy or architecture review.
