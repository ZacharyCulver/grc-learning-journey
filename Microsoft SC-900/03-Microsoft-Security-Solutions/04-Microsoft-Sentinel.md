# SC-900 — Section 3, Module 4
# Describe Security Capabilities of Microsoft Sentinel

> **Source:** Microsoft Learn — SC-900  
> **Learning Path:** Introduction to Microsoft security solutions  
> **Module:** Describe security capabilities of Microsoft Sentinel  
> **Verified against current Microsoft Learn content:** November 23, 2026  
> **Duration:** 14 minutes | 6 units | 1,400 XP  
> **Official Module:** https://learn.microsoft.com/en-us/training/modules/describe-security-capabilities-of-azure-sentinel/

---

# Module Overview

Microsoft Sentinel is a cloud-native:

**Security Information and Event Management (SIEM)**

and

**Security Orchestration, Automation, and Response (SOAR)**

solution.

It provides centralized security monitoring, threat detection, investigation, threat hunting, and automated response.

Microsoft Sentinel collects security information from Microsoft products, third-party systems, cloud platforms, and on-premises infrastructure.

Modern Sentinel also includes AI-powered detection, a security data lake, graph-based analysis, and integrations with Microsoft Security Copilot.

## The Big Idea

Organizations generate enormous amounts of security data.

Examples include:

- User sign-in events
- Firewall activity
- Endpoint security alerts
- Application logs
- Cloud resource activity
- Identity risk detections
- Network traffic records

An individual event might seem harmless.

However, several related events could indicate a serious attack.

Microsoft Sentinel helps security teams **connect those events, detect suspicious behavior, investigate threats, and respond efficiently**.

### ELI5

Imagine a military installation with thousands of security cameras, access-control systems, alarms, and activity records.

Each system generates information independently.

An intruder might trigger several minor warnings that appear unrelated.

A centralized security operations system can combine those warnings into one incident.

It can then notify security personnel and initiate appropriate response procedures.

**Microsoft Sentinel provides similar capabilities for digital environments.**

---

# 1. The Two Foundational Technologies

| Technology | Primary purpose |
|---|---|
| SIEM | Collect, analyze, correlate, and monitor security events |
| SOAR | Coordinate and automate incident-response actions |

### Memory Trick

**SIEM = SEE THE THREAT**

**SOAR = RESPOND TO THE THREAT**

Microsoft Sentinel combines both capabilities.

---

# 2. Security Information and Event Management — SIEM

## Big Idea

A SIEM collects and analyzes security information from multiple sources.

Its purpose is to help organizations identify suspicious activity and potential security incidents.

## What Does a SIEM Do?

A SIEM provides:

**Log Aggregation**

**Event Correlation**

**Threat Detection**

**Alert Generation**

**Incident Management**

**Centralized Visibility**

### ELI5

Imagine reviewing thousands of security reports from different installations.

One report describes an unusual visitor.

Another identifies a vehicle entering a restricted area.

A third identifies unauthorized equipment access.

Individually, these might appear unrelated.

A SIEM can correlate them and reveal a larger security problem.

---

# 3. Log Aggregation

## Big Idea

Log aggregation means collecting security logs from multiple systems into a centralized location.

### What Is a Log?

A log is a record of an event or activity.

Examples:

```text
10:15 — User successfully authenticated

10:17 — User accessed a protected application

10:19 — User attempted an unauthorized operation

10:20 — Firewall blocked suspicious traffic
```

A SIEM can combine logs from:

- Firewalls
- Servers
- Endpoints
- Identity systems
- Cloud services
- Applications
- Network devices

### Memory Trick

**Aggregation = Bring the logs together**

---

# 4. Event Correlation

## Big Idea

Correlation identifies relationships between events.

An event that looks harmless alone may become suspicious when connected to other activity.

### Example

A user authenticates at 2:00 AM.

That alone may not be suspicious.

Five minutes later, the same account downloads an unusually large volume of confidential documents.

The account then connects to an unfamiliar external destination.

Together, these events may indicate compromised credentials or data exfiltration.

### Memory Trick

**Correlation = Connect the dots**

---

# 5. Security Alerts

An alert is a notification that suspicious activity or a potentially dangerous condition has been detected.

### Examples

- Multiple failed sign-ins
- Suspicious PowerShell activity
- Connections to malicious IP addresses
- Unusual data transfers
- Malware-related behavior

An alert does not automatically prove that an attack has occurred.

Security analysts must determine whether the detected activity represents a genuine threat.

---

# 6. Security Incidents

## Big Idea

An incident groups related security alerts and evidence into one investigation.

### ELI5

**Alert = Something suspicious happened**

**Incident = Case file containing related suspicious activity**

An incident may include:

- Multiple alerts
- Affected users
- Affected devices
- Relevant timestamps
- Threat indicators
- Investigation notes
- Assigned analysts
- Status and severity

### Example

```text
INCIDENT: Potential Account Compromise
│
├── Alert: Unusual sign-in location
├── Alert: Suspicious PowerShell execution
├── Alert: Access to sensitive files
└── Alert: Connection to suspicious IP
```

Instead of investigating four separate alerts without context, the analyst reviews one incident.

### Memory Trick

**ALERT = Signal**

**INCIDENT = Investigation Case**

---

# 7. Security Orchestration, Automation, and Response — SOAR

## Big Idea

SOAR helps organizations coordinate and automate security response activities.

### ELI5

Imagine a security system detects unauthorized access.

Instead of requiring someone to manually notify every department and initiate every procedure, an automated workflow begins the approved response.

SOAR applies this concept to cybersecurity.

## SOAR Provides Two Major Capabilities

**Orchestration:** Coordinate multiple systems and tools.

**Automation:** Perform predefined tasks without requiring someone to execute each step manually.

---

# 8. Orchestration

Orchestration connects multiple security tools so they can work together.

### Example

A suspicious account is detected.

An orchestrated workflow might:

- Query Microsoft Entra for user information
- Check threat intelligence
- Retrieve device information
- Notify a SOC analyst
- Open an incident ticket

### Memory Trick

**Orchestration = Coordinate systems**

---

# 9. Automation

Automation performs repetitive tasks based on configured rules.

### Example

When a high-confidence account compromise is detected, an authorized automated workflow could:

- Disable the account
- Notify the security team
- Open a support ticket
- Gather relevant evidence

Automation helps reduce the delay between detecting a threat and responding to it.

### Memory Trick

**Automation = Execute tasks**

---

# 10. SIEM vs. SOAR

| SIEM | SOAR |
|---|---|
| Collects logs | Automates workflows |
| Correlates security events | Coordinates security tools |
| Detects suspicious activity | Executes response actions |
| Generates alerts | Performs predefined tasks |
| Creates incidents | Helps contain and remediate incidents |

### Critical Exam Distinction

If the question emphasizes:

**Collecting, correlating, analyzing, or detecting**

Think:

**SIEM**

If the question emphasizes:

**Automating response actions**

Think:

**SOAR**

---

# 11. Why SIEM and SOAR Work Together

A SIEM without SOAR can identify threats but may require significant manual response work.

SOAR without reliable detection and information would have limited context for deciding when and how to respond.

Together:

**SIEM detects the threat.**

**SOAR helps execute the response.**

### Simplified Workflow

```text
Security Events
      |
      v
SIEM Collects and Correlates Logs
      |
      v
Suspicious Activity Detected
      |
      v
Security Alert Generated
      |
      v
Related Alerts Grouped into Incident
      |
      v
SOAR Workflow Triggered
      |
      v
Response Actions Performed
```

---

# 12. Artificial Intelligence in Security Operations

Modern security environments generate more information than analysts can manually review.

AI and machine learning help security teams process large volumes of data more efficiently.

## Common AI and ML Capabilities

### Anomaly Detection

Identify behavior that differs from expected activity.

### Alert Correlation

Determine which alerts are related.

### Incident Prioritization

Help analysts identify the most important threats.

### False Positive Reduction

Reduce unnecessary investigations caused by benign activity.

### Multistage Attack Detection

Identify attacks that unfold through multiple activities over time.

### Natural-Language Assistance

Help analysts generate queries and summarize investigations.

---

# 13. Anomaly Detection

## Big Idea

An anomaly is an unusual deviation from expected behavior.

### Example

An employee normally signs in from Texas during business hours.

The account suddenly authenticates from an unfamiliar location and accesses resources it has never used.

That activity may warrant investigation.

### Important Distinction

**Anomaly does not automatically equal compromise.**

There may be a legitimate explanation.

AI and machine learning help identify suspicious patterns, but analysts must evaluate relevant context.

### Memory Trick

**Anomaly = Something is unusual**

---

# 14. False Positives

A **false positive** occurs when legitimate activity is incorrectly identified as malicious.

### Example

A system generates an alert because an administrator ran a legitimate security maintenance script.

The activity was authorized.

The alert was therefore a false positive.

## False Negative

A **false negative** occurs when actual malicious activity is not detected.

| Term | Meaning |
|---|---|
| True Positive | Correctly detected threat |
| False Positive | Benign activity incorrectly flagged |
| True Negative | Correctly recognized benign activity |
| False Negative | Threat incorrectly missed |

### Why This Matters

Too many false positives create unnecessary work.

False negatives can allow attacks to continue undetected.

Security teams must balance detection coverage with alert quality.

---

# 15. Alert Fatigue

## Big Idea

Alert fatigue occurs when analysts become overwhelmed by excessive security alerts.

### ELI5

Imagine receiving thousands of alarms every day.

Most turn out to be harmless.

Eventually, personnel may struggle to identify which alarms require immediate attention.

This creates a dangerous operational problem.

## How AI Helps

AI can assist by:

- Grouping related alerts
- Prioritizing incidents by severity
- Adding useful context
- Reducing false positives
- Identifying patterns across multiple events

### Memory Trick

**Alert Fatigue = Too many alarms, not enough useful context**

---

# 16. Four Main Microsoft Sentinel Operations

Microsoft Learn identifies four interconnected security operations.

**Collect**

**Detect**

**Investigate**

**Respond**

These represent the core Sentinel workflow.

### Memory Trick

**C-D-I-R**

**Collect → Detect → Investigate → Respond**

---

# 17. Collect Security Data

Microsoft Sentinel collects security information from many sources.

The current module describes **more than 350 built-in data connectors**.

These include integrations for:

- Microsoft security services
- Microsoft Azure
- Microsoft Entra ID
- Microsoft 365
- Microsoft Defender
- AWS
- Google Cloud
- Third-party platforms
- Custom data sources

### ELI5

A data connector allows Sentinel to receive information from another system.

---

# 18. Data Connectors

## Big Idea

A data connector integrates a security data source with Microsoft Sentinel.

### Example

An organization wants Sentinel to receive authentication logs from Microsoft Entra.

It configures an appropriate connector.

Sentinel can then use that information for supported analysis and detection.

## Common Sources

| Source | Example data |
|---|---|
| Microsoft Entra ID | Sign-ins and identity activity |
| Microsoft Defender | Security alerts and threat information |
| Azure resources | Resource and activity logs |
| Firewalls | Network connections and blocked traffic |
| AWS | Cloud security events |
| GCP | Cloud security events |

### Memory Trick

**Data Connector = Bring external security data into Sentinel**

---

# 19. Data Normalization

Different security products may describe similar events using different fields and formats.

Data normalization converts or maps information into a more consistent structure.

### ELI5

Imagine receiving reports from different Army units.

One report uses a particular terminology or layout.

Another uses a different format.

Before comparing the reports, you standardize how important information is represented.

Sentinel uses normalization to improve analysis across varied data sources.

### Memory Trick

**Normalization = Make different log formats easier to compare**

---

# 20. Detect Threats

Microsoft Sentinel uses several detection approaches.

The current module emphasizes:

**Rule-Based Detection**

**AI and Machine Learning**

**Threat Intelligence Matching**

---

# 21. Analytics Rules

## Big Idea

Analytics rules examine security data for conditions that may indicate a threat.

When suspicious activity matches a rule, Sentinel can generate alerts.

Related alerts can become incidents.

### Example

An analytics rule detects repeated unsuccessful authentication attempts followed by suspicious account activity.

The rule generates an alert.

### Memory Trick

**Analytics Rule = Detect suspicious activity**

---

# 22. Rule-Based Detection

Rule-based detection uses defined conditions or known patterns.

### Example

Generate an alert when:

```text
More than 20 failed sign-in attempts
occur within 5 minutes
for the same account.
```

This is a simplified illustrative rule, not a default Sentinel detection threshold.

## Benefits

- Consistent detection
- Repeatable logic
- Clear criteria
- Customizable scenarios

## Limitation

Attackers may use techniques that do not match existing rules.

This is one reason AI-powered detection is useful.

---

# 23. AI and Machine Learning Detection

Machine learning can examine behavior and identify unusual or suspicious patterns.

### Example

An attacker compromises an identity.

The attacker slowly performs several actions over multiple days.

Each action appears relatively minor.

Machine learning may identify a suspicious relationship across the activity.

---

# 24. Microsoft Sentinel Fusion

## Big Idea

**Fusion** is Microsoft's AI-powered correlation capability.

It combines related low-severity signals into more meaningful security incidents.

### ELI5

Imagine several minor security observations:

- Unusual sign-in
- Suspicious network access
- Unexpected privilege-related activity
- Abnormal file access

Each may look insignificant.

Fusion can recognize that the events collectively indicate a larger attack.

### Memory Trick

**Fusion = Combine weak signals into a stronger threat picture**

---

# 25. Threat Intelligence

## Big Idea

Threat intelligence provides information about known or suspected cyber threats.

Examples include:

- Malicious IP addresses
- Malicious domains
- Suspicious URLs
- Indicators of compromise
- Threat actor techniques

Microsoft Sentinel can use threat intelligence to help identify activity associated with known threats.

---

# 26. Indicators of Compromise — IoCs

An Indicator of Compromise is an observable artifact associated with potentially malicious activity.

Examples:

- Known malicious IP address
- Suspicious file hash
- Malicious domain
- Identified attack-related URL

### Example

A firewall log shows a device communicating with an IP address associated with malicious activity.

Sentinel can correlate that observation with threat intelligence.

### Important Distinction

An IoC is evidence useful for investigation.

It is not automatically proof that every related event represents an active compromise.

### Memory Trick

**IoC = Technical clue associated with compromise**

---

# 27. MITRE ATT&CK Framework

Microsoft Sentinel uses the MITRE ATT&CK framework to help organize detection coverage.

## What Is MITRE ATT&CK?

A knowledge base describing adversary tactics and techniques based on observed attack behavior.

### Tactic

Describes an attacker's objective.

Examples:

- Initial Access
- Persistence
- Credential Access
- Lateral Movement
- Exfiltration

### Technique

Describes how an attacker attempts to accomplish an objective.

### ELI5

**Tactic = What the attacker wants to accomplish**

**Technique = How the attacker attempts it**

## Sentinel Connection

Sentinel can map detection capabilities to MITRE ATT&CK techniques.

This helps organizations understand:

- Which techniques are covered
- Where detection gaps may exist
- Which new detections may be useful

### Memory Trick

**MITRE ATT&CK = Map attacker behavior to defensive coverage**

---

# 28. Microsoft Sentinel Content Hub

## Big Idea

The **Content hub** provides packaged security solutions.

A solution may contain multiple content types needed for a particular monitoring or investigation scenario.

Examples:

- Data connectors
- Workbooks
- Analytics rules
- Hunting queries
- Playbooks

### ELI5

Instead of configuring every component individually, an administrator can deploy a package containing related Sentinel content.

### Memory Trick

**Content Hub = Find and deploy packaged Sentinel solutions**

---

# 29. Microsoft Sentinel Workbooks

## Big Idea

Workbooks provide interactive visualizations and dashboards for security information.

### ELI5

Imagine a security operations dashboard showing:

- Authentication trends
- Incident counts
- Security alert activity
- Geographic information
- Relevant investigation metrics

A workbook can present this information through charts, tables, and other visual elements.

### Important Distinction

**Workbook = VISUALIZE**

**Analytics Rule = DETECT**

**Playbook = AUTOMATE**

**Hunting Query = INVESTIGATE**

This is one of the most important Sentinel feature distinctions.

---

# 30. Investigate Threats

When suspicious activity creates an incident, security analysts investigate.

Sentinel helps organize the available evidence.

An incident may include:

- Related alerts
- Affected users
- Devices
- IP addresses
- Timelines
- Associated entities
- Investigation activity

The analyst may:

- Assign the incident
- Review evidence
- Determine severity
- Investigate related entities
- Document findings
- Take appropriate response actions

### Memory Trick

**Incident = Central case file for investigation**

---

# 31. Threat Hunting

## Big Idea

Threat hunting means proactively searching for suspicious behavior.

Unlike waiting for an alert, threat hunting begins with an investigation or hypothesis.

### ELI5

A security officer suspects that someone may have accessed a restricted area.

No alarm has triggered.

Instead of waiting for an alarm, the officer reviews available records and searches for suspicious activity.

That is the idea behind threat hunting.

### Sentinel Example

An analyst suspects unusual account activity involving privileged users.

The analyst searches available Sentinel data for suspicious patterns.

If significant activity is discovered, the analyst investigates further.

### Memory Trick

**Hunting = Search BEFORE an alert is required**

---

# 32. Hunting Queries

Analysts can use queries to search security data.

Microsoft Sentinel supports:

**Kusto Query Language — KQL**

KQL provides a structured way to analyze large volumes of data.

### Example Questions

A threat hunter might ask:

- Which accounts have unusual authentication activity?
- Which devices communicated with suspicious destinations?
- Which resources experienced unusual activity?
- Which identities accessed an unfamiliar application?

If a useful hunting query identifies reliable suspicious behavior, it may be adapted into a detection rule.

### Key Distinction

**Hunting Query = Investigate data**

**Analytics Rule = Automatically detect defined conditions**

---

# 33. Kusto Query Language — KQL

## Big Idea

KQL is a query language used for analyzing security and operational data.

### Illustrative Example

```kql
SigninLogs
| where TimeGenerated > ago(24h)
| summarize TotalSignIns = count() by UserPrincipalName
| order by TotalSignIns desc
```

This illustrative query counts sign-in records by user over the previous 24 hours.

It requires the relevant sign-in data to be available in the environment.

## Basic KQL Concepts

| Keyword | Purpose |
|---|---|
| `where` | Filter records |
| `project` | Select fields |
| `summarize` | Aggregate values |
| `count()` | Count records |
| `order by` | Sort results |
| `ago()` | Reference relative time |

### Important Note

This is additional practical study context. The SC-900 Sentinel module focuses on recognizing Sentinel capabilities rather than mastering advanced KQL syntax.

For deeper Sentinel work, KQL becomes considerably more important.

---

# 34. Automation Rules

## Big Idea

Automation rules control how Sentinel handles incidents or alerts based on configured conditions.

An automation rule can perform supported actions such as:

- Assign an incident
- Change incident status
- Add investigation tasks
- Trigger a playbook

### Example

An incident is created with High severity.

An automation rule assigns it to the designated analyst group.

The rule may also trigger an appropriate response workflow.

### Memory Trick

**Automation Rule = Decide when to act and what action to initiate**

---

# 35. Microsoft Sentinel Playbooks

## Big Idea

A **playbook** is an automated response workflow.

Sentinel playbooks are built using:

**Azure Logic Apps**

### What Is Azure Logic Apps?

Azure Logic Apps is a cloud service for building automated workflows between supported systems and services.

### ELI5

Think of a cybersecurity response checklist that a system can execute automatically.

For example:

```text
Suspicious Account Incident
          |
          v
Incident Meets Automation Rule
          |
          v
Playbook Starts
          |
          +--> Disable affected account
          |
          +--> Notify security team
          |
          +--> Create help desk ticket
          |
          +--> Gather additional context
```

Actions require appropriate connectors, permissions, and configuration.

### Memory Trick

**Playbook = Automated response procedure**

---

# 36. Automation Rules vs. Playbooks

| Automation Rule | Playbook |
|---|---|
| Evaluates configured conditions | Executes a defined workflow |
| Can assign incident ownership | Can coordinate multiple services |
| Can update incident status | Can perform supported remediation |
| Can trigger a playbook | Built on Azure Logic Apps |

### ELI5

**Automation Rule = WHEN should something happen?**

**Playbook = WHAT sequence of actions happens?**

### Example

An automation rule detects that a new incident meets specific conditions.

The rule starts a playbook.

The playbook disables an affected identity, creates a ticket, and notifies the appropriate team.

---

# 37. Microsoft Sentinel's Modern Security Platform

Microsoft Learn now describes Sentinel as more than a conventional SIEM/SOAR system.

It provides a broader security data and analytics platform.

Three important components are:

**Microsoft Sentinel Data Lake**

**Microsoft Sentinel Graph**

**Microsoft Sentinel MCP Server**

These support large-scale analysis, AI-driven workflows, and more complex security investigations.

---

# 38. Microsoft Sentinel Data Lake

## Big Idea

The Sentinel data lake provides scalable, cost-effective storage and analysis of security data.

The current module describes two complementary tiers:

**Analytics Tier**

**Data Lake Tier**

### Memory Trick

**Analytics Tier = Active security operations**

**Data Lake Tier = Large-scale historical security data**

---

# 39. Analytics Tier

The analytics tier uses an:

**Azure Log Analytics workspace**

It supports:

- Security data ingestion
- Analytics rules
- Alert generation
- Incident management
- Interactive KQL analysis
- Operational investigations

### ELI5

The analytics tier is where active security monitoring and detection take place.

Microsoft Learn describes it as the initial ingestion location for the relevant security data.

---

# 40. Data Lake Tier

The data lake tier supports large-scale, long-term security data storage.

The current module describes retention of up to **12 years**.

This capability can support:

- Long-term investigations
- Historical analysis
- Threat research
- Extended behavioral baselines
- AI-assisted analytics

The module describes data from the analytics tier being mirrored to the data lake tier in an open format.

### ELI5

Imagine keeping years of historical security records.

You may not need all those records in the most expensive active analysis environment.

A data lake allows the organization to retain large volumes of information more economically.

### Important Note

Actual retention, supported capabilities, and costs depend on the organization's current service configuration and licensing.

---

# 41. Analytics Tier vs. Data Lake Tier

| Analytics Tier | Data Lake Tier |
|---|---|
| Active security monitoring | Long-term security analysis |
| Log Analytics workspace | Security data lake storage |
| Analytics rules | Historical investigation |
| Alert generation | Large-scale research |
| Incident management | AI and graph-related analysis |
| Operational KQL analysis | Long-term security data retention |

### Memory Trick

**Analytics = Detect what is happening**

**Data Lake = Investigate the larger history**

---

# 42. Microsoft Sentinel Graph

## Big Idea

The Sentinel graph analyzes relationships among security entities.

Examples of entities include:

- User identities
- Devices
- Applications
- Cloud resources
- Security events
- Threat indicators

### ELI5

Instead of looking only at isolated log records, imagine drawing connections between everything involved in an attack.

```text
Compromised User
       |
       v
Privileged Role
       |
       v
Cloud Application
       |
       v
Sensitive Database
```

A graph can help analysts understand how an attacker might move from one entity to another.

## Potential Uses

- Investigating attack paths
- Understanding asset relationships
- Identifying affected systems
- Analyzing connected security events
- Supporting AI-driven investigations

### Memory Trick

**Sentinel Graph = Understand security relationships**

---

# 43. Microsoft Sentinel MCP Server

## MCP

**Model Context Protocol**

## Big Idea

The Microsoft Sentinel MCP server provides an interface through which supported AI tools and agents can interact with Sentinel data.

### ELI5

Imagine an AI assistant needs information from Sentinel.

Without an appropriate integration, it may not know how to communicate with Sentinel's data systems.

An MCP server provides a standardized interaction layer for supported tools.

The current module describes the Sentinel MCP server as a hosted interface that supports natural-language interaction without requiring users to understand every underlying data schema.

### Memory Trick

**MCP Server = Interface between supported AI systems and Sentinel data**

---

# 44. MCP Server vs. Plugins vs. Data Connectors

These concepts are related but different.

| Component | Purpose |
|---|---|
| Data Connector | Bring security data into Sentinel |
| Security Copilot Plugin | Enable Copilot to use supported Sentinel capabilities |
| MCP Server | Provide a standardized interface for supported AI tools and agents |

### Example

A firewall sends logs to Sentinel through a data connector.

An analyst uses Security Copilot to investigate those logs through supported Copilot integrations.

A supported AI agent may interact with Sentinel through the MCP server.

### Critical Distinction

**Data Connector = Ingest**

**Plugin = Extend Copilot capabilities**

**MCP Server = Connect supported AI tools with data/services**

---

# 45. Microsoft Defender Portal

The current Microsoft Learn module states that Microsoft Sentinel is available in the:

**Microsoft Defender portal**

This portal provides a unified security operations environment.

It can bring together supported Sentinel and Defender XDR incidents and investigation workflows.

## Important Upcoming Change

Microsoft states that the Sentinel experience in the Azure portal will be retired on:

**March 31, 2027**

After that date, Sentinel will be available only through the Microsoft Defender portal.

### Exam and Operational Memory

**Microsoft Defender portal = Current recommended Sentinel experience**

This is a time-sensitive platform change.

---

# 46. Unified Detections

The Microsoft Defender portal provides a unified experience for supported detection rules across Sentinel and Defender XDR.

The current module describes:

**Custom Detections**

These enable security teams to define relevant detection logic using supported data.

### Why This Matters

Organizations may need to detect threats involving:

- Identities
- Endpoints
- Applications
- Cloud resources
- Other connected sources

A unified detection experience helps reduce unnecessary fragmentation between security products.

---

# 47. Sentinel vs. Defender XDR

This is one of the most important Microsoft security product distinctions.

## Microsoft Sentinel

Primarily provides broad enterprise:

**SIEM + SOAR**

It collects and correlates security data across Microsoft and non-Microsoft environments.

## Microsoft Defender XDR

Provides unified:

**Extended Detection and Response — XDR**

It correlates threats across supported security domains, including:

- Endpoints
- Identities
- Email
- Applications

| Microsoft Sentinel | Microsoft Defender XDR |
|---|---|
| SIEM and SOAR | Extended Detection and Response |
| Broad log ingestion | Cross-domain threat protection |
| Microsoft and third-party sources | Supported Microsoft Defender security domains |
| Analytics and hunting | Detection, investigation, and response |
| Security data lake | Unified XDR incidents |
| Automation rules and playbooks | Cross-domain remediation capabilities |

### Memory Trick

**Sentinel = Broad security visibility and orchestration**

**Defender XDR = Unified cross-domain threat detection and response**

They integrate and complement one another.

---

# 48. Microsoft Security Copilot Integration

Microsoft Sentinel integrates with Microsoft Security Copilot.

Security Copilot uses generative AI to help analysts interpret security information, investigate threats, and produce reports.

Microsoft Learn describes two experiences:

**Embedded Experience**

**Standalone Experience**

---

# 49. Embedded Security Copilot

The embedded experience provides Security Copilot assistance inside the Microsoft Defender portal.

When Sentinel is integrated with the Defender portal, Security Copilot can support incidents originating in Sentinel.

Examples include:

- Incident summarization
- Guided responses
- Script analysis
- Suspicious file analysis
- Identity summaries
- Device summaries
- Incident report generation

### ELI5

The analyst opens an incident.

Security Copilot helps explain the evidence without requiring the analyst to leave the security operations environment.

### Memory Trick

**Embedded = Copilot within the security product**

---

# 50. Incident Summarization

Security Copilot can generate an incident summary using available evidence.

A summary may include:

- What happened
- Affected entities
- Attack timeline
- Indicators of compromise
- Potential impact
- Relevant threat information

### Why It Matters

An analyst does not need to manually assemble every piece of context before beginning an investigation.

However, the analyst should verify important findings.

---

# 51. Guided Responses

Security Copilot can recommend response steps.

The current module groups guided responses into four categories.

**Triage**

**Containment**

**Investigation**

**Remediation**

## Triage

Determine what the incident is and how seriously it should be treated.

## Containment

Limit the attacker's ability to continue causing damage.

## Investigation

Gather additional evidence and determine the scope of compromise.

## Remediation

Correct or remove the underlying problem.

### Memory Trick

**TRIAGE → CONTAIN → INVESTIGATE → REMEDIATE**

These are AI-generated recommendations, not automatically executed actions.

---

# 52. Script and Command-Line Analysis

Security Copilot can analyze suspicious scripts and commands.

Examples include:

- PowerShell commands
- Obfuscated scripts
- Command-line activity

An analyst may ask:

> Explain what this script does and identify any suspicious behavior.

Security Copilot can help interpret the script and relate activity to relevant MITRE ATT&CK techniques.

### Important Distinction

Security Copilot provides analysis.

It does not guarantee that every script classification is correct.

Analysts must evaluate the findings appropriately.

---

# 53. Suspicious File Analysis

Security Copilot can help summarize information about suspicious files.

Depending on available evidence, the analysis may include:

- Detection information
- File certificates
- API calls
- Relevant strings
- Other investigation details

### ELI5

Instead of immediately interpreting a large set of file-analysis details, an analyst receives a structured explanation to guide further investigation.

---

# 54. Identity and Device Summaries

Security Copilot can summarize relevant identity and device information.

## Identity Information

Examples:

- Recent sign-in activity
- Role changes
- Risk flags
- Authentication methods

## Device Information

Examples:

- Security posture
- Protection status
- Vulnerable software
- Suspicious activity
- Supported Microsoft Intune information

### Important Concept

Security Copilot helps combine relevant investigation context from connected systems.

Underlying product permissions still apply.

---

# 55. Incident Report Generation

Security Copilot can assist with producing structured incident reports.

Reports may include:

- Incident summary
- Timeline
- Findings
- Investigators
- Response actions
- Classification reasoning

The current module describes PDF export and posting reports to the incident activity log.

### GRC Connection

Structured incident documentation can help organizations preserve evidence of incident-handling activities.

---

# 56. Natural Language to KQL

Security Copilot can help analysts generate KQL from natural-language descriptions.

### Example

Analyst prompt:

> Find sign-in attempts from unfamiliar locations during the past 48 hours.

Security Copilot can generate a relevant KQL query.

The analyst can review, run, and refine the query using the supported Sentinel data.

### Memory Trick

**Natural Language to KQL = Describe the search, generate the query**

---

# 57. Standalone Security Copilot

The standalone experience allows analysts to interact with supported Sentinel information from the dedicated Security Copilot interface.

The current module identifies two Sentinel-related plugins:

**Microsoft Sentinel**

**Natural Language to KQL for Microsoft Sentinel**

### Example

An analyst asks:

> Show the highest-priority Sentinel incidents.

Copilot can retrieve and summarize available information through authorized integrations.

---

# 58. Microsoft Sentinel Incident Investigation Promptbook

A **promptbook** is a predefined series of prompts.

Microsoft describes a Sentinel incident investigation promptbook that can gather information such as:

- Incident summary
- Related alerts
- Reputation scores
- Affected users
- Affected devices
- Other investigation context

### ELI5

Instead of manually asking several related investigation questions, the analyst uses a prepared sequence.

### Memory Trick

**Prompt = One question**

**Promptbook = Organized sequence of prompts**

---

# 59. Security Copilot Agents

The live Sentinel module introduces specialized AI agents that help automate security operations.

Two named agents are particularly important.

**Security Alert Triage Agent**

**Dynamic Threat Detection Agent**

---

# 60. Security Alert Triage Agent

## Big Idea

The Security Alert Triage Agent assists with evaluating security alerts at scale.

It can analyze evidence to help determine whether activity represents a genuine threat or a false positive.

The module describes support for relevant security workloads, including:

- Phishing alerts
- Identity alerts
- Cloud alerts

### ELI5

Imagine hundreds of incoming security alerts.

A triage agent helps organize and evaluate them so analysts can focus on the most significant threats.

### Memory Trick

**Alert Triage Agent = Determine which alerts need attention**

---

# 61. Dynamic Threat Detection Agent

## Big Idea

The Dynamic Threat Detection Agent identifies suspicious activity that traditional detection rules may miss.

It can correlate:

- Alerts
- Events
- Anomalies
- Threat intelligence

When appropriate, it can generate a dynamic alert with contextual information.

### ELI5

A predefined rule knows what it was configured to search for.

A dynamic detection system looks for suspicious relationships that may not match a previously written rule.

### Memory Trick

**Dynamic Threat Detection Agent = Find threats missed by traditional rules**

### Important Note

Agent features, licensing, and availability can evolve. These notes describe the capabilities presented in the verified module.

---

# 62. Security Copilot vs. Sentinel Automation

Do not confuse AI-generated recommendations with automatically executed remediation.

## Security Copilot

Helps analysts understand incidents and recommend actions.

## Sentinel Playbooks

Execute configured automated response workflows.

### Example

Security Copilot recommends disabling a compromised account.

An authorized analyst approves the response.

A properly configured automation or playbook may perform the action.

### Memory Trick

**Copilot = Recommend and assist**

**Playbook = Execute configured workflow**

---

# 63. Complete Security Operations Scenario

Imagine an organization experiences a suspected account compromise.

## Phase 1 — Collect

Microsoft Sentinel receives:

- Entra sign-in logs
- Firewall records
- Endpoint security alerts
- Cloud activity logs

## Phase 2 — Detect

An analytics rule identifies suspicious authentication behavior.

Other detections identify unusual device activity.

Fusion correlates the related signals.

## Phase 3 — Create Incident

Sentinel groups related alerts into one incident.

The case contains the relevant evidence and affected entities.

## Phase 4 — Investigate

A security analyst:

- Reviews the incident
- Examines the timeline
- Investigates the user
- Reviews affected devices
- Runs relevant KQL queries

Security Copilot assists with summarization.

## Phase 5 — Respond

An automation rule identifies that the incident meets configured response conditions.

A playbook may:

- Disable an affected identity
- Open a ticket
- Notify relevant personnel
- Gather additional evidence

## Phase 6 — Document

The analyst records findings and response actions.

Security Copilot may assist with incident report generation.

### End-to-End Model

```text
Security Logs
      |
      v
Data Connectors
      |
      v
Microsoft Sentinel
      |
      v
Analytics Rules / AI Detection / Fusion
      |
      v
Alerts
      |
      v
Incident
      |
      v
Investigation / Hunting / Copilot
      |
      v
Automation Rules
      |
      v
Playbooks / Response Actions
      |
      v
Documentation and Follow-Up
```

---

# 64. Critical Sentinel Feature Distinctions

| Capability | What it does |
|---|---|
| Data Connector | Brings security data into Sentinel |
| Analytics Rule | Detects suspicious activity |
| Alert | Signals a detected security condition |
| Incident | Groups related alerts and evidence |
| Workbook | Displays dashboards and visualizations |
| Hunting Query | Proactively searches security data |
| Automation Rule | Applies incident-handling conditions and actions |
| Playbook | Executes an automated response workflow |
| Content Hub | Provides packaged Sentinel solutions |
| Fusion | Correlates related signals using AI |
| Threat Intelligence | Supplies information about known threats |
| Sentinel Graph | Analyzes relationships among security entities |
| Sentinel Data Lake | Supports large-scale historical security analysis |
| Sentinel MCP Server | Connects supported AI systems to Sentinel data |
| Security Copilot | Provides AI-assisted security investigation |

---

# 65. Commonly Confused Concepts

## Alert vs. Incident

**Alert = Individual suspicious signal**

**Incident = Grouped investigation case**

---

## Analytics Rule vs. Hunting Query

**Analytics Rule = Automated detection**

**Hunting Query = Proactive investigation**

---

## Workbook vs. Playbook

**Workbook = Visualization**

**Playbook = Automation**

---

## Automation Rule vs. Playbook

**Automation Rule = Evaluate conditions and initiate actions**

**Playbook = Perform an automated workflow**

---

## SIEM vs. SOAR

**SIEM = Collect, correlate, and detect**

**SOAR = Coordinate and automate response**

---

## Fusion vs. Analytics Rules

**Fusion = AI-powered correlation of related signals**

**Analytics Rules = Detect suspicious conditions**

---

## Data Connector vs. Content Hub

**Data Connector = Ingest information**

**Content Hub = Deploy packaged solutions**

---

## Sentinel vs. Defender XDR

**Sentinel = Broad enterprise SIEM/SOAR**

**Defender XDR = Unified cross-domain detection and response**

---

## Sentinel vs. Security Copilot

**Sentinel = Security monitoring and operations platform**

**Security Copilot = AI assistant for investigations and workflows**

---

# 66. GRC / ISSO Career Connection

The following section provides additional professional context. It is not a separate Microsoft Learn instructional unit.

Microsoft Sentinel is relevant to Information System Security Officer, Risk Management Framework, and Governance, Risk, and Compliance responsibilities.

Sentinel produces security monitoring data, incident information, and response records that may support security-control assessments.

---

# 67. NIST SP 800-53 Relationships

These mappings are illustrative. Using Microsoft Sentinel does not automatically establish compliance with any control.

| Sentinel capability | Related NIST control |
|---|---|
| Security log collection | AU-2 — Event Logging |
| Analysis of security records | AU-6 — Audit Record Review, Analysis, and Reporting |
| Centralized audit processing | AU-12 — Audit Record Generation |
| Security monitoring | SI-4 — System Monitoring |
| Incident investigation | IR-4 — Incident Handling |
| Incident tracking and reporting | IR-5 — Incident Monitoring |
| Incident reporting workflows | IR-6 — Incident Reporting |
| Continuous security monitoring | CA-7 — Continuous Monitoring |

### Important Principle

The existence of logs does not automatically prove that they are reviewed or that incidents are handled appropriately.

An assessor should verify how the organization implements the relevant controls.

---

# 68. Sentinel and Continuous Monitoring

An ISSO may need to determine whether important security events are being collected and analyzed.

Relevant questions include:

- Are required log sources connected?
- Are critical events monitored?
- Are detection rules configured appropriately?
- Who reviews incidents?
- Are high-severity incidents escalated?
- Are response actions documented?
- Is security monitoring operating consistently?

### Example

An organization claims that all privileged account activity is monitored.

An assessor should verify whether the relevant audit and sign-in data are collected and whether the monitoring process can identify suspicious activity.

### GRC Lesson

**A configured tool is not the same thing as an effective security control.**

---

# 69. Sentinel and Incident Response

Sentinel can support different stages of incident handling.

Examples include:

- Detection
- Investigation
- Containment support
- Remediation workflows
- Documentation
- Post-incident analysis

### Example

A suspicious authentication incident occurs.

The SOC investigates and confirms compromise.

The security team disables affected credentials and documents the response.

An ISSO may review whether the organization followed its incident-response procedures.

### Important Distinction

**Sentinel = Technical operations and evidence**

**Incident Response Plan = Organizational procedures and responsibilities**

Both are necessary for effective incident handling.

---

# 70. Sentinel and Audit Evidence

Sentinel can provide relevant technical evidence for investigations and assessments.

Examples:

- Security event timestamps
- Incident records
- Related alerts
- Affected assets
- Analyst actions
- Automated response records

Evidence must be assessed for completeness and reliability.

### Important Considerations

An assessor should determine:

- Whether the required data was collected
- Whether retention periods are appropriate
- Whether access to logs is controlled
- Whether time information is accurate
- Whether the records support the claimed control operation

### Memory Trick

**Security Evidence = Records demonstrating what actually occurred**

---

# 71. The Security Operations Center — SOC

A Security Operations Center is responsible for monitoring, detecting, investigating, and responding to security threats.

## Common SOC Responsibilities

- Monitor security events
- Investigate alerts
- Triage incidents
- Analyze threat intelligence
- Perform threat hunting
- Coordinate responses
- Document findings

Microsoft Sentinel supports these responsibilities.

### SOC vs. ISSO

| SOC Analyst | ISSO |
|---|---|
| Investigates suspicious activity | Oversees system security posture and requirements |
| Triage security alerts | Reviews whether controls are implemented and effective |
| Performs threat hunting | Reviews monitoring and risk processes |
| Coordinates incident response | Supports compliance and risk reporting |
| Uses security operational tools | Uses control evidence and governance processes |

The roles can collaborate closely.

An ISSO benefits from understanding Sentinel even without serving as the primary SOC analyst.

---

# 72. Practical Sentinel Study Scenarios

## Scenario 1

An organization wants to centralize logs from AWS, Azure, firewalls, and endpoint security systems.

**Correct capability: Microsoft Sentinel / SIEM**

---

## Scenario 2

An analyst wants to visually display incident trends and authentication activity.

**Correct capability: Workbook**

---

## Scenario 3

An organization wants to automatically create alerts when suspicious patterns appear in collected data.

**Correct capability: Analytics Rules**

---

## Scenario 4

An analyst suspects an attacker is active but no alert has triggered.

**Correct capability: Threat Hunting**

---

## Scenario 5

Several low-severity signals may indicate a coordinated multistage attack.

**Correct capability: Fusion**

---

## Scenario 6

An incident should automatically trigger a predefined workflow that disables an account and notifies the security team.

**Correct capability: Playbook**

An automation rule can trigger the playbook.

---

## Scenario 7

The SOC wants a collection of predefined detection rules, queries, workbooks, and connectors.

**Correct capability: Content Hub**

---

## Scenario 8

An analyst wants an AI-generated incident summary without leaving the Defender portal.

**Correct capability: Embedded Security Copilot**

---

## Scenario 9

An analyst wants a natural-language request converted into a KQL query.

**Correct capability: Natural Language to KQL**

---

## Scenario 10

An organization wants to analyze years of historical security records.

**Correct capability: Sentinel Data Lake**

---

## Scenario 11

An investigator wants to identify relationships among compromised identities, devices, and critical cloud assets.

**Correct capability: Sentinel Graph**

---

## Scenario 12

An organization wants an AI agent to identify threats missed by traditional detection rules.

**Correct capability: Dynamic Threat Detection Agent**

---

# 73. SC-900 Quick Reference

| If the question mentions... | Think... |
|---|---|
| Centralized security log collection | SIEM |
| Correlate events from many systems | SIEM |
| Automated security response | SOAR |
| Microsoft's cloud-native SIEM/SOAR | Microsoft Sentinel |
| Collect security data | Data Connectors |
| Standardize log formats | Normalization |
| Detect suspicious conditions | Analytics Rules |
| Individual detection signal | Alert |
| Group related alerts | Incident |
| Security dashboard or visual report | Workbook |
| Search for threats proactively | Hunting |
| Generate security queries | KQL |
| AI correlation of multistage attacks | Fusion |
| Malicious IPs, domains, or URLs | Threat Intelligence |
| Adversary tactics and techniques | MITRE ATT&CK |
| Deploy packaged security solutions | Content Hub |
| Automate incident assignment/status | Automation Rule |
| Automated remediation workflow | Playbook |
| Workflow technology used by playbooks | Azure Logic Apps |
| Long-term security data storage | Sentinel Data Lake |
| Graph-based security relationships | Sentinel Graph |
| AI tool integration interface | Sentinel MCP Server |
| AI-generated incident summary | Security Copilot |
| Generate KQL from English | Natural Language to KQL |
| Reusable investigation prompts | Promptbook |
| AI-driven security alert triage | Security Alert Triage Agent |
| Identify threats missed by rules | Dynamic Threat Detection Agent |

---

# 74. Final Module 4 Cram Sheet

```text
MICROSOFT SENTINEL
= CLOUD-NATIVE SIEM + SOAR

SIEM
= SECURITY INFORMATION AND EVENT MANAGEMENT

SOAR
= SECURITY ORCHESTRATION,
  AUTOMATION, AND RESPONSE

SIEM
= COLLECT + CORRELATE + DETECT

SOAR
= ORCHESTRATE + AUTOMATE + RESPOND

SENTINEL'S FOUR CORE OPERATIONS
= COLLECT → DETECT → INVESTIGATE → RESPOND

DATA CONNECTOR
= INGEST SECURITY DATA

DATA NORMALIZATION
= STANDARDIZE LOG FORMATS

ANALYTICS RULE
= AUTOMATED THREAT DETECTION

ALERT
= DETECTED SECURITY SIGNAL

INCIDENT
= GROUPED INVESTIGATION CASE

WORKBOOK
= VISUAL DASHBOARD

HUNTING QUERY
= PROACTIVE THREAT INVESTIGATION

KQL
= KUSTO QUERY LANGUAGE

FUSION
= AI CORRELATION OF RELATED SIGNALS

THREAT INTELLIGENCE
= INFORMATION ABOUT KNOWN THREATS

IoC
= INDICATOR OF COMPROMISE

MITRE ATT&CK
= ADVERSARY TACTICS AND TECHNIQUES

CONTENT HUB
= PACKAGED SENTINEL SOLUTIONS

AUTOMATION RULE
= INCIDENT CONDITIONS AND ACTIONS

PLAYBOOK
= AUTOMATED RESPONSE WORKFLOW

AZURE LOGIC APPS
= PLAYBOOK WORKFLOW TECHNOLOGY

SENTINEL DATA LAKE
= LONG-TERM SECURITY DATA ANALYSIS

ANALYTICS TIER
= ACTIVE DETECTION AND INCIDENT MANAGEMENT

DATA LAKE TIER
= HISTORICAL SECURITY DATA AT SCALE

SENTINEL GRAPH
= ANALYZE SECURITY RELATIONSHIPS

MCP SERVER
= AI INTERFACE TO SENTINEL DATA

ALERT FATIGUE
= TOO MANY SECURITY ALERTS

FALSE POSITIVE
= BENIGN ACTIVITY FLAGGED AS A THREAT

FALSE NEGATIVE
= REAL THREAT NOT DETECTED

SECURITY COPILOT
= AI-ASSISTED SECURITY INVESTIGATION

EMBEDDED COPILOT
= AI INSIDE MICROSOFT DEFENDER PORTAL

STANDALONE COPILOT
= DEDICATED AI SECURITY EXPERIENCE

NATURAL LANGUAGE TO KQL
= GENERATE QUERIES FROM PLAIN ENGLISH

PROMPTBOOK
= PREDEFINED SERIES OF PROMPTS

SECURITY ALERT TRIAGE AGENT
= AI-ASSISTED ALERT CLASSIFICATION

DYNAMIC THREAT DETECTION AGENT
= IDENTIFY THREATS MISSED BY TRADITIONAL RULES

DEFENDER XDR
= UNIFIED CROSS-DOMAIN DETECTION AND RESPONSE

MICROSOFT SENTINEL
= BROAD ENTERPRISE SECURITY OPERATIONS

MICROSOFT DEFENDER PORTAL
= RECOMMENDED SENTINEL INTERFACE

AZURE PORTAL SENTINEL RETIREMENT
= MARCH 31, 2027
```

---

# 75. Final Mental Model

Imagine an attacker compromises an organization's account.

The account generates suspicious authentication activity.

An affected device communicates with a malicious server.

The attacker begins accessing sensitive resources.

**Microsoft Sentinel collects logs** from identity, endpoint, network, and cloud systems.

**Analytics rules and AI detections** identify suspicious behavior.

**Fusion** can connect related signals that might otherwise appear insignificant.

**Alerts** are generated and grouped into an **incident**.

A security analyst uses **KQL** and **threat hunting** to investigate additional suspicious behavior.

**Workbooks** display relevant security information.

**Microsoft Security Copilot** assists with summarizing the incident, analyzing suspicious activity, and recommending response steps.

An **automation rule** can trigger a **playbook** built using Azure Logic Apps.

The playbook executes appropriately configured response actions.

The analyst verifies the results and documents the incident.

**Microsoft Sentinel combines broad security visibility, detection, investigation, and automated response in one security operations platform.**

That is the central concept of this module.

---

# Official Microsoft Learn References

The following instructional pages were verified on November 23, 2026.

[Module Overview](https://learn.microsoft.com/en-us/training/modules/describe-security-capabilities-of-azure-sentinel/)

[Introduction](https://learn.microsoft.com/en-us/training/modules/describe-security-capabilities-of-azure-sentinel/1-introduction)

[Define the Concepts of SIEM and SOAR](https://learn.microsoft.com/en-us/training/modules/describe-security-capabilities-of-azure-sentinel/2-define-concepts-of-siem-soar)

[Describe Threat Detection and Mitigation Capabilities in Microsoft Sentinel](https://learn.microsoft.com/en-us/training/modules/describe-security-capabilities-of-azure-sentinel/3-describe-sentinel-provide-integrated-threat-management)

[Describe Microsoft Sentinel Integration with Microsoft Security Copilot](https://learn.microsoft.com/en-us/training/modules/describe-security-capabilities-of-azure-sentinel/4-describe-security-copilot)

[Module Assessment](https://learn.microsoft.com/en-us/training/modules/describe-security-capabilities-of-azure-sentinel/5-knowledge-check)

[Summary and Resources](https://learn.microsoft.com/en-us/training/modules/describe-security-capabilities-of-azure-sentinel/6-summary-resources)
