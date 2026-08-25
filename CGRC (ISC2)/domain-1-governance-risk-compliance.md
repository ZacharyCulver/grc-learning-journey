# CGRC Domain 1: Security and Privacy Governance, Risk Management, and Compliance

## Domain Purpose

Domain 1 establishes how an organization governs security and privacy, manages risk, and demonstrates compliance.

An effective GRC program must:

- Align security and privacy with organizational objectives.
- Manage risk at both organizational and system levels.
- Protect information throughout its entire life cycle.
- Integrate security into business processes and system development.
- Assign qualified personnel to defined roles.
- Continuously monitor controls, risks, and compliance obligations.

---

## 1. Core GRC Concepts

### 1.1 Governance

Governance is the framework of policies, processes, and rules used to direct, control, and hold an organization accountable.

Governance establishes how security and privacy decisions are directed and overseen.

Key governance elements include:

- Policies, standards, procedures, and guidelines
- Defined authority and accountability
- Roles and responsibilities
- Strategic objectives
- Risk appetite and risk tolerance
- Leadership oversight
- Performance measurement and reporting

#### Governance Objectives

- Establish organizational goals and strategic direction.
- Support transparent, accountable, and effective decisions.
- Balance the interests of internal and external stakeholders.
- Translate high-level objectives into lower-level guidance.
- Ensure consistent decision-making across the organization.

#### Governance Levels

Governance begins with senior leadership but operates hierarchically:

1. Enterprise governance
2. Information security and privacy governance
3. Business-unit or departmental governance
4. System- and process-level implementation

#### Governance Approaches

- **Centralized:** A central authority makes governance decisions, improving consistency.
- **Decentralized:** Authority is delegated to departments, improving flexibility but potentially creating inconsistencies.
- **Hybrid:** Central leadership establishes core requirements while delegating selected decisions.

#### Governance Outputs

Governance decisions are communicated through:

- Policies
- Standards
- Procedures
- Guidelines
- Roles and responsibilities
- Awareness and training

> **Key distinction:** Governance determines organizational direction and expectations, while management implements them through programs, processes, and controls.

---

### 1.2 Risk Management

Risk management is the coordinated process of identifying, assessing, treating, and monitoring risks that could affect an organization’s objectives, operations, assets, reputation, stakeholders, or financial stability.

Cybersecurity risk is one part of broader **enterprise risk management (ERM)** and should be connected to business and mission risk.

The risk management process generally includes four phases:

1. Risk identification, framing, and scoping
2. Risk assessment
3. Risk treatment or response
4. Risk monitoring

#### 1. Risk Identification, Framing, and Scoping

This phase establishes the context and boundaries of the risk management effort.

Key activities include:

- Identifying assets, threats, vulnerabilities, and potential adverse events.
- Determining which risk types and business areas are in scope.
- Identifying affected operations, assets, and stakeholders.
- Connecting system-level risks to enterprise-level objectives.
- Establishing risk appetite and risk tolerance.
- Identifying internal and external dependencies.
- Documenting assumptions and constraints.

Risk can be evaluated at multiple levels:

- Enterprise
- Mission or business process
- Business unit
- System
- Application
- Technical component

##### Important Risk Terms

- **Risk appetite:** The broad amount and type of risk an organization is willing to pursue or retain.
- **Risk tolerance:** The acceptable degree of variation or exposure for a specific objective or risk category.
- **Acceptable risk:** Risk that leadership has determined can be retained without additional treatment.

Risk appetite is strategic and organization-wide, while risk tolerance is more specific and measurable.

#### 2. Risk Assessment

Risk assessment evaluates:

- The likelihood that a threat event will occur or succeed.
- The potential impact if the event occurs.
- Existing vulnerabilities and predisposing conditions.
- Controls already implemented.
- The resulting level of risk.

A simplified relationship is:

> **Risk = Likelihood × Impact**

Assessments may use:

- **Qualitative methods:** Ratings such as low, moderate, and high.
- **Quantitative methods:** Numerical values or estimated financial loss.
- **Semi-quantitative methods:** Numerical scoring combined with professional judgment.

Risk assessments should be:

- Consistent
- Repeatable
- Evidence-based
- Objective
- Documented
- Comparable across systems and business units

Inconsistent or overly subjective assessments produce unreliable information and weaken leadership decisions.

##### Risk Assessment Results

Risk assessment results commonly identify:

- Risk description
- Affected assets and processes
- Threats and vulnerabilities
- Likelihood
- Impact
- Existing controls
- Inherent risk
- Residual risk
- Recommended response
- Risk owner

These results are often recorded in a **risk register**.

#### 3. Risk Treatment or Response

Risk treatment selects actions that align identified risks with organizational objectives, risk appetite, and risk tolerance.

##### Accept

Leadership acknowledges and retains the risk without additional treatment.

Risk acceptance should be:

- Authorized by the appropriate risk owner.
- Based on adequate information.
- Documented.
- Reviewed periodically.

##### Avoid

The organization eliminates the activity or condition creating the risk.

**Example:** Discontinuing a vulnerable service rather than attempting to secure it.

##### Mitigate

The organization applies controls to reduce the likelihood or impact of the risk.

**Example:** Implementing multifactor authentication to reduce account-compromise risk.

##### Share or Transfer

The organization assigns or distributes part of the risk to another party.

Examples include:

- Cybersecurity insurance
- Contractual agreements
- Outsourcing
- Managed service providers

Transferring responsibility does not necessarily eliminate the organization’s accountability or all residual risk.

#### 4. Risk Monitoring

Risk monitoring continuously evaluates identified risks and detects new or changing risks.

Monitoring activities include:

- Reviewing control effectiveness.
- Tracking risk indicators and metrics.
- Monitoring threats and vulnerabilities.
- Identifying changes to systems and business processes.
- Reviewing accepted risks.
- Tracking remediation activities.
- Updating risk assessments and risk registers.
- Reporting material changes to decision-makers.

Monitoring is necessary because risks change as:

- Threats evolve.
- Vulnerabilities are discovered.
- Systems are modified.
- Controls weaken or fail.
- Business objectives change.
- Legal or contractual requirements change.
- New suppliers and technologies are introduced.

#### Risk Management Relationships

```text
Business objective
        ↓
Business or mission risk
        ↓
Cybersecurity and privacy risk
        ↓
System-level threats and vulnerabilities
        ↓
Controls, remediation, and monitoring
```

Technical weaknesses matter because of their potential effect on organizational objectives—not merely because a vulnerability exists.

#### Risk Management Key Takeaways

- Cybersecurity risk is a component of enterprise risk.
- Risk management must support business and mission objectives.
- Risks should be evaluated consistently and objectively.
- Risk responses must align with risk appetite and risk tolerance.
- Risk acceptance requires informed and documented authorization.
- Applying controls reduces risk but rarely eliminates it.
- Residual risk remains after controls are implemented.
- Risk monitoring is continuous, not a one-time assessment.
- System-level risks must be connected to organizational impact.

---

### 1.3 Compliance

Compliance means meeting applicable:

- Laws and regulations
- Contractual requirements
- Industry standards
- Organizational policies
- Framework requirements

Compliance does not automatically equal security. An organization may meet a minimum requirement while still retaining significant risk.

> **Key distinction:** Compliance establishes obligations that must be satisfied, while risk management determines whether additional protections are necessary based on organizational risk.

---

## 2. Organizational and System-Level GRC

GRC operates at multiple levels.

### Organizational Level

The organizational level focuses on:

- Enterprise policies
- Risk strategy
- Governance structure
- Legal and regulatory obligations
- Organization-wide control requirements
- Resource allocation

### Mission and Business Process Level

The mission and business process level focuses on:

- Business functions
- Process dependencies
- Information flows
- Operational risk
- Shared services

### System Level

The system level focuses on:

- System categorization
- Security and privacy controls
- System boundaries
- Control implementation
- Assessment evidence
- Authorization decisions
- Continuous monitoring

Decisions at the organizational level influence the controls implemented on individual systems.

---

## 3. Security and Privacy Principles

### Confidentiality

Information is accessible only to authorized individuals, systems, and processes.

### Integrity

Information remains accurate, complete, and protected against unauthorized modification or destruction.

### Availability

Information and systems remain accessible to authorized users when needed.

### Non-repudiation

Non-repudiation provides evidence that an action or transaction occurred so the responsible party cannot credibly deny it.

### Privacy

Privacy governs how personal information is collected, processed, stored, shared, retained, and disposed of.

Privacy focuses on the appropriate handling of personal information, while security protects information and systems from unauthorized activity.

---

## 4. Information Life Cycle

Security and privacy protections must follow information through every stage of its life cycle:

1. Creation or collection
2. Processing and use
3. Storage
4. Sharing or transmission
5. Retention or archival
6. Destruction or disposal

Controls should reflect the information’s:

- Classification
- Sensitivity
- Value
- Legal requirements
- Retention requirements
- Potential impact if compromised

Common classification examples include:

- Public
- Internal
- Confidential
- Restricted

Classification schemes vary by organization.

---

## 5. System Development Life Cycle

Security and privacy should be incorporated throughout the system development life cycle.

### Requirements

- Identify business needs.
- Determine legal and regulatory obligations.
- Establish security and privacy requirements.
- Define acceptable risk.

### Design

- Select the architecture.
- Establish system boundaries.
- Select and design controls.
- Apply secure-design principles.

### Development or Acquisition

- Build or obtain the system.
- Configure controls.
- Document implementation details.
- Conduct secure-code and supply-chain reviews when applicable.

### Testing and Assessment

- Test security functions.
- Assess control implementation and effectiveness.
- Document weaknesses.
- Develop remediation plans.

### Operations and Maintenance

- Monitor controls and risks.
- Manage changes and vulnerabilities.
- Review access.
- Apply patches.
- Collect evidence.
- Update documentation.

### Disposal

- Preserve required records.
- Sanitize or destroy information.
- Decommission accounts, hardware, and services.
- Update system inventories and documentation.

---

## 6. Assets and System Boundaries

### Asset Categories

Assets may include:

- Information and data
- Hardware
- Software
- Cloud services
- Networks
- Facilities
- Personnel
- Business processes
- Intellectual property
- Third-party services

### System Boundary

A system boundary defines what is included within the system being managed or assessed.

A clear boundary identifies:

- Components included in the system
- Data processed, stored, or transmitted
- Users and administrators
- Internal and external connections
- Shared services
- Third-party dependencies
- Control responsibility

Poorly defined boundaries can create security gaps, duplicated work, and unclear accountability.

---

## 7. Security and Privacy Controls

Controls are safeguards or countermeasures used to manage risk.

### Control Categories

- **Management:** Governance, planning, risk assessment, and oversight
- **Operational:** Controls primarily performed by people and processes
- **Technical:** Controls implemented through hardware, software, or system configurations

### Control Functions

Controls may be:

- Preventive
- Detective
- Corrective
- Deterrent
- Compensating
- Recovery

Controls must be:

- Selected based on risk and requirements
- Assigned to responsible owners
- Implemented and documented
- Assessed for effectiveness
- Monitored continuously
- Updated when systems or risks change

---

## 8. Major Frameworks and Programs

### NIST Risk Management Framework

The NIST Risk Management Framework provides a structured process for managing security and privacy risk:

1. Prepare
2. Categorize
3. Select
4. Implement
5. Assess
6. Authorize
7. Monitor

### NIST SP 800-53

NIST SP 800-53 provides a catalog of security and privacy controls.

### NIST SP 800-53A

NIST SP 800-53A provides procedures for assessing security and privacy controls.

### NIST SP 800-53B

NIST SP 800-53B provides control baselines and guidance for tailoring them.

### ISO/IEC 27001

ISO/IEC 27001 defines requirements for establishing, operating, maintaining, and continually improving an information security management system.

### COBIT

COBIT provides governance and management objectives for enterprise information and technology.

### FedRAMP

FedRAMP standardizes security assessment, authorization, and continuous monitoring for cloud services used by U.S. federal agencies.

### PCI DSS

PCI DSS establishes security requirements for organizations that store, process, or transmit payment-card data.

### CMMC

CMMC evaluates whether organizations in the defense industrial base meet applicable cybersecurity requirements for protecting sensitive government information.

---

## 9. Important Laws and Requirements

### FISMA

FISMA requires U.S. federal agencies to develop, document, and implement information security programs.

### HIPAA

HIPAA establishes requirements for protecting certain health information handled by covered entities and applicable business associates.

### GDPR

GDPR establishes privacy and data-protection requirements for personal data within its jurisdiction.

### Executive Orders

Executive orders can direct federal agencies to implement specific cybersecurity and privacy initiatives.

Organizations must determine which requirements apply based on factors such as:

- Industry
- Jurisdiction
- Information type
- Customers
- Contracts
- Government relationships
- System purpose

---

## 10. Roles and Responsibilities

Common security, privacy, risk management, and compliance roles include:

- **Authorizing official:** Accepts system risk on behalf of the organization.
- **System owner:** Remains responsible for the system throughout its life cycle.
- **Information owner:** Establishes protection and handling requirements for information.
- **Control owner:** Oversees the implementation and operation of assigned controls.
- **Security or privacy officer:** Leads security or privacy governance activities.
- **Risk executive:** Helps align risk decisions across the organization.
- **Assessor:** Independently evaluates control implementation and effectiveness.
- **System administrator:** Implements and maintains technical configurations.
- **Users:** Follow policies and protect the resources they access.
- **Legal and compliance personnel:** Interpret applicable obligations.
- **Internal audit:** Evaluates governance, risk management, and control processes.

Important distinctions:

- **Control owners implement and maintain controls.**
- **Assessors evaluate controls.**
- **Authorizing officials accept or reject the resulting risk.**

---

## 11. High-Value Exam Distinctions

Know the differences between:

- Governance, risk management, and compliance
- Security and privacy
- Risk appetite and risk tolerance
- Inherent risk and residual risk
- Threat, vulnerability, likelihood, and impact
- Organizational risk and system-level risk
- System owner, information owner, control owner, assessor, and authorizing official
- Control selection, implementation, assessment, authorization, and monitoring
- NIST RMF, COBIT, and ISO/IEC 27001
- NIST SP 800-53, SP 800-53A, and SP 800-53B
- Laws, regulations, standards, frameworks, and contractual requirements
- Security controls and compensating controls
- Compliance and actual risk reduction

---

## Domain Summary

A GRC program connects:

- Organizational objectives
- Legal and contractual obligations
- Risk decisions
- Information protection
- System development
- Control implementation
- Control assessment
- Authorization
- Continuous monitoring

The central principle is:

> Security and privacy risks must be managed throughout the organization and across the information and system life cycles, with clearly assigned responsibility and evidence that controls operate effectively.
