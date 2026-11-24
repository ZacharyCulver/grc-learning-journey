# CGRC Domain 5: Assessment and Audit of Security and Privacy Controls

> Original study notes aligned to the official ISC2 CGRC self-paced Domain 5 catalogue and Official ISC2 CGRC Digital Textbook, 7th edition (sections 5.1–5.6). Reviewed November 2026. Licensed assessment and textbook questions are not reproduced.

## Domain purpose

Assessment asks whether implemented security/privacy controls are present, operate as intended, and achieve the protection requirements. An audit usually measures performance against defined compliance criteria with an appropriate degree of independence. Both depend on a clear scope, trustworthy evidence, documented findings, and a risk response. Neither a clean-looking spreadsheet nor a successful penetration test alone proves the whole system is secure.

The official sequence is **prepare → conduct → initial report → review and respond → final report → risk response plan**.

## 1. Prepare the assessment or audit

Define the objective before choosing tools. Is the engagement validating an RMF control implementation, a contractual requirement, an ISO-aligned process, or a particular privacy obligation? Identify the system boundary and authorization, assessment period, applicable control set and enhancements, inherited/common controls, prior findings, and relevant laws/policies.

Choose assessors with the necessary competence and appropriate independence. Assign points of contact, system/control owners, common-control providers, privacy stakeholders, and management reviewers. Separate the assessor's evaluation from the owner's decision to remediate or accept risk.

An assessment plan should specify objectives, assets, controls, methods, **depth and coverage**, schedule, resources, access, test environment, safety constraints, deliverables, evidence handling, and reporting. Determine which prior assessment results can be reused and whether they still cover the current control, version, provider, and system scope. Coordinate interview availability and access to facilities and records. Obtain the required authorization for intrusive testing before conducting it.

**Depth** asks how rigorously a selected object is examined; **coverage** asks how much of the relevant population is assessed. A small sample may be reasonable if justified, representative, and consistent with the framework, but it cannot establish every possible failure mode.

## 2. Conduct assessments with appropriate methods

The textbook and NIST-aligned course emphasize three non-adversarial methods: **examine** documents/configurations/records, **interview** people who design or operate controls, and **test** a mechanism or process to observe behavior. Objects can be specifications, mechanisms, activities, and individuals. Use complementary methods: a policy can demonstrate intent, an interview can explain operation, and a test can show enforcement.

**Example:** To assess account termination, examine the procedure and sample tickets, interview HR and IAM staff, and test whether a separated user's account was disabled within the required timeframe. A documented policy by itself does not prove execution. For a privacy control, examine the data-flow and retention records, interview the owner, and test whether data actually leaves the system on schedule.

Penetration testing is an adversarial technique with explicit scope, rules of engagement, safety constraints, authorized targets, test windows, and reporting. Discovery, attack simulation, validation, and report are useful phases; do not conflate a penetration test with the full controls assessment. Coordinate potentially disruptive actions and protect sensitive findings. Never test outside the approved boundary or authorization.

## 3. Verify and validate evidence

Evidence should be relevant to the criterion, authentic, complete enough for the conclusion, current for the assessment period, and traceable to the system/version/control. Log how it was collected, by whom, when, and from which source. Preserve integrity and handle sensitive data under applicable policy. Corroborate screenshots with underlying configuration, logs, or observed behavior when possible.

**Verification** asks whether the control satisfies specified requirements. **Validation** asks whether it achieves the intended need in the operating context. A mechanism could be configured as specified yet fail the mission's protection objective. Test the expected outcomes, not merely the presence of a product or document.

Be cautious with inherited-control evidence. A provider's report may cover a different service tier, location, assessment period, or set of control responsibilities. Identify the system-specific portion of any hybrid control.

## 4. Write the initial report

The initial report states scope, criteria, methods, objects, evidence, limitations, results, and preliminary risks. A useful finding can be framed as **condition** (what is), **criteria** (what should be), **cause** (why the gap occurred), **effect** (why it matters), and **recommendation** (possible corrective action). Findings should identify the affected asset/control and credible risk, not merely say “noncompliant.”

Distinguish an observed fact from an inferred cause or a proposed treatment. Record both successful controls and deficiencies, including uncertainty or sampling limitations. Give owners an opportunity to validate factual accuracy; do not let the assessment's independence disappear in negotiation.

## 5. Review, respond, and reassess

The system owner and stakeholders evaluate each deficiency in mission context and select a risk response: mitigate, avoid, transfer/share where appropriate, or propose acceptance by the authorized risk decision-maker. Some issues can be corrected promptly under approved change control; others require a POA&M with owner, resources, milestones, due date, interim measures, and status.

A corrective action should be **reassessed** before the final report claims the finding is closed. Applying a patch is not the same as demonstrating that the vulnerability and its underlying cause were resolved. Reassessment should verify both the changed control and any unintended effect on other controls or operations.

**Scenario:** A privileged-account review was missing for two quarters. Conducting one review now may resolve current excess access, but it does not erase the historical lapse. Document the period, cause, exposure, retrospective analysis, process fix, and evidence that the new cadence works.

## 6. Final report and risk response plan

The final report reflects reassessments and the system's final observed state. Include an executive summary, system and scope, assessor identity/qualifications where required, methodology, results, evidence references, limitations, organization comments, and recommendations. A recommendation is advice; the assessor does not make the authorizing official's risk decision.

Identify residual risks and unresolved findings. Prioritize by potential mission/individual harm, likelihood, urgency, exposure, and dependencies. Define realistic owners, resources, milestones, and verification criteria. Keep the POA&M synchronized with the assessment report, SSP, risk register, and later authorization package. An unresolved high-severity finding should be visible to the decision-maker, even if an interim mitigation exists.

The output flows to Domain 6, where officials review the package and decide whether the remaining risk is acceptable.

## Exam distinctions

| Concept | What it means |
|---|---|
| Assessment plan | Agreed scope, objectives, methods, objects, logistics, and deliverables *before* testing |
| Examine / interview / test | Inspect evidence / ask knowledgeable people / observe behavior |
| Penetration test | Authorized adversarial exercise; one assessment technique, not the whole audit |
| Initial report | Preliminary observed state and risks for owner review |
| Reassessment | Independent verification that corrective actions actually work |
| Final report | Final documented assessment state, including remaining gaps |
| POA&M | Ownership, schedule, and milestones for unresolved corrective work |
| Audit vs assessment | Audit emphasizes compliance with criteria; assessment may more broadly evaluate control effectiveness and risk |

## Original application exercise

An assessor finds that backups exist but no restoration test was retained, an inherited identity control's report is 18 months old, and an operator says access reviews are “usually done” with no record. For each finding, choose examine/interview/test steps, identify the missing evidence, describe a plausible risk, propose a correction, and state what must be verified before closure. Then decide which unresolved issues the authorizing official should see.

## Recall drill

Without notes, explain why a policy document, an operator interview, and a technical test answer different questions. Describe what would change between an initial and final report if a vulnerability is fixed and reassessed.

## Official source path

ISC2 account → Courses and Exams → CGRC Online Self-Paced Training → Domain 5: Assessment/Audit of Security and Privacy Controls; Official ISC2 CGRC Digital Textbook, 7th edition, sections 5.1–5.6 and Domain 5 Key Takeaways. [Open your ISC2 courses dashboard](https://www.isc2.org/Dashboard/Courses-Exams).
