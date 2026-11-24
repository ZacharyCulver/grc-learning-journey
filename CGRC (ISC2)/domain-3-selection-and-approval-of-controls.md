# CGRC Domain 3: Selection and Approval of Framework, Security, and Privacy Controls

> Independent, paraphrased notes mapped to the official ISC2 CGRC self-paced Domain 3 catalogue and the Official ISC2 CGRC Digital Textbook, 7th edition (sections 3.1–3.2). Reviewed November 2026. These are not official course material; no licensed questions or answer keys are reproduced.

## The decision this domain is about

Domain 2 tells us what the system is and what harms matter. Domain 3 converts that understanding into an approved, documented set of security and privacy controls. The central workflow is **requirements → framework and baseline → inheritance → tailoring/enhancements → allocation → security/privacy plan → approval to implement**. Approval of the *plan* here is not the later authorization to operate in Domain 6.

A control objective states the intended outcome; a control is a safeguard or countermeasure intended to achieve it. Selection is not complete merely because a catalogue ID appears in a spreadsheet. The chosen control must have a rationale, implementation owner, expected behavior, assessment approach, and monitoring path.

## 1. Frameworks, control types, and categories

A controls framework organizes requirements and safeguards. The course compares generic information-security frameworks (notably NIST and ISO/IEC), sector- or industry-specific approaches such as PCI DSS and FedRAMP, and privacy frameworks. First identify binding obligations and organizational policy, then choose the framework and controls suitable for the system. Different catalogues may overlap, but a crosswalk is not evidence that a control is implemented or effective.

The textbook groups controls by **form** (physical, administrative, technical) and by **function** (administrative, preventive, deterrent, detective, corrective, recovery, compensating). These labels describe different dimensions, and a safeguard may perform several functions. A door lock prevents entry; a camera detects; a restoration process supports recovery; a documented exception control compensates when the normal safeguard is unsuitable. The course also discusses management, operational, and technical controls in the implementation domain. Do not force every taxonomy into one mutually exclusive list.

Defense in depth means complementary safeguards remain when one fails. It does not mean buying multiple tools with identical failure modes. Ask which risk each layer addresses and how an assessor could tell it works.

## 2. Baselines and inheritance

A **baseline** is an initial, preselected set of controls for a defined impact level or organizational context. It is a starting point, not a final answer. Map the categorization and requirements from Domain 2 to the applicable baseline; then identify additional obligations and gaps. An inherited safeguard must really be provided, assessed, and maintained by its provider.

| Allocation | Who does the work? | Example and SSP consequence |
|---|---|---|
| System-specific | System owner/team implements and maintains it | Application-specific access rules; describe actual implementation and evidence |
| Common | Central provider operates a control for multiple systems | Enterprise physical security or central policy; name provider and inheritance evidence |
| Hybrid | Provider and system team each perform part | Central identity service plus application role mapping; document both parts and owners |

Inheritance is not abdication. Verify that the shared service's scope, configuration, authorization/assessment evidence, and operating assumptions cover *this* system. A common control that protects the data center does not automatically protect an application's authorization logic. If common protection is inadequate, add a system-specific component or enhancement and record the residual risk.

**Scenario:** The enterprise identity provider authenticates users, but the application assigns roles. Authentication may be inherited while role authorization and periodic application-access review remain local. An SSP that says simply “IAM inherited” misses the hybrid responsibility.

## 3. Requirements engineering and trustworthy systems

Systems security engineering decomposes mission objectives into stakeholder needs, system requirements, architecture/design decisions, controls, and evidence. The textbook discusses NIST SP 800-160 and ISO/IEC/IEEE 15288 as ways to structure lifecycle engineering. Traceability makes a control defensible: requirement → objective → safeguard → responsible party → test → evidence → risk decision.

A **trusted** system is one people rely on; a **trustworthy** system has evidence that it merits that reliance. A design claim without verification offers weak assurance. Distinguish verification (“did we build according to the specified requirements?”) from validation (“does the resulting system satisfy the intended mission need in use?”). Consider measurement and future assessment while selecting controls, not after implementation.

## 4. Privacy selection and impact analysis

Privacy is not interchangeable with confidentiality. A system may keep personal information secret yet collect too much, retain it too long, or share it for an unauthorized purpose. The course covers privacy frameworks, privacy compliance, and privacy controls alongside security selection.

A **privacy threshold analysis** screens whether a fuller privacy impact assessment (PIA) is warranted under the applicable program. A PIA examines the collection, use, sharing, retention, data flows, possible harm to individuals, and mitigations; it can shape the control baseline and privacy plan. In a federal setting, determine whether the relevant statutory or agency PIA requirement applies. Elsewhere, use the organization's applicable law and policy rather than claiming every system has the same mandatory PIA process.

Ask who is affected, why the information is needed, whether less information would suffice, who receives it, and how an individual or regulator can understand the handling. Record privacy-specific requirements before declaring the selected control set complete.

## 5. Tailoring, scoping, enhancements, overlays

**Scoping guidance** describes the permissible adjustment range and conditions for a baseline. **Tailoring** applies that guidance to this particular system, documenting additions, refinements, parameters, and justified exclusions. An **enhancement** adds capability to a selected control. An **overlay** supplies a specialized set of control choices for a particular mission, technology, or environment. A **compensating control** seeks a comparable objective when the prescribed control cannot be used; it needs justification, approval, evidence, and monitoring.

Do not quietly delete a difficult baseline control. State the reason, applicable requirement, affected risk, alternative protection, approver, and how effectiveness will be tested. Record organization-defined values such as retention periods or review frequencies rather than leaving placeholders.

**Example:** A legacy device cannot support centrally managed MFA. A proposed combination of restricted network access, privileged-session gateway, logging, and a retirement deadline may reduce risk, but it is not automatically equivalent. Assess the protection objective and residual risk, obtain the required approval, and capture the exception in the plans/POA&M.

## 6. Data handling and marking

The course explicitly covers personnel security, intellectual property, archiving/records, confidentiality, IAM, data availability, and marking. Select controls based on the data's classification, legal obligations, lifecycle, and mission impact:

- **Personnel:** role suitability, screening where appropriate, onboarding, training, access changes, separation, and insider-risk procedures.
- **Intellectual property:** ownership, need-to-know access, agreements, monitoring, and secure storage/sharing; business sensitivity may exceed a simple “personal data” label.
- **Records:** retention schedule, integrity, discoverability, archival access, legal holds, and verified disposal.
- **Confidentiality and IAM:** identity proofing, unique identities, least privilege, role assignment, access review, privileged access, encryption and key management where appropriate.
- **Availability:** backup, restoration testing, redundancy, contingency planning, and agreed recovery targets. **RPO** is tolerable data loss measured in time; **RTO** is the restoration-time target; **maximum tolerable downtime** is the business limit beyond which disruption becomes unacceptable. These are not interchangeable.
- **Marking and localization:** labels/handling rules must be understandable and consistently applied across media, exports, and third parties. Some information must remain in specified jurisdictions; verify applicable requirements rather than assuming all data does.

**Application drill:** For a personnel database, identify who can view a record, who can change it, whether changes are logged, when archived copies are destroyed, where backups reside, and how fast service must return after outage. Map each answer to a control owner and test.

## 7. Document selection and prepare continued compliance

The control-selection record should show the source requirement, baseline and tailoring decisions, control objective, implementation statement or planned state, inheritance/ownership, chosen enhancements, assessment method, and residual issues. A requirements-to-controls matrix is useful for proving coverage and spotting orphaned controls. The **SSP** and **system privacy plan (SPP)**, or a combined plan where allowed, become the authoritative description of the proposed system safeguards. Plans should explain actual inherited, hybrid, and system-specific responsibilities rather than merely list control IDs.

Domain 3 also asks for a continuing-compliance strategy *before* the system goes live. Define the goals, metrics, assessment frequency, monitoring architecture, vulnerability-management workflow, and planned audits. An **ISCM** program gathers and analyzes evidence at system, mission/business, and organization levels. A **KPI** measures performance; a **KRI** signals risk exposure. Set thresholds and reporting paths so deviations prompt decisions. Monitoring frequency should reflect control volatility, criticality, threats, known weaknesses, and organizational direction; “annual for everything” is not a risk-based strategy.

Vulnerability management requires an inventory and scope, validated tools or methods, scan/assessment cadence, classification and remediation criteria, exception handling, owners, reporting, and continuous improvement. False positives waste effort, while false negatives mean no scan can prove absence of weakness. Audits test compliance against specified criteria; assessments can be broader management evaluations. Their evidence and findings inform remediation and the later authorization package.

## 8. Allocate controls and secure stakeholder agreement

Selection has to resolve who implements, funds, operates, assesses, and monitors each safeguard. In cloud services the provider generally secures the cloud infrastructure while the customer retains responsibilities for its data, identities, configurations, and workloads; the exact split changes with the service model and contract. Validate inherited provider controls and keep evidence of the shared-responsibility boundary.

Consult the system owner, privacy and security officials, common-control providers, architects, assessors, mission owners, and authorizing official as appropriate. The authorizing official's review of the security/privacy plans determines whether the proposed controls are acceptable for implementation. This is **not** a finding that implementation succeeded and **not** the later ATO.

## Exam and job distinctions

| If the prompt says… | Think… |
|---|---|
| “Preselected controls for an impact/context” | Baseline |
| “Specialized baseline for a mission or technology” | Overlay |
| “Adjust the baseline for this specific system” | Tailoring under scoping guidance |
| “Provider performs part; system owner performs part” | Hybrid control, both responsibilities documented |
| “Provider supplies to multiple systems” | Common control with validated inheritance |
| “Required control cannot be used” | Documented compensating alternative and residual-risk decision |
| “Evidence that a claimed system behavior actually works” | Verification/validation and assessment design |
| “Will the system meet privacy obligations?” | Data flows, threshold/impact analysis, privacy requirements and controls |
| “Who is accountable for the cloud workload?” | Shared-responsibility agreement plus system-specific ownership |
| “Control plan approved before build” | Domain 3 plan approval, not Domain 6 authorization |

## Original active-recall drills

1. Walk from a high-availability categorization to a baseline, tailored controls, owner, assessment evidence, and monitoring metric.
2. Explain common, hybrid, and system-specific controls using an enterprise identity service and one application.
3. State the difference between scoping guidance, tailoring, enhancement, overlay, and compensation without using a definition sheet.
4. Why can a compliant-looking control still be untrustworthy?
5. When might a PIA change control selection even if strong encryption exists?
6. Compare RPO, RTO, and maximum tolerable downtime in a backup-recovery scenario.
7. Name the fields you would expect in an SSP implementation statement and a control-selection rationale.
8. A provider changes its service boundary. Which inherited controls, contracts, plans, and monitoring assumptions must be revisited?

## Official source path

ISC2 account → Courses and Exams → CGRC Online Self-Paced Training → Domain 3: Selection and Approval of Framework, Security, and Privacy Controls; Official ISC2 CGRC Digital Textbook, 7th edition, sections 3.1–3.2 and Domain 3 Key Takeaways. [Open your ISC2 courses dashboard](https://www.isc2.org/Dashboard/Courses-Exams).
