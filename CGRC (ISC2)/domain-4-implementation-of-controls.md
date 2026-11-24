# CGRC Domain 4: Implementation of Security and Privacy Controls

> Original study notes mapped to the official ISC2 CGRC self-paced Domain 4 lessons and Official ISC2 CGRC Digital Textbook, 7th edition (sections 4.1–4.3). Reviewed November 2026. No course text, figures, or quiz items are reproduced.

## What changes in this domain

Domain 3 approved the *intended* safeguards. Domain 4 turns those decisions into an operating system and an accurate record of what was actually built. A control selected on paper but not configured, staffed, trained, and evidenced is not implemented.

The course's three movements are **develop an implementation strategy**, **implement selected controls**, and **document control implementation**. The implementation statement and evidence must agree with the approved SSP and privacy plan; deviations require review, not silent retroactive editing.

## 1. Build an implementation strategy

Start with the system's purpose, scope, data categorization, risk profile, selected baseline, tailoring decisions, legal/contractual obligations, and architecture. For each control, identify the responsible owner and provider, dependencies, resources, schedule, acceptance criteria, deployment path, and how its performance will be tested. Sequence foundational services first: identity, logging, configuration management, backup, and common controls often enable other safeguards.

Map every implementation task to a control objective and requirement. A “deploy MFA” task should identify eligible identities, privileged paths, exceptions, enrollment, failure recovery, logs, and proof of enforcement. A privacy control needs similar detail about collection, use, retention, sharing, or individual rights, not merely a checkbox.

The strategy must fit organizational expectations *and* applicable national/international obligations. A local procedure cannot waive a statutory requirement. Conversely, a framework's example is not necessarily the only valid implementation; the selected result must meet the objective and be demonstrable.

**RMF/ISSO view:** Maintain an implementation tracker linked to SSP control IDs, ownership, configuration artifacts, test results, and unresolved exceptions. This allows a future assessor to follow a claim to evidence.

## 2. Distinguish control types and ownership

**Management** controls provide policy, planning, oversight, and accountability. **Operational** controls are carried out through people and processes (for example, account review or incident exercises). **Technical** controls use system mechanisms (for example, access enforcement and audit logging). A control may require all three: policy defines privileged access, a workflow approves it, and technology enforces it.

**Common** controls serve multiple systems; a system may inherit them if the provider's scope and evidence are applicable. **Hybrid** controls divide work between the common provider and the system team. **System-specific** controls belong to the system boundary. These ownership labels are different from management/operational/technical categories.

Create an explicit responsibility matrix. If the enterprise supplies the backup platform but the application team configures backup jobs and performs restoration tests, both implementation portions belong in the record. Do not mark the entire backup control “inherited” without confirming coverage.

## 3. Implement consistently with requirements

Follow approved change and configuration-management processes. Establish a baseline configuration, define and label configuration items, control changes, retain status/history, and compare deployed settings with the approved baseline. Testing should confirm not only that a setting exists but that the control achieves the desired protection outcome in the real environment.

Examples of evidence include policy approval, configuration export, access-control matrix, sample log events, change tickets, training records, backup/restore results, and provider assessment reports. Preserve dates, system scope, responsible party, version, and collection method. A screenshot without context is weak evidence; a documented, reproducible test is stronger.

Implementation may occur throughout the system development lifecycle. Integrate security and privacy requirements into design and build, test them before deployment, and maintain them after go-live. If a control changes after assessment, update the implementation record and determine whether reassessment is necessary.

**Scenario:** A selected session-timeout control is configured on the web front end but not on an administrative API. The SSP's blanket statement “sessions expire after inactivity” would be inaccurate. Finish the API implementation or document the exception, risk, compensating measures, and plan to resolve it.

## 4. Compensating and alternate controls

A compensating control responds to an infeasible or unsuitable baseline control while seeking the same protection objective. Analyze the original requirement, the gap, feasible alternatives, residual risk, approver, and evidence of comparable effectiveness. Implement and monitor the substitute; a proposed alternative does not count as functioning protection.

The justification should address *why* the prescribed safeguard cannot be used, *how* the substitute reduces likelihood or impact, *who* owns it, *when* it will be tested, and *whether* a time-limited exception or remediation milestone is required. Never present a compensating control as a blanket waiver of a legal or contractual obligation.

## 5. Document residual risk and planned work

Record controls as implemented, partially implemented, planned, or inherited according to the governing process and the actual evidence. Capture the gap, affected objective, threat/impact, interim safeguards, responsible owner, target date, and decision authority. A POA&M is a living plan for weaknesses and milestones; it does not itself make a system compliant.

Distinguish **inherent risk** before considering controls from **residual risk** after current controls. If the planned improvement has not yet been deployed, do not reduce the *current* residual-risk estimate as though it had. Escalate material risk to the officials authorized to decide it.

## 6. Produce an assessor-ready implementation record

An SSP control entry should explain *how, where, by whom, and with what dependencies* the safeguard operates. Include configuration parameters and referenced procedures, common-control inheritance and provider, planned enhancements, implementation status, and evidence location. A privacy plan should describe the corresponding processing/handling controls. Keep diagrams, component inventory, and data flows synchronized with deployed reality.

Set frequencies for review of compliance documentation and for training based on requirements, change rate, risk, and role. Review artifacts when laws, contracts, technology, organizational processes, or system boundaries change; an annual calendar alone will not catch every material change. Record completion and retention of training for personnel who perform controls.

Before handing the system to Domain 5 assessors, reconcile the control inventory with the running configuration and evidence. The assessor should be able to select a control, identify its owner and implementation, examine a relevant artifact, and know what still needs remediation.

## Exam distinctions

| Statement | Correct interpretation |
|---|---|
| “Selected” | Planned/approved safeguard, not proof it operates |
| “Implemented” | Deployed process or mechanism with an owner and verifiable behavior |
| “Documented” | Accurate description and evidence of actual or explicitly planned state |
| “Compensating” | Justified alternate way to meet an objective; assess residual risk |
| “Common” | Shared provider-owned implementation that the system may inherit |
| “Hybrid” | Provider and system each have a documented portion |
| “POA&M” | Tracks gaps and milestones; not an ATO or risk acceptance by itself |

## Original practice scenario

A system inherits the enterprise firewall, uses local administrator accounts on legacy servers, and claims encryption of all sensitive exports. The firewall evidence covers only production; a test environment is also in scope. Administrators share one account, and exports are encrypted only when sent by email. Write three control-implementation corrections, three evidence requests, and a POA&M entry. Explain which official must decide whether the remaining risk is acceptable; do not let the control implementer authorize their own risk.

## Recall drill

Explain in plain English the difference among an approved plan, a working control, an assessment result, and an authorization decision. Then pick one control and trace it from Domain 2 requirement through Domain 3 selection to Domain 4 configuration and evidence.

## Official source path

ISC2 account → Courses and Exams → CGRC Online Self-Paced Training → Domain 4: Implementation of Security and Privacy Controls; Official ISC2 CGRC Digital Textbook, 7th edition, sections 4.1–4.3 and Domain 4 Key Takeaways. [Open your ISC2 courses dashboard](https://www.isc2.org/Dashboard/Courses-Exams).
