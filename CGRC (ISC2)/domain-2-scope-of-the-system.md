# CGRC Domain 2: Scope of the System

> Independent study notes based on the official ISC2 CGRC self-paced Domain 2 catalogue and the Official ISC2 CGRC Digital Textbook, 7th edition (sections 2.1–2.2). Written in my own words; not official ISC2 content or a substitute for the course. Reviewed November 2026.

## Domain purpose and mental model

Before choosing controls, define *what the system is*, what information it handles, what it depends on, and what a loss of confidentiality, integrity, or availability would do to the mission. A vague boundary produces vague ownership, missing interfaces, unreliable categorization, and ultimately an SSP that cannot support a defensible risk decision.

The course's two major tasks are **describe the system** and **determine the security compliance required**. Think of the output as an evidence-backed system description plus an impact/categorization rationale.

## 1. Name and scope the system

A useful system name is unique enough to distinguish the authorization boundary and meaningful enough that stakeholders recognize the mission. A scope statement answers what is in, what is out, who owns it, where it operates, what it connects to, and which services or controls it inherits. Naming conventions and inventory identifiers support traceability, but the name is not itself the boundary.

Document the mission or business owner, system owner, operators, users, locations, lifecycle stage, processing environment, hardware, software, firmware, data stores, interfaces, network segments, external connections, and third-party services. Draw the boundary so that components and responsibilities can be mapped consistently. A cloud-hosted application still has a customer-defined system boundary even when the provider owns the underlying infrastructure.

**Boundary test:** If an assessor asks who is responsible for a database, identity provider, API, backup repository, or external data feed, the system description should answer without guesswork. Dependencies outside the boundary remain relevant; identify the provider, agreement, inherited controls, and data flow.

An RMF/ISSO artifact set might include an inventory entry, boundary diagram, network/data-flow diagram, interconnection agreement, component inventory, and initial SSP description. These are practical examples, not a claim that every framework mandates the same named documents.

## 2. Describe purpose, functionality, and context

**Purpose** is why the organization needs the system; **functionality** is what the system does. Keep these separate from implementation details. A personnel portal's purpose might be to support workforce administration; its functions might include accepting records, validating entries, storing them, and producing reports.

Record the intended users, mission outcomes, operating environment, architecture, inputs and outputs, interfaces, performance and availability needs, assumptions, constraints, and relevant stakeholders. Trace a functional requirement to a security or privacy requirement where the function creates a protection need.

The course contrasts ISO and NIST approaches. In broad terms, ISO risk-management and ISMS work emphasizes organizational context, interested parties, scope, and adaptable risk criteria; NIST RMF gives a more explicit federal-system workflow, including boundary and categorization decisions. Neither approach excuses an incomplete system description. Avoid treating a system diagram as a complete risk assessment.

**Scenario:** A logistics application receives maintenance records from another agency. Scope must identify the inbound interface, data type, ownership, transfer method, dependency, and whether the receiving system or upstream provider implements each safeguard. An interface left off the diagram can hide an actual route for data exposure.

## 3. Inventory information types and data flows

List the information the system **processes, stores, or transmits**, not just its primary database. Include transient data, logs, backups, exports, caches, support tickets, and archived copies where relevant. Information may include personal data, health or financial records, mission/business data, intellectual property, internal operational data, and public material. A single system can contain several information types with different legal and protection requirements.

Map where data is created or received, validated, used, shared, retained, archived, and disposed of. Identify the source and destination of each flow, including cross-boundary transfers and vendors. A privacy analysis asks whether personal information is necessary, who can access it, what notices or lawful basis apply, where it travels, how long it is retained, and how it is disposed of. Do not assume that encryption alone resolves a privacy requirement.

**Active-recall prompt:** Can I identify the most sensitive information type in the system and draw its journey from collection to deletion without looking at the diagram?

## 4. Determine security and privacy requirements

Requirements may arise from mission needs, organizational policy, contract, law, regulation, applicable standards, and the selected risk framework. Applicability depends on the organization, jurisdiction, data, system purpose, and contractual relationships. A framework is not a law; a control catalogue is not proof of compliance.

For each information type, ask what could happen if confidentiality, integrity, or availability were lost. Include potential effects on individuals, operations, assets, mission delivery, legal obligations, and reputation. Privacy and non-repudiation may add distinct requirements. Record the source of each obligation and the owner who interprets it.

Translate obligations into measurable objectives. “Protect personnel information” is vague; “limit access by role, log privileged changes, and retain records according to the approved schedule” is testable. Determine whether a privacy impact analysis or other specialized assessment is triggered; document the rationale either way.

## 5. Categorize information and system impact

NIST/FIPS-style impact levels are **low** (limited adverse effect), **moderate** (serious adverse effect), and **high** (severe or catastrophic adverse effect). Evaluate confidentiality, integrity, and availability separately for each information type, then determine the system's overall impact under the applicable categorization method. Do not average away a high-impact objective. In a U.S. federal RMF setting, FIPS 199 and NIST SP 800-60 provide the central categorization concepts; apply the organization's approved mappings and any special statutory rules.

Distinguish **impact of a loss** from **likelihood of an event**. Categorization asks how damaging the loss would be; a subsequent risk assessment considers threats, vulnerabilities, likelihood, and controls. A high-impact system is not automatically “more likely to be breached,” and public data is not automatically low impact for integrity or availability.

ISO-style risk evaluation is generally tailored to agreed criteria and context. Consider the nature, scope, severity, duration, and affected stakeholders of potential consequences, then evaluate risk using the approved method. Do not transfer NIST's federal low/moderate/high schema into an ISO implementation without an explicit mapping.

**Worked example:** An application holds public weather data but feeds emergency response decisions. Confidentiality could be low while integrity and availability could be high. The reason is mission harm from false or missing information, not secrecy. Record the rationale, reviewers, and date so a later change can trigger recategorization.

## 6. Turn scope into an actionable handoff

A defensible Domain 2 output contains a system name and purpose, boundary and interface description, asset/data inventory, information-type and data-flow mapping, applicable obligations, security/privacy objectives, impact determinations, and documented assumptions and approvals. These outputs feed Domain 3's baseline and control-selection work.

If the boundary, mission, data, or connected services change, revisit the scope and categorization. Categorization is a living decision, not a label assigned once for a dashboard.

## High-value distinctions

| Do not confuse | The useful distinction |
|---|---|
| Purpose vs functionality | Why the system exists vs what it performs |
| System boundary vs dependency | What is in the assessed system vs external service or connection that affects it |
| Information type vs asset | The kind of information vs the component, service, or resource handling it |
| Impact vs risk | Consequence of a loss vs a broader evaluation that also considers events, likelihood, and controls |
| Confidentiality vs privacy | Preventing unauthorized disclosure vs appropriate handling of information about people throughout its lifecycle |
| Categorization vs control selection | Determine protection needs first; choose and tailor safeguards in Domain 3 |
| Framework vs obligation | A method or control set does not supersede applicable law, policy, or contract |

## Quick application drill

A new Army-facing case-management system accepts personal records, stores attachments in a cloud service, exports monthly reports, and depends on an enterprise identity provider. Write a five-sentence boundary statement. List the information types and all four data paths (intake, storage, export, identity exchange). Rate C/I/A consequences independently, justify the highest impact, and identify which control responsibilities are inherited versus system-specific. Then ask what changes if the reports start driving real-time decisions.

## Original recall questions

1. Why is a list of servers insufficient to define a system boundary?
2. Which information copies are easily omitted when inventorying data?
3. What distinction separates impact categorization from a risk assessment?
4. Can information be public and still require high integrity or availability? Explain.
5. What evidence would an assessor need to verify the scope and its external dependencies?
6. When does a system change require revisiting information-type and impact decisions?

## Official source path

ISC2 account → Courses and Exams → CGRC Online Self-Paced Training → Domain 2: Scope of the System; Official ISC2 CGRC Digital Textbook, 7th edition, Domain 2, sections 2.1–2.2 and Key Takeaways. Access through the [ISC2 courses dashboard](https://www.isc2.org/Dashboard/Courses-Exams). No proprietary course quiz or study-question items are reproduced here.
