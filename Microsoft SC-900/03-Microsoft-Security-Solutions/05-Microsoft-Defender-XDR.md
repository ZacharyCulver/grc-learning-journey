# SC-900 — Section 3, Module 5
# Describe Threat Protection with Microsoft Defender XDR

> **Source:** Microsoft Learn — SC-900  
> **Learning Path:** Introduction to Microsoft security solutions  
> **Module:** Describe threat protection with Microsoft Defender XDR  
> **Verified against current Microsoft Learn content:** November 23, 2026  
> **Duration:** 2 hours 5 minutes | 13 units | 1,400 XP  
> **Official Module:** https://learn.microsoft.com/en-us/training/modules/describe-threat-protection-with-microsoft-365-defender/

---

# Module Overview

Microsoft Defender XDR is a unified cybersecurity solution that helps organizations prevent, detect, investigate, and respond to threats.

**XDR = Extended Detection and Response**

Microsoft Defender XDR integrates security information across four major environments:

- Endpoints
- Identities
- Email
- Applications

It also works with Microsoft's broader security portfolio, including Microsoft Sentinel, Microsoft Defender for Cloud, and Microsoft Security Copilot.

## The Big Idea

Modern cyberattacks rarely affect just one system.

An attacker might:

1. Send a phishing email.
2. Steal an employee's credentials.
3. Compromise the employee's laptop.
4. Move laterally into another system.
5. Access sensitive company information.
6. Attempt to steal data or deploy ransomware.

If security tools operate independently, each may detect only part of the attack.

**Microsoft Defender XDR combines signals from multiple security products to reveal the larger attack.**

### ELI5

Imagine several security teams protecting a military installation.

One monitors entrances.

Another monitors computer systems.

Another investigates personnel security issues.

Another monitors sensitive communications.

If the teams never share information, an attacker might exploit weaknesses between them.

Defender XDR creates a coordinated security operation where information from different teams contributes to a single investigation.

### Master Memory Trick

**Defender XDR = Connect the dots across security domains**

---

# 1. What Is Extended Detection and Response?

## Big Idea

Extended Detection and Response combines information from multiple security technologies to improve threat detection, investigation, and response.

The four major functions are:

**Prevent**

**Detect**

**Investigate**

**Respond**

## Prevention

Apply security protections that reduce the likelihood of compromise.

## Detection

Identify activity that may indicate an attack.

## Investigation

Determine what happened, which systems are affected, and how the attack progressed.

## Response

Contain and remediate identified threats.

### Memory Trick

**P-D-I-R**

**Prevent → Detect → Investigate → Respond**

---

# 2. Pre-Breach vs. Post-Breach Protection

Microsoft Defender XDR provides both pre-breach and post-breach capabilities.

## Pre-Breach

Security protections intended to reduce the likelihood of successful compromise.

Examples:

- Anti-malware protection
- Attack surface reduction
- Anti-phishing controls
- Vulnerability management
- Security configuration improvements

## Post-Breach

Security capabilities used after suspicious or malicious activity occurs.

Examples:

- Endpoint detection and response
- Incident correlation
- Threat hunting
- Automated investigation
- Remediation

### ELI5

**Pre-Breach = Try to stop the attack from succeeding**

**Post-Breach = Detect and respond when an attacker gets through**

### Important Concept

An effective security program needs both.

No preventive control can guarantee that every attack will be stopped.

---

# 3. The Microsoft Defender XDR Family

Microsoft Defender XDR integrates several Microsoft security solutions.

| Product | Primary purpose |
|---|---|
| Microsoft Defender for Endpoint | Protect devices and endpoints |
| Microsoft Defender for Office 365 | Protect email and collaboration |
| Microsoft Defender for Cloud Apps | Protect and govern SaaS applications |
| Microsoft Defender for Identity | Detect identity-based threats |
| Microsoft Defender Vulnerability Management | Identify and prioritize vulnerabilities |
| Microsoft Defender Threat Intelligence capabilities | Provide information about threats and attackers |
| Microsoft Security Exposure Management | Understand attack surfaces and exposure risk |

Microsoft Entra ID Protection complements Defender for Identity by detecting risks affecting cloud identities.

### Memory Trick

**Endpoint = Devices**

**Office 365 = Email**

**Cloud Apps = SaaS**

**Identity = Identity attacks**

**Vulnerability Management = Weaknesses**

**Threat Intelligence = Adversary information**

**Exposure Management = Enterprise-wide risk relationships**

---

# 4. How Defender XDR Connects Security Products

## Combined Incident Queue

Microsoft Defender XDR correlates related alerts and suspicious events across products.

Instead of creating several disconnected investigations, related signals can be grouped into one incident.

### Example

```text
Incident: Suspected Credential Compromise
│
├── Defender for Office 365
│   └── Phishing email detected
│
├── Defender for Identity
│   └── Suspicious identity activity
│
├── Defender for Endpoint
│   └── Malicious activity on laptop
│
└── Defender for Cloud Apps
    └── Suspicious SaaS activity
```

All these signals may contribute to one coordinated investigation.

### Memory Trick

**Alert = Individual suspicious signal**

**Incident = Combined investigation case**

---

# 5. Cross-Product Automated Response

Microsoft Defender XDR allows supported products to share threat information and coordinate actions.

### Example

Defender for Endpoint detects a malicious file.

The security information can help Defender for Office 365 identify the same malicious file in email messages.

Appropriate protection can prevent the threat from spreading through additional channels.

### Important Concept

**Cross-product intelligence allows one Defender product's detection to help protect another security domain.**

---

# 6. Automatic Attack Disruption

## Big Idea

Automatic attack disruption uses high-confidence security signals to identify and contain attacks already in progress.

Depending on the attack and supported capabilities, actions may include:

- Isolating compromised devices
- Disabling compromised accounts
- Containing malicious IP addresses

### ELI5

Imagine security personnel identify an active intruder.

Instead of waiting for a lengthy manual process, predefined emergency containment measures are activated.

Automatic attack disruption applies a comparable principle to cybersecurity.

### Memory Trick

**Automatic Attack Disruption = Contain an active attack quickly**

---

# 7. Self-Healing and Automated Remediation

Microsoft Defender XDR includes automated investigation and remediation capabilities.

Supported actions can help restore affected devices, identities, and mailboxes to a safer condition.

### Example

A malicious file is identified on a device.

Automated investigation can examine the related evidence and take supported remediation actions according to the organization's configuration.

### Important Distinction

**Detection = Identify the threat**

**Containment = Limit the threat's ability to spread**

**Remediation = Address the threat and its effects**

Automated remediation does not eliminate the need for validation and follow-up.

---

# 8. Advanced Hunting Across Products

Microsoft Defender XDR provides query-based access to security signals.

Analysts can use:

**Kusto Query Language (KQL)**

to investigate events across supported security products.

The current Microsoft Learn module describes access to up to **30 days of raw historical signals and alert data** for relevant Defender XDR hunting scenarios.

### ELI5

Instead of waiting for a detection rule to find suspicious behavior, an analyst searches available security records for evidence of a threat.

### Memory Trick

**Advanced Hunting = Proactively search security data**

---

# 9. Microsoft Defender for Office 365

## Big Idea

Microsoft Defender for Office 365 protects organizations against threats associated with:

- Email messages
- Malicious links
- Malicious attachments
- Phishing
- Collaboration tools

Supported collaboration environments include Microsoft Teams, SharePoint, and Outlook-related workflows.

### ELI5

Email is one of the most common ways attackers attempt to compromise an organization.

Defender for Office 365 protects the organization against malicious content delivered through email and collaboration services.

---

# 10. Defender for Office 365 Plans

Microsoft provides:

**Defender for Office 365 Plan 1**

**Defender for Office 365 Plan 2**

The plans offer different levels of protection and investigation functionality.

For SC-900, recognize that the service provides protection, investigation, hunting, and response capabilities.

Detailed feature entitlements depend on licensing.

---

# 11. Anti-Malware Protection

Anti-malware protections help identify and block malicious software.

Examples include:

- Viruses
- Spyware
- Ransomware
- Other malicious files

### Memory Trick

**Anti-Malware = Detect malicious software**

---

# 12. Anti-Spam Protection

Spam refers to unsolicited or unwanted messages.

Anti-spam technology identifies and filters suspicious or unwanted email.

### Important Distinction

Spam and phishing are not identical.

**Spam = Unwanted or unsolicited messages**

**Phishing = Deceptive communication intended to steal information or induce harmful actions**

Some phishing messages are also spam, but the categories describe different characteristics.

---

# 13. Anti-Phishing Protection

## Big Idea

Phishing attempts to deceive users into revealing credentials, disclosing information, or performing harmful actions.

### Example

An employee receives an email that appears to come from the company's IT department.

The message instructs the employee to enter their credentials into a fraudulent sign-in page.

Defender for Office 365 provides anti-phishing and spoofing protections.

### Memory Trick

**Phishing = Deceive the user**

**Spoofing = Impersonate a trusted identity or source**

---

# 14. Safe Attachments

## Big Idea

Safe Attachments provides additional protection against malicious attachments.

Microsoft describes a process called:

**Detonation**

## What Is Detonation?

Detonation opens or executes a suspicious attachment in an isolated virtual environment to observe its behavior.

### ELI5

Instead of opening a suspicious package in a busy office, security personnel examine it in a controlled environment.

If the attachment attempts malicious activity, the system can identify that behavior without executing the file directly on the recipient's device.

### Memory Trick

**Safe Attachments = Test suspicious files in isolation**

---

# 15. Safe Links

## Big Idea

Safe Links helps protect users from malicious URLs.

A URL is a web address.

Safe Links helps detect dangerous destinations associated with phishing and other attacks.

### Example

An employee receives an email containing a link to a fraudulent authentication page.

Safe Links can help identify and block the malicious destination.

### Memory Trick

**Safe Links = Protect against malicious URLs**

---

# 16. Safe Links vs. Safe Attachments

| Capability | Protects against |
|---|---|
| Safe Links | Malicious URLs |
| Safe Attachments | Malicious files and attachments |
| Anti-Phishing | Deceptive email and impersonation |
| Anti-Spam | Unwanted email |

### Exam Shortcut

**Suspicious URL = Safe Links**

**Suspicious attachment = Safe Attachments**

---

# 17. Attack Simulation Training

Microsoft Defender for Office 365 provides attack simulation training.

Administrators can simulate realistic attacks to help employees recognize and respond to phishing and similar threats.

### ELI5

Instead of waiting for a real phishing attack to discover whether employees can recognize suspicious messages, the organization conducts a controlled training exercise.

### Example

An organization sends a simulated phishing email.

Employees who interact with the simulation may receive additional training.

### Memory Trick

**Attack Simulation = Practice recognizing attacks safely**

---

# 18. Investigating Email Threats

Defender for Office 365 provides investigation capabilities including:

- Message trace
- Threat Explorer
- Real-time detections
- Threat trackers
- Campaign analysis
- Reports

These help analysts understand email-related threats.

---

# 19. Message Trace

## Big Idea

Message trace tracks email as it moves through a Microsoft 365 organization.

It can identify whether a message was:

- Received
- Rejected
- Deferred
- Delivered

### ELI5

Message trace is like checking the delivery history of a package.

It helps determine where the message went and what happened during processing.

### Memory Trick

**Message Trace = Follow the email's delivery path**

---

# 20. Threat Explorer

Threat Explorer helps analysts investigate threats involving email and related content.

Examples include:

- Malicious messages
- Malware detections
- Suspicious URLs
- Phishing campaigns

### Important Distinction

Threat Explorer is not the same as the Microsoft Purview Content Explorer.

**Threat Explorer = Investigate email security threats**

**Content Explorer = Locate classified or sensitive information**

---

# 21. Campaigns

The Campaigns feature helps analysts understand coordinated phishing or malware attacks.

### Example

An attacker sends similar phishing messages to hundreds of employees.

Rather than examining each message separately, the security team can investigate the overall campaign.

### Memory Trick

**Campaign = Coordinated attack involving related messages**

---

# 22. Zero-Hour Auto Purge — ZAP

## Big Idea

Zero-hour auto purge provides retroactive protection against malicious email.

### ELI5

An email initially passes security checks and reaches an employee's mailbox.

Later, Microsoft identifies the message as malicious.

ZAP can take action against the already-delivered message.

### Memory Trick

**ZAP = Remove newly recognized malicious email after delivery**

---

# 23. Automated Investigation and Response — AIR

AIR supports automated investigation of identified threats.

It can reduce repetitive work and help security teams prioritize complex incidents.

### Example

A suspicious email is detected.

Automated investigation examines related messages, recipients, and available evidence.

Supported remediation can follow the findings and configured approval requirements.

### Memory Trick

**AIR = Automated Investigation and Response**

---

# 24. Microsoft Defender for Endpoint

## Big Idea

Microsoft Defender for Endpoint protects devices against cybersecurity threats.

Endpoints include:

- Laptops
- Desktop computers
- Servers
- Mobile devices
- Other supported network-connected devices

### ELI5

An endpoint is a device connected to an organization's computing environment.

Defender for Endpoint protects those devices before and after an attempted compromise.

---

# 25. Endpoint Security Architecture

Microsoft Learn describes three important technologies.

## Endpoint Behavioral Sensors

Collect supported security signals from devices.

## Cloud Security Analytics

Analyze collected signals to identify suspicious behavior.

## Threat Intelligence

Provide information about known attacker tools, techniques, and procedures.

### Memory Trick

**Sensors = Observe**

**Analytics = Interpret**

**Threat Intelligence = Add attacker context**

---

# 26. Attack Surface Reduction — ASR

## Big Idea

Attack Surface Reduction reduces opportunities for attackers to exploit endpoints.

An attack surface represents the potential entry points an attacker might use.

### Examples

- Restrict dangerous application behavior
- Reduce unnecessary executable activity
- Block malicious network destinations
- Apply exploit mitigations
- Improve device security settings

### ELI5

Every unnecessary opening in a security perimeter gives an attacker another possible route inside.

Attack surface reduction closes or restricts unnecessary openings.

### Memory Trick

**ASR = Reduce ways an attacker can get in**

---

# 27. Next-Generation Protection

Next-generation protection includes antivirus and cloud-based security capabilities.

Microsoft Defender for Endpoint uses:

- Real-time protection
- Behavioral analysis
- Heuristic detection
- Cloud-delivered protection
- Antivirus security updates

### Important Distinction

Traditional signature matching is valuable but insufficient against every modern threat.

Behavioral and cloud-based detection help identify emerging malicious activity.

---

# 28. Endpoint Detection and Response — EDR

## Big Idea

EDR helps analysts identify, investigate, and respond to threats on endpoints.

### Example

A laptop begins executing suspicious PowerShell commands.

EDR records relevant activity, generates detections, and provides investigation information.

An analyst can determine whether the activity represents a threat and initiate appropriate response actions.

### Memory Trick

**EDR = Detect and respond to threats on devices**

---

# 29. Automated Investigation and Remediation

Defender for Endpoint supports automated investigation and remediation.

The goal is to reduce manual investigation workload and accelerate response to known threat patterns.

### Example

A suspicious file is detected.

Automated investigation examines related evidence and determines possible corrective actions.

Supported actions depend on policy and configuration.

---

# 30. Microsoft Secure Score for Devices

Microsoft Defender for Endpoint provides device security posture information.

**Microsoft Secure Score for Devices** helps organizations assess and improve endpoint configurations.

### Example

An organization discovers that many devices lack recommended protections.

Security recommendations identify actions that could improve device security.

### Memory Trick

**Secure Score for Devices = Device security configuration posture**

---

# 31. Defender for Endpoint and Microsoft Intune

Microsoft Defender for Endpoint integrates with Microsoft Intune.

## Microsoft Intune

Primarily supports device and application management.

## Defender for Endpoint

Primarily provides endpoint protection and threat detection/response.

### Example

Defender identifies a security weakness.

Microsoft Intune may help administrators deploy an appropriate configuration or remediation action.

### Memory Trick

**Intune = Manage Devices**

**Defender for Endpoint = Protect Devices**

---

# 32. Microsoft Defender for Cloud Apps

## Big Idea

Microsoft Defender for Cloud Apps provides cloud application security.

It helps organizations discover, monitor, govern, and protect cloud applications and their data.

Defender for Cloud Apps is a:

**Cloud Access Security Broker — CASB**

### ELI5

Employees use cloud applications for communication, file sharing, storage, and collaboration.

An organization needs visibility into those services and the risks they introduce.

Defender for Cloud Apps helps identify which applications are being used and how securely they operate.

---

# 33. The Four CASB Pillars

For SC-900, remember four traditional CASB capabilities.

**Visibility**

**Compliance**

**Data Security**

**Threat Protection**

| Pillar | Meaning |
|---|---|
| Visibility | Discover cloud application usage |
| Compliance | Evaluate applications against relevant requirements |
| Data Security | Control sensitive information in cloud apps |
| Threat Protection | Detect suspicious cloud-app activity |

### Memory Trick

**CASB = See Apps, Assess Risk, Protect Data, Detect Threats**

---

# 34. Shadow IT

## Big Idea

Shadow IT refers to technology used without appropriate organizational approval or visibility.

### Example

Employees begin using an unauthorized cloud file-sharing service to exchange sensitive company documents.

The security team may not know that the service is being used.

Defender for Cloud Apps can help discover this activity.

### Memory Trick

**Shadow IT = Technology used outside approved IT oversight**

---

# 35. Cloud Discovery

Defender for Cloud Apps can use network activity and Microsoft's cloud app catalog to identify applications used by an organization.

The current module describes evaluating discovered applications against **more than 90 risk indicators**.

## Common Workflow

**Identify → Assess → Manage**

### Identify

Discover applications employees use.

### Assess

Evaluate associated risk and compliance information.

### Manage

Apply appropriate policies and governance actions.

### Memory Trick

**Discover = Find the apps**

**Assess = Evaluate their risks**

**Manage = Apply controls**

---

# 36. Sanctioned vs. Unsanctioned Applications

## Sanctioned

An application approved for organizational use.

## Unsanctioned

An application the organization identifies as unapproved or prohibited.

### Example

An organization approves one enterprise file-sharing platform.

Employees begin using a different service that does not meet organizational requirements.

Security personnel can evaluate and manage that application.

### Important Concept

Discovering an application does not automatically mean it is malicious.

The organization must evaluate whether its use is appropriate.

---

# 37. Defender for Cloud Apps Information Protection

Defender for Cloud Apps helps identify sensitive information stored in supported SaaS applications.

Possible protection actions include:

- Apply sensitivity labels
- Block downloads to unmanaged devices
- Remove unauthorized external collaborators
- Apply applicable data protection policies

Microsoft Purview integration supports classification and data loss prevention capabilities.

### Exam Distinction

**Defender for Cloud Apps = Security and control of cloud applications**

**Microsoft Purview DLP = Prevent inappropriate sharing of sensitive information**

The products can integrate.

---

# 38. SaaS Security Posture Management — SSPM

## Big Idea

SSPM evaluates the security configuration of SaaS applications.

### ELI5

A cloud application might be approved for organizational use but configured insecurely.

SSPM helps identify and correct those misconfigurations.

### Examples

- Excessive sharing permissions
- Inadequate security settings
- Unnecessary application access

### Memory Trick

**SSPM = SaaS configuration security**

---

# 39. SSPM vs. CSPM

| SSPM | CSPM |
|---|---|
| SaaS Security Posture Management | Cloud Security Posture Management |
| Cloud application configurations | Broader cloud infrastructure configurations |
| Microsoft Defender for Cloud Apps | Microsoft Defender for Cloud |
| SaaS security recommendations | Cloud resource security recommendations |

### Memory Trick

**SSPM = Security of SaaS applications**

**CSPM = Security of cloud infrastructure**

---

# 40. App-to-App Protection

Modern applications often communicate with other applications through authorized integrations.

An organization must evaluate those connections because third-party applications may receive extensive permissions.

### Example

An employee authorizes a third-party cloud application to access their Microsoft 365 data.

The application might receive permissions that exceed what is necessary.

Defender for Cloud Apps provides application governance capabilities to help identify and control this risk.

---

# 41. OAuth and Application Governance

## OAuth

**Open Authorization**

OAuth is an authorization framework that allows applications to obtain delegated or other authorized access without requiring users to share their passwords directly with those applications.

### ELI5

A third-party application requests permission to access certain information.

The user or administrator approves the requested permissions.

The application receives a token representing the authorized access.

## Security Risk

An application may request broad permissions.

If compromised, the application could misuse those permissions.

### App Governance

Defender for Cloud Apps helps organizations:

- Identify OAuth-enabled applications
- Review app permissions
- Investigate risky application activity
- Monitor credentials and app usage
- Apply appropriate governance actions

### Memory Trick

**OAuth = Delegated application authorization**

**App Governance = Control application permissions and behavior**

---

# 42. AI Agent Protection in Cloud Apps

The current Microsoft Learn module includes protection for custom AI agents.

These agents may be created using platforms such as Microsoft Copilot Studio.

Potential threats include:

- Prompt injection
- Unauthorized tool execution
- Privilege escalation
- Data exfiltration

Defender for Cloud Apps can monitor supported agents and collect activity information for investigation.

The current module also describes real-time protection against suspicious or harmful agent actions.

### Important Distinction

**Microsoft Entra Agent ID = Identity for AI agents**

**Defender for Cloud Apps = Monitor and protect supported cloud applications and agents**

---

# 43. Microsoft Defender for Identity

## Big Idea

Microsoft Defender for Identity detects and investigates identity-related threats.

It monitors supported identity signals from:

- On-premises Active Directory
- Microsoft Entra ID
- Other supported identity providers

### ELI5

An attacker who steals credentials may attempt to move through the network using someone else's identity.

Defender for Identity helps identify suspicious identity behavior.

---

# 44. Defender for Identity Sensors

Microsoft Defender for Identity uses sensors on supported on-premises identity infrastructure.

Examples include:

- Active Directory domain controllers
- Active Directory Federation Services (AD FS) servers
- Active Directory Certificate Services (AD CS) servers

The sensors analyze relevant activity and send processed security information to the cloud service.

### Memory Trick

**Identity Sensors = Monitor identity infrastructure**

---

# 45. Identity Threat Detection and Response — ITDR

Defender for Identity is an:

**Identity Threat Detection and Response (ITDR)** solution.

Its capabilities include:

- Assessing identity security posture
- Detecting identity-based threats
- Investigating suspicious activity
- Responding to compromised identities

### Memory Trick

**ITDR = Detect and respond to identity attacks**

---

# 46. Reconnaissance

Reconnaissance is an attack phase in which adversaries gather information about the target.

### Example

An attacker attempts to discover:

- Privileged accounts
- Network resources
- Domain structure
- Valuable systems

Defender for Identity can help identify suspicious reconnaissance activity.

### Memory Trick

**Reconnaissance = Find information before attacking**

---

# 47. Credential Compromise

Attackers may attempt to compromise accounts through techniques such as:

- Brute-force attempts
- Password attacks
- Credential theft
- Abuse of compromised authentication information

Defender for Identity can help detect suspicious activity associated with these techniques.

---

# 48. Lateral Movement

## Big Idea

Lateral movement occurs when an attacker moves from one compromised system or identity to other resources.

### Example

An attacker compromises an employee's computer.

They use stolen credentials to access another system.

From there, they attempt to reach privileged accounts or sensitive resources.

### Memory Trick

**Lateral Movement = Move deeper into the environment**

---

# 49. Privilege Escalation

Privilege escalation occurs when an attacker gains permissions beyond their original authorization.

### Example

A compromised standard user account obtains administrative privileges.

This allows the attacker to perform actions that were previously unavailable.

### Memory Trick

**Privilege Escalation = Gain more authority**

---

# 50. Domain Dominance

Domain dominance describes a situation where an attacker gains extensive control over an Active Directory environment.

### ELI5

An attacker does not merely control one user account.

They gain control of infrastructure or permissions that allow broad influence over the organization's identity environment.

This can represent a severe security compromise.

---

# 51. Defender for Identity Remediation

Defender for Identity supports response actions involving compromised identities.

Examples include:

- Disable a user account in Active Directory
- Require a password reset
- Initiate supported Microsoft Entra identity actions

### Important Concept

Identity remediation helps reduce an attacker's ability to continue using compromised accounts.

---

# 52. Defender for Identity vs. Entra ID Protection

This distinction is very important.

| Defender for Identity | Microsoft Entra ID Protection |
|---|---|
| Identity threat detection and response | Cloud identity risk detection |
| Monitors Active Directory and hybrid identity signals | Evaluates risky users and risky sign-ins |
| Detects lateral movement and identity attacks | Identifies suspicious authentication and compromised-account risk |
| Uses supported identity infrastructure sensors | Uses Entra risk signals |

### Scenario

**Suspicious Active Directory lateral movement = Defender for Identity**

**Risky cloud sign-in = Microsoft Entra ID Protection**

The products complement each other.

---

# 53. Microsoft Defender Vulnerability Management

## Big Idea

Defender Vulnerability Management identifies, assesses, prioritizes, and tracks security weaknesses.

It supports a risk-based approach to vulnerability remediation.

### ELI5

Imagine a security inspection discovers 200 deficiencies.

Not every deficiency presents the same risk.

Some are minor.

Others could allow attackers to compromise critical systems.

Vulnerability Management helps security and IT teams determine what needs attention first.

---

# 54. The Three Vulnerability Management Capabilities

Microsoft identifies three core capabilities.

**Continuous Asset Discovery**

**Risk-Based Prioritization**

**Remediation and Tracking**

### Memory Trick

**Find → Prioritize → Fix**

---

# 55. Continuous Asset Discovery

An organization cannot protect devices it does not know exist.

Defender Vulnerability Management provides visibility into supported assets and their security state.

The current module describes inventories involving:

- Software applications
- Hardware
- Firmware
- Digital certificates
- Browser extensions
- Network devices

### ELI5

Before conducting an equipment inspection, the organization needs an accurate inventory.

Security vulnerability management works the same way.

---

# 56. Security Baselines

A security baseline defines recommended security configuration settings.

Defender Vulnerability Management supports comparisons against security benchmarks such as:

- Center for Internet Security (CIS) benchmarks
- Security Technical Implementation Guides (STIGs)

## STIG

**Security Technical Implementation Guide**

STIGs provide security configuration guidance widely used in U.S. Department of Defense environments.

### Example

A Windows device does not meet a required security setting.

A baseline assessment identifies the configuration deficiency.

### GRC Connection

Baselines help establish consistent, assessable configuration expectations.

---

# 57. CVE vs. CVSS

## CVE

**Common Vulnerabilities and Exposures**

A standardized identifier for a publicly disclosed vulnerability.

Example format:

```text
CVE-2026-12345
```

This is an illustrative identifier.

## CVSS

**Common Vulnerability Scoring System**

A framework for assessing vulnerability severity.

### Important Distinction

**CVE = Which vulnerability?**

**CVSS = How severe is the vulnerability according to the scoring framework?**

---

# 58. Risk-Based Vulnerability Prioritization

A vulnerability's severity is important, but severity alone does not determine organizational risk.

Defender Vulnerability Management considers factors such as:

- Known exploitation activity
- Threat intelligence
- Business importance
- Device exposure
- Likelihood of compromise
- Impact on critical assets

### Example

Two devices contain the same vulnerability.

One is an isolated test computer.

The other is a critical server exposed to the internet.

The critical server may require faster remediation.

### Memory Trick

**Risk = More than CVSS severity**

---

# 59. Remediation and Tracking

Defender Vulnerability Management helps coordinate remediation with IT teams.

Capabilities include:

- Security recommendations
- Remediation requests
- Microsoft Intune integration
- Status tracking
- Alternative mitigations
- Blocking vulnerable applications where supported

### Example

A security analyst identifies outdated software.

They create a remediation request for the IT team.

The team updates or mitigates the software.

The remediation status is tracked.

### GRC Connection

This resembles formal corrective action and vulnerability remediation tracking.

---

# 60. Device Exposure Score

Microsoft Defender Vulnerability Management provides an exposure score reflecting how exposed devices are to threats and vulnerabilities.

**Lower device exposure score = Lower measured exposure**

Do not confuse this with Microsoft Secure Score.

### Important Distinction

**Exposure Score = How exposed are the devices?**

**Secure Score = How well have security recommendations been implemented?**

---

# 61. Microsoft Defender Threat Intelligence

## Important Current Product Change

Microsoft Learn identifies **August 1, 2026**, as the retirement date for the standalone Microsoft Defender Threat Intelligence product.

Its capabilities are being integrated into Microsoft Defender XDR and Microsoft Sentinel.

These threat intelligence capabilities remain relevant even though the standalone product is no longer the focus of the current experience.

## Big Idea

Threat intelligence provides information about:

- Threat actors
- Malicious infrastructure
- Attack methods
- Vulnerabilities
- Indicators of compromise

### ELI5

Instead of investigating an unknown malicious IP address without context, an analyst can use threat intelligence to determine what is known about it.

---

# 62. Threat Analytics

Threat analytics helps organizations understand relevant current and emerging threats.

The Microsoft Learn module identifies three report categories.

## Latest Threats

Recently published or updated threat information.

## High-Impact Threats

Threats associated with significant activity affecting the organization.

## Highest Exposure

Threats for which organizational resources may be especially exposed.

### Memory Trick

**Latest = New**

**High-Impact = Significant activity**

**Highest Exposure = Vulnerability and organizational risk**

---

# 63. Intel Profiles

Intel profiles provide curated information about:

- Threat actors
- Malicious tools
- Vulnerabilities

### Example

An analyst investigates a known ransomware group.

An intelligence profile provides relevant information about the group's tools, tactics, and activity.

---

# 64. Intel Explorer

Intel Explorer supports searches involving:

- Keywords
- Indicators
- CVE identifiers
- Threat actors
- Malicious infrastructure

### Memory Trick

**Intel Explorer = Search threat intelligence**

---

# 65. Threat Intelligence Projects

Projects help analysts organize threat indicators and investigation artifacts.

### Example

An analyst investigates a phishing campaign.

They create a project containing:

- Suspicious domains
- Malicious IP addresses
- Related indicators
- Investigation notes
- Relevant collaborators

### Memory Trick

**Threat Intelligence Project = Organized intelligence investigation**

---

# 66. Threat Intelligence vs. Threat Hunting

These concepts are related but different.

## Threat Intelligence

Provides information about threats.

## Threat Hunting

Proactively searches the environment for signs of threats.

### Example

Threat intelligence identifies a malicious domain.

A threat hunter searches organizational logs for evidence of communication with that domain.

### Memory Trick

**Threat Intelligence = Know the adversary**

**Threat Hunting = Search for the adversary**

---

# 67. Microsoft Security Exposure Management

## Big Idea

Microsoft Security Exposure Management provides a unified view of an organization's attack surface and exposure risks.

It combines security context from multiple systems.

Sources include:

- Defender for Endpoint
- Defender for Cloud
- Defender for Identity
- Microsoft Entra ID
- Supported third-party security tools

### ELI5

An organization may have thousands of security weaknesses scattered across different systems.

Exposure Management helps determine which weaknesses combine into dangerous attack paths.

---

# 68. What Is an Attack Surface?

An attack surface is the collection of entry points, assets, and pathways an attacker could potentially exploit.

Examples include:

- Devices
- User identities
- Applications
- Cloud resources
- External-facing systems
- Excessive permissions

### Memory Trick

**Attack Surface = All the places an attacker might exploit**

---

# 69. Enterprise Exposure Graph

The enterprise exposure graph represents relationships among assets, identities, and security weaknesses.

### Example

```text
Internet-Facing Application
          |
          v
Vulnerable Server
          |
          v
Overprivileged Identity
          |
          v
Sensitive Database
```

The graph helps identify how separate weaknesses might connect.

### Memory Trick

**Exposure Graph = Map relationships among risks**

---

# 70. Attack Surface Map

The attack surface map visually represents relationships in the enterprise exposure graph.

Security teams can inspect connected assets and potential exposures.

### ELI5

Instead of reading separate security reports, analysts can view relationships among systems.

### Important Distinction

**Enterprise Exposure Graph = Relationship data**

**Attack Surface Map = Visual representation**

---

# 71. Attack Paths

An attack path represents a possible sequence of weaknesses an attacker could exploit to reach an important target.

### Example

An attacker gains access to an exposed server.

They exploit a vulnerability.

They obtain a privileged identity.

They access a sensitive database.

The connected weaknesses form an attack path.

### Memory Trick

**Attack Path = How the attacker could reach the target**

---

# 72. Choke Points

## Big Idea

A choke point is a location in the attack graph where multiple possible attack paths converge.

### ELI5

Imagine several roads leading into one narrow bridge.

Securing that bridge can prevent movement along multiple routes.

A choke point in Exposure Management works similarly.

### Security Benefit

Correcting one high-impact weakness may disrupt several attack paths.

### Memory Trick

**Choke Point = One fix can block multiple attack routes**

---

# 73. Critical Asset Management

Not every asset is equally important.

Examples of critical assets include:

- Domain controllers
- Privileged accounts
- Sensitive databases
- Critical cloud resources
- Important file servers

Exposure Management helps organizations identify and prioritize these assets.

### Example

A vulnerability affecting a domain controller may have greater organizational consequences than the same vulnerability affecting a low-value test system.

### Memory Trick

**Critical Asset = High-impact target**

---

# 74. Exposure Insights and Initiatives

Exposure Management groups related metrics and recommendations into security initiatives.

The module identifies several initiative types.

## Workload Initiatives

Focus on a particular workload or security domain.

Examples:

- Endpoint security
- Identity security
- Cloud security

## Horizontal Threat Initiatives

Focus on a broader threat category.

Examples:

- Ransomware
- Business email compromise

## Threat Analytics Initiatives

Use current threat research to evaluate relevant risks.

## Zero Trust Initiative

Evaluates exposure related to Zero Trust security practices.

---

# 75. Exposure Metrics and Recommendations

Initiatives contain metrics used to assess exposure.

Metrics are connected to security recommendations.

As the organization implements appropriate recommendations, initiative scores can improve.

### ELI5

An initiative represents a security improvement objective.

Metrics measure different parts of that objective.

Recommendations identify possible corrective actions.

### Memory Trick

**Initiative = Security objective**

**Metric = Measurement**

**Recommendation = Corrective action**

---

# 76. Microsoft Secure Score

Microsoft Secure Score evaluates progress toward recommended security actions across supported Microsoft security products.

The current module describes coverage involving:

- Identities
- Devices
- SaaS applications
- Data
- Other supported security controls

### Important Concept

A higher Secure Score generally reflects greater implementation of evaluated recommended actions.

It is not a guarantee that an environment is secure.

---

# 77. Secure Scores Compared

| Score | Meaning |
|---|---|
| Microsoft Secure Score | Overall Microsoft security posture |
| Cloud Secure Score | Cloud resource security posture |
| Microsoft Secure Score for Devices | Device security configuration posture |
| Device Exposure Score | Measured device vulnerability/exposure risk |
| Microsoft Purview Compliance Score | Progress on compliance improvement actions |

### Memory Trick

**Secure Score = Security control implementation**

**Exposure Score = Risk exposure**

**Compliance Score = Compliance improvement progress**

Always identify which product and type of score the question describes.

---

# 78. Defender Vulnerability Management vs. Exposure Management

These products are closely related.

## Defender Vulnerability Management

Focuses primarily on individual vulnerabilities and misconfigurations involving devices, software, and related assets.

## Security Exposure Management

Evaluates broader exposure relationships across identities, endpoints, cloud resources, and other systems.

| Vulnerability Management | Exposure Management |
|---|---|
| Individual weaknesses | Enterprise-wide exposure |
| CVEs and software vulnerabilities | Attack paths and critical assets |
| Device vulnerability assessment | Cross-domain risk relationships |
| Prioritized remediation | Strategic risk prioritization |

### Memory Trick

**Vulnerability Management = What is vulnerable?**

**Exposure Management = How could weaknesses combine to cause harm?**

---

# 79. Microsoft Defender Portal

## Big Idea

The Microsoft Defender portal provides a unified security operations interface.

The portal brings together capabilities from:

- Defender XDR
- Microsoft Sentinel
- Defender for Cloud
- Microsoft Security Copilot
- Related Microsoft security services

Official portal:

https://security.microsoft.com

### ELI5

Instead of opening several separate consoles, security analysts can use one central environment for many security tasks.

---

# 80. Portal Permissions

Access to the Microsoft Defender portal is controlled through appropriate roles.

Examples include:

- Security Reader
- Security Operator
- Security Administrator
- Global Reader
- Global Administrator

### Important Concept

**Portal access does not automatically mean unrestricted access to every underlying security product.**

Appropriate authorization still applies.

This reinforces:

**Zero Trust — Least Privilege**

---

# 81. Microsoft Defender Portal Navigation

The current module describes several major areas.

| Portal area | Primary purpose |
|---|---|
| Investigation & response | Incidents, alerts, hunting, actions |
| Exposure management | Vulnerabilities, attack surface, recommendations |
| Threat intelligence | Threat actors, indicators, vulnerabilities |
| Assets | Devices, identities, applications, cloud resources |
| Identities | Defender for Identity |
| Endpoints | Defender for Endpoint |
| Email & collaboration | Defender for Office 365 |
| Cloud apps | Defender for Cloud Apps |
| Cloud security | Defender for Cloud |
| Microsoft Sentinel | SIEM/SOAR capabilities |
| Security Copilot | AI assistance and agents |
| Reports | Security reporting |
| System | Permissions, settings, service health |

Portal layouts and available options depend on permissions, licensing, and product configuration.

---

# 82. Unified Incidents and Alerts

The Defender portal provides a combined view of related security incidents.

An incident can contain:

- Alerts
- Affected users
- Affected devices
- Affected applications
- Investigation evidence
- Automated response actions
- Analyst comments and decisions

### Memory Trick

**Unified Incident Queue = One place to investigate related threats**

---

# 83. Advanced Hunting in the Defender Portal

Advanced hunting allows analysts to query available security data.

Supported approaches include:

- Kusto Query Language
- Query builders
- Security Copilot-generated queries

The module describes the ability to use queries to create custom detection rules.

### Important Distinction

**Hunting Query = Investigate security information**

**Custom Detection Rule = Automatically identify defined suspicious behavior**

---

# 84. Unified Action Center

The Action Center displays pending and completed remediation actions across supported Defender products.

### Examples

- Device-related remediation
- Email-related actions
- Identity-related actions

### ELI5

The Action Center is the central place to review supported security actions that have been performed or await action.

---

# 85. Assets Inventory

The Defender portal provides inventory information involving:

- Devices
- Identities
- Applications
- Cloud resources
- AI agents

This helps analysts understand which assets exist and how they relate to incidents.

### GRC Connection

Accurate asset inventories support risk assessments, vulnerability management, and control evaluations.

---

# 86. SOC Optimization

Microsoft Defender includes capabilities for identifying opportunities to improve security operations.

### Examples

- Improve detection coverage
- Evaluate security control effectiveness
- Prioritize operational improvements

### Memory Trick

**SOC Optimization = Improve security operations over time**

---

# 87. Microsoft Security Copilot Integration

## Big Idea

Microsoft Defender XDR integrates with Microsoft Security Copilot to help security professionals analyze and investigate threats.

Microsoft describes two experiences:

**Standalone**

**Embedded**

---

# 88. Standalone Security Copilot

The standalone experience uses the dedicated Security Copilot interface.

The current module identifies two relevant plugins:

- Microsoft Defender XDR
- Natural Language to KQL for Microsoft Defender XDR

The plugins provide supported investigation capabilities.

### Example

An analyst asks Security Copilot:

> Summarize the highest-severity incidents affecting our endpoints during the last 24 hours.

The answer depends on available data and permissions.

---

# 89. Embedded Security Copilot

The embedded experience provides Security Copilot capabilities directly inside the Microsoft Defender portal.

The module identifies capabilities including:

- Incident summarization
- Guided responses
- Script analysis
- Natural-language KQL generation
- Incident reports
- File analysis
- Device summaries
- Identity summaries

### Memory Trick

**Standalone = Open Security Copilot**

**Embedded = Copilot inside Defender XDR**

---

# 90. Incident Summarization

Security Copilot can summarize an incident and explain:

- What happened
- Which assets were involved
- The apparent attack timeline
- Significant evidence
- Relevant investigation context

The current module describes incident summarization for incidents containing up to **100 alerts**.

### ELI5

Instead of reviewing dozens of security alerts individually before understanding the situation, an analyst receives an organized overview.

---

# 91. Guided Responses

Security Copilot provides guided response recommendations.

The module identifies four categories.

**Triage**

**Containment**

**Investigation**

**Remediation**

## Triage

Determine what type of incident occurred and whether it represents a true positive or false positive.

## Containment

Limit the attacker's ability to continue.

## Investigation

Gather evidence and determine the scope.

## Remediation

Correct the problem and remove the threat where possible.

### Memory Trick

**Triage → Contain → Investigate → Remediate**

---

# 92. Script and File Analysis

Security Copilot can help analysts understand suspicious scripts and files.

Examples include:

- PowerShell scripts
- Command-line activity
- Malicious files
- Suspicious executable behavior

### Important Principle

AI-generated analysis should be validated against the available evidence.

Copilot supports security professionals; it does not replace professional judgment.

---

# 93. Natural Language to KQL

Security Copilot can convert natural-language investigation requests into KQL queries.

### Example

```text
Find devices that executed suspicious PowerShell
commands during the past 24 hours.
```

Copilot can generate a query suitable for review and use in a supported hunting environment.

### Memory Trick

**Natural Language to KQL = Describe the search, generate the query**

---

# 94. Incident Reports

Security Copilot can generate structured incident reports.

These may consolidate:

- Investigation findings
- Affected entities
- Response actions
- Analyst notes
- Incident timelines
- Related security evidence

### GRC Connection

Incident documentation helps organizations demonstrate that identified security events were investigated and handled.

However, original records and authoritative evidence should be preserved.

---

# 95. AI Agents in Microsoft Defender XDR

The current Microsoft Learn module describes autonomous AI agents supporting security operations.

Examples include:

- Phishing Triage Agent
- Threat Intelligence Briefing Agent
- Threat Hunting Assistant
- Dynamic Threat Detection Agent

These agents extend Security Copilot from direct question-and-answer assistance toward supported autonomous workflows.

---

# 96. Phishing Triage Agent

## Big Idea

Automatically evaluates user-reported phishing messages.

The agent can:

- Review submitted messages
- Classify suspicious activity
- Distinguish likely phishing from false positives
- Provide explanations
- Incorporate analyst feedback

The module identifies requirements including Defender for Office 365 Plan 2 and Security Copilot.

### Memory Trick

**Phishing Triage Agent = Evaluate reported phishing emails**

---

# 97. Threat Intelligence Briefing Agent

## Big Idea

Generates customized threat intelligence briefings.

The agent can summarize relevant threat information for security teams.

### Example

A security team receives a briefing about emerging threats relevant to its environment.

### Memory Trick

**Threat Intelligence Briefing Agent = Summarize relevant emerging threats**

---

# 98. Threat Hunting Assistant

## Big Idea

Assists analysts with proactive threat hunting.

The agent can:

- Interpret natural-language requests
- Generate KQL
- Analyze query results
- Provide investigation context
- Support follow-up questions

### Memory Trick

**Threat Hunting Assistant = Help investigate suspicious activity proactively**

---

# 99. Dynamic Threat Detection Agent

## Big Idea

Helps identify threats that traditional detection rules may miss.

It correlates:

- Alerts
- Events
- Anomalies
- Threat intelligence

The agent can generate contextual alerts when it identifies suspicious behavior.

### Memory Trick

**Dynamic Threat Detection Agent = Find hidden threats**

---

# 100. Defender XDR vs. Sentinel vs. Defender for Cloud

This distinction is essential.

## Microsoft Defender XDR

Unified threat detection and response across endpoints, identities, email, and applications.

## Microsoft Sentinel

Broad SIEM/SOAR platform that collects and correlates security data from Microsoft and non-Microsoft sources.

## Microsoft Defender for Cloud

Cloud security posture management and workload threat protection.

| Product | Primary purpose |
|---|---|
| Defender XDR | Cross-domain threat detection and response |
| Sentinel | SIEM, SOAR, broad security monitoring |
| Defender for Cloud | Cloud posture and workload protection |
| Security Copilot | AI-assisted security analysis |

### Memory Trick

**XDR = Correlate and respond across Defender domains**

**Sentinel = Collect and analyze broad security data**

**Defender for Cloud = Assess and protect cloud workloads**

**Security Copilot = AI assistance**

---

# 101. Complete Attack Scenario

Imagine an attacker targets an organization's employees.

## Stage 1 — Phishing

The attacker sends a malicious email.

**Defender for Office 365** detects suspicious email content.

## Stage 2 — Credential Compromise

The attacker steals credentials.

**Microsoft Entra ID Protection** may detect risky cloud authentication.

**Defender for Identity** may detect suspicious identity activity involving the hybrid identity environment.

## Stage 3 — Endpoint Compromise

The attacker executes malicious activity on a device.

**Defender for Endpoint** detects suspicious endpoint behavior.

## Stage 4 — Lateral Movement

The attacker attempts to access additional systems.

**Defender for Identity** identifies suspicious identity-related activity.

## Stage 5 — Cloud Application Access

The attacker attempts to misuse cloud applications.

**Defender for Cloud Apps** detects suspicious SaaS activity.

## Stage 6 — Unified Investigation

**Microsoft Defender XDR** correlates relevant alerts into one incident.

## Stage 7 — Automated Response

Defender XDR may use supported automated response and attack disruption capabilities.

## Stage 8 — Expanded Security Analysis

**Microsoft Sentinel** can correlate additional network, cloud, and third-party security data.

## Stage 9 — AI Assistance

**Microsoft Security Copilot** summarizes the incident and helps analysts identify appropriate investigation and response steps.

### Complete Flow

```text
Phishing Email
      |
      v
Defender for Office 365
      |
      v
Credential Compromise
      |
      v
Entra ID Protection / Defender for Identity
      |
      v
Endpoint Compromise
      |
      v
Defender for Endpoint
      |
      v
Lateral Movement
      |
      v
Defender for Identity
      |
      v
Cloud Application Abuse
      |
      v
Defender for Cloud Apps
      |
      v
Microsoft Defender XDR
      |
      v
Unified Incident and Response
      |
      +--> Microsoft Sentinel
      |    Broad security data correlation
      |
      +--> Microsoft Security Copilot
           AI-assisted investigation
```

**This is a conceptual attack scenario showing product responsibilities, not a required deployment architecture.**

---

# 102. GRC / ISSO Career Connection

The following section provides additional professional context and is not a separate Microsoft Learn instructional unit.

Microsoft Defender XDR is relevant to Information System Security Officer, Risk Management Framework, and Governance, Risk, and Compliance responsibilities.

An ISSO may need to determine whether an organization has appropriate protections for:

- Endpoints
- Identities
- Email
- Applications
- Vulnerabilities
- Security monitoring
- Incident response

Defender XDR can provide technical evidence related to these responsibilities.

---

# 103. NIST SP 800-53 Relationships

The mappings below are illustrative, not automatic compliance claims.

| Defender capability | Related NIST control |
|---|---|
| Defender for Endpoint | SI-3 — Malicious Code Protection |
| Endpoint detection and response | SI-4 — System Monitoring |
| Defender for Identity | AC-2 — Account Management |
| Identity monitoring | SI-4 — System Monitoring |
| Defender Vulnerability Management | RA-5 — Vulnerability Monitoring and Scanning |
| Security baseline assessment | CM-6 — Configuration Settings |
| Security event analysis | AU-6 — Audit Record Review, Analysis, and Reporting |
| Automated incident response | IR-4 — Incident Handling |
| Continuous security monitoring | CA-7 — Continuous Monitoring |
| Attack surface reduction | CM-7 — Least Functionality |

### Important Principle

Implementing Microsoft Defender does not automatically satisfy a NIST security control.

The organization must demonstrate appropriate implementation and operating effectiveness.

---

# 104. Vulnerability Management and POA&M

## POA&M

**Plan of Action and Milestones**

A POA&M tracks identified security weaknesses and planned corrective actions.

Defender Vulnerability Management can help identify technical findings relevant to remediation tracking.

### Example

```text
Finding:
Outdated software on a critical workstation

Risk:
Known vulnerability could enable compromise

Recommended Action:
Update or mitigate the affected software

Assigned Owner:
Endpoint Management Team

Target Completion:
December 15

Status:
In Progress
```

### GRC Perspective

A technical recommendation is not automatically a completed remediation.

A formal process may still require:

- Risk evaluation
- Assignment of responsibility
- Target completion date
- Corrective action
- Validation
- Closure documentation

---

# 105. Security Control Assessment

An ISSO may evaluate whether endpoint security controls operate effectively.

### Example Assessment Questions

Does the organization have visibility into managed endpoints?

Are security alerts generated appropriately?

Are high-risk vulnerabilities identified and tracked?

Are phishing-related incidents investigated?

Are privileged identity threats monitored?

Are automated remediation actions reviewed?

Are security events retained as required?

### GRC Lesson

**Security product deployment is only part of control implementation.**

The organization must also demonstrate that processes, configurations, monitoring, and corrective actions are effective.

---

# 106. Incident Response Evidence

Defender XDR can generate information relevant to incident investigations.

Examples include:

- Security alerts
- Incident timelines
- Affected identities
- Device evidence
- Response actions
- Investigation notes
- Automated remediation records

### Important Considerations

An assessor should evaluate:

- Whether relevant evidence was collected
- Whether the incident was classified correctly
- Whether containment occurred
- Whether required notifications were made
- Whether remediation was validated
- Whether documentation is complete

---

# 107. Security Monitoring vs. Governance

## Security Operations

Primarily focuses on detecting and responding to threats.

## Governance and Compliance

Primarily focuses on ensuring that security requirements are defined, implemented, monitored, and assessed.

### Example

A SOC analyst investigates a compromised workstation.

An ISSO may later verify that the incident-response process operated as required and that identified weaknesses were documented and addressed.

### Memory Trick

**SOC = Operate security controls**

**ISSO/GRC = Evaluate security requirements, risks, and control effectiveness**

The functions overlap and support each other.

---

# 108. SC-900 High-Value Product Recognition

| Scenario | Correct solution |
|---|---|
| Protect email and collaboration | Defender for Office 365 |
| Malicious URL | Safe Links |
| Suspicious email attachment | Safe Attachments |
| Remove malicious email after delivery | ZAP |
| Simulated phishing training | Attack Simulation Training |
| Investigate coordinated phishing | Campaigns |
| Track email delivery | Message Trace |
| Endpoint protection | Defender for Endpoint |
| Detect active endpoint threats | EDR |
| Reduce endpoint attack surface | ASR |
| Improve device configuration security | Secure Score for Devices |
| Discover unauthorized SaaS apps | Defender for Cloud Apps |
| SaaS misconfiguration | SSPM |
| Investigate risky OAuth applications | App Governance |
| Detect AD identity attacks | Defender for Identity |
| Detect lateral movement | Defender for Identity |
| Detect risky cloud sign-ins | Entra ID Protection |
| Identify vulnerable software | Defender Vulnerability Management |
| Compare device configuration to STIGs | Baseline Assessment |
| Track CVEs | Vulnerability Management |
| Information about threat actors | Threat Intelligence |
| Investigate malicious domains | Intel Explorer |
| Understand enterprise attack surface | Security Exposure Management |
| Analyze relationships among assets | Enterprise Exposure Graph |
| Identify multiple attack paths converging | Choke Point |
| Prioritize high-impact assets | Critical Asset Management |
| Unified cross-domain incidents | Defender XDR |
| Centralized Defender security interface | Microsoft Defender Portal |
| AI-generated incident summary | Security Copilot |
| AI triage of reported phishing | Phishing Triage Agent |
| AI threat intelligence briefings | Threat Intelligence Briefing Agent |
| AI-assisted KQL hunting | Threat Hunting Assistant |
| AI detection of hidden threats | Dynamic Threat Detection Agent |

---

# 109. Final Module 5 Cram Sheet

```text
MICROSOFT DEFENDER XDR
= EXTENDED DETECTION AND RESPONSE

XDR
= UNIFIED CROSS-DOMAIN THREAT PROTECTION

FOUR MAJOR SECURITY DOMAINS
= ENDPOINTS + IDENTITIES + EMAIL + APPLICATIONS

PRE-BREACH
= PREVENT COMPROMISE

POST-BREACH
= DETECT + INVESTIGATE + RESPOND

COMBINED INCIDENT QUEUE
= CORRELATE RELATED ALERTS

AUTOMATIC ATTACK DISRUPTION
= CONTAIN ACTIVE ATTACKS

DEFENDER FOR OFFICE 365
= EMAIL AND COLLABORATION SECURITY

SAFE LINKS
= MALICIOUS URL PROTECTION

SAFE ATTACHMENTS
= MALICIOUS ATTACHMENT PROTECTION

DETONATION
= TEST SUSPICIOUS FILE IN ISOLATION

ZAP
= ZERO-HOUR AUTO PURGE

AIR
= AUTOMATED INVESTIGATION AND RESPONSE

DEFENDER FOR ENDPOINT
= ENDPOINT SECURITY

ASR
= ATTACK SURFACE REDUCTION

EDR
= ENDPOINT DETECTION AND RESPONSE

INTUNE
= DEVICE AND APPLICATION MANAGEMENT

DEFENDER FOR CLOUD APPS
= CASB / SAAS PROTECTION

CASB
= CLOUD ACCESS SECURITY BROKER

CASB PILLARS
= VISIBILITY + COMPLIANCE + DATA SECURITY
  + THREAT PROTECTION

SHADOW IT
= UNAPPROVED OR UNMANAGED TECHNOLOGY

SSPM
= SAAS SECURITY POSTURE MANAGEMENT

APP GOVERNANCE
= OAUTH APPLICATION RISK MANAGEMENT

DEFENDER FOR IDENTITY
= IDENTITY THREAT DETECTION AND RESPONSE

ITDR
= IDENTITY THREAT DETECTION AND RESPONSE

LATERAL MOVEMENT
= MOVE THROUGH COMPROMISED ENVIRONMENT

PRIVILEGE ESCALATION
= GAIN ADDITIONAL AUTHORITY

DOMAIN DOMINANCE
= BROAD CONTROL OF ACTIVE DIRECTORY

ENTRA ID PROTECTION
= RISKY CLOUD USERS AND SIGN-INS

VULNERABILITY MANAGEMENT
= DISCOVER + PRIORITIZE + REMEDIATE

CVE
= VULNERABILITY IDENTIFIER

CVSS
= VULNERABILITY SEVERITY SCORING

STIG
= SECURITY TECHNICAL IMPLEMENTATION GUIDE

DEVICE EXPOSURE SCORE
= MEASURE DEVICE EXPOSURE RISK

THREAT INTELLIGENCE
= INFORMATION ABOUT ADVERSARIES

THREAT ANALYTICS
= UNDERSTAND RELEVANT THREATS

INTEL PROFILES
= THREAT ACTORS / TOOLS / VULNERABILITIES

INTEL EXPLORER
= SEARCH THREAT INTELLIGENCE

SECURITY EXPOSURE MANAGEMENT
= ENTERPRISE-WIDE ATTACK SURFACE RISK

ENTERPRISE EXPOSURE GRAPH
= RELATIONSHIPS AMONG ASSETS AND WEAKNESSES

ATTACK PATH
= ROUTE AN ATTACKER COULD EXPLOIT

CHOKE POINT
= SHARED WEAKNESS IN MULTIPLE ATTACK PATHS

CRITICAL ASSET
= HIGH-IMPACT SECURITY TARGET

MICROSOFT SECURE SCORE
= OVERALL SECURITY POSTURE

CLOUD SECURE SCORE
= CLOUD RESOURCE SECURITY POSTURE

SECURE SCORE FOR DEVICES
= ENDPOINT SECURITY CONFIGURATION

MICROSOFT DEFENDER PORTAL
= UNIFIED SECURITY OPERATIONS

ADVANCED HUNTING
= SEARCH SECURITY DATA WITH KQL

ACTION CENTER
= TRACK SUPPORTED REMEDIATION ACTIONS

SECURITY COPILOT
= AI-ASSISTED SECURITY INVESTIGATION

PHISHING TRIAGE AGENT
= CLASSIFY USER-REPORTED PHISHING

THREAT INTELLIGENCE BRIEFING AGENT
= GENERATE THREAT BRIEFINGS

THREAT HUNTING ASSISTANT
= AI-ASSISTED THREAT HUNTING

DYNAMIC THREAT DETECTION AGENT
= FIND THREATS MISSED BY TRADITIONAL RULES

DEFENDER XDR
= UNIFIED THREAT DETECTION AND RESPONSE

MICROSOFT SENTINEL
= SIEM + SOAR

DEFENDER FOR CLOUD
= CLOUD POSTURE + WORKLOAD PROTECTION

MICROSOFT PURVIEW
= DATA SECURITY + GOVERNANCE + COMPLIANCE
```

---

# 110. Final Mental Model

Imagine an attacker sends a phishing email to an employee.

**Microsoft Defender for Office 365** attempts to detect and block the malicious message.

The attacker steals the employee's credentials.

**Microsoft Entra ID Protection** detects suspicious cloud authentication activity.

**Microsoft Defender for Identity** identifies potentially malicious behavior involving identity infrastructure.

The attacker compromises a workstation.

**Microsoft Defender for Endpoint** detects suspicious activity on the device.

The attacker accesses an unauthorized SaaS application.

**Microsoft Defender for Cloud Apps** identifies potentially risky cloud-app behavior.

**Microsoft Defender XDR** correlates related alerts across these products.

The analyst investigates a single incident containing the available evidence.

**Microsoft Security Exposure Management** helps identify weaknesses and attack paths that could increase the impact of the compromise.

**Defender Vulnerability Management** identifies relevant software weaknesses and supports remediation tracking.

**Microsoft Sentinel** provides broader security monitoring and correlation across additional Microsoft and third-party data sources.

**Microsoft Security Copilot** assists with investigating the attack, understanding evidence, generating queries, and preparing reports.

Together, these products support:

**Prevention**

**Detection**

**Investigation**

**Response**

and

**Continuous Security Improvement**

The central concept is:

**Microsoft Defender XDR connects multiple security domains to detect and respond to attacks that individual security products might otherwise see only in fragments.**

---

# Official Microsoft Learn References

These instructional pages were checked against the live module on November 23, 2026.

[Module Overview](https://learn.microsoft.com/en-us/training/modules/describe-threat-protection-with-microsoft-365-defender/)

[Introduction](https://learn.microsoft.com/en-us/training/modules/describe-threat-protection-with-microsoft-365-defender/1-introduction)

[Describe Microsoft Defender XDR Services](https://learn.microsoft.com/en-us/training/modules/describe-threat-protection-with-microsoft-365-defender/2-describe-services)

[Describe Microsoft Defender for Office 365](https://learn.microsoft.com/en-us/training/modules/describe-threat-protection-with-microsoft-365-defender/3-describe-defender-office)

[Describe Microsoft Defender for Endpoint](https://learn.microsoft.com/en-us/training/modules/describe-threat-protection-with-microsoft-365-defender/4-describe-defender-endpoint)

[Describe Microsoft Defender for Cloud Apps](https://learn.microsoft.com/en-us/training/modules/describe-threat-protection-with-microsoft-365-defender/5-describe-microsoft-cloud-app-security)

[Describe Microsoft Defender for Identity](https://learn.microsoft.com/en-us/training/modules/describe-threat-protection-with-microsoft-365-defender/6-describe-defender-identity)

[Describe Microsoft Defender Vulnerability Management](https://learn.microsoft.com/en-us/training/modules/describe-threat-protection-with-microsoft-365-defender/6a-describe-defender-vulnerability-management)

[Describe Microsoft Defender Threat Intelligence](https://learn.microsoft.com/en-us/training/modules/describe-threat-protection-with-microsoft-365-defender/6b-describe-defender-threat-intelligence)

[Describe Microsoft Security Exposure Management](https://learn.microsoft.com/en-us/training/modules/describe-threat-protection-with-microsoft-365-defender/6c-describe-security-exposure-management)

[Describe the Microsoft Defender Portal](https://learn.microsoft.com/en-us/training/modules/describe-threat-protection-with-microsoft-365-defender/7-describe-microsoft-defender-portal)

[Describe Copilot Integration with Microsoft Defender XDR](https://learn.microsoft.com/en-us/training/modules/describe-threat-protection-with-microsoft-365-defender/7a-describe-copilot-in-defender-xdr)
