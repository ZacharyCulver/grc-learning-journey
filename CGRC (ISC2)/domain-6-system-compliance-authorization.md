# CGRC Domain 6: System Compliance and Authorization

> Original notes aligned to the official ISC2 CGRC self-paced Domain 6 catalogue (whose lesson view emphasizes authorization/approval) and Official ISC2 CGRC Digital Textbook, 7th edition (sections 6.1–6.3). Reviewed November 2026. These notes paraphrase concepts rather than reproduce licensed material.

## The decision this domain is about

After the controls are implemented and assessed, an authorized decision-maker must understand what risk remains and whether the system may operate under defined conditions. Domain 6 connects the **documentation package**, **system risk posture**, **risk treatment**, and **formal compliance/authorization decision**.

A passing control test is evidence, not an ATO. An ATO is an explicit risk decision for a defined system, scope, use, and period or ongoing conditions under the governing framework. “Compliant” does not mean “risk-free.”

## 1. Compile and review the security/privacy package

Ensure the information reaching the authorizing official is accurate, current, internally consistent, and traceable. The core RMF-style package commonly includes the system security plan (SSP), privacy plan where applicable, assessment results/report, and plan of action and milestones (POA&M). Depending on the system and framework, supporting artifacts can include configuration documentation, risk assessment, control and evidence inventory, contingency plan, test results, interconnection and supplier records, training records, and incident records.

The **SSP** describes the boundary, requirements, control implementation, inheritance, and operating environment. The **assessment report** explains what was tested and found. The **POA&M** tracks unresolved weaknesses, owners, actions, and milestones. A risk register or risk profile helps decision-makers see aggregate and related risks. These documents should not contradict one another: a control cannot be “fully implemented” in the SSP while an open finding says it is absent without an explanation of timing and status.

Review privacy impacts and legal/contractual obligations as well as cybersecurity impact. Confirm the appropriate people have reviewed the package and that common-control evidence covers the system. A neatly formatted authorization packet with stale architecture or missing interfaces does not support a sound decision.

## 2. Establish risk acceptance criteria

Risk acceptance criteria define when a risk can be retained, when treatment is required, and who may approve exceptions. They should be connected to organizational risk appetite and more specific tolerance/thresholds, mission consequences, applicable law, policy, and stakeholder needs. The decision-maker should be able to tell *why* a risk falls inside or outside those criteria.

Use the same risk language consistently. An initial/inherent estimate considers exposure before the current safeguards; **residual risk** is the exposure left after implemented safeguards and validated responses. Planned work may lower *future* risk but does not erase current residual risk.

Risk treatment choices include mitigating with safeguards, avoiding the risky activity, transferring or sharing aspects through agreements or insurance, and accepting risk through the proper authority. Transfer does not remove all accountability. A risk that violates a mandatory obligation cannot be made lawful merely by signing an acceptance form.

## 3. Determine the system's actual risk posture

Synthesize impact categorization, threat events, vulnerabilities, control effectiveness, assessment limitations, open findings, dependencies, and the effect of available responses. Analyze both individual findings and cumulative risk. Several moderate weaknesses can interact to create a more serious path to mission harm.

For each material residual risk, record the affected asset and objective, cause or scenario, likelihood/impact assumptions, implemented safeguards, remaining exposure, proposed response, owner, deadline, and supporting evidence. Compare it with approved acceptance criteria and identify uncertainty. If the system has a new cloud provider or a changed data flow, revisit the assessment rather than carrying forward an obsolete rating.

**Scenario:** A personnel system has encryption and logging but no tested restoration process. A high availability impact remains even if confidentiality safeguards are excellent. The decision package should distinguish this risk, show the planned restoration test and interim measure, and state who is empowered to accept temporary exposure.

## 4. Obtain stakeholder concurrence without confusing roles

The system owner coordinates the package and proposed treatment. Security and privacy officials, mission owners, common-control providers, legal/compliance staff, and assessors may provide input. The assessor reports findings and may recommend actions; they do not approve their own findings away. The authorizing official (or the role named by the applicable framework) makes the formal decision to accept or reject the risk of operation.

Stakeholder concurrence can reveal unrecognized mission, privacy, contractual, or operational effects. It is valuable, but a group consensus does not substitute for the specifically delegated authority to authorize a system. Record disagreements and conditions so the decision-maker sees them.

## 5. Document the decision and communicate it

The written decision should identify the system and boundary, the authorized use and conditions, the residual risks considered, applicable limitations, required remediation/monitoring, responsible officials, decision date, and any review or expiration triggers. Depending on the governance process, the outcome may authorize operation, authorize with conditions, deny operation, or later suspend/revoke a prior authorization. Use the organization's formal decision terminology rather than assuming an ISO certification and a federal ATO are identical.

Notify affected owners, operators, assessors, common-control providers, mission stakeholders, and oversight roles as required. Update the system inventory, SSP, POA&M, risk register, and monitoring strategy. If operation is conditioned on a deadline or compensating measure, set a measurable follow-up and escalation path.

**Key separation:** A control plan is approved in Domain 3; implementation is documented in Domain 4; effectiveness is assessed in Domain 5; the operating risk decision belongs in Domain 6; Domain 7 keeps the evidence and decision current.

## ISO and NIST context

The course compares NIST SP 800-37-style authorization documentation with ISO/IEC 27001-style management-system documentation. NIST RMF explicitly describes system/control authorization decisions by an authorizing official. ISO/IEC 27001 concerns an organization's ISMS, risk treatment, evidence, management review, and certification/ongoing audits where relevant. They have related risk principles but different objects of approval and terminology. Do not call an ISO certificate an ATO or treat a federal ATO as proof of organization-wide ISO certification.

## High-value exam distinctions

| Term | Ask |
|---|---|
| Assessment result | What did independent evaluation find? |
| Residual risk | What exposure remains after current, effective safeguards? |
| POA&M | What unresolved weakness will be addressed by whom and when? |
| Risk acceptance | Which delegated authority knowingly retains the exposure? |
| Authorization | Under what scope, conditions, and risk decision may the system operate? |
| Compliance evidence | Which requirement, period, boundary, and artifact does it actually support? |
| Stakeholder concurrence | Who has reviewed the implications, and who still makes the final decision? |

## Original practice scenario

An assessor reports one high and two moderate findings. The high finding is mitigated and retested; one moderate finding has an interim control, and the other is merely scheduled for future work. The SSP still shows all three controls as fully implemented. Explain which documents must be corrected, how to calculate *current* residual risk, what the POA&M should contain, and why the system owner cannot simply declare an ATO. Then draft a two-sentence recommendation to the authorizing official that states the uncertainty and possible condition, without making the official's decision.

## Recall drill

Explain to a nontechnical commander why “we passed most tests” is not the same as “the system is authorized.” Name the three documents you would open first to assess a proposed risk acceptance and explain what each contributes.

## Official source path

ISC2 account → Courses and Exams → CGRC Online Self-Paced Training → Domain 6: System Compliance; Official ISC2 CGRC Digital Textbook, 7th edition, sections 6.1–6.3 and Domain 6 Key Takeaways. [Open your ISC2 courses dashboard](https://www.isc2.org/Dashboard/Courses-Exams).
