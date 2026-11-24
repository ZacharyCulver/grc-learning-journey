# SC-900 — Section 3, Module 3
# Describe the Security Management Capabilities in Azure

> **Source:** Microsoft Learn — SC-900  
> **Learning Path:** Introduction to Microsoft security solutions  
> **Module:** Describe the security management capabilities in Azure  
> **Verified against current Microsoft Learn content:** November 23, 2026  
> **Duration:** 29 minutes | 8 units | 900 XP  
> **Official Module:** https://learn.microsoft.com/en-us/training/modules/describe-security-management-capabilities-of-azure/

---

# Module Overview

Microsoft Defender for Cloud helps organizations identify security weaknesses, improve their cloud security posture, and protect cloud workloads from cyber threats.

It supports resources running in:

- Microsoft Azure
- Amazon Web Services (AWS)
- Google Cloud Platform (GCP)
- On-premises and hybrid environments

The current module also explains how Defender for Cloud protects generative AI applications and integrates security into software development.

## The Big Idea

**Microsoft Defender for Cloud helps answer three important questions:**

**Are our cloud resources configured securely?**

**Are our running workloads protected against threats?**

**Are we identifying security problems before software reaches production?**

Three major capabilities address these questions.

| Capability | Main purpose |
|---|---|
| Cloud Security Posture Management (CSPM) | Assess configurations and recommend security improvements |
| Cloud Workload Protection Platform (CWPP) | Detect and respond to threats affecting cloud workloads |
| Development Security Operations (DevSecOps) | Integrate security into software development and deployment |

### ELI5

Imagine managing security across a military installation.

**CSPM** is the inspection team checking whether buildings, gates, equipment, and procedures meet security requirements.

**CWPP** is the active protection system that monitors facilities and detects suspicious activity.

**DevSecOps** ensures that new facilities and systems are built securely before they become operational.

All three support the organization's overall security.

### Master Memory Trick

**CSPM = FIND WEAKNESSES**

**CWPP = PROTECT WORKLOADS**

**DevSecOps = SECURE DEVELOPMENT**

---

# 1. What Is Microsoft Defender for Cloud?

Microsoft Defender for Cloud is a:

**Cloud-Native Application Protection Platform (CNAPP)**

A CNAPP combines multiple cloud security capabilities in one integrated platform.

## ELI5

An organization might have:

- Hundreds of Azure virtual machines
- Databases containing customer information
- Applications running in containers
- Storage accounts
- Resources in AWS and Google Cloud
- On-premises systems
- AI applications
- Software development pipelines

Protecting each independently would be difficult.

Microsoft Defender for Cloud provides a centralized way to understand security risks and apply workload-specific protection.

## The Three Pillars

Microsoft organizes Defender for Cloud around three primary pillars:

**DevSecOps**

**CSPM**

**CWPP**

The platform also includes dedicated AI security capabilities.

These include AI Security Posture Management and AI Threat Protection.

---

# 2. Cloud-Native Application Protection Platform — CNAPP

## Big Idea

A CNAPP combines capabilities that traditionally might have required separate security products.

These include:

- Cloud security posture assessment
- Workload threat protection
- Security across development pipelines
- Multicloud visibility
- Cloud risk prioritization

### ELI5

Rather than having completely separate systems for checking configurations, protecting servers, and inspecting application code, a CNAPP brings those capabilities together.

### Important Distinction

**CNAPP = Overall platform category**

**Defender for Cloud = Microsoft's CNAPP solution**

**CSPM, CWPP, and DevSecOps = Its major capability areas**

---

# 3. Cloud Security Posture Management — CSPM

## Big Idea

CSPM helps an organization:

**Find and correct weaknesses in the configuration of its cloud environment.**

### What Is Security Posture?

Security posture describes the overall security condition of an organization or environment.

It considers factors such as:

- Configuration weaknesses
- Missing protections
- Excessive exposure
- Vulnerabilities
- Compliance with selected security standards

### ELI5

Imagine inspecting a barracks building.

You discover:

- An unsecured entrance
- An improperly configured access system
- A missing inspection record
- A room accessible to unauthorized personnel

The building might not currently be under attack.

However, those weaknesses increase the likelihood or impact of a future incident.

CSPM serves a similar function for cloud infrastructure.

---

# 4. CSPM Is Proactive

CSPM does not require an active cyberattack before identifying a problem.

It continuously evaluates the environment for weaknesses.

Examples:

- A resource is unnecessarily exposed to the internet
- A system has a security misconfiguration
- Required security settings are missing
- Administrative privileges are overly broad
- A cloud resource fails a security benchmark

Microsoft Defender for Cloud then provides recommendations for improving the environment.

### Memory Trick

**CSPM = Prevent problems by identifying weaknesses**

Do not confuse this with detecting an attacker who is already active.

That belongs more directly to workload threat protection and security operations.

---

# 5. Cloud Workload Protection Platform — CWPP

## Big Idea

CWPP protects actual cloud workloads against security threats.

### What Is a Workload?

A workload is a computing resource or application performing useful work.

Examples include:

- Virtual machines
- Servers
- Databases
- Containers
- Storage services
- Web applications
- AI services

## ELI5

CSPM notices that a server has a risky configuration.

CWPP helps protect the server against malicious activity and potential compromise.

### Typical CWPP Activities

- Threat detection
- Security alert generation
- Workload-specific protection
- Vulnerability assessment
- Investigation support
- Threat response

### Memory Trick

**CSPM = Check security configuration**

**CWPP = Protect the operating workload**

---

# 6. Development Security Operations — DevSecOps

## Big Idea

DevSecOps integrates security into the software development lifecycle.

Instead of waiting until an application is deployed to discover vulnerabilities, security checks are introduced earlier.

This is sometimes called:

**Shift-Left Security**

## ELI5

Imagine discovering that a new building's doors and locks do not meet security standards after construction is finished.

Fixing everything afterward is more expensive and disruptive.

It would have been better to identify those problems during planning and construction.

DevSecOps applies the same principle to software.

### Memory Trick

**DevSecOps = Build security in from the beginning**

---

# 7. The Three Pillars Compared

| Scenario | Correct pillar |
|---|---|
| Discover a misconfigured cloud resource | CSPM |
| Evaluate security recommendations | CSPM |
| Calculate a cloud secure score | CSPM |
| Investigate a threat against an Azure server | CWPP |
| Protect a running database workload | CWPP |
| Detect suspicious activity against cloud storage | CWPP |
| Identify secrets accidentally committed to code | DevSecOps |
| Find vulnerable open-source dependencies | DevSecOps |
| Scan infrastructure templates before deployment | DevSecOps |

### Important Exam Distinction

**CSPM focuses on the security condition of the environment.**

**CWPP focuses on protecting the workloads operating in that environment.**

**DevSecOps focuses on security throughout application development and deployment.**

---

# 8. Microsoft Defender for Cloud and Security Copilot

Microsoft Defender for Cloud integrates with Microsoft Security Copilot.

Security Copilot is Microsoft's AI-powered security assistant.

Inside Defender for Cloud, Security Copilot can help security professionals:

- Explain a security recommendation
- Summarize security findings
- Understand why an issue matters
- Receive remediation guidance
- Delegate a recommendation to an appropriate resource owner

### Example

Defender for Cloud identifies an improperly configured resource.

An administrator asks Security Copilot:

> Explain why this configuration is dangerous and identify the recommended corrective actions.

Security Copilot can help interpret the finding.

### Important Distinction

**Defender for Cloud = Identifies security findings**

**Security Copilot = Helps explain and work with those findings**

Security Copilot does not replace the underlying security management platform.

---

# 9. Microsoft Defender Portal Integration

The current Microsoft Learn module describes Defender for Cloud as integrated with the broader Microsoft Defender portal.

This helps unify cloud security posture information and threat protection across:

- Cloud environments
- Hybrid environments
- Development environments
- Other supported Microsoft security services

### ELI5

Instead of switching between several disconnected security interfaces, analysts can use a more unified experience.

### Remember

The portal is a management interface.

The security protections come from the underlying Defender services and configured plans.

---

# 10. Security Policies, Initiatives, and Recommendations

Microsoft Defender for Cloud continuously evaluates resources against security requirements.

To understand how this works, distinguish four concepts:

**Policy Definition**

**Security Initiative**

**Security Standard**

**Security Recommendation**

These are related but not interchangeable.

---

# 11. Azure Policy Definitions

## Big Idea

An **Azure Policy definition** specifies a rule or condition that an organization wants to evaluate or enforce.

Microsoft Azure Policy is the underlying governance service.

### ELI5

A policy definition is one inspection rule.

Example:

> Storage accounts must meet the organization's specified security configuration requirements.

Azure Policy evaluates applicable resources against that condition.

## Built-In vs. Custom Policies

Microsoft supplies many built-in definitions.

Organizations can also create custom policy definitions for their own requirements.

### Memory Trick

**Policy Definition = Individual rule**

---

# 12. Security Initiatives

A **security initiative** groups multiple Azure Policy definitions.

### ELI5

One inspection rule might require that doors are secured.

Another rule might require working fire extinguishers.

Another might require access-control records.

Instead of evaluating those rules separately, the organization groups them into one inspection program.

That is the basic idea behind an initiative.

### Example

```text
Security Initiative: Cloud Infrastructure Security
│
├── Policy: Require approved network configurations
├── Policy: Check encryption requirements
├── Policy: Evaluate access restrictions
└── Policy: Check security monitoring settings
```

### Memory Trick

**Policy = One rule**

**Initiative = Collection of rules**

---

# 13. Assigning Policies and Initiatives

Definitions and initiatives must be assigned to an applicable scope.

Examples of Azure scopes include:

- Management groups
- Subscriptions
- Resource groups
- Individual resources, where supported

## ELI5

Writing a security rule does not automatically mean every system is being evaluated under that rule.

An organization must determine which systems are subject to it.

### Memory Trick

**Definition = What rule?**

**Assignment = Where does it apply?**

---

# 14. Microsoft Cloud Security Benchmark — MCSB

## Big Idea

The **Microsoft Cloud Security Benchmark (MCSB)** is Microsoft's cloud-focused security guidance.

It provides best practices and recommendations to improve security across Azure and supported multicloud environments.

The benchmark draws on industry frameworks including:

- Center for Internet Security (CIS)
- National Institute of Standards and Technology (NIST)

It also maps guidance to standards such as PCI DSS.

### Important Exam Fact

**The Microsoft Cloud Security Benchmark is the default security initiative assigned when Defender for Cloud is enabled.**

---

# 15. MCSB Control Domains

The benchmark organizes security requirements into control domains.

Examples include:

- Network security
- Identity and access management
- Privileged access
- Data protection
- Endpoint security
- Incident response
- Data recovery

## ELI5

Imagine an installation inspection divided into categories.

One category examines physical security.

Another examines fire prevention.

Another examines safety equipment.

The MCSB organizes cloud security requirements in a comparable manner.

---

# 16. What Does the MCSB Provide?

For relevant controls, the Microsoft Cloud Security Benchmark provides:

## Control Identifier and Domain

Identifies the security requirement and its category.

## Framework Mappings

Shows relationships to established security frameworks.

Examples:

- CIS
- NIST
- PCI DSS

## Security Recommendations

Describes measures that support the security requirement.

## Azure Implementation Guidance

Explains how applicable Azure capabilities can support the control.

## AWS and GCP Guidance

Provides relevant implementation guidance for supported multicloud environments.

### GRC Connection

These mappings can help security professionals relate technical cloud configurations to broader control requirements.

However, mapping a service to a framework does not automatically establish that the organization is compliant.

---

# 17. Security Recommendations

## Big Idea

Microsoft Defender for Cloud generates recommendations when evaluated resources do not satisfy applicable security requirements.

### ELI5

Think of an inspection deficiency report.

An inspection identifies an issue.

The report describes:

- What is wrong
- Where the issue exists
- How serious it is
- What needs to be corrected

Defender for Cloud recommendations work similarly.

---

# 18. Information in Security Recommendations

A recommendation can identify:

- Description of the security issue
- Affected resources
- Recommended remediation steps
- Severity
- Associated risk factors
- Attack path context, when available

## Recommendation Severity

The module describes three severity levels:

**High**

**Medium**

**Low**

### High Severity

Indicates a significant issue that may require urgent attention.

### Medium Severity

Indicates a security concern that should be addressed according to risk and operational priorities.

### Low Severity

Indicates a lower-priority issue that still represents a security weakness.

### Important Distinction

**A recommendation identifies a problem and suggests corrective action.**

It does not necessarily mean that Defender for Cloud has already performed the remediation.

---

# 19. Security Policies vs. Recommendations

| Concept | Meaning |
|---|---|
| Policy definition | Security condition or requirement |
| Initiative | Collection of policy definitions |
| Standard | Organized security or compliance requirements |
| Recommendation | Finding and suggested corrective action |
| Remediation | Action taken to address the finding |

### Example

A policy evaluates whether a resource meets an expected security configuration.

The evaluation identifies a resource that does not meet the requirement.

Defender for Cloud generates a recommendation.

An administrator corrects the configuration.

The system reassesses the resource.

### Memory Trick

**RULE → ASSESSMENT → FINDING → REMEDIATION**

---

# 20. Regulatory Compliance Dashboard

Microsoft Defender for Cloud includes a regulatory compliance dashboard.

Organizations can use it to assess applicable resources against security and compliance standards.

Microsoft Learn identifies examples such as:

- ISO 27001
- SOC 2
- NIST SP 800-53
- PCI DSS

The dashboard can show which evaluated requirements have passing or failing resources.

### ELI5

Instead of manually comparing every cloud setting with a lengthy security framework, Defender for Cloud helps organize the technical assessment results.

## Important Distinction

The dashboard provides compliance-related technical information.

It does not automatically prove that the organization satisfies every legal, procedural, or documentary requirement of a regulatory framework.

---

# 21. One Recommendation, Multiple Frameworks

Some security controls appear in several frameworks.

### Example

An organization improves administrative authentication protections.

That improvement might support requirements associated with multiple standards.

### Why This Matters

Correcting one security weakness can improve the organization's position against several applicable control frameworks.

### GRC Memory Trick

**One technical improvement can support multiple compliance requirements.**

However, each applicable framework still requires appropriate evidence and assessment.

---

# 22. Cloud Security Posture Management in Detail

CSPM helps organizations continuously understand their cloud security condition.

The module identifies several capabilities:

- Secure score
- Hardening recommendations
- Attack path analysis
- Cloud security explorer
- Governance
- Data security posture management
- AI security posture management

Some are included in foundational CSPM.

Others require the advanced Defender CSPM plan.

---

# 23. Secure Score

## Big Idea

Secure score summarizes an organization's cloud security posture using evaluated security recommendations.

Microsoft Defender for Cloud assesses supported resources and aggregates results into a score.

### ELI5

Imagine a security inspection where every finding contributes to an overall measure of how much security improvement remains.

As the organization addresses relevant weaknesses, its secure score can improve.

### General Interpretation

**Higher secure score = Better alignment with evaluated security recommendations**

However:

**Secure score is not a guarantee that an organization cannot be compromised.**

---

# 24. How Secure Score Relates to Recommendations

Microsoft Defender for Cloud groups recommendations into security controls.

Each control represents related security objectives.

For scoring, the module explains that a resource's contribution to a control improves when the relevant recommendations associated with that control are remediated.

### Example

A cloud resource has several recommended configuration improvements.

Fixing only one issue might not satisfy the entire evaluated control.

The remaining findings still require attention.

### Important Concept

Secure score reflects the status of evaluated controls and recommendations.

It should be used to prioritize improvements, not as a substitute for professional risk assessment.

---

# 25. Secure Score vs. Compliance Score

These terms sound similar but describe different products.

## Defender for Cloud Secure Score

Measures progress toward improving evaluated cloud security configurations.

## Microsoft Purview Compliance Score

Measures progress toward completing compliance-related improvement actions in Compliance Manager.

| Secure Score | Compliance Score |
|---|---|
| Microsoft Defender for Cloud | Microsoft Purview Compliance Manager |
| Cloud security posture | Compliance improvement progress |
| Cloud recommendations | Compliance controls and improvement actions |
| Security configuration weaknesses | Compliance requirements and remediation work |

### Memory Trick

**Defender Secure Score = Cloud Security**

**Purview Compliance Score = Compliance Progress**

Neither score independently guarantees security or regulatory compliance.

---

# 26. Foundational CSPM

Microsoft Defender for Cloud includes foundational CSPM capabilities.

These are available without requiring the optional advanced Defender CSPM plan.

The current module identifies:

- Asset discovery
- Continuous security assessment
- Security recommendations
- Microsoft Cloud Security Benchmark assessment
- Secure score

Foundational CSPM capabilities become available when the relevant subscription or account is onboarded to Defender for Cloud.

### ELI5

Foundational CSPM is the basic security inspection capability.

It helps identify misconfigurations and recommends improvements.

---

# 27. Advanced Defender CSPM Plan

Microsoft offers an optional Defender CSPM plan with advanced capabilities.

These include:

- Attack path analysis
- Cloud security explorer
- Governance
- Data security posture management
- AI security posture management
- Enhanced risk prioritization

### Memory Trick

**Foundational CSPM = Visibility + Recommendations + Secure Score**

**Advanced Defender CSPM = Attack Paths + Advanced Investigation + Governance + Data/AI Risk**

---

# 28. Foundational vs. Advanced CSPM

| Capability | Foundational CSPM | Advanced Defender CSPM |
|---|---|---|
| Asset discovery | Yes | Yes |
| Continuous posture assessment | Yes | Yes |
| Security recommendations | Yes | Yes |
| Secure score | Yes | Yes |
| Microsoft Cloud Security Benchmark | Yes | Yes |
| Attack path analysis | Not part of foundational | Yes |
| Cloud security explorer | Not part of foundational | Yes |
| Enhanced governance | Not part of foundational | Yes |
| AI security posture management | Not part of foundational | Yes |

Some data security posture management features are also available through supported workload-specific plans, including Defender for Storage.

---

# 29. Attack Path Analysis

## Big Idea

Attack path analysis identifies combinations of weaknesses that an attacker could exploit to reach important resources.

A single vulnerability may not tell the entire story.

### ELI5

Imagine an attacker discovers an unsecured maintenance entrance.

That entrance leads to an unlocked hallway.

The hallway leads to a sensitive communications room.

Individually, each weakness creates risk.

Together, they form a dangerous path.

Attack path analysis looks for similar relationships in cloud environments.

---

# 30. Example Attack Path

```text
Internet
   |
   v
Exposed Virtual Machine
   |
   v
Known Vulnerability
   |
   v
Excessive Permissions
   |
   v
Sensitive Storage Account
   |
   v
Potential Data Exposure
```

The chain of weaknesses may create greater risk than any single misconfiguration.

## Why Attack Paths Matter

Security teams have limited time and resources.

Attack path analysis helps identify combinations of weaknesses that could lead to serious compromise.

### Memory Trick

**Attack Path Analysis = How can weaknesses be chained together?**

---

# 31. Risk-Based Prioritization

The advanced Defender CSPM plan considers contextual risk factors.

Examples include:

- Internet exposure
- Vulnerabilities
- Access relationships
- Sensitive data
- Potential attack paths

### Example

Two virtual machines have similar vulnerabilities.

One is isolated from external access.

The other is internet-facing and connected to a sensitive database.

The second may deserve greater priority because of its exposure and potential impact.

### Key Concept

**Risk depends on more than vulnerability severity.**

Exposure, accessibility, and potential consequences also matter.

---

# 32. Cloud Security Explorer

## Big Idea

Cloud Security Explorer allows security teams to proactively investigate cloud security conditions using graph-based queries.

### ELI5

Instead of waiting for a security recommendation to appear, an analyst can investigate relationships among cloud resources.

### Example Question

> Which internet-exposed resources have access to sensitive data?

Cloud Security Explorer helps discover security relationships that may require further investigation.

### Memory Trick

**Attack Path Analysis = Identify dangerous chains**

**Cloud Security Explorer = Query relationships between cloud resources**

Both are advanced Defender CSPM capabilities.

---

# 33. Governance in Defender CSPM

The advanced Defender CSPM plan includes governance capabilities for managing remediation responsibilities.

Administrators can:

- Assign recommendations to resource owners
- Set remediation due dates
- Track accountability
- Follow the progress of corrective actions

### ELI5

Finding a deficiency is only the beginning.

Someone must be responsible for fixing it.

A due date and assigned owner help ensure the problem is not forgotten.

### GRC Connection

This is closely related to managing corrective actions and tracking remediation commitments.

---

# 34. Data Security Posture Management — DSPM

## Big Idea

Data Security Posture Management helps organizations identify and protect sensitive data stored in cloud resources.

Microsoft Defender for Cloud can discover datastores containing sensitive information.

Examples include:

- Databases
- Storage accounts
- Other supported data services

It can identify situations where sensitive information is exposed or inadequately protected.

### ELI5

Imagine discovering that a database containing customer information is publicly accessible.

The database's exposure is especially serious because of the type of information it contains.

DSPM helps connect data sensitivity with security posture.

### Memory Trick

**DSPM = Sensitive Data + Security Exposure**

---

# 35. CSPM vs. DSPM

| CSPM | DSPM |
|---|---|
| Cloud infrastructure security posture | Sensitive-data security posture |
| Misconfigurations across resources | Security exposure affecting data |
| Broad cloud resource assessment | Data-aware risk assessment |
| Secure score and recommendations | Sensitive-data discovery and protection recommendations |

### Important Note

Microsoft Purview also has data security posture management capabilities.

Within this module, the term DSPM refers to data-aware cloud security capabilities available through Microsoft Defender for Cloud.

---

# 36. AI Security Posture Management — AI SPM

The current Microsoft Learn module includes dedicated security posture management for generative AI workloads.

## Big Idea

AI Security Posture Management helps organizations discover and assess their generative AI applications and services.

### ELI5

Before an organization can protect AI systems, it needs to know:

> What AI systems do we have?

> Where are they running?

> What data can they access?

> Are they configured securely?

AI SPM helps answer those questions.

---

# 37. AI Bill of Materials — AI BOM

## Big Idea

An **AI Bill of Materials** is an inventory of the organization's AI-related components.

It can include:

- AI models
- AI applications
- AI services

### ELI5

A traditional equipment inventory identifies vehicles, radios, computers, and other equipment.

An AI BOM serves as an inventory of the AI systems an organization uses.

## Why It Matters

Organizations need visibility into the AI components operating in their environments.

That inventory helps security personnel assess risks and identify configuration weaknesses.

### Memory Trick

**AI BOM = Inventory of AI components**

---

# 38. AI SPM and Attack Paths

AI systems can create new routes to sensitive information.

### Example

An AI application:

- Is accessible from the internet
- Has inadequate authentication
- Can access a database containing sensitive customer records

An attacker might exploit the AI application to reach that information.

AI SPM can help identify these kinds of dangerous relationships.

### Key Concept

**AI SPM focuses on identifying and reducing security weaknesses in AI workloads.**

---

# 39. AI Security Posture vs. AI Threat Protection

These capabilities are different.

## AI Security Posture Management

Identifies AI assets, misconfigurations, and security exposure.

## AI Threat Protection

Detects suspicious or malicious activity involving AI applications.

### ELI5

AI SPM asks:

> Is the AI system configured securely?

AI Threat Protection asks:

> Is someone attacking or misusing the AI system?

### Memory Trick

**AI SPM = PREVENTIVE ASSESSMENT**

**AI Threat Protection = ACTIVE THREAT DETECTION**

---

# 40. Microsoft Defender for Cloud Workload Protection Plans

Microsoft Defender for Cloud provides workload-specific protection through different Microsoft Defender plans.

These plans belong to the CWPP pillar.

Organizations can enable relevant plans according to their resource types and security needs.

---

# 41. Defender Plans

| Defender plan | Protects |
|---|---|
| Defender for Servers | Windows and Linux servers |
| Defender for App Service | Applications running on Azure App Service |
| Defender for Storage | Azure Storage accounts |
| Defender for Databases | Supported database workloads |
| Defender for Containers | Kubernetes and containerized workloads |
| Defender for Key Vault | Azure Key Vault |
| Defender for Resource Manager | Azure resource management operations |
| Defender for AI Services | Supported Azure AI workloads |
| Defender for APIs | Business-critical APIs |

### Exam Strategy

Identify the workload named in the question.

Then select the Defender plan designed to protect that workload.

---

# 42. Microsoft Defender for Servers

Provides advanced threat protection for supported Windows and Linux machines.

The current module identifies capabilities including:

- Threat detection
- Endpoint detection and response
- Vulnerability assessment
- Security recommendations
- Investigation support

## Defender for Endpoint Integration

Defender for Servers includes Microsoft Defender for Endpoint capabilities for supported machines.

### Important Distinction

**Defender for Servers = Server protection through Defender for Cloud**

**Defender for Endpoint = Endpoint security product**

The products can integrate without being identical.

---

# 43. Microsoft Defender for App Service

Protects applications running through Azure App Service.

It helps identify threats targeting supported application workloads.

### Memory Trick

**App Service workload = Defender for App Service**

---

# 44. Microsoft Defender for Storage

Helps detect potentially harmful activity involving Azure Storage accounts.

### Example

An attacker attempts to misuse or compromise a storage resource.

Defender for Storage helps identify suspicious activity.

### Important Distinction

Defender for Storage does not replace appropriately configured access restrictions, encryption, or data governance controls.

---

# 45. Microsoft Defender for Databases

Provides threat detection and response capabilities for supported database workloads.

The module identifies support for database environments including:

- Azure SQL
- Supported open-source relational databases
- Azure Cosmos DB

### Exam Shortcut

**Database threat protection = Defender for Databases**

---

# 46. Microsoft Defender for Containers

Provides security capabilities for container and Kubernetes workloads.

Examples include:

- Environment hardening
- Workload protection
- Runtime threat detection
- Security of container-related resources

### What Is a Container?

A container packages an application with the dependencies required to run it.

Containers help applications operate consistently across supported environments.

### What Is Kubernetes?

Kubernetes is a system for deploying, organizing, and managing containerized applications.

### Memory Trick

**Containers / Kubernetes = Defender for Containers**

---

# 47. Microsoft Defender for Key Vault

Provides advanced threat protection for Azure Key Vault.

Remember the distinction:

**Azure Key Vault** stores and manages secrets, keys, and certificates.

**Defender for Key Vault** provides threat detection for the service.

### Memory Trick

**Key Vault = Store sensitive cryptographic information**

**Defender for Key Vault = Detect threats involving the vault**

---

# 48. Microsoft Defender for Resource Manager

Monitors supported Azure resource-management operations.

### ELI5

Cloud administrators and automation systems constantly perform actions involving Azure resources.

Defender for Resource Manager helps detect suspicious or potentially harmful resource-management activity.

### Memory Trick

**Resource Manager = Cloud management operations**

---

# 49. Microsoft Defender for APIs

Provides security visibility and protection for APIs.

## API

**Application Programming Interface**

An API allows software systems to communicate with one another.

### Relevant Security Concerns

- Exposed APIs
- Vulnerable API configurations
- Unauthorized API activity
- Active threats against API endpoints

Defender for APIs helps organizations assess posture, prioritize vulnerabilities, and detect active threats.

### Memory Trick

**Defender for APIs = Protect software interfaces**

---

# 50. Microsoft Defender for AI Services

The current module includes a workload protection plan specifically for AI services.

## Big Idea

Defender for AI Services detects suspicious or malicious activity involving supported AI applications and services.

Microsoft Learn identifies threats such as:

- Prompt injection
- Data leakage
- Data poisoning
- Credential theft

These threats are particularly important as organizations adopt generative AI.

---

# 51. Prompt Injection

A prompt injection attack attempts to manipulate an AI system by inserting malicious instructions into information it processes.

### ELI5

An AI assistant is supposed to perform an authorized task.

An attacker places deceptive instructions in content the assistant encounters.

The attacker wants the AI system to ignore its intended instructions and perform something unauthorized.

### Memory Trick

**Prompt Injection = Malicious instructions targeting AI behavior**

---

# 52. AI Data Leakage

Data leakage occurs when sensitive information is exposed or extracted through an AI system.

### Example

An AI application returns confidential information to someone who should not have access.

### Important Distinction

Traditional data loss prevention and AI-specific threat protection can address related but different aspects of information exposure.

---

# 53. AI Data Poisoning

Data poisoning attempts to corrupt information used by an AI model or application.

The goal may be to manipulate outputs or undermine reliability.

### ELI5

Imagine someone secretly changes information in a reference source so that an AI system produces incorrect answers.

### Memory Trick

**Data Poisoning = Corrupt the information AI relies on**

---

# 54. AI Credential Theft

Attackers may attempt to steal:

- API keys
- Authentication tokens
- Other credentials associated with AI services

Stolen credentials may allow unauthorized use of AI resources.

### Security Controls

Appropriate protections include:

- Least privilege
- Secure secrets management
- Authentication controls
- Monitoring and threat detection

Microsoft Defender for AI Services helps detect supported AI-related threats.

---

# 55. Defender for AI Services and Defender XDR

The current module explains that alerts involving AI workloads can integrate with Microsoft Defender XDR.

### Example

An organization detects suspicious activity involving an AI application.

Defender XDR can help correlate that alert with other supported security signals.

This might provide additional context involving:

- Identities
- Endpoints
- Applications

### Important Distinction

**Defender for AI Services = AI workload threat protection**

**Defender XDR = Correlate and investigate threats across supported security domains**

---

# 56. Enhanced CWPP Features

Beyond protecting specific workloads, the Microsoft Learn module describes several enhanced security capabilities.

## Endpoint Detection and Response

Defender for Servers integrates Defender for Endpoint capabilities.

## Vulnerability Scanning

Supported capabilities can identify vulnerabilities in:

- Virtual machines
- Container registries
- SQL resources

## Multicloud Protection

Defender for Cloud can extend supported security capabilities to AWS and GCP resources.

## Hybrid Security

Organizations can assess and protect supported on-premises and cloud workloads.

## Threat Alerts

Defender plans provide alerts about suspicious activity and potential compromise.

## Regulatory Compliance

Enhanced plans support additional standards and security assessments.

## Application Controls

Supported features can recommend or enforce application restrictions to reduce malware and unwanted software.

## Just-in-Time VM Access

Supported configurations can limit exposure of virtual machine management ports.

---

# 57. Just-in-Time Virtual Machine Access

## Big Idea

Just-in-Time (JIT) VM access helps reduce unnecessary exposure of administrative network ports.

### ELI5

A management port does not need to remain accessible continuously if administrators only need it occasionally.

JIT controls help limit when the port is accessible.

### Example

A virtual machine normally does not permit management access through a designated network port.

An administrator requests temporary access.

The configuration permits the appropriate connection for the authorized period.

### Important Distinction

**JIT VM Access = Reduce exposure of VM management ports**

**Microsoft Entra PIM = Govern temporary privileged role activation**

**Azure Bastion = Provide secure remote VM connectivity**

These are related security concepts but perform different functions.

---

# 58. DevOps Security Management

The final instructional lesson focuses on security during software development.

Modern organizations use development platforms to:

- Write code
- Store application source files
- Manage dependencies
- Test software
- Build applications
- Deploy applications

Attackers can target these development systems and pipelines.

---

# 59. What Is DevOps?

**DevOps = Development + Operations**

DevOps brings development and operations together to improve the process of building, delivering, and managing software.

### ELI5

Developers write applications.

Operations teams deploy and maintain them.

DevOps helps those teams coordinate their work more efficiently.

However, faster software delivery must not come at the expense of security.

---

# 60. What Is DevSecOps?

**DevSecOps = Development + Security + Operations**

Security becomes part of the software development process.

### Memory Trick

**DevOps = Build and operate software efficiently**

**DevSecOps = Build and operate software securely**

---

# 61. Shift-Left Security

## Big Idea

Shift-left security means introducing security testing and review earlier in the software development process.

### Traditional Approach

```text
Develop → Build → Deploy → Discover Security Problem → Fix
```

### Shift-Left Approach

```text
Plan → Develop → Security Checks → Build → Test → Deploy
```

The goal is to identify security problems before they reach production.

### Important Principle

Fixing a security weakness during development is often easier than correcting it after deployment.

---

# 62. Microsoft Defender for DevOps

Microsoft Defender for DevOps is a capability available through Defender for Cloud.

It helps security teams manage security across supported development environments.

The current module identifies platforms including:

- GitHub
- Azure DevOps
- GitLab

### ELI5

An organization may have software development projects spread across several platforms.

Defender for DevOps helps security teams view findings in one central environment.

---

# 63. Defender for DevOps Capabilities

## Unified Visibility

Security teams can view findings across connected development environments.

## Code Scanning Findings

Identify security weaknesses in application code.

## Exposed Secrets

Detect credentials or other sensitive values accidentally included in code.

## Open-Source Software Vulnerabilities

Identify known vulnerabilities in supported third-party dependencies.

## Infrastructure-as-Code Security

Analyze infrastructure templates for potential security misconfigurations.

## Remediation Prioritization

Use contextual information to prioritize important findings and connect remediation work to development processes.

---

# 64. Code Scanning Vulnerabilities

A vulnerability is a weakness that could potentially be exploited.

Code scanning helps identify security weaknesses before software is deployed.

### Example

A developer introduces a vulnerable function into an application.

A security scan identifies the potential problem before the application reaches production.

### Memory Trick

**Code Scanning = Find weaknesses in application code**

---

# 65. Exposed Secrets

Developers sometimes accidentally place sensitive values into source code.

Examples:

- Passwords
- API keys
- Tokens
- Connection strings

### Example

A developer commits an API key to a GitHub repository.

If exposed, the key could be stolen and misused.

Defender for DevOps can surface findings related to exposed secrets.

### Important Concept

**Secrets should be managed securely rather than embedded unnecessarily in application code.**

Azure Key Vault is one service that supports secure secrets management.

---

# 66. Open-Source Software Vulnerabilities

Many applications depend on third-party software libraries.

These dependencies may contain known vulnerabilities.

### Example

An application uses an outdated open-source package with a published security weakness.

Security scanning can identify the vulnerable dependency.

### Memory Trick

**OSS Scan = Check third-party dependencies**

---

# 67. Infrastructure as Code — IaC

## Big Idea

Infrastructure as Code uses configuration files or templates to define and deploy infrastructure.

### ELI5

Instead of manually configuring every server, network, or cloud resource, engineers write files describing the desired environment.

Automation uses those files to create or update infrastructure.

### Example

A deployment template specifies:

- A virtual machine
- A storage account
- Network configuration
- Security settings

If the template contains a security mistake, that mistake can affect every deployment created from it.

---

# 68. IaC Security Scanning

Defender for DevOps can identify security issues in infrastructure templates before deployment.

### Example

An infrastructure template configures an AI application without appropriate authentication controls.

Security scanning identifies the risk during development.

The development team can correct the configuration before the resource is deployed.

### Memory Trick

**IaC Scan = Find infrastructure misconfigurations before deployment**

---

# 69. Pull Requests and Remediation

A **pull request** proposes changes to code and allows reviewers to examine those changes before they are merged.

Defender for DevOps can provide relevant security findings and remediation context in development workflows.

These may include:

- Security findings
- Code-related recommendations
- Pull request annotations
- Assigned ownership
- Remediation workflows

### ELI5

A developer submits a proposed code change.

Security tooling identifies a potential issue.

The developer receives the finding and can correct it before the change becomes part of the main project.

---

# 70. Code-to-Cloud Visibility

One of the major benefits of Defender for DevOps is connecting development findings with deployed cloud resources.

### Example

A security team discovers:

- A risky infrastructure template
- A deployment using that template
- A cloud resource exposed because of the configuration

The organization can trace the issue back to its development source.

### Memory Trick

**Code-to-Cloud = Connect development weaknesses with cloud exposure**

This helps organizations address the underlying cause rather than repeatedly fixing individual deployed resources.

---

# 71. DevSecOps and AI Development

AI applications also use development pipelines.

Those pipelines may contain:

- Source code
- API keys
- Infrastructure templates
- Configuration files
- Software dependencies

Security weaknesses in these components can expose AI services.

### Example

A developer accidentally commits an AI service API key.

Defender for DevOps can identify the exposed secret.

Another scan may identify an infrastructure template that deploys the AI service without adequate authentication.

### Important Concept

**AI development must follow the same secure development principles as other software.**

---

# 72. The Entire Defender for Cloud Workflow

Imagine an organization building and deploying a new application.

## During Development

**Defender for DevOps** identifies:

- Vulnerable application code
- Exposed secrets
- Unsafe infrastructure templates

## During Cloud Configuration

**CSPM** identifies:

- Misconfigured resources
- Excessive exposure
- Missing recommended security settings
- Risks requiring remediation

## During Production

**CWPP** helps detect:

- Suspicious server activity
- Attacks against storage
- Database threats
- Container security threats
- AI application attacks

### Complete Mental Model

```text
SOFTWARE DEVELOPMENT
        |
        v
DEFENDER FOR DEVOPS
Scan code, secrets, dependencies, IaC
        |
        v
CLOUD DEPLOYMENT
        |
        v
CSPM
Assess posture, secure score, recommendations
        |
        v
RUNNING CLOUD WORKLOADS
        |
        v
CWPP
Detect threats and protect workloads
        |
        v
SECURITY INVESTIGATION AND REMEDIATION
```

This is a conceptual workflow rather than a required Azure deployment procedure.

---

# 73. Defender for Cloud vs. Other Microsoft Security Products

| Product | Primary purpose |
|---|---|
| Microsoft Defender for Cloud | Cloud posture and workload protection |
| Microsoft Defender XDR | Unified detection, investigation, and response across supported security domains |
| Microsoft Sentinel | SIEM and SOAR |
| Microsoft Security Copilot | AI-assisted security analysis |
| Microsoft Purview | Data security, governance, risk, and compliance |
| Microsoft Entra | Identity and access management |

### Example

A vulnerable Azure virtual machine is discovered.

**Defender for Cloud** identifies the cloud configuration or workload security issue.

An associated threat may generate an alert.

**Defender XDR** can help correlate supported security signals.

**Microsoft Sentinel** can combine logs from multiple sources for SIEM/SOAR investigations.

**Security Copilot** can assist with understanding and investigating the relevant information.

These products can work together without performing identical jobs.

---

# 74. Secure Score vs. Defender Plans

Another important distinction:

## Secure Score

Shows the evaluated security posture of the environment.

## Defender Workload Protection Plans

Provide active protections for different workload types.

### Example

A cloud environment has a low secure score because several resources are misconfigured.

The organization may also have Defender for Servers enabled to detect server-based threats.

The secure score and the workload protection plan serve different purposes.

### Memory Trick

**Secure Score = How securely configured are we?**

**Defender Plans = What workloads are we protecting?**

---

# 75. AI Security: Three Critical Distinctions

| Capability | Main question |
|---|---|
| AI Security Posture Management | Are our AI assets configured securely? |
| Defender for AI Services | Are our AI workloads experiencing malicious activity? |
| Security Copilot | Can AI assist our security analysts? |

### Memory Trick

**AI SPM = Assess AI**

**Defender for AI Services = Protect AI**

**Security Copilot = Use AI to support security professionals**

---

# 76. GRC / ISSO Career Connection

The following is additional professional context, not a separate Microsoft Learn lesson.

Microsoft Defender for Cloud is directly relevant to governance, risk, compliance, and information assurance work.

An ISSO may need to:

- Identify security weaknesses
- Review configuration baselines
- Track remediation
- Monitor vulnerabilities
- Assess control effectiveness
- Demonstrate compliance
- Communicate risk to leadership

Defender for Cloud supports several of these activities.

---

# 77. NIST SP 800-53 Relationships

The following relationships are illustrative. Using a Microsoft service does not automatically satisfy the entire NIST control.

| Defender for Cloud capability | Related NIST control |
|---|---|
| Continuous security assessment | CA-7 — Continuous Monitoring |
| Vulnerability scanning and findings | RA-5 — Vulnerability Monitoring and Scanning |
| Secure configuration recommendations | CM-6 — Configuration Settings |
| Security monitoring and threat alerts | SI-4 — System Monitoring |
| Security remediation tracking | CA-5 — Plan of Action and Milestones |
| Secure development analysis | SA-11 — Developer Testing and Evaluation |
| Access and permission controls | AC-6 — Least Privilege |

### Example

Defender for Cloud identifies a critical configuration issue.

The security team creates a remediation task.

A system owner is assigned responsibility.

A target completion date is established.

The issue is corrected and reassessed.

### GRC Perspective

This resembles the process of identifying, documenting, tracking, and resolving a security weakness.

---

# 78. Plan of Action and Milestones — POA&M

A POA&M documents security weaknesses and planned corrective actions.

It commonly includes:

- Description of the weakness
- Affected system or control
- Corrective action
- Responsible owner
- Required resources
- Target completion date
- Current status

### Example

```text
Finding:
Publicly exposed administrative service

Risk:
Unauthorized remote access

Corrective Action:
Restrict unnecessary network access

Responsible Owner:
Cloud Infrastructure Team

Target Date:
December 15

Status:
In Progress
```

Defender for Cloud recommendations can provide useful technical information for remediation tracking.

However, an organization still needs to manage its formal POA&M requirements and supporting documentation.

### Important Distinction

**Defender Recommendation = Technical security finding**

**POA&M = Formal remediation-management record**

---

# 79. Risk Management Framework — RMF Connection

The NIST Risk Management Framework emphasizes ongoing security and risk management.

Microsoft Defender for Cloud can provide technical information useful during activities such as:

- Implementing controls
- Assessing controls
- Monitoring security posture
- Tracking weaknesses
- Supporting remediation

### Important Principle

**Continuous monitoring is not simply checking whether a security product is installed.**

An organization should verify that the controls operate effectively and that identified weaknesses are addressed.

---

# 80. SC-900 Exam Quick Reference

| If the question mentions... | Think... |
|---|---|
| Cloud-native application protection platform | Microsoft Defender for Cloud |
| Three pillars of Defender for Cloud | DevSecOps, CSPM, CWPP |
| Cloud configuration weaknesses | CSPM |
| Security posture recommendations | CSPM |
| Running workload protection | CWPP |
| Security checks during development | DevSecOps |
| Shift-left security | DevSecOps |
| Default security benchmark | MCSB |
| Frameworks underlying MCSB | CIS and NIST |
| Single Azure Policy rule | Policy definition |
| Collection of policies | Initiative |
| Where a policy applies | Assignment |
| Corrective action suggestion | Recommendation |
| Overall cloud security posture measure | Secure score |
| Basic cloud posture assessment | Foundational CSPM |
| Advanced risk analysis | Defender CSPM |
| Chained cloud weaknesses | Attack path analysis |
| Proactive graph-based investigation | Cloud Security Explorer |
| Assign remediation owner and deadline | CSPM governance |
| Sensitive cloud datastore exposure | DSPM |
| Inventory AI models and services | AI BOM |
| Assess AI configuration risk | AI SPM |
| Detect attacks against AI workloads | Defender for AI Services |
| Protect Windows/Linux cloud servers | Defender for Servers |
| Protect Azure Storage | Defender for Storage |
| Protect databases | Defender for Databases |
| Protect Kubernetes workloads | Defender for Containers |
| Protect secrets-management service | Defender for Key Vault |
| Protect APIs | Defender for APIs |
| Centralized development security findings | Defender for DevOps |
| Secrets committed to source code | Defender for DevOps |
| Vulnerable open-source packages | Defender for DevOps |
| Insecure IaC templates | Defender for DevOps |
| AI-powered remediation explanation | Microsoft Security Copilot |

---

# 81. Final Module 3 Cram Sheet

```text
MICROSOFT DEFENDER FOR CLOUD
= CLOUD SECURITY POSTURE + WORKLOAD PROTECTION

CNAPP
= CLOUD-NATIVE APPLICATION PROTECTION PLATFORM

THREE PILLARS
= DEVSECOPS + CSPM + CWPP

CSPM
= FIND AND CORRECT CLOUD SECURITY WEAKNESSES

CWPP
= PROTECT RUNNING CLOUD WORKLOADS

DEVSECOPS
= SECURITY THROUGHOUT SOFTWARE DEVELOPMENT

SHIFT LEFT
= FIND SECURITY PROBLEMS EARLY

AZURE POLICY DEFINITION
= INDIVIDUAL SECURITY RULE

SECURITY INITIATIVE
= COLLECTION OF POLICY DEFINITIONS

POLICY ASSIGNMENT
= WHERE THE RULE APPLIES

MCSB
= MICROSOFT CLOUD SECURITY BENCHMARK

MCSB FRAMEWORKS
= CIS + NIST

SECURITY RECOMMENDATION
= FINDING + SUGGESTED REMEDIATION

REGULATORY COMPLIANCE DASHBOARD
= ASSESS TECHNICAL CONTROL STATUS

SECURE SCORE
= CLOUD SECURITY POSTURE MEASURE

FOUNDATIONAL CSPM
= BASIC ASSESSMENTS + RECOMMENDATIONS + SCORE

DEFENDER CSPM
= ADVANCED POSTURE MANAGEMENT

ATTACK PATH ANALYSIS
= CHAIN OF WEAKNESSES TO IMPORTANT RESOURCES

CLOUD SECURITY EXPLORER
= GRAPH-BASED CLOUD SECURITY QUERIES

CSPM GOVERNANCE
= ASSIGN OWNERS + TRACK REMEDIATION

DSPM
= SENSITIVE DATA SECURITY POSTURE

AI SPM
= AI SECURITY POSTURE MANAGEMENT

AI BOM
= INVENTORY OF AI MODELS/APPLICATIONS/SERVICES

AI THREAT PROTECTION
= DETECT ATTACKS ON AI WORKLOADS

DEFENDER FOR SERVERS
= WINDOWS/LINUX SERVER PROTECTION

DEFENDER FOR STORAGE
= AZURE STORAGE THREAT PROTECTION

DEFENDER FOR DATABASES
= DATABASE THREAT PROTECTION

DEFENDER FOR CONTAINERS
= KUBERNETES/CONTAINER PROTECTION

DEFENDER FOR KEY VAULT
= THREAT PROTECTION FOR KEY VAULT

DEFENDER FOR RESOURCE MANAGER
= MONITOR RESOURCE MANAGEMENT OPERATIONS

DEFENDER FOR APIs
= API SECURITY

DEFENDER FOR AI SERVICES
= AI WORKLOAD THREAT PROTECTION

PROMPT INJECTION
= MALICIOUS INSTRUCTIONS TARGETING AI

DATA POISONING
= CORRUPTING INFORMATION USED BY AI

DATA LEAKAGE
= EXPOSURE OF SENSITIVE INFORMATION

DEFENDER FOR DEVOPS
= DEVELOPMENT PIPELINE SECURITY

CODE SCANNING
= FIND APPLICATION CODE WEAKNESSES

SECRET SCANNING
= FIND EXPOSED CREDENTIALS IN CODE

OSS SCANNING
= FIND VULNERABLE SOFTWARE DEPENDENCIES

IaC SCANNING
= FIND INFRASTRUCTURE MISCONFIGURATIONS

CODE-TO-CLOUD
= CONNECT DEVELOPMENT ISSUES WITH CLOUD RISKS

SECURITY COPILOT
= AI ASSISTANCE FOR ANALYSIS AND REMEDIATION

DEFENDER XDR
= UNIFIED THREAT DETECTION AND RESPONSE

MICROSOFT SENTINEL
= SIEM + SOAR
```

---

# 82. Final Mental Model

Imagine an organization developing and deploying an application in Microsoft Azure.

**Microsoft Defender for DevOps** helps identify security weaknesses in application code, dependencies, secrets, and infrastructure templates.

The application is deployed.

**Cloud Security Posture Management (CSPM)** continuously evaluates the environment for misconfigurations and weaknesses.

**Microsoft Cloud Security Benchmark (MCSB)** provides default security guidance.

**Security recommendations** identify corrective actions.

**Secure score** summarizes the evaluated security posture.

The advanced **Defender CSPM** plan adds capabilities such as attack path analysis and Cloud Security Explorer.

**Cloud Workload Protection (CWPP)** helps detect and respond to threats against the application's servers, databases, storage, containers, and other supported resources.

**AI Security Posture Management** evaluates the security configuration of AI workloads.

**Defender for AI Services** helps detect malicious activity involving supported AI applications.

**Microsoft Security Copilot** assists administrators in understanding and prioritizing relevant findings.

All these capabilities work together to support one objective:

**Continuously identify, prioritize, and reduce cloud security risks while protecting workloads against active threats.**

---

# Official Microsoft Learn References

These pages were checked against the live module on November 23, 2026.

[Module Overview](https://learn.microsoft.com/en-us/training/modules/describe-security-management-capabilities-of-azure/)

[Introduction](https://learn.microsoft.com/en-us/training/modules/describe-security-management-capabilities-of-azure/1-introduction)

[Describe Microsoft Defender for Cloud](https://learn.microsoft.com/en-us/training/modules/describe-security-management-capabilities-of-azure/2-describe-defender-cloud)

[Describe How Security Policies, Standards, and Recommendations Improve Cloud Security Posture](https://learn.microsoft.com/en-us/training/modules/describe-security-management-capabilities-of-azure/3-baselines-for-azure)

[Describe Cloud Security Posture Management](https://learn.microsoft.com/en-us/training/modules/describe-security-management-capabilities-of-azure/4-describe-cloud-security-posture-management)

[Describe the Enhanced Security of Microsoft Defender for Cloud](https://learn.microsoft.com/en-us/training/modules/describe-security-management-capabilities-of-azure/5a-describe-enhanced-security-defender-cloud)

[Describe DevOps Security Management](https://learn.microsoft.com/en-us/training/modules/describe-security-management-capabilities-of-azure/6-describe-dev-ops-security-management)

[Module Assessment](https://learn.microsoft.com/en-us/training/modules/describe-security-management-capabilities-of-azure/7-knowledge-check)

[Summary and Resources](https://learn.microsoft.com/en-us/training/modules/describe-security-management-capabilities-of-azure/8-summary-resources)
