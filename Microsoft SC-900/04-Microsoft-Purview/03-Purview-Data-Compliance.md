# SC-900 — Section 4, Module 3
# Describe the Data Compliance Solutions of Microsoft Purview

> **Source:** Microsoft Learn — SC-900  
> **Learning Path:** Introduction to Microsoft Purview and Microsoft's privacy principles  
> **Module:** Describe the data compliance solutions of Microsoft Purview  
> **Verified against current Microsoft Learn content:** November 23, 2026  
> **Duration:** 41 minutes | 9 units | 1,000 XP  
> **Official Module:** https://learn.microsoft.com/en-us/training/modules/describe-purview-risk-compliance-governance/

---

# Module Overview

Microsoft Purview provides data compliance solutions that help organizations manage regulatory requirements, investigate activities, preserve evidence, and control how information is retained and deleted.

This module focuses on six major capabilities.

| Capability | Primary purpose |
|---|---|
| Compliance Manager | Assess compliance requirements and track improvement actions |
| Communication Compliance | Detect and investigate inappropriate communications |
| eDiscovery | Find, preserve, review, and export electronic evidence |
| Audit | Record and investigate user and administrator activity |
| Data Lifecycle Management | Retain and delete information according to policy |
| Records Management | Apply stricter controls to important organizational records |

## The Big Idea

Organizations must do more than protect information against cyberattacks.

They also need to demonstrate that information is handled according to applicable laws, regulations, contracts, and organizational policies.

That includes determining:

**Are we meeting our compliance requirements?**

**Are employees communicating appropriately?**

**Can we preserve information needed for investigations?**

**Can we determine who performed an action?**

**How long must information be retained?**

**Which records require additional legal or regulatory protection?**

Microsoft Purview provides specialized solutions for these responsibilities.

### ELI5

Imagine an organization responsible for thousands of personnel files, operational records, emails, contracts, and financial documents.

**Compliance Manager** provides a way to track whether security and compliance requirements are being addressed.

**Communication Compliance** helps identify potentially inappropriate messages.

**eDiscovery** preserves and collects information needed for legal investigations.

**Audit** records who performed specific activities.

**Data Lifecycle Management** determines when information must be retained or deleted.

**Records Management** applies additional controls to records with legal, regulatory, or business significance.

### Master Memory Trick

**COMPLIANCE MANAGER = ARE WE MEETING REQUIREMENTS?**

**COMMUNICATION COMPLIANCE = ARE MESSAGES APPROPRIATE?**

**eDISCOVERY = FIND AND PRESERVE EVIDENCE**

**AUDIT = WHO DID WHAT AND WHEN?**

**DATA LIFECYCLE = HOW LONG DO WE KEEP IT?**

**RECORDS MANAGEMENT = PROTECT OFFICIAL RECORDS**

---

# 1. The Microsoft Purview Portal

## Big Idea

The Microsoft Purview portal provides centralized access to Microsoft's data governance, data security, and data compliance solutions.

The current Microsoft Learn lesson organizes solutions into four general areas.

| Portal area | Purpose |
|---|---|
| Core | Foundational functionality, including Audit, Data Map, settings, and workflows |
| Risk & Compliance | Compliance Manager, Communication Compliance, eDiscovery, Information Barriers, and Records Management |
| Data Governance | Data catalog, lifecycle, and policy-related capabilities |
| Data Security | Information Protection, DLP, and Insider Risk Management |

The portal's actual navigation and available solutions depend on configuration, permissions, and licensing.

Official portal:

https://purview.microsoft.com/

### ELI5

Instead of accessing separate administrative interfaces for every compliance activity, administrators can use Microsoft Purview as a central starting point.

### Memory Trick

**Purview Portal = Central location for data security, governance, and compliance tools**

---

# 2. Microsoft Purview Compliance Manager

## Big Idea

Microsoft Purview Compliance Manager helps organizations assess, manage, and improve their compliance posture.

It provides a structured way to work with applicable regulations, standards, and organizational policies.

Compliance Manager supports assessments across Microsoft cloud services and supported multicloud environments.

### ELI5

Imagine preparing for a command inspection.

You need to know:

**What are the requirements?**

**Which requirements are already satisfied?**

**Which deficiencies remain?**

**Who is responsible for correcting them?**

**What documentation proves the corrective actions were completed?**

Compliance Manager helps organizations organize similar activities for compliance requirements.

---

# 3. Four Key Compliance Manager Capabilities

Microsoft Learn identifies four important capabilities.

## Prebuilt Assessments

Microsoft provides assessment templates based on recognized regulations and standards.

Organizations can also create custom assessments.

## Workflows

Administrators can manage compliance tasks and track progress.

## Improvement Actions

Microsoft provides recommended actions that help organizations address relevant compliance requirements.

## Compliance Score

A calculated score helps organizations understand progress toward completing improvement actions.

### Memory Trick

**ASSESS → ASSIGN → IMPROVE → MEASURE**

---

# 4. Compliance Score

## Big Idea

Compliance Manager uses a compliance score to measure progress toward completing actions associated with compliance requirements.

The score increases as qualifying improvement actions are completed.

### ELI5

Imagine an inspection checklist containing requirements worth different amounts of points.

Some requirements have greater potential impact than others.

As the organization addresses outstanding requirements, its overall score improves.

## Important Concept

**A higher compliance score means more evaluated improvement actions have been completed.**

It does not guarantee complete legal or regulatory compliance.

The current module explains that action points are weighted according to potential risk.

---

# 5. Two Sources of Compliance Score Points

Microsoft Learn identifies two categories.

## Your Points

Points earned when the organization completes improvement actions for which it is responsible.

### Example

The organization implements an appropriate data protection policy and documents the required testing.

## Microsoft-Managed Points

Points associated with improvement actions Microsoft has already completed as the cloud service provider.

### Example

Microsoft implements a provider-side control covered by the applicable assessment.

### Memory Trick

**Your Points = Customer responsibilities**

**Microsoft-Managed Points = Provider responsibilities**

---

# 6. Microsoft 365 Data Protection Baseline

When an organization initially uses Compliance Manager, Microsoft provides an initial score based on the Microsoft 365 data protection baseline.

The baseline addresses important data protection and governance requirements.

### ELI5

An organization does not necessarily start with an entirely blank compliance assessment.

Microsoft provides baseline information to support the initial assessment.

### Important Distinction

**Initial compliance score does not mean the customer has completed every required improvement action.**

---

# 7. Four Compliance Manager Elements

Microsoft Learn identifies four important elements.

**Controls**

**Assessments**

**Regulations**

**Improvement Actions**

These have different meanings.

| Element | Meaning |
|---|---|
| Control | Individual security or compliance requirement |
| Assessment | Group of controls associated with a standard or requirement |
| Regulation | Applicable law, standard, or certification framework |
| Improvement Action | Recommended activity for implementing or improving a control |

### Memory Trick

**REGULATION → ASSESSMENT → CONTROL → IMPROVEMENT ACTION**

---

# 8. Controls

## Big Idea

A control defines an expected security or compliance requirement.

Controls may involve:

- Technical configurations
- Organizational procedures
- Employee responsibilities
- Security processes
- Operational safeguards

### Example

An organization must restrict access to sensitive personnel information.

The relevant control establishes the requirement.

The organization must implement and demonstrate appropriate access restrictions.

### ELI5

**Control = What needs to be implemented or demonstrated**

---

# 9. Three Types of Controls

Microsoft Compliance Manager identifies three categories.

## Microsoft-Managed Controls

Implemented by Microsoft as the cloud service provider.

## Your Controls

Implemented and maintained by the customer organization.

These are also called customer-managed controls.

## Shared Controls

Require implementation responsibilities from both Microsoft and the customer.

### Example

An organization uses Microsoft cloud storage.

Microsoft may implement certain underlying infrastructure controls.

The customer must still configure appropriate user permissions.

Some requirements involve both parties.

### Memory Trick

**MICROSOFT = Provider responsibility**

**YOUR = Customer responsibility**

**SHARED = Both parties contribute**

---

# 10. Continuous Control Assessment

Compliance Manager can continuously evaluate supported technical settings in an organization's Microsoft 365 environment.

It can automatically update the status of relevant technical improvement actions.

### Important Distinction

Not every compliance requirement can be evaluated automatically.

For example, proving that employees completed required training may require organizational records or other evidence.

### ELI5

Some inspection items can be checked automatically.

Others require a person to inspect documents, verify procedures, or provide evidence.

---

# 11. Assessments

## Big Idea

An assessment groups controls related to a particular regulation, standard, or organizational requirement.

### Example

An organization wants to evaluate requirements associated with ISO 27001.

It creates an assessment based on the relevant template.

The assessment organizes applicable controls and associated improvement actions.

## Assessment Components

The current module identifies:

**Services in scope**

**Microsoft-managed controls**

**Customer-managed controls**

**Shared controls**

**Assessment score**

### Memory Trick

**Assessment = Organized evaluation against a requirement**

---

# 12. Assessment Templates

Microsoft provides templates to help organizations create assessments.

The current module states that Compliance Manager provides **more than 360 regulatory templates**.

These include different industry and regional regulations and standards.

Organizations can also customize assessments.

### ELI5

Instead of manually building a large compliance checklist from the beginning, an administrator can begin with an existing template.

### Important Concept

An available template does not automatically mean a regulation applies to the organization.

Applicability must be determined separately.

---

# 13. AI Regulatory Templates

The current Microsoft Learn module includes regulatory templates designed to support AI-related compliance requirements.

These can help organizations evaluate requirements involving:

- AI applications
- AI interactions
- Data protection
- Organizational AI governance

### Example

An organization adopts generative AI applications.

Its compliance team needs to evaluate requirements involving sensitive information handled by those systems.

Relevant Compliance Manager templates can help organize that assessment.

### Memory Trick

**AI Regulatory Templates = Organize AI compliance requirements**

---

# 14. Improvement Actions

## Big Idea

Improvement actions are recommended activities intended to help organizations meet compliance requirements.

They can include:

- Implementation guidance
- Assigned owners
- Testing responsibilities
- Status information
- Documentation
- Notes
- Supporting evidence

### Example

A compliance assessment identifies an incomplete security requirement.

An administrator creates or assigns an associated improvement action.

The responsible team implements the control, performs testing, and documents the result.

### Memory Trick

**Improvement Action = What needs to be done**

---

# 15. Compliance Manager Workflow

```text
Applicable Regulation or Standard
              |
              v
Create Assessment
              |
              v
Identify Relevant Controls
              |
              v
Review Improvement Actions
              |
              v
Assign Responsible Personnel
              |
              v
Implement and Test Controls
              |
              v
Document Evidence
              |
              v
Update Compliance Score
```

### Important Principle

**Compliance Manager tracks progress toward compliance.**

It does not automatically certify an organization as compliant.

---

# 16. Compliance Manager vs. Service Trust Portal

These products were introduced across two different Purview modules.

| Compliance Manager | Service Trust Portal |
|---|---|
| Assess the customer's compliance posture | Review Microsoft's assurance documentation |
| Manage improvement actions | Obtain independent audit reports |
| Track controls | Review certifications |
| Calculate compliance score | Access provider compliance evidence |
| Assign assessment responsibilities | Review Microsoft's implemented controls |

### ELI5

**Service Trust Portal = Microsoft's compliance evidence**

**Compliance Manager = Your organization's compliance assessment process**

This distinction is particularly relevant to GRC work.

---

# 17. Microsoft Purview Communication Compliance

## Big Idea

Communication Compliance helps organizations detect, review, and address potentially inappropriate communications.

It is part of Microsoft's broader insider risk capabilities.

### ELI5

An organization has policies governing professional communications.

Examples include prohibitions against:

- Harassment
- Threatening language
- Inappropriate disclosure of confidential information
- Unauthorized communications about sensitive projects
- Certain regulated communications

Communication Compliance helps identify messages that may violate those requirements.

### Memory Trick

**Communication Compliance = Detect risky or inappropriate messages**

---

# 18. Communication Compliance Coverage

The current Microsoft Learn module identifies support for text and image-based communications in Microsoft and supported non-Microsoft applications.

Examples include:

- Microsoft Teams
- Outlook
- Viva Engage
- WhatsApp
- Microsoft 365 Copilot
- Microsoft 365 Copilot Chat

Actual monitoring coverage depends on configured policies, supported integrations, and permissions.

### Important Concept

**Communication Compliance is not limited to email.**

It can evaluate multiple communications platforms.

---

# 19. What Communication Compliance Detects

## Corporate Policy Violations

Examples:

- Harassment
- Offensive language
- Threatening messages
- Violations of acceptable-use requirements

## Confidential Information Risks

Examples:

- Unauthorized discussion of sensitive projects
- Inappropriate sharing of business information

## Regulatory Violations

Examples:

- Potential insider trading communications
- Bribery-related communications
- Other regulated messaging activities

### ELI5

The objective is to identify communications that might create organizational, legal, or regulatory risk.

### Important Limitation

A message flagged by a policy is not automatically proof of a violation.

An authorized reviewer must evaluate the context.

---

# 20. Communication Compliance Workflow

Microsoft Learn identifies four stages.

**Configure → Investigate → Remediate → Maintain**

## Configure

Establish policies and identify the communication activities requiring review.

## Investigate

Review alerts and messages that match configured policies.

## Remediate

Take an appropriate response based on the investigation.

## Maintain

Monitor effectiveness, review records, and improve policies.

### Memory Trick

**C-I-R-M**

**Configure → Investigate → Remediate → Maintain**

---

# 21. Communication Compliance Investigations

Designated reviewers can investigate messages matching policy conditions.

Supported tools include:

- Alerts
- Message review
- User history
- Filters
- Issue management
- Related documentation

Reviewers determine whether an alert represents an actual concern.

### Example

An employee's message contains language identified by a harassment classifier.

A designated reviewer examines the message and surrounding context.

The reviewer decides whether action is appropriate.

---

# 22. Communication Compliance Remediation

Microsoft Learn identifies several possible actions.

| Action | Purpose |
|---|---|
| Resolve an alert | Close a reviewed issue |
| Tag a message | Categorize the message |
| Notify a user | Provide feedback or policy guidance |
| Escalate | Refer the issue to another authorized reviewer |
| Mark false positive | Identify a benign policy match |
| Remove a Teams message | Remove supported inappropriate content |
| Escalate for investigation | Begin a more formal investigation |

### Important Concept

**Communication Compliance supports investigation and remediation; it does not automatically determine employee wrongdoing.**

---

# 23. Separation of Duties

Communication Compliance supports role-based access controls.

This helps distinguish responsibilities involving:

**IT Administrators**

and

**Compliance Investigators**

### Example

An IT team configures permissions and technical settings.

A separate compliance team reviews flagged communications.

### Why This Matters

Separating responsibilities reduces unnecessary access and helps prevent conflicts of interest.

### Memory Trick

**Separation of Duties = No single person unnecessarily controls every stage**

---

# 24. Communication Compliance and AI

The current module includes coverage of generative AI communications.

Communication Compliance can evaluate supported AI interactions, including:

- User prompts
- AI responses
- Interactions with Microsoft 365 Copilot
- Supported Copilot Studio applications
- Supported connected AI services

### Example

An employee enters inappropriate or confidential information into an AI conversation.

A configured Communication Compliance policy may detect the interaction.

### Important Distinction

**Communication Compliance = Review AI conversations for policy violations**

**DLP = Restrict inappropriate sharing of sensitive information**

**Audit = Record supported AI-related activities**

The capabilities serve different purposes.

---

# 25. Communication Compliance and Security Copilot

The current lesson describes embedded Microsoft Security Copilot integration.

Supported capabilities include:

**Contextual Summaries**

Help reviewers understand why a message or attachment matched a policy.

**Follow-Up Questions**

Allow reviewers to ask additional questions about the relevant content.

### Example

A message triggers a classifier associated with inappropriate communication.

Security Copilot summarizes the message and its attachments in the context of the detection.

### Important Concept

**Security Copilot assists the reviewer.**

It does not replace the organization's investigation and disciplinary processes.

---

# 26. Communication Compliance vs. Insider Risk Management

| Communication Compliance | Insider Risk Management |
|---|---|
| Focuses on messages and communications | Focuses on broader risky internal behavior |
| Detects inappropriate language | Detects suspicious user activities |
| Reviews messages and attachments | Reviews relevant user and data activity |
| Can investigate regulatory communications | Can investigate data theft or policy violations |

### Example

**Harassing Teams message = Communication Compliance**

**Employee downloads large volumes of sensitive files before departure = Insider Risk Management**

---

# 27. Microsoft Purview eDiscovery

## Big Idea

**eDiscovery = Electronic Discovery**

Electronic discovery is the process of identifying, preserving, collecting, reviewing, and providing electronic information that may be used as evidence in legal proceedings or formal investigations.

### ELI5

Imagine a legal investigation requiring an organization's relevant emails and documents.

The investigation team must locate the information, ensure it is not deleted, evaluate what is relevant, and provide appropriate evidence.

Microsoft Purview eDiscovery supports that process.

### Memory Trick

**eDISCOVERY = FIND + PRESERVE + REVIEW + EXPORT EVIDENCE**

---

# 28. Electronically Stored Information — ESI

## Big Idea

ESI refers to information stored electronically.

Examples include:

- Emails
- Documents
- Teams messages
- SharePoint files
- OneDrive content
- Collaboration records

Microsoft Purview eDiscovery supports investigations involving content from:

| Microsoft 365 service | Example evidence |
|---|---|
| Exchange Online | Emails and attachments |
| Microsoft Teams | Chats and messages |
| Microsoft 365 Groups | Group-related information |
| OneDrive | Stored documents |
| SharePoint | Site files and content |
| Viva Engage | Organizational conversations |

### Memory Trick

**ESI = Electronically Stored Information**

---

# 29. The Unified eDiscovery Experience

Microsoft Learn describes a unified eDiscovery experience within the Microsoft Purview portal.

Organizations access the available capabilities through a single interface.

Advanced capabilities depend on licensing and permissions.

### Important Concept

Some older study materials distinguish separate eDiscovery interfaces.

The current module emphasizes the unified Microsoft Purview eDiscovery experience.

---

# 30. eDiscovery Cases

## Big Idea

An eDiscovery case organizes the evidence-related activities for one investigation.

A case can contain:

- Searches
- Holds
- Review sets
- Investigation information

### ELI5

Think of an eDiscovery case as a digital legal case folder.

The investigators keep their searches, preservation requirements, and reviewed evidence organized together.

### Memory Trick

**Case = Central investigation workspace**

---

# 31. eDiscovery Workflow

Microsoft Learn presents the following general sequence.

**Trigger Event → Case → Search → Preserve or Collect → Review → Export**

## Trigger Event

An incident, legal request, or other event requires investigation.

## Create Case

An authorized investigator creates an eDiscovery case.

## Search

Investigators locate potentially relevant information.

## Preserve or Collect

Investigators may place content on hold or collect content into review sets.

## Review

Relevant information is filtered, evaluated, and tagged.

## Export

Authorized personnel export relevant evidence.

---

# 32. eDiscovery Holds

## Big Idea

An eDiscovery hold preserves information that may be relevant to an investigation.

It helps prevent permanent loss through accidental or intentional deletion.

### ELI5

Imagine a legal investigation involving an employee's mailbox.

The employee deletes several relevant messages.

If the mailbox is subject to an appropriate hold, the preserved information can remain available for the investigation.

### Memory Trick

**HOLD = PRESERVE EVIDENCE**

---

# 33. eDiscovery Holds vs. Retention Policies

Both can preserve information, but their purposes differ.

## eDiscovery Hold

Used to preserve relevant content associated with an investigation or legal obligation.

## Retention Policy

Used to apply ordinary organizational retention and deletion requirements.

| eDiscovery Hold | Retention Policy |
|---|---|
| Investigation-driven | Lifecycle-driven |
| Preserves relevant evidence | Retains or deletes content according to policy |
| Associated with a case | Associated with selected locations or content |
| Supports legal and formal investigations | Supports ordinary information governance |

### Important Concept

**eDiscovery holds should not be confused with routine retention policies.**

Both may affect whether content can be permanently deleted.

---

# 34. eDiscovery Search

Investigators search supported Microsoft 365 content locations.

Searches can identify potentially relevant:

- Email messages
- Documents
- Conversations
- Attachments
- Other electronic information

Results can be evaluated and refined.

### Example

A legal investigation requires communications involving a particular project.

The investigator searches relevant mailboxes and collaboration locations.

---

# 35. Review Sets

## Big Idea

An eDiscovery review set contains a collected copy of information for examination.

Microsoft describes a review set as a secure Microsoft-provided Azure Storage location.

The copied information forms a static collection that can be searched, filtered, tagged, and analyzed.

### ELI5

Imagine an investigator takes authorized copies of relevant documents and places them in a controlled evidence-review room.

The review set serves a similar purpose for electronic content.

### Important Detail

**Review sets are a premium eDiscovery capability.**

---

# 36. Review Set Capabilities

Microsoft Learn identifies several advanced capabilities.

## Analytics

Help reduce irrelevant information.

## Tagging

Allow reviewers to classify evidence.

## Predictive Coding

Use supported models to help evaluate relevance.

## Optical Character Recognition — OCR

Extract searchable text from images.

## Conversation Threading

Preserve conversation context for supported chat messages.

## Decryption

Support review of specified encrypted Microsoft content.

### Memory Trick

**Review Set = Organized evidence collection for detailed analysis**

---

# 37. Optical Character Recognition — OCR

## Big Idea

OCR extracts text from images.

### Example

An investigator has a scanned document containing relevant information.

Ordinary text search may not recognize the words because the document contains image data.

OCR extracts the text so it can be searched.

### Memory Trick

**OCR = Make image text searchable**

---

# 38. Conversation Threading

## Big Idea

Conversation threading helps reviewers understand messages in their conversational context.

### Example

One Teams message might appear suspicious when viewed alone.

The surrounding discussion may show whether the message was legitimate or inappropriate.

Conversation threading helps preserve that context.

### Memory Trick

**Conversation Threading = Review the complete discussion**

---

# 39. eDiscovery Decryption

The current module identifies supported decryption capabilities for certain Microsoft-protected content added to review sets.

Examples include:

- Protected email
- Encrypted attachments
- Documents protected by sensitivity labels

### Important Concept

Authorized evidence review may require mechanisms for accessing protected information.

This does not mean every investigator automatically has unrestricted access to encrypted content.

Appropriate permissions and supported configurations still apply.

---

# 40. eDiscovery and Security Copilot

Microsoft Purview eDiscovery integrates with Microsoft Security Copilot.

The live module identifies two major capabilities.

## Evidence Summarization

Security Copilot can summarize supported items in review sets.

Examples include:

- Documents
- Attachments
- Meeting transcripts

## Natural Language to KeyQL

Security Copilot can generate search queries from natural-language instructions.

### Important Acronym

**KeyQL = Keyword Query Language**

This is different from:

**KQL = Kusto Query Language**

### Memory Trick

**KeyQL = eDiscovery content searching**

**KQL = Security log and telemetry analysis**

---

# 41. eDiscovery and Insider Risk Management

An Insider Risk Management case may require legal review.

The case can be escalated to eDiscovery.

### Example

An employee is suspected of improperly removing confidential business information.

The organization's insider-risk team identifies concerning activity.

If formal legal review is necessary, authorized personnel can use eDiscovery to preserve and review relevant content.

### Important Distinction

**Insider Risk Management = Identify and investigate risky activity**

**eDiscovery = Preserve and review electronically stored evidence**

---

# 42. Microsoft Purview Audit

## Big Idea

Microsoft Purview Audit records user and administrator activities across supported Microsoft 365 services.

It helps organizations investigate incidents and demonstrate accountability.

### ELI5

Imagine an organization needs to determine:

**Who accessed this file?**

**When was it downloaded?**

**Was a mailbox forwarding rule changed?**

**Who modified an administrative setting?**

Audit records can help answer those questions.

### Memory Trick

**AUDIT = WHO DID WHAT AND WHEN?**

---

# 43. Unified Audit Log

## Big Idea

Microsoft Purview uses a unified audit log containing records of supported activities across Microsoft 365.

Examples include:

| Service | Example audit events |
|---|---|
| Exchange Online | Email access, deletion, forwarding, mailbox changes |
| SharePoint | File access, uploads, downloads, sharing |
| OneDrive | File activity and permission changes |
| Teams | Messages, meetings, and team changes |
| Microsoft Entra ID | Sign-ins, role assignments, password changes |
| Microsoft 365 Copilot | Supported AI interactions |
| Microsoft Security Copilot | Supported interactions when audit capture is enabled |

### Important Concept

**The unified audit log centralizes relevant activity records.**

It is not the same thing as an incident-management platform.

---

# 44. Searching Audit Records

The current module identifies several methods.

## Purview Audit Search

Search records through the Microsoft Purview portal.

## Microsoft Graph Audit Search API

Access supported audit search functionality programmatically.

## Exchange Online PowerShell

Use:

`Search-UnifiedAuditLog`

## Office 365 Management Activity API

Retrieve audit information for programmatic processing or integration with a SIEM.

### Memory Trick

**Purview Portal = Interactive audit search**

**APIs and PowerShell = Programmatic audit access**

---

# 45. Audit Standard vs. Audit Premium

Microsoft provides two auditing solutions.

| Capability | Audit Standard | Audit Premium |
|---|---|---|
| Searchable audit records | Yes | Yes |
| Audit search interface | Yes | Yes |
| CSV export | Yes | Yes |
| Standard retention | 180 days | Longer retention for applicable records |
| Intelligent insights | Standard capabilities | Additional high-value audit insights |
| Custom retention policies | Limited | Yes |
| Higher API bandwidth | No | Yes |

### Exam Shortcut

**Basic audit searching = Audit Standard**

**Longer retention and advanced insights = Audit Premium**

---

# 46. Audit Standard

## Big Idea

Audit Standard provides foundational audit capabilities.

The current Microsoft Learn module states that Audit Standard:

**Is enabled by default in eligible organizations.**

**Supports thousands of searchable audit events.**

**Retains audit records for 180 days.**

**Supports CSV export.**

### Memory Trick

**STANDARD = 180 DAYS**

Licensing and organizational configuration still matter.

---

# 47. Audit Premium

## Big Idea

Audit Premium provides enhanced capabilities for organizations requiring more extensive auditing.

The current module identifies:

- Longer audit retention
- Custom audit retention policies
- Intelligent insights
- Higher API bandwidth

### Default Premium Retention

For applicable records from:

**Microsoft Entra ID**

**Exchange**

**OneDrive**

**SharePoint**

the current module describes **one-year default retention**.

Other activity types generally retain the default 180-day period unless another applicable policy extends retention.

### Extended Retention

With appropriate licensing, organizations can configure retention up to **10 years** for eligible users and records.

### Memory Trick

**PREMIUM = ONE YEAR FOR CERTAIN RECORDS**

**ELIGIBLE ADD-ON = UP TO TEN YEARS**

---

# 48. Audit Premium Intelligent Insights

Audit Premium provides additional information useful for detailed investigations.

Examples include:

- Mail items accessed
- Mail items replied to
- Mail forwarding activity
- Supported search activities in Exchange or SharePoint

### ELI5

A basic audit event may show that an action occurred.

A more detailed audit record may provide useful information about the scope or nature of the action.

### Important Concept

Advanced audit records can help investigators determine the impact of a potential compromise.

---

# 49. Audit Retention Is Not Content Retention

These are different concepts.

## Audit Retention

Determines how long activity records are preserved.

## Data Lifecycle Retention

Determines how long emails, documents, and other content are preserved.

### Example

An organization retains audit logs for one year.

That does not automatically mean the underlying documents must also be retained for one year.

### Memory Trick

**AUDIT RETENTION = Preserve records of actions**

**CONTENT RETENTION = Preserve the actual information**

---

# 50. Copilot Audit Logging

The current module distinguishes Microsoft 365 Copilot from Microsoft Security Copilot.

## Microsoft 365 Copilot

Supported interactions are automatically logged in Microsoft Purview Audit.

The module identifies the event:

`CopilotInteraction`

Examples include Copilot activity within supported Microsoft 365 applications.

## Microsoft Security Copilot

A Security Copilot owner must enable the relevant Microsoft Purview audit integration.

The system can then record supported:

- Administrative actions
- User actions
- Copilot responses

### Memory Trick

**Microsoft 365 Copilot = Automatic supported audit capture**

**Security Copilot = Owner enables Purview integration**

---

# 51. Audit vs. Sentinel

Both can provide information useful for security investigations.

However, their primary purposes differ.

| Microsoft Purview Audit | Microsoft Sentinel |
|---|---|
| Records supported user/admin activities | SIEM and SOAR |
| Supports audit searches | Correlates security events |
| Provides compliance evidence | Generates detections and incidents |
| Supports forensic investigations | Supports threat hunting and response |
| Retains audit records | Analyzes broader security telemetry |

### Example

**Find who downloaded a SharePoint file:** Purview Audit.

**Correlate identity, endpoint, and firewall events into a security incident:** Microsoft Sentinel.

They can integrate.

---

# 52. Microsoft Purview Data Lifecycle Management

## Big Idea

Data Lifecycle Management helps organizations retain information they need and delete information they no longer need.

### ELI5

Imagine an organization has thousands of outdated documents.

Some must be preserved for legal or operational reasons.

Others no longer provide business value.

Retaining everything indefinitely can increase:

- Storage requirements
- Data exposure
- Investigation burden
- Privacy risk

Data Lifecycle Management helps organizations implement controlled retention and deletion.

### Memory Trick

**DATA LIFECYCLE = KEEP WHAT IS REQUIRED, DELETE WHAT IS NOT**

---

# 53. Three Retention Outcomes

Microsoft Learn describes three possibilities.

## Retain Only

Keep information forever or for a defined period.

## Delete Only

Delete information after a defined period.

## Retain and Then Delete

Keep information for a required period, then permanently delete it.

| Retention behavior | Purpose |
|---|---|
| Retain only | Preserve content |
| Delete only | Remove content after a defined time |
| Retain then delete | Satisfy retention period and then remove content |

### Example

An organization must preserve certain documents for seven years.

After the retention period, the documents should be deleted according to policy.

**Relevant configuration: Retain and then delete**

---

# 54. Retention Policies

## Big Idea

A retention policy applies retention settings to selected content locations.

Examples include:

- SharePoint sites
- OneDrive accounts
- Exchange mailboxes
- Teams-related locations
- Viva Engage content

### ELI5

An organization wants all documents in a particular SharePoint site retained for five years.

Rather than labeling each document individually, it applies an appropriate retention policy to the location.

### Memory Trick

**RETENTION POLICY = LOCATION-LEVEL RETENTION**

---

# 55. Retention Labels

## Big Idea

Retention labels apply retention settings to individual items.

Examples include:

- Documents
- Emails
- Folders, where supported

A document or email can have only one retention label at a time.

### ELI5

A SharePoint site contains both ordinary administrative records and high-value legal records.

The organization wants different retention periods for different documents.

Retention labels allow more granular treatment.

### Memory Trick

**RETENTION LABEL = ITEM-LEVEL RETENTION**

---

# 56. Retention Policy vs. Retention Label

| Retention Policy | Retention Label |
|---|---|
| Location-level settings | Item-level settings |
| Broad application | More granular application |
| Applies to mailboxes or sites | Applies to documents and emails |
| Settings generally do not travel with moved items | Label settings can travel within the tenant |
| Efficient for uniform retention requirements | Useful for mixed retention requirements |

### Critical Example

A SharePoint site needs most documents retained for five years.

Certain documents require ten years.

Microsoft Learn illustrates applying:

**Five-year retention policy to the site**

and

**Ten-year retention labels to individual documents requiring longer retention**

### Important Concept

Where retention settings conflict, organizations must evaluate Microsoft's applicable retention precedence rules. A simple label/policy comparison does not describe every possible conflict.

---

# 57. Retention Settings Follow the Content Differently

## Retention Policies

Apply based on the relevant location or container.

When an item moves outside that location, the policy does not simply travel with the item.

Preserved copies may remain in secure workload locations.

## Retention Labels

Can remain associated with content moved within the same Microsoft 365 tenant.

However, the module states that label retention settings do not persist when content moves outside the tenant.

### Memory Trick

**POLICY = LOCATION**

**LABEL = ITEM**

---

# 58. Retention Label Policies

Creating a retention label does not automatically make it available to every user.

Administrators publish labels using retention label policies.

These determine:

- Applicable locations
- Applicable users
- Available labels

### Example

An organization creates a retention label for personnel records.

A label policy makes it available to authorized HR users.

### Important Distinction

**Retention Label = Retention settings**

**Retention Label Policy = Publication and availability**

---

# 59. Retention Label vs. Sensitivity Label

This distinction connects Module 2 and Module 3.

| Sensitivity Label | Retention Label |
|---|---|
| Classify and protect sensitive information | Control how long information is retained |
| May apply encryption | Can preserve or delete content |
| May restrict access | May support disposition review |
| Helps prevent disclosure | Helps manage lifecycle obligations |

### Example

A confidential contract might have:

**Sensitivity label:** Confidential.

**Retention label:** Retain seven years after contract expiration.

These labels serve different purposes.

### Memory Trick

**SENSITIVITY = WHO MAY ACCESS IT?**

**RETENTION = HOW LONG MUST IT EXIST?**

---

# 60. Preservation During Retention

When information is subject to retention, users may continue working with the content.

However, when they modify or delete content, Microsoft 365 can preserve copies in secure locations as required by the configured retention settings.

### ELI5

An employee deletes an email.

The email disappears from the employee's normal view.

However, a preserved copy may remain available because of an applicable retention requirement.

### Important Concept

**Deleting an item from the user's view does not necessarily mean the retained information is permanently deleted.**

---

# 61. Mailbox Archiving

Data Lifecycle Management includes mailbox archiving capabilities.

Archiving can provide additional storage for supported mailboxes.

The current lesson describes auto-expanding archive capabilities for eligible mailboxes.

### Important Distinction

**Archiving = Additional mailbox storage and management**

**Retention = Rules governing preservation and deletion**

An archive does not automatically satisfy every recordkeeping requirement.

---

# 62. Inactive Mailboxes

## Big Idea

An inactive mailbox preserves mailbox content after an employee leaves the organization.

The current module describes creating an inactive mailbox when the mailbox is placed on an appropriate hold before the associated user account is deleted.

### Example

An employee leaves the organization.

The organization must preserve certain correspondence for ongoing legal requirements.

An inactive mailbox can support that preservation.

### Memory Trick

**Inactive Mailbox = Preserve departed employee's mailbox content**

---

# 63. Data Lifecycle Management and AI Interactions

The current Microsoft Learn module describes retention of supported AI interactions.

These include prompts and responses associated with Microsoft 365 Copilot and supported AI applications.

The module describes relevant interaction records being stored in the user's Exchange mailbox.

Retention policies can then govern their preservation and deletion.

### Example

An organization must preserve certain AI-related communications for compliance purposes.

It configures applicable retention settings.

### Important Concept

**AI-generated interactions can be subject to records and retention requirements.**

They are not automatically exempt because they were created through AI.

---

# 64. Adaptive Protection and Retention

The current module identifies integration between Data Lifecycle Management and Adaptive Protection.

Adaptive Protection uses insider risk signals to help adjust data protection controls.

### Example

An identity shows elevated insider risk.

Appropriate retention controls can help preserve relevant information against accidental or malicious deletion.

### Memory Trick

**Adaptive Protection = Adjust safeguards based on risk**

---

# 65. Microsoft Purview Records Management

## Big Idea

Records Management provides additional controls for information with legal, regulatory, or important business value.

It builds on Data Lifecycle Management.

### ELI5

Not every organizational document should be treated as an official record.

An ordinary working document may be edited or deleted under routine policy.

An official record may need stronger controls to preserve its integrity and demonstrate compliance.

### Memory Trick

**RECORDS MANAGEMENT = FORMAL CONTROL OF IMPORTANT RECORDS**

---

# 66. Records Management Capabilities

Microsoft Learn identifies several capabilities.

| Capability | Purpose |
|---|---|
| Declare a record | Apply special record restrictions |
| Retention labeling | Define record retention requirements |
| Event-based retention | Begin retention after a defined event |
| Disposition review | Review records before deletion |
| Proof of disposition | Document completed deletion |
| File plan | Organize retention requirements |
| Audit trail | Track record-related actions |

### Important Concept

**Records Management extends ordinary retention with additional accountability and restrictions.**

---

# 67. Declaring Records

A record is an item designated for formal records management.

Administrators configure retention labels that can mark items as records.

When content is declared a record:

**Certain activities are restricted.**

**Relevant activities are logged.**

**Disposition evidence can be maintained.**

### ELI5

Declaring a record is like placing an official restriction on an important document.

It cannot be handled exactly like an ordinary working file.

---

# 68. Records vs. Regulatory Records

Microsoft Purview distinguishes between:

**Records**

and

**Regulatory Records**

Regulatory records have stricter protections.

### Regulatory Record Restrictions

The current module emphasizes:

**A regulatory record label cannot be removed after application, even by a Global Administrator.**

**The retention period cannot be shortened after the label is applied.**

### Important Warning

The module describes regulatory records as potentially irreversible.

Administrators must explicitly enable the capability through PowerShell.

### Memory Trick

**RECORD = RESTRICTED**

**REGULATORY RECORD = STRICTER, POTENTIALLY IRREVERSIBLE**

---

# 69. Why Regulatory Records Matter

Some industries and organizations must preserve records under strict legal or regulatory requirements.

Examples might include:

- Regulated financial records
- Certain legal documentation
- Required government records
- Other high-value regulated information

### Example

An organization must maintain specific records for a mandated retention period.

It applies an appropriate regulatory record label.

The stricter restrictions reduce the likelihood of unauthorized modification or premature deletion.

### Important Concept

Regulatory record labels should only be used when justified by the organization's actual requirements.

---

# 70. Event-Based Retention

## Big Idea

Event-based retention begins the retention period when a defined event occurs.

This differs from retention beginning when a document is created or modified.

### Examples

**Employee Departure**

Retain specified personnel records for a defined number of years after employment ends.

**Contract Expiration**

Retain a contract for a defined period after its expiration.

**Product Discontinuation**

Retain specified records for a defined period after the product is retired.

### Memory Trick

**EVENT-BASED RETENTION = THE CLOCK STARTS WHEN THE EVENT HAPPENS**

---

# 71. Event-Based Retention Example

Imagine an employee's personnel record was created in 2020.

The employee leaves the organization in 2027.

The applicable requirement states:

> Retain the record for seven years after employment ends.

The retention period begins in 2027, not 2020.

### Conceptual Timeline

```text
2020
Personnel Record Created
        |
        v
2027
Employee Leaves
        |
        v
Retention Trigger Occurs
        |
        v
2034
Seven-Year Retention Period Ends
        |
        v
Disposition Process
```

The dates are illustrative.

### Important Concept

The date that starts retention depends on the applicable policy or event.

---

# 72. Disposition Review

## Big Idea

Disposition review allows authorized reviewers to evaluate information before permanent deletion.

### ELI5

A retention period expires.

Instead of immediately deleting an important document, the system routes it to a designated reviewer.

The reviewer determines whether deletion should proceed or retention should be extended.

### Possible Outcomes

**Approve deletion**

or

**Extend retention**

### Memory Trick

**Disposition Review = Final check before deletion**

---

# 73. Proof of Disposition

## Big Idea

Proof of disposition provides documentation about the completed disposal of records.

It helps organizations demonstrate that deletion occurred according to applicable procedures.

### Example

An auditor asks:

> Can you demonstrate when these records were permanently deleted?

Proof of disposition can support that request.

### Memory Trick

**Proof of Disposition = Evidence that records were properly deleted**

---

# 74. File Plans

## Big Idea

A file plan provides a structured way to organize records and retention requirements.

Microsoft Purview file plans can help organizations:

- Import existing retention schedules
- Review retention labels
- Track retention periods
- Associate records with business functions
- Document applicable regulatory authorities

### ELI5

Imagine an organizational records-management schedule listing:

**Record type**

**Responsible department**

**Required retention period**

**Legal authority**

**Disposition requirements**

A file plan helps organize similar information within Microsoft Purview.

### Memory Trick

**FILE PLAN = Organized retention and records-management schedule**

---

# 75. Data Lifecycle Management vs. Records Management

| Data Lifecycle Management | Records Management |
|---|---|
| General content retention and deletion | Formal management of important records |
| Broad retention policies | Record-specific controls |
| Ordinary retention labels | Record and regulatory record labels |
| Mailbox archiving | Disposition review |
| Inactive mailboxes | Proof of disposition |
| AI interaction retention | Event-based record retention |

### ELI5

**Data Lifecycle Management = Manage information throughout its useful life**

**Records Management = Apply stronger controls to official records**

---

# 76. Complete Data Compliance Scenario

Imagine a government contractor managing employee records, sensitive communications, and legal documentation.

## Compliance Requirements

**Compliance Manager** organizes applicable requirements, controls, and improvement actions.

## Employee Communications

**Communication Compliance** identifies potentially inappropriate messages requiring review.

## Legal Investigation

**eDiscovery** preserves relevant emails and documents.

## Activity Records

**Audit** helps determine who accessed or modified information.

## Retention Requirements

**Data Lifecycle Management** preserves information for required periods.

## Official Records

**Records Management** applies additional protection and disposition requirements.

### Complete Conceptual Flow

```text
ORGANIZATIONAL COMPLIANCE REQUIREMENTS
                 |
                 v
        COMPLIANCE MANAGER
       Assess and track controls
                 |
                 v
      COMMUNICATION COMPLIANCE
       Monitor policy violations
                 |
                 v
          PURVIEW AUDIT
         Record user activity
                 |
                 v
            eDISCOVERY
       Preserve and review evidence
                 |
                 v
      DATA LIFECYCLE MANAGEMENT
         Retain or delete content
                 |
                 v
        RECORDS MANAGEMENT
      Govern official records
```

These capabilities operate together but do not have to be implemented in the sequence shown.

---

# 77. Commonly Confused Capabilities

## Compliance Manager vs. Service Trust Portal

**Compliance Manager = Customer compliance assessment**

**Service Trust Portal = Microsoft provider assurance documents**

---

## Communication Compliance vs. Insider Risk Management

**Communication Compliance = Inappropriate communications**

**Insider Risk Management = Broader suspicious internal behavior**

---

## Communication Compliance vs. DLP

**Communication Compliance = Investigate communications that may violate policy**

**DLP = Prevent or restrict inappropriate sensitive-data handling**

---

## eDiscovery vs. Audit

**eDiscovery = Find and preserve content as evidence**

**Audit = Determine which activities occurred**

---

## eDiscovery Hold vs. Retention Policy

**Hold = Investigation-related preservation**

**Retention Policy = Routine retention and deletion requirements**

---

## Audit Standard vs. Audit Premium

**Standard = Foundational auditing and 180-day retention**

**Premium = Enhanced retention, insights, and API capabilities**

---

## Retention Policy vs. Retention Label

**Policy = Location-level**

**Label = Item-level**

---

## Retention Label vs. Sensitivity Label

**Retention Label = Retention and deletion**

**Sensitivity Label = Classification and protection**

---

## Data Lifecycle Management vs. Records Management

**Data Lifecycle = General information lifecycle**

**Records Management = Formal controls for important records**

---

## Record vs. Regulatory Record

**Record = Additional restrictions**

**Regulatory Record = Strict restrictions, including nonremovable label**

---

## KQL vs. KeyQL

**KQL = Kusto Query Language for security telemetry and analytics**

**KeyQL = Keyword Query Language for eDiscovery content searching**

---

# 78. GRC / ISSO Career Connection

> **Additional professional context:** This section connects Microsoft Purview capabilities to governance, risk, compliance, and information assurance responsibilities. It is not a separate official Microsoft Learn lesson.

This module has strong practical relevance to GRC because it focuses on documented requirements, control assessments, audit evidence, retention, and investigations.

An ISSO or GRC analyst may need to determine whether an organization has:

**Defined applicable compliance requirements**

**Assigned control responsibilities**

**Implemented appropriate procedures**

**Documented compliance evidence**

**Established audit logging**

**Preserved important records**

**Managed investigation evidence**

**Tracked corrective actions**

Microsoft Purview provides tools that can support these activities.

---

# 79. NIST SP 800-53 Relationships

The mappings below are illustrative. Deploying a Microsoft Purview solution does not automatically satisfy the associated control.

| Purview capability | Related NIST control |
|---|---|
| Compliance assessments | CA-2 — Control Assessments |
| Ongoing compliance monitoring | CA-7 — Continuous Monitoring |
| Improvement actions | CA-5 — Plan of Action and Milestones |
| Separation of responsibilities | AC-5 — Separation of Duties |
| Audit event collection | AU-2 — Event Logging |
| Review of audit records | AU-6 — Audit Record Review, Analysis, and Reporting |
| Audit record retention | AU-11 — Audit Record Retention |
| Incident investigations | IR-4 — Incident Handling |
| Information retention and handling | SI-12 — Information Management and Retention |
| Protection of evidence | Applicable audit, incident-response, and records requirements |

### Important Principle

**A tool provides capabilities. An assessment determines whether the organization's controls satisfy the actual requirements.**

---

# 80. Compliance Manager and Control Assessment

Imagine an organization claims that it meets a particular security standard.

An assessor must determine whether:

**The correct requirements are identified.**

**Control responsibilities are assigned.**

**Controls are implemented.**

**Supporting evidence exists.**

**Testing demonstrates effectiveness.**

**Deficiencies are tracked.**

**Outstanding risks are appropriately addressed.**

Compliance Manager can help organize the activities and documentation.

### GRC Memory Trick

**Assessment = Evaluate the control**

**Evidence = Demonstrate implementation**

**Improvement Action = Address the gap**

---

# 81. Compliance Manager and POA&M

## POA&M

**Plan of Action and Milestones**

A POA&M tracks security deficiencies and planned corrective actions.

### Example

```text
Finding:
Privileged account access reviews are not
performed at the required frequency.

Risk:
Excessive or unauthorized privileged access.

Corrective Action:
Implement a documented periodic access
review process.

Responsible Owner:
Identity and Access Management Team

Required Evidence:
Approved procedure, review records,
and implementation validation.

Status:
In Progress
```

Compliance Manager improvement actions can help track comparable remediation work.

However, a Compliance Manager action is not automatically a complete formal POA&M entry.

### Important Distinction

**Improvement Action = Compliance task**

**POA&M = Formal weakness and remediation tracking**

---

# 82. Audit Evidence and Investigation Integrity

Audit records can support investigations, but their value depends on their reliability.

An assessor should consider:

**Coverage**

Were relevant activities logged?

**Retention**

Were records preserved for the required period?

**Access Control**

Who could modify or retrieve the evidence?

**Time Information**

Are timestamps useful and reliable?

**Completeness**

Does the evidence cover the relevant investigation period?

**Documentation**

Can investigators demonstrate what was examined and concluded?

### GRC Principle

**Having audit logs is not the same as having complete, reliable investigative evidence.**

---

# 83. Legal Holds and Evidence Preservation

An important responsibility during legal or administrative investigations is ensuring relevant evidence is preserved.

### Example

An organization receives a legal preservation request involving employee communications.

The legal team determines what content is relevant.

Authorized personnel establish appropriate eDiscovery holds.

The organization preserves the information until the legal obligation is resolved.

### Important Concept

Routine deletion policies should not be allowed to undermine applicable legal preservation obligations.

Organizations must understand how holds, retention, and records-management rules interact.

---

# 84. Records Management and Government Work

Government organizations frequently operate under formal records schedules and retention requirements.

Records Management capabilities may support:

- Document classification
- Retention schedules
- Preservation of official records
- Controlled deletion
- Disposition documentation
- Audit accountability

### Example

An organization must retain specified official correspondence for a defined period following an operational event.

Event-based retention and appropriate record labeling may support that requirement.

### Important Limitation

The applicable retention schedule and legal authority must be established by the organization.

Microsoft Purview supplies technical capabilities but does not determine the legal retention requirement automatically.

---

# 85. Compliance and AI Governance

The current module addresses several ways Microsoft Purview supports AI-related compliance.

| Capability | AI-related use |
|---|---|
| Compliance Manager | Assess AI regulations and standards |
| Communication Compliance | Review AI prompts and responses for policy concerns |
| eDiscovery | Search and preserve supported AI-related evidence |
| Audit | Record supported Copilot interactions |
| Data Lifecycle Management | Apply retention to supported AI interactions |
| Records Management | Apply appropriate recordkeeping controls |

### GRC Connection

Organizations adopting AI should evaluate:

**Which interactions must be monitored?**

**Which data must be retained?**

**Which activities require audit evidence?**

**Who may review AI conversations?**

**Which AI outputs may constitute official records?**

These responsibilities should be addressed through applicable policy and risk management processes.

---

# 86. SC-900 High-Value Product Recognition

| If the question mentions... | Think... |
|---|---|
| Evaluate compliance posture | Compliance Manager |
| Compliance improvement actions | Compliance Manager |
| Customer and Microsoft control responsibilities | Compliance Manager |
| Track compliance points | Compliance Score |
| Group controls for ISO-related evaluation | Assessment |
| Prebuilt regulatory templates | Compliance Manager |
| Detect harassment in messages | Communication Compliance |
| Review regulatory communication violations | Communication Compliance |
| Review AI prompts for inappropriate communication | Communication Compliance |
| Preserve evidence for legal investigation | eDiscovery Hold |
| Organize a legal investigation | eDiscovery Case |
| Analyze collected legal evidence | Review Set |
| Search text in scanned evidence | OCR |
| Preserve conversation context | Conversation Threading |
| Search content using natural language | Security Copilot with KeyQL |
| Identify who downloaded a file | Audit |
| Find mailbox activity | Purview Audit |
| Search user and admin activities | Unified Audit Log |
| Basic audit capabilities | Audit Standard |
| Advanced audit retention and insights | Audit Premium |
| Standard audit retention | 180 days |
| Default Premium retention for specified records | One year |
| Extended eligible audit retention | Up to ten years |
| Retain all documents in one SharePoint site | Retention Policy |
| Retain individual documents differently | Retention Label |
| Publish available retention labels | Retention Label Policy |
| Preserve departed employee's mailbox | Inactive Mailbox |
| Apply retention to AI interactions | Data Lifecycle Management |
| Declare an official record | Records Management |
| Apply irreversible regulatory record labeling | Regulatory Record |
| Start retention after contract expiration | Event-Based Retention |
| Review records before deletion | Disposition Review |
| Document permanent record deletion | Proof of Disposition |
| Organize retention schedules | File Plan |

---

# 87. Final Module 3 Cram Sheet

```text
MICROSOFT PURVIEW DATA COMPLIANCE
= MANAGE REGULATORY AND INFORMATION REQUIREMENTS

COMPLIANCE MANAGER
= ASSESS AND IMPROVE COMPLIANCE POSTURE

COMPLIANCE SCORE
= PROGRESS TOWARD IMPROVEMENT ACTIONS

YOUR POINTS
= CUSTOMER-MANAGED ACTIONS

MICROSOFT-MANAGED POINTS
= PROVIDER-MANAGED ACTIONS

CONTROL
= SPECIFIC COMPLIANCE REQUIREMENT

ASSESSMENT
= GROUP OF RELATED CONTROLS

REGULATION
= APPLICABLE STANDARD OR REQUIREMENT

IMPROVEMENT ACTION
= TASK TO IMPROVE CONTROL IMPLEMENTATION

SHARED CONTROL
= MICROSOFT AND CUSTOMER RESPONSIBILITIES

COMMUNICATION COMPLIANCE
= DETECT AND REVIEW INAPPROPRIATE MESSAGES

COMMUNICATION WORKFLOW
= CONFIGURE → INVESTIGATE → REMEDIATE → MAINTAIN

eDISCOVERY
= ELECTRONIC EVIDENCE DISCOVERY

ESI
= ELECTRONICALLY STORED INFORMATION

eDISCOVERY CASE
= ORGANIZE INVESTIGATION EVIDENCE

eDISCOVERY HOLD
= PRESERVE RELEVANT INFORMATION

REVIEW SET
= COLLECTED EVIDENCE FOR REVIEW

OCR
= EXTRACT SEARCHABLE TEXT FROM IMAGES

CONVERSATION THREADING
= PRESERVE DISCUSSION CONTEXT

KeyQL
= KEYWORD QUERY LANGUAGE

KQL
= KUSTO QUERY LANGUAGE

PURVIEW AUDIT
= RECORD USER AND ADMINISTRATOR ACTIONS

UNIFIED AUDIT LOG
= CENTRALIZED MICROSOFT 365 ACTIVITY RECORDS

AUDIT STANDARD
= BASIC AUDITING + 180-DAY RETENTION

AUDIT PREMIUM
= LONGER RETENTION + INTELLIGENT INSIGHTS

AUDIT PREMIUM DEFAULT
= ONE YEAR FOR SPECIFIED AUDIT RECORDS

EXTENDED AUDIT RETENTION
= UP TO TEN YEARS WITH ELIGIBLE LICENSING

DATA LIFECYCLE MANAGEMENT
= RETAIN AND DELETE INFORMATION

RETENTION POLICY
= LOCATION-LEVEL RETENTION

RETENTION LABEL
= ITEM-LEVEL RETENTION

RETENTION LABEL POLICY
= PUBLISH AVAILABLE RETENTION LABELS

RETAIN ONLY
= PRESERVE INFORMATION

DELETE ONLY
= REMOVE CONTENT AFTER DEFINED PERIOD

RETAIN THEN DELETE
= PRESERVE, THEN DISPOSE

INACTIVE MAILBOX
= PRESERVE DEPARTED USER MAILBOX CONTENT

RECORDS MANAGEMENT
= FORMAL MANAGEMENT OF IMPORTANT RECORDS

RECORD
= CONTENT WITH ADDITIONAL RESTRICTIONS

REGULATORY RECORD
= STRICTER RESTRICTIONS AND NONREMOVABLE LABEL

EVENT-BASED RETENTION
= START RETENTION AFTER A DEFINED EVENT

DISPOSITION REVIEW
= APPROVE OR EXTEND BEFORE DELETION

PROOF OF DISPOSITION
= EVIDENCE OF PERMANENT RECORD DELETION

FILE PLAN
= ORGANIZED RETENTION AND RECORDS SCHEDULE

SERVICE TRUST PORTAL
= MICROSOFT PROVIDER ASSURANCE

COMPLIANCE MANAGER
= CUSTOMER COMPLIANCE ASSESSMENT

DLP
= PREVENT INAPPROPRIATE DATA SHARING

COMMUNICATION COMPLIANCE
= REVIEW INAPPROPRIATE COMMUNICATIONS

INSIDER RISK MANAGEMENT
= INVESTIGATE BROADER RISKY INTERNAL BEHAVIOR

eDISCOVERY
= PRESERVE AND REVIEW EVIDENCE

AUDIT
= ESTABLISH WHAT ACTIONS OCCURRED

DATA LIFECYCLE
= GOVERN RETENTION AND DELETION

RECORDS MANAGEMENT
= PRESERVE OFFICIAL RECORD INTEGRITY
```

---

# 88. Final Mental Model

Imagine an organization must demonstrate compliance with regulations governing its documents, communications, and security operations.

**Microsoft Purview Compliance Manager** identifies relevant requirements, organizes control assessments, assigns improvement actions, and tracks progress.

**Communication Compliance** helps detect and review communications that may violate organizational or regulatory policies.

A suspicious event requires formal investigation.

**Microsoft Purview Audit** helps determine which activities occurred and who performed them.

**Microsoft Purview eDiscovery** helps preserve, locate, review, and export relevant electronic information.

The organization must also maintain records according to applicable retention requirements.

**Data Lifecycle Management** determines which information should be preserved and when information may be deleted.

**Records Management** applies stricter controls to important documents, including regulatory records and event-based retention.

Together, these solutions support:

**Regulatory Compliance**

**Accountability**

**Evidence Preservation**

**Information Lifecycle Management**

**Records Integrity**

**Risk Reduction**

The central concept is:

**Microsoft Purview Data Compliance helps organizations demonstrate accountability for how information is managed, monitored, preserved, investigated, and disposed of.**

---

# Official Microsoft Learn References

The following instructional pages were verified against the live module on November 23, 2026.

[Module Overview](https://learn.microsoft.com/en-us/training/modules/describe-purview-risk-compliance-governance/)

[Introduction](https://learn.microsoft.com/en-us/training/modules/describe-purview-risk-compliance-governance/1-introduction)

[Describe Compliance Manager](https://learn.microsoft.com/en-us/training/modules/describe-purview-risk-compliance-governance/4-describe-compliance-manager)

[Describe Communication Compliance](https://learn.microsoft.com/en-us/training/modules/describe-purview-risk-compliance-governance/5-describe-communication-compliance)

[Describe eDiscovery](https://learn.microsoft.com/en-us/training/modules/describe-purview-risk-compliance-governance/3-describe-ediscovery)

[Describe Audit in Microsoft Purview](https://learn.microsoft.com/en-us/training/modules/describe-purview-risk-compliance-governance/2-describe-audit)

[Describe Data Lifecycle Management](https://learn.microsoft.com/en-us/training/modules/describe-purview-risk-compliance-governance/6-describe-data-lifecycle-management)

[Describe Microsoft Purview Records Management](https://learn.microsoft.com/en-us/training/modules/describe-purview-risk-compliance-governance/7-describe-records-management)

[Module Assessment](https://learn.microsoft.com/en-us/training/modules/describe-purview-risk-compliance-governance/8-knowledge-check)

[Summary and Resources](https://learn.microsoft.com/en-us/training/modules/describe-purview-risk-compliance-governance/9-summary)

---

# Additional Official Microsoft References

[Microsoft Purview Data Compliance Solutions](https://learn.microsoft.com/en-us/purview/purview-compliance)

[Microsoft Purview Portal](https://purview.microsoft.com/)

[Microsoft Purview Overview](https://learn.microsoft.com/en-us/purview/purview)
