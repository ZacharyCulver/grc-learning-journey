# CGRC Domain 7: Compliance Maintenance and Continuous Monitoring

> Original study notes based on the official ISC2 CGRC self-paced Domain 7 catalogue (lesson view: Continuous Monitoring) and Official ISC2 CGRC Digital Textbook, 7th edition (sections 7.1–7.4). Reviewed November 2026. No proprietary practice questions or passages are reproduced.

## Domain purpose

Authorization is a risk decision at a point in time; a system, its threats, obligations, and dependencies keep changing. Domain 7 maintains confidence that controls still work, findings are addressed, changes are approved, incidents are handled, compliance evidence stays current, and retirement is orderly.

The official textbook groups the work into **system change management**, **ongoing compliance activities**, **audit activities**, and **decommissioning**. The course lesson list also emphasizes monitoring strategies, risk remediation, maintenance, awareness/training, evidence, and stakeholder communication.

## 1. Changes trigger risk analysis

A change can alter performance, risk, compliance obligations, or stakeholder expectations. Examples include software releases, a new information type, a cloud-provider migration, policy changes, a significant vulnerability, an incident, and a modified interface. Compare the proposed state with the approved configuration and security/privacy baseline. Decide whether the change needs new testing, recategorization, control selection, privacy analysis, or an authorization update.

A baseline is a known reference state, not a prohibition on improvement. Revisions must be reviewed, approved, versioned, and communicated. Keep the asset inventory, boundary/data-flow diagrams, SSP, privacy plan, test cases, risk register, and monitoring measures consistent with the deployed state. NIST-style RMF monitoring and ISO-style ISMS monitoring may use different terminology, but both require disciplined evaluation of change and evidence of continued control operation.

**Scenario:** A personnel application begins sending an export to a new analytics service. Even if the code change is small, the new recipient, purpose, contract, jurisdiction, privacy exposure, and inherited safeguards may materially change the risk decision.

## 2. Use formal change control

A useful change request records the requester, business need, affected components and controls, implementation and backout plan, security/privacy analysis, test evidence, dependencies, schedule, approvals, and post-change validation. The change control board (CCB) or technical review board (TRB) evaluates technical and operational impacts; the risk/authorization authority handles decisions reserved to that role. Approval of a change ticket is not automatically acceptance of a new high residual risk.

Flow: **request → impact analysis → review/approval → test → deploy → verify/validate → update records → monitor**. Emergency changes may use an expedited path but still need documented authority and retrospective review. A rollback plan should state the trigger, responsible person, restoration steps, expected data impact, and how the prior secure state will be verified.

Track readiness, progress, and outcomes. If a deployment fails, capture the actual configuration and new risks; a rollback that restores functionality but leaves unauthorized accounts is not a successful security rollback. Configuration-management records should reconcile the approved baseline with what is running.

## 3. Design ongoing compliance monitoring

Information Security Continuous Monitoring (ISCM) is a coordinated strategy for observing controls, assets, vulnerabilities, and changes, analyzing the results, reporting risk, and responding. Decide what must be monitored, by whom, with what tools and evidence, at which frequency, and to which decision-maker. Monitoring is broader than a dashboard: its data must cause informed action.

Set review frequency according to law/contract/policy, control criticality and volatility, system impact, exposure, open findings, and stakeholder needs. NIST guidance often places frequency in an organization-wide strategy refined at system level; ISO management-system work also calls for planned monitoring, evaluation, internal audits, and management review. Do not invent a universal monthly or annual interval when the requirement is risk- and context-dependent.

Use **KPIs** to track performance (for example, on-time access reviews) and **KRIs** to signal exposure (for example, overdue critical vulnerabilities). Define thresholds, data sources, owners, data quality checks, and escalation. Sample or automate where appropriate, but understand coverage and blind spots. A metric that nobody reviews or trusts is not a control.

## 4. Monitor systems, assets, incidents, and contingencies

Maintain an inventory of components, users, data stores, interfaces, service providers, and inherited controls. Compare expected with observed configuration, availability, access, logs, vulnerability status, and control test results. Alert on material changes and relate them to the system's impact and current authorization conditions.

Incident response and contingency activities are part of continued compliance. Detect and analyze events, coordinate response under the approved plan, preserve evidence, notify appropriate parties, recover service, and feed lessons learned into controls and monitoring. Test recovery arrangements, not just backups. Applicable breach-notification rules and contractual reporting timeframes must be determined for the actual data and jurisdiction.

An incident can trigger immediate reassessment or authorization review even if the routine monitoring calendar has not reached its next date.

## 5. Remediate and track risk

Risk analysis identifies a changed threat, weakness, likelihood, impact, and affected mission; treatment selects an authorized response. A practical remediation cycle is **identify and prioritize → implement the response → verify and track to closure**. Assess the effect of both security and privacy changes.

Vulnerability management needs authorized scanning scope, safe methods, asset coverage, severity/context, ownership, deadlines, exceptions, retests, and reporting. A scanner finding is not automatically a confirmed exploit path; a clean scan is not proof of no vulnerabilities. Combine scan results with configuration, intelligence, testing, and mission context. Record false-positive rationale and treat false negatives as a known limitation.

Use a POA&M or equivalent action tracker to show deficiency, risk, interim measure, responsible owner, milestones, due date, evidence of closure, and status. A late milestone should be escalated, not quietly rolled forward. Retest after remediation and update the SSP and risk picture.

## 6. Maintenance, evidence, and communication

System maintenance includes authorized patching, replacement, configuration changes, repairs, and supporting logistics. Assess potential effects before work, control access to maintenance personnel and tools, test afterward, and restore the approved baseline. Preserve change tickets, scan results, configuration histories, assessment results, logs, and test artifacts with provenance and retention appropriate to the requirement.

Update documentation when the system's real behavior changes: SSP implementation statements, privacy plan, diagrams, component inventory, risk assessment, POA&M, contingency plan, operating procedures, and monitoring strategy. Communicate material changes and residual risk to system owners, common-control providers, assessors, mission officials, and authorizing officials according to their roles. Evidence collection is not an annual scramble; design operational processes to generate it routinely.

Awareness and role-based training must be delivered, documented, and retained. Training needs change when duties, threats, systems, laws, or procedures change. A signed attendance sheet is evidence of participation, not necessarily proof that the person can carry out a control; add exercises or performance checks where risk warrants them.

## 7. Audit and revise the monitoring strategy

Required audits and assessments may involve control tests, vulnerability scans, personnel interviews, and review of configuration-management, risk-analysis, and risk-treatment records. Use the specific criteria and period required by the governing framework or contract. An interview can explain a process but should be corroborated with records and tests where possible.

Revisit monitoring strategies when legal, regulatory, supplier, security, privacy, mission, or architecture requirements change. Compare findings and metrics with the current risk appetite. Adjust coverage, frequency, tools, thresholds, and reporting recipients; document why. A newly inherited cloud control may demand provider evidence rather than a local technical scan, while customer-controlled configurations still require local checks.

## 8. Decommission deliberately

Retirement is a risk-managed lifecycle step, not “turn the server off.” Consult stakeholders about records-retention, legal holds, contracts, data ownership, privacy obligations, interfaces, dependencies, and continuity. Plan migration or archiving, revoke access and credentials, terminate services, update inventories and diagrams, notify connected systems, and ensure no data path or billing/resource remains forgotten.

Sanitize or destroy media by the approved method appropriate to the data and device. **Cryptographic erase** can be suitable when encryption and key-management conditions actually support it; verify scope, keys, and evidence. Other media may need a different approved sanitization process. Retain the required decommissioning decision, sanitization proof, final configuration/records, and communications, then share them with relevant stakeholders.

**Scenario:** A retired application still has active service accounts and a cloud backup containing regulated records. Removing the front-end URL did not decommission the system. Find the remaining identities, data, integrations, contracts, and retention obligations before closing the inventory entry.

## Exam distinctions

| Situation | Appropriate focus |
|---|---|
| Normal monitoring shows a new risk | Analyze, report, respond, and possibly reassess/reauthorize |
| Proposed system modification | Impact assessment and approved change request before deployment |
| Emergency patch | Controlled expedited approval plus retrospective evidence |
| Control drift | Compare actual configuration with approved baseline and correct or authorize change |
| Overdue weakness | Escalate and update POA&M/risk decision; do not conceal it |
| Backup exists | Test restoration against RPO/RTO and evidence the result |
| Audit wants proof | Relevant, current, authentic records for the specified control and period |
| System retired | Dispose of data and access, update dependencies/inventory, retain records |

## Original active-recall exercise

A cloud-hosted system receives a critical vulnerability notice, a vendor changes its shared-responsibility terms, and a developer requests an emergency release. In ten minutes, explain which inventories, agreements, controls, risk assumptions, change approvals, tests, monitoring metrics, POA&M entries, and decision-makers must be involved. Then decide what you would do differently if the system were being retired next month.

## Official source path

ISC2 account → Courses and Exams → CGRC Online Self-Paced Training → Domain 7: Compliance Maintenance; Official ISC2 CGRC Digital Textbook, 7th edition, sections 7.1–7.4 and Domain 7 Key Takeaways. [Open your ISC2 courses dashboard](https://www.isc2.org/Dashboard/Courses-Exams).
