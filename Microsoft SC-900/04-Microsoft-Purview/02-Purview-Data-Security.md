# SC-900 — Section 4, Module 2
# Describe the Data Security Solutions of Microsoft Purview

> **Source:** Microsoft Learn — SC-900  
> **Learning Path:** Introduction to Microsoft Purview and Microsoft's privacy principles  
> **Module:** Describe the data security solutions of Microsoft Purview  
> **Verified against current Microsoft Learn content:** November 23, 2026  
> **Duration:** 55 minutes | 10 units | 1,100 XP  
> **Official Module:** https://learn.microsoft.com/en-us/training/modules/describe-purview-data-solutions/

---

# Module Overview

Microsoft Purview provides integrated solutions that help organizations discover, classify, protect, monitor, and investigate sensitive information.

This module focuses on **data security**.

It explains how organizations can protect information across Microsoft 365, endpoints, cloud platforms, third-party applications, and AI interactions.

## The Big Idea

An organization cannot adequately protect sensitive information unless it understands:

**What information is sensitive?**

**Where is that information located?**

**Who can access it?**

**How is it being used?**

**What should happen when someone handles it inappropriately?**

Microsoft Purview provides different tools to answer these questions.

## Seven Major Topics

| Capability | Primary purpose |
|---|---|
| Information Protection | Discover and classify sensitive data |
| Sensitivity Labels | Classify and apply protection settings |
| Data Loss Prevention (DLP) | Detect and restrict inappropriate sharing |
| Insider Risk Management | Identify and investigate risky internal activities |
| Adaptive Protection | Dynamically adjust controls based on insider risk |
| Data Security Posture Management (DSPM) | Provide unified visibility into data security risks |
| Data Security Investigations | Investigate the content and impact of data security incidents |

### ELI5

Imagine an organization maintaining thousands of sensitive records.

**Information Protection** identifies which records contain sensitive information.

**Sensitivity Labels** mark important records and can restrict who may access them.

**DLP** prevents someone from improperly sending those records outside the organization.

**Insider Risk Management** identifies potentially suspicious behavior involving employees or other internal users.

**Adaptive Protection** increases or decreases restrictions according to the user's current risk.

**DSPM** provides a broad view of where the organization's sensitive data is exposed.

**Data Security Investigations** helps investigators determine what information was affected when an incident occurs.

### Master Memory Trick

**CLASSIFY → LABEL → PROTECT → MONITOR → ADAPT → ASSESS → INVESTIGATE**

---

# 1. Microsoft Purview Information Protection

## Big Idea

Microsoft Purview Information Protection helps organizations identify and protect sensitive information.

Before an organization can implement effective data protection, it needs to understand the data it possesses.

Examples include:

- Personally identifiable information
- Financial records
- Medical information
- Employee records
- Customer information
- Intellectual property
- Confidential business documents

### ELI5

Imagine sorting thousands of records into categories.

Some documents are public.

Others contain internal business information.

Some contain extremely sensitive personal or financial information.

Microsoft Purview helps identify those differences so the organization can apply appropriate security controls.

## Data Classification

**Data classification = Identifying and categorizing information according to its characteristics or sensitivity.**

Classification can occur through several mechanisms.

The current module emphasizes:

**Sensitive Information Types**

**Trainable Classifiers**

---

# 2. Sensitive Information Types — SITs

## Big Idea

A **Sensitive Information Type (SIT)** uses pattern-based detection to recognize certain categories of sensitive information.

Examples include:

- Social Security numbers
- Credit card numbers
- Passport numbers
- Bank account numbers
- Health service numbers

### ELI5

Imagine searching a document for a credit card number.

Credit card numbers generally follow recognizable formats.

A sensitive information type can use those patterns and supporting information to determine whether a document likely contains sensitive information.

### Memory Trick

**SIT = Recognize sensitive data using patterns**

---

# 3. How Sensitive Information Types Work

Microsoft Learn describes four important components.

## Primary Element

The primary element is the main pattern or information the classifier looks for.

Examples include:

- Regular expression
- Keyword list
- Keyword dictionary
- Function
- Pattern validated by a checksum

### Regular Expression — Regex

A regular expression is a pattern used to recognize text with particular characteristics.

For example, an organization might look for a specific employee identification-number format.

## Supporting Elements

Supporting elements provide additional evidence that a pattern represents sensitive information.

### Example

A nine-digit number appears in a document.

That number alone may not be a Social Security number.

However, the nearby phrase:

> Social Security Number

provides supporting evidence.

## Confidence Level

Confidence describes how strongly the detected evidence supports a match.

Microsoft Purview uses:

- Low confidence
- Medium confidence
- High confidence

High-confidence detection generally requires stronger supporting evidence.

### Important Distinction

A higher confidence threshold can reduce false positives, but it may also miss some legitimate matches.

## Proximity

Proximity determines how close supporting evidence must appear to the primary element.

It is measured in characters.

### Memory Trick

**Primary = Pattern**

**Supporting = Additional evidence**

**Confidence = Strength of evidence**

**Proximity = Distance between evidence**

---

# 4. Four Categories of Sensitive Information Types

Microsoft Purview supports four major categories.

## Built-In Sensitive Information Types

Microsoft creates and maintains predefined SITs.

Examples include common financial, government, and identity-related information.

Administrators cannot directly modify the original built-in definition, but they can use it as the basis for custom variations.

## Named Entity Sensitive Information Types

Detect information such as:

- Person names
- Physical addresses
- Medical terms
- Medical conditions

Microsoft describes two forms:

**Unbundled:** Narrowly focused detection.

**Bundled:** Broader detection across an entire category.

## Custom Sensitive Information Types

Organizations can define their own detection rules.

Examples:

- Internal employee numbers
- Organization-specific account identifiers
- Proprietary project codes

These may use patterns, keywords, and dictionaries.

## Exact Data Match — EDM

EDM-based classification identifies values that match known sensitive data maintained by the organization.

### Example

An HR database contains a defined list of employee identifiers.

The organization wants to identify those exact identifiers when they appear in other content.

EDM supports this scenario.

---

# 5. SIT vs. Exact Data Match

| Sensitive Information Type | Exact Data Match |
|---|---|
| Recognizes a defined type of sensitive information | Recognizes known specific sensitive values |
| Uses patterns and supporting evidence | Uses protected reference data |
| Credit card number format | Specific customer account numbers |
| Passport-number pattern | Exact employee identifiers |

### Memory Trick

**SIT = Does it match the TYPE?**

**EDM = Does it match a KNOWN VALUE?**

EDM is a specialized SIT-based classification approach, not an unrelated classification platform.

---

# 6. Trainable Classifiers

## Big Idea

Trainable classifiers use artificial intelligence and machine learning to classify content based on its characteristics and meaning.

Pattern recognition works well for structured information.

However, some documents cannot be recognized reliably using a fixed numerical pattern.

Examples include:

- Resumes
- Employment agreements
- Legal contracts
- Financial documents
- Customer complaints
- Harassment-related communications

### ELI5

A credit card number has a recognizable pattern.

A resume does not necessarily have one predictable format.

A machine-learning classifier can recognize characteristics of a resume even when different applicants use different document layouts.

### Memory Trick

**SIT = PATTERN**

**Trainable Classifier = MEANING AND CHARACTERISTICS**

---

# 7. Pretrained vs. Custom Trainable Classifiers

Microsoft Purview provides two classifier types.

## Pretrained Classifiers

Microsoft develops and trains these classifiers.

They can be available for use without additional customer training.

Examples include categories involving:

- Human resources documents
- Financial records
- Legal materials
- Harassment
- Profanity
- Threatening communications

## Custom Trainable Classifiers

Organizations can train their own classifiers.

### Example

A company has a specialized document type that Microsoft does not already recognize.

The company trains a classifier using representative examples.

The classifier learns characteristics associated with that category.

---

# 8. Training a Custom Classifier

The current Microsoft Learn lesson describes a process involving:

## Seeding

Provide examples of documents belonging to the desired category.

Also provide examples that do not belong to it.

## Training

Machine learning analyzes the examples to build a classification model.

## Validation

Test the classifier against known examples.

Review results involving:

- True positives
- True negatives
- False positives
- False negatives

## Publication

Once the model performs satisfactorily, it can be published and used with supported Microsoft Purview policies.

### Important Limitation

The current module states that trainable classifiers work with **unencrypted items**.

This is important when evaluating whether the classifier can actually inspect particular content.

---

# 9. Classification and AI Interactions

The current module extends data classification to AI interactions.

Sensitive information types and trainable classifiers can identify sensitive information associated with supported generative AI applications.

### Example

An employee enters customer credit card information into an AI prompt.

Microsoft Purview classification capabilities can help detect that the interaction contains sensitive information.

Classification information can appear in Purview reporting and Activity Explorer.

### Important Concept

**The same classification principles that protect documents and email can also help protect information used in AI interactions.**

---

# 10. Content Explorer

## Big Idea

Content Explorer helps administrators determine:

**WHERE sensitive or labeled information exists.**

It provides visibility into information classified using:

- Sensitive information types
- Sensitivity labels
- Retention labels

Supported sources include Microsoft 365 locations such as:

- Exchange
- SharePoint
- OneDrive

### ELI5

Imagine asking:

> Where are all the documents containing credit card information?

Content Explorer helps answer that question.

## Content Explorer Capabilities

Administrators can examine:

- Numbers of classified items
- Types of classification
- Locations containing sensitive data
- Distribution of sensitive content

Authorized administrators may be able to inspect source content.

### Important Security Requirement

Access to Content Explorer is restricted because it may expose sensitive document contents.

Appropriate role permissions are required.

### Memory Trick

**CONTENT EXPLORER = WHERE IS THE DATA?**

---

# 11. Activity Explorer

## Big Idea

Activity Explorer shows how users interact with sensitive or labeled content.

It answers:

**WHAT ARE USERS DOING WITH THE DATA?**

Examples include:

- Applying sensitivity labels
- Changing sensitivity labels
- Downgrading labels
- Copying files to removable storage
- Copying files to network shares
- Printing sensitive documents
- Other monitored activities involving protected information

### ELI5

Content Explorer tells you where a confidential document exists.

Activity Explorer helps determine whether someone copied, printed, relabeled, or otherwise interacted with it.

## Endpoint Integration

Activity Explorer can display relevant Endpoint DLP activities from supported Windows and macOS devices.

### Memory Trick

**CONTENT EXPLORER = LOCATION**

**ACTIVITY EXPLORER = ACTION**

---

# 12. Content Explorer vs. Activity Explorer

| Content Explorer | Activity Explorer |
|---|---|
| Where is sensitive content? | What happened to sensitive content? |
| Shows classified items | Shows monitored user activity |
| Shows data locations | Shows printing, copying, labeling |
| Helps understand data distribution | Helps assess data-handling behavior |

### Exam Examples

**Find files containing Social Security numbers:** Content Explorer.

**Determine who downgraded a document's sensitivity label:** Activity Explorer.

**Review where confidential documents are stored:** Content Explorer.

**Review USB-copying activity involving sensitive files:** Activity Explorer.

---

# 13. Sensitivity Labels

## Big Idea

Sensitivity labels classify and protect organizational information.

A sensitivity label is stored in the content's metadata.

The label can remain associated with the document or email as it moves between supported locations.

### ELI5

Imagine stamping a document:

> CONFIDENTIAL

But the stamp also carries technical security rules.

Depending on its configuration, a label may restrict access, encrypt the file, or apply visible markings.

### Example Label Structure

```text
Public
General
Confidential
Highly Confidential
```

Organizations create label categories appropriate to their needs.

### Memory Trick

**Sensitivity Label = CLASSIFY AND PROTECT**

---

# 14. Three Properties of Sensitivity Labels

Microsoft Learn emphasizes three characteristics.

## Customizable

Organizations define the labels they require.

## Clear Text Metadata

A sensitivity label is stored in readable metadata.

Supported third-party services can read that classification information and apply appropriate controls.

## Persistent

The label remains associated with the content in supported workflows.

Its protection settings can continue to apply as the content moves.

### Important Detail

An individual item supporting sensitivity labels can have **one sensitivity label at a time**.

A sensitivity label and a retention label are different types of labels and can serve different purposes.

---

# 15. What Sensitivity Labels Can Do

Sensitivity labels can provide several protections.

## Encryption

Restrict access to authorized identities.

Administrators can define supported permissions and access durations.

## Content Markings

Apply visible markings such as:

- Headers
- Footers
- Watermarks

Available markings depend on the content type.

## Automatic Labeling

Automatically apply a label based on defined conditions.

## Recommended Labeling

Suggest a label when sensitive information is detected.

## Container Protection

Apply certain protection settings to collaborative environments such as:

- Teams
- Microsoft 365 Groups
- SharePoint sites
- Viva Engage communities
- Loop workspaces

## Sharing Controls

Configure supported default sharing behaviors for SharePoint and OneDrive.

## Classification-Only Labels

Apply a classification without necessarily applying encryption or another technical restriction.

### Important Concept

**A sensitivity label does not always have to encrypt a document.**

A label may simply classify content or apply other available settings.

---

# 16. Sensitivity Label Scopes

A label's scope determines which content types and settings it applies to.

The current module identifies four major scopes.

| Scope | Applies to |
|---|---|
| Files and other data assets | Documents, PDFs, supported Fabric/Power BI content |
| Emails | Outlook email |
| Meetings | Meetings and supported Teams collaboration settings |
| Groups and sites | Teams, SharePoint, Microsoft 365 Groups, and other supported containers |

### Important Distinction

Applying a sensitivity label to a Teams site or SharePoint site does **not automatically label every document inside that container**.

Container labels primarily control supported settings for the container.

### Memory Trick

**File label = Protect the item**

**Container label = Protect the collaborative environment**

---

# 17. Sensitivity Labels and Microsoft 365 Copilot

The current Learn module explains that Microsoft 365 Copilot respects supported sensitivity labels and their protections.

When a Copilot response uses content from multiple labeled items, it can inherit the most restrictive applicable label.

If information is protected through encryption, the user's permissions are checked before the content is used in supported Copilot workflows.

### ELI5

A user should not gain unrestricted access to confidential information simply because they ask an AI assistant to summarize it.

The underlying access controls still matter.

### Important Concept

**AI assistance does not remove established information protection requirements.**

---

# 18. Sensitivity Label Policies

## Big Idea

Creating a sensitivity label is not the same thing as making it available to users.

Labels are published through:

**Sensitivity Label Policies**

### ELI5

The label defines what the classification and protection mean.

The policy determines how the organization's users receive and use the label.

## Label Policy Capabilities

Administrators can:

- Publish labels to specific users or groups
- Configure default labels
- Require mandatory labeling
- Require justification when removing or lowering a label
- Provide links to organizational labeling guidance

---

# 19. Sensitivity Label vs. Label Policy

| Sensitivity Label | Sensitivity Label Policy |
|---|---|
| Defines classification and protection | Publishes and governs label usage |
| Can encrypt content | Determines who sees available labels |
| Can add markings | Can configure default labels |
| Can restrict access | Can require labeling |
| Travels with supported content | Can require downgrade justification |

### Example

An organization creates:

**Highly Confidential**

The label encrypts documents and restricts access to authorized employees.

A label policy publishes that label to the Finance department and requires users to classify applicable documents.

### Memory Trick

**LABEL = PROTECTION RULES**

**LABEL POLICY = DISTRIBUTION AND USAGE RULES**

---

# 20. Mandatory Labeling and Downgrade Justification

## Mandatory Labeling

Requires users to apply an appropriate label before completing certain actions.

Examples include:

- Saving a document
- Sending an email
- Creating supported collaborative spaces

## Downgrade Justification

Requires a user to explain why they are removing a label or changing to a less sensitive classification.

### Example

A user changes a document from:

**Confidential → Public**

Microsoft Purview can require an explanation.

### GRC Connection

These features support accountability and consistent application of organizational data-handling policies.

---

# 21. Microsoft Purview Data Loss Prevention — DLP

## Big Idea

Microsoft Purview DLP helps organizations detect, monitor, and prevent inappropriate sharing or handling of sensitive information.

### ELI5

Imagine an employee tries to send a confidential spreadsheet containing customer Social Security numbers to a personal email address.

DLP can detect the sensitive information and apply the organization's configured policy.

The action may be:

- Allowed with a warning
- Blocked unless justified
- Blocked completely

### Memory Trick

**DLP = DON'T LET SENSITIVE DATA LEAK**

---

# 22. What DLP Protects

DLP can protect sensitive information in different states.

## Data at Rest

Stored information.

Examples:

- SharePoint documents
- OneDrive files
- Stored email content

## Data in Transit

Information being transferred.

Examples:

- Email attachments
- Teams messages
- File sharing

## Data in Use

Information actively handled by a user or application.

Examples:

- Printing a document
- Copying information to USB storage
- Using an application to access protected files

### Memory Trick

**REST = STORED**

**TRANSIT = MOVING**

**USE = BEING HANDLED**

---

# 23. DLP Protection Locations

The current module identifies broad DLP coverage across supported locations.

Examples include:

- Exchange Online
- Microsoft Teams
- SharePoint Online
- OneDrive
- Word, Excel, and PowerPoint
- Windows 10 and 11 endpoints
- Supported macOS endpoints
- Non-Microsoft cloud applications
- On-premises file shares
- On-premises SharePoint
- Microsoft Fabric and Power BI
- Microsoft Edge for Business

Supported actions and licensing vary by location.

### Important Concept

**DLP is not limited to email.**

It can protect sensitive information across multiple services, devices, and workflows.

---

# 24. How DLP Detects Sensitive Data

DLP can use classification technologies including:

- Sensitive information types
- Regular expressions
- Keywords
- Supporting evidence
- Trainable classifiers
- Sensitivity labels
- Other supported policy conditions

### Example

A policy detects documents containing financial account information.

The policy can apply a protective action if a user attempts to share the document with an unauthorized destination.

### Key Relationship

**Classification identifies sensitive content.**

**DLP determines which monitored actions should be restricted or allowed.**

---

# 25. DLP Protective Actions

Microsoft Learn identifies several possible protective actions.

## Policy Tip

Display an informative warning.

### Example

> This document appears to contain sensitive information.

## Block with Override

Block the activity but allow the user to override the restriction when permitted.

The system can capture the user's justification.

## Block without Override

Prevent the action entirely.

## Quarantine

Move supported sensitive items to a secure quarantine location.

## Protect Teams Communications

Prevent sensitive content from being displayed in supported Teams chat scenarios.

### Important Concept

**DLP does not always block an activity outright.**

The policy determines the response.

---

# 26. DLP Policy Configuration

A DLP policy contains several important elements.

## Information Type

What sensitive information should the policy identify?

## Administrative Scope

Which users, groups, or administrative units are within scope?

## Location

Where should the policy apply?

## Conditions

What circumstances trigger the policy?

## Actions

What happens when the conditions are met?

### Example

```text
Policy: Protect Employee Records

Information:
Employee identification numbers

Locations:
Exchange, SharePoint, OneDrive

Condition:
Sensitive content shared externally

Action:
Block sharing and notify the user
```

This is an illustrative policy, not a complete configuration procedure.

### Memory Trick

**WHAT DATA → WHERE → UNDER WHAT CONDITIONS → WHAT ACTION**

---

# 27. Endpoint Data Loss Prevention

## Big Idea

Endpoint DLP monitors and protects sensitive information used on supported Windows and macOS devices.

Monitored activities can include:

- Creating files
- Renaming files
- Copying files to USB storage
- Copying files to network shares
- Printing
- Using unapproved applications or browsers

### ELI5

An employee downloads a sensitive document to their workstation.

The document is no longer only inside SharePoint or OneDrive.

Endpoint DLP can help monitor and control how the employee handles that file.

### Example

An employee tries to copy confidential customer records to a removable USB drive.

An Endpoint DLP policy can restrict that activity.

### Memory Trick

**ENDPOINT DLP = Protect sensitive data on user devices**

---

# 28. DLP in Microsoft Teams

DLP supports Teams chat and channel communications, including supported private-channel scenarios.

### Example

An employee enters a Social Security number in a Teams message.

A DLP policy detects the sensitive information.

The policy prevents the content from appearing and provides an explanation.

### Exam Shortcut

**Prevent sensitive information from being shared in Teams = Microsoft Purview DLP**

Not Microsoft Defender for Office 365.

---

# 29. DLP and AI Interactions

The current module describes DLP protection for supported generative AI interactions.

### Example

An employee attempts to paste confidential financial information into a third-party AI website.

An appropriately configured Endpoint DLP policy can:

- Warn the user
- Require justification where supported
- Block the action

### Important Concept

AI applications introduce additional destinations through which sensitive information might be disclosed.

Microsoft Purview extends existing data protection principles to these interactions.

### Memory Trick

**DLP + AI = Prevent sensitive data from entering inappropriate AI workflows**

---

# 30. DLP Alerts and Activity Explorer

Monitored DLP activities are recorded in the Microsoft 365 audit log.

Relevant information also appears in Activity Explorer.

When configured alert conditions are met, DLP can generate alerts.

These alerts may appear in:

- DLP alert management
- Microsoft Defender portal incidents

### Example

A user repeatedly attempts to share confidential files externally.

DLP generates alerts associated with the activity.

A security analyst reviews the alerts and decides whether further investigation is warranted.

### Important Distinction

**DLP Policy = Define what to monitor and restrict**

**DLP Alert = Notification of relevant activity**

**Activity Explorer = Review the recorded actions**

---

# 31. DLP and Microsoft Security Copilot

Microsoft Purview DLP integrates with Microsoft Security Copilot.

Supported experiences include:

## Standalone

Analysts ask questions using supported DLP-related capabilities.

## Embedded

Copilot functionality appears in the Purview DLP interface.

The current module identifies:

- Alert summarization
- Alert Triage Agent

## DLP Alert Triage Agent

The agent evaluates alerts using factors such as:

- Content risk
- Exfiltration risk
- Policy risk

It helps prioritize alerts requiring analyst attention.

### Memory Trick

**DLP Alert Triage Agent = Prioritize data-loss alerts**

---

# 32. Microsoft Purview Insider Risk Management

## Big Idea

Microsoft Purview Insider Risk Management helps organizations identify, investigate, and respond to potentially risky activities involving people inside the organization.

### ELI5

Not every security risk comes from an external hacker.

An employee might:

- Accidentally share confidential information
- Intentionally steal intellectual property
- Download sensitive records before leaving
- Violate security policies
- Misuse business information

Insider Risk Management helps identify suspicious activity associated with these situations.

### Important Concept

**Insider risk does not automatically mean malicious intent.**

Risk may arise from negligence, mistakes, compromised accounts, or deliberate misconduct.

---

# 33. Common Insider Risk Scenarios

The current module identifies scenarios including:

- Confidential data leaks
- Intellectual property theft
- Data theft by departing employees
- Fraud
- Insider trading
- Security policy violations
- Risky AI usage
- Misuse of healthcare information
- Risky behavior associated with organizational changes

### Example

An employee approaching departure downloads a large volume of confidential files.

Insider Risk Management can identify that activity as potentially requiring investigation.

### Memory Trick

**INSIDER RISK = Suspicious internal behavior involving organizational information**

---

# 34. Insider Risk Management Principles

Microsoft Learn identifies four guiding principles.

## Transparency

Balance organizational risk with user privacy.

## Configurable

Use policies appropriate to business, regional, and organizational requirements.

## Integrated

Coordinate with other Microsoft Purview solutions.

## Actionable

Provide information that supports appropriate investigation and response.

### Memory Trick

**Transparent — Configurable — Integrated — Actionable**

---

# 35. Privacy by Design

Insider Risk Management handles sensitive information about user behavior.

Therefore, organizations must carefully consider:

- Access restrictions
- Appropriate investigation purposes
- User privacy
- Legal requirements
- Reviewer accountability
- Organizational policies

### Important Principle

**A risk detection is not proof of employee misconduct.**

An authorized investigation must evaluate the evidence in context.

This distinction is especially important in government, regulated, and employment environments.

---

# 36. Insider Risk Analytics

Insider Risk Analytics can help identify areas of potential insider risk before the organization establishes specific insider-risk policies.

### Example

An organization wants to understand whether certain categories of internal data-handling activity create elevated risk.

Analytics can help the organization identify appropriate areas for monitoring and policy development.

### Memory Trick

**Insider Risk Analytics = Evaluate potential risks before configuring specific policies**

---

# 37. Insider Risk Management Workflow

Microsoft Learn describes five stages.

**Policies → Alerts → Triage → Investigate → Action**

## Policies

Define which indicators and activities should be evaluated.

## Alerts

Notify reviewers when activity matches relevant policy conditions.

## Triage

Determine whether an alert requires investigation.

## Investigate

Create or use a case to examine the relevant evidence.

## Action

Resolve or escalate the case according to its findings.

### Memory Trick

**POLICY → ALERT → TRIAGE → CASE → ACTION**

---

# 38. Insider Risk Policies

Policies define which activities should be examined.

Policy templates can support different risk scenarios.

Examples:

- Departing employee data theft
- Confidential information leaks
- Security policy violations
- Risky AI usage

Policies may also define:

- Included users
- Monitored indicators
- Monitoring periods
- Priority services
- Conditions that generate alerts

### Important Distinction

**Policy = What Purview should look for**

**Alert = Activity requiring evaluation**

---

# 39. Insider Risk Alerts

An alert is generated when activity meets applicable policy conditions.

The alert dashboard helps reviewers identify:

- Alerts requiring review
- Severity
- Relevant activities
- Associated users
- Alert trends

### ELI5

An alert is a signal that something potentially concerning occurred.

It is not automatically a completed investigation.

---

# 40. Insider Risk Triage

Triage determines how an alert should be handled.

Reviewers may:

- Dismiss an alert
- Open a new case
- Add an alert to an existing case

### Memory Trick

**TRIAGE = Decide whether the alert warrants investigation**

---

# 41. Insider Risk Cases

## Big Idea

A case consolidates information needed for a formal investigation.

The current module identifies several investigative tools.

## User Activity

An interactive timeline or chart showing relevant activity.

## Content Explorer

Review content associated with the alert.

## Case Notes

Document the investigation.

## Data Risk Graph

Visualize relationships among:

- Users
- Devices
- Cloud resources
- Data flows

The current lesson describes integration with Microsoft Sentinel supporting the data risk graph.

### Exam Shortcut

**Potential insider misconduct requiring further investigation = Create a CASE**

Do not create a new policy merely because an existing alert requires investigation.

---

# 42. Insider Risk Actions

Possible response activities include:

- Sending policy reminders
- Resolving or dismissing a case
- Escalating serious cases
- Referring content to Microsoft Purview eDiscovery (Premium)
- Exporting information to supported security systems

### Important Distinction

**Insider Risk Management = Detect and investigate risky behavior**

**eDiscovery = Preserve, collect, and review relevant information for legal or formal investigations**

These solutions can support the same investigation from different perspectives.

---

# 43. Insider Risk and AI

The current module includes policy templates addressing risky AI usage.

Examples include:

- Sharing sensitive content with unauthorized AI services
- Accessing protected information inappropriately
- AI-related data exfiltration
- Prompt injection-related activity

The lesson also describes a **Risky Agents** policy template in preview.

### Risky Agents

AI agents may have access to enterprise systems and sensitive information.

A misconfigured or compromised agent may:

- Share information with unauthorized recipients
- Access restricted resources
- Perform risky actions

The Risky Agents template helps identify relevant activities in supported environments.

### Important Concept

**Insider-risk monitoring is expanding beyond human activity to include AI-agent behavior.**

---

# 44. Insider Risk and Security Copilot

The current module describes two Security Copilot experiences.

## Alert Summarization

Copilot helps summarize the evidence associated with an alert.

## Insider Risk Triage Agent

The agent analyzes factors such as:

- User risk
- File risk
- Activity risk

It helps classify and prioritize relevant alerts.

### Important Distinction

**DLP Triage Agent = Focus on data-loss alerts**

**Insider Risk Triage Agent = Focus on risky user behavior and associated evidence**

Both assist investigators rather than automatically establishing wrongdoing.

---

# 45. Adaptive Protection

## Big Idea

Adaptive Protection dynamically adjusts protective controls according to an identity's current insider risk level.

It uses information from Microsoft Purview Insider Risk Management.

### ELI5

Imagine an organization with a standard level of security for normal operations.

A user begins displaying unusually risky behavior.

Instead of manually changing several policies, the system can automatically apply stronger protections.

If the user's risk decreases, the restrictions can relax.

### Memory Trick

**ADAPTIVE PROTECTION = Protection changes as risk changes**

---

# 46. Adaptive Protection Integrations

The current Microsoft Learn module identifies three major control surfaces.

**Microsoft Purview DLP**

**Microsoft Purview Data Lifecycle Management**

**Microsoft Entra Conditional Access**

| Integration | Purpose |
|---|---|
| DLP | Adjust restrictions on sensitive-data activity |
| Data Lifecycle Management | Preserve certain deleted information |
| Conditional Access | Adjust application access based on insider risk |

### Important Concept

Adaptive Protection uses risk information to coordinate multiple security controls.

It is not simply a different name for DLP.

---

# 47. Three Insider Risk Levels

Microsoft Learn identifies three levels.

## Minor

Lower levels of detected insider risk.

## Moderate

Intermediate risk requiring stronger intervention.

## Elevated

Significant risk requiring the strongest configured controls.

### Memory Trick

**MINOR → MODERATE → ELEVATED**

**More risk = More restrictive controls**

Risk levels can change automatically as monitored activity changes.

---

# 48. Adaptive DLP Examples

An organization could configure:

| Risk level | Example DLP response |
|---|---|
| Minor | Display an educational policy tip |
| Moderate | Warn and require justification |
| Elevated | Block inappropriate external sharing |

### ELI5

A lower-risk user might receive a warning.

A user showing more concerning activity might need to justify the action.

A high-risk user might be completely prevented from exporting sensitive data.

### Important Detail

The actual action depends on the organization's policies.

Risk levels do not independently mandate the same action in every organization.

---

# 49. Adaptive Data Lifecycle Management

The current lesson describes a specific retention capability for users with an Elevated insider risk level.

When configured, a retention label policy preserves content that the user deletes from supported locations, including:

- SharePoint
- OneDrive
- Exchange Online

Microsoft Learn describes a **120-day** preservation period for this adaptive protection scenario.

### ELI5

If a high-risk user deletes potentially relevant information, the organization may need to retain the content for investigation.

Adaptive Protection can help preserve that information.

### Important Distinction

**DLP = Control inappropriate sharing**

**Data Lifecycle Management = Control preservation and retention**

---

# 50. Adaptive Conditional Access

Adaptive Protection can integrate with Microsoft Entra Conditional Access.

### Example

An organization might configure:

**Minor risk:** Require acknowledgment of Terms of Use.

**Moderate risk:** Restrict access to particular sensitive applications.

**Elevated risk:** Block access to organizational applications until the risk is resolved.

### Important Concept

**Insider Risk Management calculates the risk level.**

**Conditional Access enforces configured application-access decisions.**

---

# 51. Adaptive Protection vs. Conditional Access

| Adaptive Protection | Conditional Access |
|---|---|
| Uses insider risk information to adjust protections | Evaluates access requests against policies |
| Coordinates DLP, lifecycle, and access controls | Enforces configured access decisions |
| Responds to changing insider risk levels | Can use insider risk as a signal |

### Memory Trick

**Adaptive Protection = Adjust controls based on insider risk**

**Conditional Access = Enforce access decisions**

---

# 52. Data Security Posture Management — DSPM

## Big Idea

Microsoft Purview Data Security Posture Management provides a unified view of the organization's data security risks.

It helps organizations discover, assess, protect, and investigate sensitive information across multiple environments.

### ELI5

Imagine an organization has sensitive information spread across:

- Microsoft 365
- Azure
- Employee devices
- External SaaS applications
- Third-party cloud environments
- AI applications

The organization needs a central understanding of where that information exists and how it is protected.

DSPM provides that broader view.

### Memory Trick

**DSPM = BIG-PICTURE DATA SECURITY POSTURE**

---

# 53. Four Questions DSPM Answers

Microsoft Learn emphasizes four practical questions.

**What data do we have?**

**Where is it stored?**

**Who can access it?**

**How is it protected?**

### Why These Matter

An organization cannot effectively reduce data exposure without understanding:

- Data classification
- Storage locations
- Access permissions
- Existing protection policies
- Risky sharing activities

DSPM combines information from different Purview solutions to help answer these questions.

---

# 54. DSPM vs. CSPM

These two capabilities share the phrase *Security Posture Management*, but they have different scopes.

## Data Security Posture Management

Focuses on sensitive data and its exposure.

## Cloud Security Posture Management

Focuses primarily on cloud infrastructure and resource security configurations.

| Microsoft Purview DSPM | Defender for Cloud CSPM |
|---|---|
| Data-centric security posture | Cloud infrastructure security posture |
| Sensitive data discovery | Cloud resource assessment |
| Data access and oversharing | Resource misconfigurations |
| Labeling and DLP coverage | Cloud security recommendations |
| AI data interactions | Cloud and AI workload configurations |

### Memory Trick

**DSPM = Protect the DATA**

**CSPM = Secure the CLOUD ENVIRONMENT**

---

# 55. DSPM Security Objectives

DSPM organizes data security activities around objectives.

The current module identifies examples including:

- Prevent sensitive-data exposure in Copilot interactions
- Prevent oversharing
- Prevent exfiltration to risky destinations
- Discover sensitive data

### ELI5

Rather than forcing an administrator to start with a specific product, DSPM starts with a security goal.

For example:

> Reduce sensitive data oversharing.

DSPM can then guide the administrator toward relevant controls and corrective actions.

---

# 56. DSPM Recommended Actions

Depending on the identified risk and supported capabilities, DSPM can recommend actions such as:

- Apply sensitivity labels
- Configure DLP policies
- Investigate suspicious activity
- Remove inappropriate public sharing links
- Reduce excessive permissions

The current module also describes one-click policy options and AI-assisted remediation workflows.

### Important Concept

DSPM identifies and coordinates corrective actions.

It does not mean every recommendation should be automatically applied without evaluating operational impact.

---

# 57. Visibility Beyond Microsoft 365

The current lesson describes DSPM visibility extending across:

- Microsoft 365
- Microsoft Azure
- Microsoft Fabric
- Supported third-party SaaS applications
- Supported third-party cloud and data environments

Examples of third-party platforms mentioned include:

- Google Cloud Platform
- Snowflake
- Databricks

Microsoft also describes integrations with selected partner solutions.

### Important Concept

**DSPM is intended to provide unified data-risk visibility beyond a single application or cloud provider.**

Actual coverage depends on configured integrations and product entitlements.

---

# 58. DSPM Asset Explorer

## Big Idea

Asset Explorer helps administrators understand the locations and classifications of data across supported workloads.

It can display:

- Labeled information
- Unlabeled information
- Relevant data locations
- Sensitive-data risks
- Information across Microsoft and integrated non-Microsoft environments

### Shadow Data

Shadow data refers to information outside normal organizational visibility or management.

### ELI5

An organization may have confidential files stored in a cloud service nobody on the security team knows about.

Asset Explorer can help uncover those hidden data locations.

### Memory Trick

**DSPM ASSET EXPLORER = Understand data assets across the estate**

---

# 59. DSPM and AI Observability

The current module includes dedicated AI observability capabilities.

## Big Idea

AI observability helps administrators understand how AI applications and agents interact with organizational data.

Examples include:

- Sensitive information included in AI prompts
- AI applications accessing confidential documents
- AI-related oversharing
- Unusual AI agent activity
- Data exfiltration through AI workflows

### ELI5

An organization deploys an AI agent.

The agent receives permissions to access business documents.

Administrators need to know whether the agent is using those permissions appropriately.

AI observability provides relevant monitoring and risk information.

---

# 60. AI Observability Dashboard

The module describes a dashboard containing information about AI apps and agents with activity during the previous **30 days**.

It can display:

- AI applications and agents
- Sensitive interactions
- Risk information
- Relevant policies
- Agent activity

### Important Concept

**AI observability = Visibility into how AI systems interact with organizational information**

This is separate from merely knowing that an AI application exists.

---

# 61. Security Copilot and DSPM Agents

DSPM can use Microsoft Security Copilot and supported AI agents to assist with data-security tasks.

Examples include:

- Identifying policy gaps
- Analyzing sensitive-data access
- Detecting oversharing
- Prioritizing alerts
- Recommending protective actions

The current module also describes AI agents that can perform approved remediation actions.

### Human Oversight

Administrators can review, approve, or customize actions.

The module emphasizes auditability of those actions.

### Memory Trick

**AI identifies and recommends. Authorized administrators remain accountable.**

---

# 62. Five Major DSPM Pages

Microsoft Learn identifies five key areas.

| DSPM page | Primary purpose |
|---|---|
| Posture | Overall data security dashboard |
| Objectives | Guided security improvement goals |
| AI Observability | AI apps, agents, and data interactions |
| Asset Explorer | Data assets and locations |
| Reports | Security metrics, trends, and policy activity |

## Posture

Displays the current data-security picture.

## Objectives

Guides administrators through recommended improvements.

## AI Observability

Tracks supported AI interactions and related risks.

## Asset Explorer

Provides data asset visibility.

## Reports

Displays trends, usage, policy activity, and risk metrics.

### Memory Trick

**POSTURE → OBJECTIVES → AI → ASSETS → REPORTS**

---

# 63. DSPM and Data Risk Assessments

DSPM supports data risk assessments.

These can help identify:

- Excessive sharing
- Inadequate labeling
- Sensitive-data exposure
- Data security gaps

### Example

An organization discovers that numerous sensitive SharePoint documents are accessible through overly permissive sharing links.

DSPM can surface the risk and recommend corrective actions.

### GRC Connection

These assessments can support ongoing monitoring and data-risk remediation tracking.

---

# 64. Microsoft Purview Data Security Investigations

## Big Idea

Microsoft Purview Data Security Investigations helps security teams investigate data breaches, data leaks, and unexpected data exposure.

It uses generative AI to help analysts examine affected content and determine the potential impact.

### ELI5

Imagine an organization discovers that hundreds of documents may have been downloaded improperly.

The investigators need to know:

**Which documents were involved?**

**What sensitive information do they contain?**

**How serious is the exposure?**

**Which corrective actions are necessary?**

Data Security Investigations provides tools to answer these questions.

### Memory Trick

**DATA SECURITY INVESTIGATIONS = WHAT DATA WAS AFFECTED, AND HOW SERIOUS IS IT?**

---

# 65. Three AI Capabilities in Data Security Investigations

The current module identifies three major AI-powered capabilities.

**Vector Search**

**Categorization**

**Examination**

These help investigators search, organize, and evaluate affected content.

---

# 66. Vector Search

## Big Idea

Vector search uses semantic relationships to identify relevant information.

It goes beyond exact keyword matching.

### ELI5

An investigator searches for documents about:

> Customer agreements

A traditional keyword search might miss relevant documents that use different wording.

Vector search can identify related content based on meaning.

### Memory Trick

**Vector Search = Search by meaning, not only exact words**

---

# 67. Categorization

## Big Idea

Categorization organizes affected information into meaningful groups.

The current module describes classification by:

- Subject matter
- Risk level
- Default categories
- Custom categories
- AI-suggested categories

### Example

An investigation contains thousands of files.

AI categorization groups them into:

- Financial information
- Personal records
- Intellectual property
- Other business information

This helps investigators identify which content requires attention first.

### Memory Trick

**Categorization = Sort affected information**

---

# 68. Examination

## Big Idea

Examination performs deeper analysis of content to identify security risks.

Examples include:

- Exposed credentials
- Network security weaknesses
- References to attacker activity
- Other dangerous information inside files

### ELI5

Vector search finds relevant documents.

Categorization organizes them.

Examination investigates what security risks they actually contain.

### Memory Trick

**Examination = Determine what makes the content risky**

---

# 69. Three Investigation Capabilities Compared

| Capability | Main purpose |
|---|---|
| Vector Search | Find relevant content by meaning |
| Categorization | Group content by type and risk |
| Examination | Analyze content for security risks |

### Complete Workflow

```text
SEARCH
   |
   v
Find Relevant Content
   |
   v
CATEGORIZE
   |
   v
Organize by Subject and Risk
   |
   v
EXAMINE
   |
   v
Identify Security Implications
```

---

# 70. Common Data Security Investigation Scenarios

## Data Breach

Determine which sensitive information was exposed or accessed.

## Insider Data Leak

Examine data associated with suspicious internal behavior.

## Unexpected Exposure

Investigate information that may have become accessible to unauthorized parties.

## Proactive Risk Assessment

Review selected information to identify security gaps before an incident occurs.

### Important Concept

**Data Security Investigations is not limited to investigations after a confirmed breach.**

It can also support proactive data-risk analysis.

---

# 71. Integration With Other Microsoft Products

The current module identifies integrations with:

## Insider Risk Management

Escalate a relevant insider-risk case for deeper data analysis.

## Microsoft Defender XDR

Open a data-security investigation associated with relevant security alerts.

## Data Security Posture Management

Investigate suspected sensitive-data exfiltration or exposure identified through DSPM.

## Unified Audit Log

Use activity records such as file downloads or label changes to help scope an investigation.

### Memory Trick

**IRM = Suspicious internal behavior**

**Defender XDR = Security incident context**

**DSPM = Data exposure risk**

**Data Security Investigations = Deep analysis of affected data**

---

# 72. Investigation Response Actions

Data Security Investigations supports actions to help reduce the impact of data exposure.

The module identifies:

**Soft Purge**

**Hard Purge**

## Soft Purge

Moves supported content to a recoverable deleted state.

### ELI5

Remove the material while retaining an available recovery path.

## Hard Purge

Permanently deletes content from the relevant data source, subject to supported service behavior and applicable controls.

### ELI5

Permanently remove the content rather than leaving it recoverable through the ordinary deletion process.

### Important Security Consideration

Deletion actions should be appropriately authorized.

Legal holds, retention requirements, evidence preservation, and organizational procedures must be considered before deleting potentially relevant information.

### Memory Trick

**SOFT PURGE = Recoverable deletion**

**HARD PURGE = Permanent deletion**

---

# 73. Data Security Investigations Billing

The current Microsoft Learn module describes a:

**Pay-as-you-go billing model**

Organizations pay for applicable storage and processing.

The lesson does not present the solution as requiring a fixed per-user licensing model.

### Important Concept

This differs from traditional fixed-seat licensing.

Actual prices, availability, and billing requirements should be verified when implementing the service.

---

# 74. Data Security Investigations vs. eDiscovery

Both capabilities may analyze organizational content, but their primary purposes differ.

## Data Security Investigations

Focuses on data security incidents and understanding the risk associated with affected content.

## Microsoft Purview eDiscovery

Focuses on identifying, preserving, collecting, reviewing, and producing information relevant to legal and formal investigations.

| Data Security Investigations | eDiscovery |
|---|---|
| Data breach and exposure investigation | Legal and formal evidence discovery |
| Analyze affected sensitive content | Collect and preserve relevant content |
| Identify data-security impact | Support legal review |
| Recommend security remediation | Support legal investigation workflows |

### Important Note

This comparison provides cross-module context. eDiscovery is covered in the next Microsoft Purview Data Compliance module.

---

# 75. The Complete Microsoft Purview Data Security Workflow

Imagine an organization discovers unusual activity involving sensitive employee records.

## Step 1 — Identify the Information

Sensitive Information Types recognize employee identification numbers.

## Step 2 — Classify and Protect It

Sensitivity labels classify applicable documents and apply configured protections.

## Step 3 — Restrict Inappropriate Sharing

DLP blocks unauthorized external sharing of the sensitive records.

## Step 4 — Detect Suspicious Behavior

Insider Risk Management identifies unusual activity involving the documents.

## Step 5 — Adjust Protective Controls

Adaptive Protection applies stronger controls if the relevant user's insider risk level increases.

## Step 6 — Assess Broader Exposure

DSPM identifies other locations where similar sensitive information may be inadequately protected.

## Step 7 — Investigate an Incident

Data Security Investigations analyzes the affected files and determines what sensitive information may have been exposed.

### Complete Flow

```text
SENSITIVE ORGANIZATIONAL DATA
             |
             v
INFORMATION PROTECTION
Identify and classify
             |
             v
SENSITIVITY LABELS
Classify and protect
             |
             v
DLP
Monitor and restrict sharing
             |
             v
INSIDER RISK MANAGEMENT
Detect suspicious internal activity
             |
             v
ADAPTIVE PROTECTION
Adjust controls based on risk
             |
             v
DSPM
Understand data exposure across environments
             |
             v
DATA SECURITY INVESTIGATIONS
Analyze affected content and respond
```

**This is a conceptual explanation of how the products complement each other, not a required chronological deployment order.**

---

# 76. Commonly Confused Capabilities

## Classification vs. Sensitivity Label

**Classification = Identify what information contains**

**Sensitivity Label = Classify and potentially protect it**

---

## SIT vs. Trainable Classifier

**SIT = Recognizable patterns**

**Trainable Classifier = Machine-learning classification**

---

## Content Explorer vs. Activity Explorer

**Content Explorer = Where is the data?**

**Activity Explorer = What happened to it?**

---

## Sensitivity Label vs. DLP

**Sensitivity Label = What classification and protections apply?**

**DLP = Is this data-handling action permitted?**

---

## Label vs. Label Policy

**Label = Classification and protection settings**

**Label Policy = Publication and usage requirements**

---

## DLP vs. Insider Risk Management

**DLP = Prevent inappropriate data sharing**

**Insider Risk Management = Investigate risky internal behavior**

---

## Insider Risk Management vs. Adaptive Protection

**IRM = Identify and evaluate risk**

**Adaptive Protection = Dynamically change controls based on risk**

---

## DSPM vs. Data Security Investigations

**DSPM = Broad data-security posture**

**Data Security Investigations = Detailed investigation of affected data**

---

## DSPM vs. CSPM

**DSPM = Sensitive-data security posture**

**CSPM = Cloud infrastructure security posture**

---

## DLP vs. eDiscovery

**DLP = Prevent inappropriate disclosure**

**eDiscovery = Find and preserve relevant evidence**

---

# 77. GRC / ISSO Career Connection

> **Additional professional context:** This section connects the Microsoft Learn topics to governance, risk, compliance, and information assurance responsibilities. It is not a separate official Microsoft Learn instructional unit.

Microsoft Purview Data Security is highly relevant to GRC because it provides controls and evidence related to the handling of sensitive organizational information.

An ISSO or GRC analyst may need to determine whether:

- Sensitive data has been identified
- Data classification rules exist
- Information is appropriately labeled
- Access restrictions are enforced
- Unauthorized disclosure is prevented
- Data-handling activity is monitored
- Security incidents are investigated
- Corrective actions are documented
- Controls remain effective over time

---

# 78. NIST SP 800-53 Control Relationships

The mappings below are illustrative and do not establish automatic compliance.

| Purview capability | Related NIST control |
|---|---|
| Sensitivity labels and access protection | AC-3 — Access Enforcement |
| DLP information-flow restrictions | AC-4 — Information Flow Enforcement |
| Protection of sensitive information | SC-28 — Protection of Information at Rest |
| Monitoring suspicious activity | SI-4 — System Monitoring |
| Reviewing recorded activity | AU-6 — Audit Record Review, Analysis, and Reporting |
| Insider-risk incident handling | IR-4 — Incident Handling |
| Continuous data-security monitoring | CA-7 — Continuous Monitoring |
| Limiting unnecessary privileges | AC-6 — Least Privilege |

### Important Principle

A Microsoft Purview policy may support a security control, but its existence alone does not prove that the control is fully effective.

---

# 79. Example GRC Assessment

An organization claims:

> We prevent unauthorized external disclosure of confidential personnel records.

An assessor should examine whether:

**Classification is adequate.**

Are sensitive records reliably identified?

**Labels are appropriately configured.**

Do relevant documents have the intended classification and restrictions?

**DLP policies cover relevant locations.**

Are email, file sharing, endpoints, and other applicable channels protected?

**The policies operate as intended.**

Have tests demonstrated that restricted actions are detected or blocked?

**Exceptions are controlled.**

Are overrides justified, authorized, and documented?

**Monitoring occurs.**

Are alerts and activity logs actually reviewed?

**Incidents are investigated.**

Does the organization have procedures for handling potential disclosure?

### GRC Lesson

**Policy existence is not the same thing as control effectiveness.**

---

# 80. Microsoft Purview and POA&M

## POA&M

**Plan of Action and Milestones**

A POA&M tracks identified security weaknesses and planned remediation actions.

### Example

```text
Finding:
Confidential employee records are accessible
through unrestricted external sharing links.

Risk:
Unauthorized disclosure of personnel information.

Recommended Remediation:
Restrict sharing permissions and implement
appropriate data loss prevention controls.

Responsible Owner:
Information Security / Microsoft 365 Administration

Validation:
Confirm unauthorized external sharing is blocked.

Status:
In Progress
```

DSPM findings and DLP investigations may provide evidence useful for identifying, tracking, and verifying remediation.

### Important Distinction

**Purview Finding = Technical evidence or risk observation**

**POA&M = Formal organizational remediation record**

---

# 81. Microsoft Purview Data Security and AI Governance

Organizations increasingly use AI applications that interact with sensitive information.

An ISSO or GRC analyst may need to evaluate:

- Which AI applications are authorized
- Which sensitive data AI agents can access
- Whether DLP applies to AI interactions
- Whether excessive permissions exist
- Whether sensitive information is exposed in prompts
- Whether AI-agent behavior is monitored
- Whether identified issues are documented and remediated

### Example

An organization deploys an AI agent to help summarize internal reports.

The security team must determine whether the agent can access sensitive information and whether appropriate protections exist.

Relevant Purview capabilities include:

**Information Protection** for classification.

**DLP** for controlling inappropriate sharing.

**Insider Risk Management** for relevant risky activity.

**Adaptive Protection** for risk-responsive controls.

**DSPM** for data exposure and AI observability.

**Data Security Investigations** for analyzing incidents involving sensitive information.

### GRC Principle

**AI adoption introduces new data-handling risks, but the underlying requirements for classification, least privilege, monitoring, and accountability remain important.**

---

# 82. High-Value Product Recognition

| If the question mentions... | Think... |
|---|---|
| Recognize Social Security number patterns | Sensitive Information Type |
| Detect named entities | Named Entity SIT |
| Identify exact employee numbers | Exact Data Match |
| Recognize resumes using machine learning | Trainable Classifier |
| Determine where sensitive files exist | Content Explorer |
| Review sensitivity label changes | Activity Explorer |
| Classify a document as Confidential | Sensitivity Label |
| Encrypt confidential email | Sensitivity Label |
| Publish labels to users | Sensitivity Label Policy |
| Require users to label content | Sensitivity Label Policy |
| Require justification for downgrading a label | Sensitivity Label Policy |
| Block unauthorized sharing | DLP |
| Warn users before sharing sensitive content | DLP Policy Tip |
| Restrict USB copying of confidential files | Endpoint DLP |
| Block a Social Security number in Teams | DLP |
| Restrict sensitive data sent to AI websites | DLP |
| Investigate unusual employee downloads | Insider Risk Management |
| Detect possible departing-employee data theft | Insider Risk Management |
| Create a formal insider-risk investigation | Case |
| Adjust DLP based on insider risk | Adaptive Protection |
| Low, medium, and high insider risk categories | Minor, Moderate, Elevated |
| Preserve deleted content from elevated-risk users | Adaptive Data Lifecycle Management |
| Adjust application access based on insider risk | Adaptive Conditional Access |
| Broad overview of sensitive-data exposure | DSPM |
| View sensitive data across multiple platforms | DSPM |
| View AI agent interactions with sensitive data | AI Observability |
| Discover unlabeled or shadow data | DSPM Asset Explorer |
| Investigate which data was exposed in a breach | Data Security Investigations |
| Find related documents by meaning | Vector Search |
| Organize impacted files by risk | Categorization |
| Analyze content for specific security hazards | Examination |
| Recoverable deletion | Soft Purge |
| Permanent deletion | Hard Purge |

---

# 83. Final Module 2 Cram Sheet

```text
MICROSOFT PURVIEW DATA SECURITY
= IDENTIFY + PROTECT + MONITOR + INVESTIGATE DATA

INFORMATION PROTECTION
= CLASSIFY SENSITIVE DATA

SIT
= SENSITIVE INFORMATION TYPE

SIT
= DETECT RECOGNIZABLE DATA PATTERNS

PRIMARY ELEMENT
= MAIN MATCHING PATTERN

SUPPORTING ELEMENT
= ADDITIONAL MATCHING EVIDENCE

CONFIDENCE LEVEL
= STRENGTH OF DETECTION EVIDENCE

PROXIMITY
= DISTANCE BETWEEN PATTERN AND SUPPORTING EVIDENCE

BUILT-IN SIT
= MICROSOFT-MAINTAINED CLASSIFIER

NAMED ENTITY SIT
= NAMES, ADDRESSES, MEDICAL TERMS

CUSTOM SIT
= ORGANIZATION-DEFINED PATTERN

EDM
= EXACT DATA MATCH

TRAINABLE CLASSIFIER
= MACHINE-LEARNING CONTENT RECOGNITION

CONTENT EXPLORER
= WHERE IS SENSITIVE DATA?

ACTIVITY EXPLORER
= WHAT ARE USERS DOING WITH THE DATA?

SENSITIVITY LABEL
= CLASSIFY AND PROTECT CONTENT

SENSITIVITY LABEL METADATA
= PERSISTENT CLASSIFICATION INFORMATION

SENSITIVITY LABEL POLICY
= PUBLISH LABELS AND CONTROL LABEL USAGE

MANDATORY LABELING
= REQUIRE AN APPROPRIATE LABEL

DOWNGRADE JUSTIFICATION
= EXPLAIN LOWERING SENSITIVITY

DLP
= DATA LOSS PREVENTION

DLP
= PREVENT INAPPROPRIATE DATA SHARING

DLP POLICY TIP
= WARN USER ABOUT SENSITIVE ACTIVITY

BLOCK WITH OVERRIDE
= BLOCK UNLESS PERMITTED EXCEPTION IS JUSTIFIED

BLOCK WITHOUT OVERRIDE
= PREVENT THE ACTION

ENDPOINT DLP
= PROTECT DATA ON WINDOWS AND MACOS

DLP AI PROTECTION
= CONTROL SENSITIVE DATA SHARED WITH AI APPS

INSIDER RISK MANAGEMENT
= DETECT AND INVESTIGATE RISKY INTERNAL ACTIVITY

INSIDER RISK WORKFLOW
= POLICY → ALERT → TRIAGE → INVESTIGATE → ACTION

INSIDER RISK CASE
= CONSOLIDATED INVESTIGATION

ADAPTIVE PROTECTION
= DYNAMICALLY ADJUST CONTROLS BASED ON RISK

ADAPTIVE RISK LEVELS
= MINOR + MODERATE + ELEVATED

ADAPTIVE DLP
= CHANGE DATA PROTECTION BASED ON USER RISK

ADAPTIVE DATA LIFECYCLE
= PRESERVE CONTENT FROM HIGH-RISK USERS

ADAPTIVE CONDITIONAL ACCESS
= ADJUST APPLICATION ACCESS BASED ON INSIDER RISK

DSPM
= DATA SECURITY POSTURE MANAGEMENT

DSPM
= BIG-PICTURE SENSITIVE DATA SECURITY

DSPM OBJECTIVES
= GUIDED RISK-REDUCTION GOALS

DSPM ASSET EXPLORER
= VIEW DATA ASSETS ACROSS ENVIRONMENTS

AI OBSERVABILITY
= MONITOR AI APPS, AGENTS, AND DATA INTERACTIONS

DATA SECURITY INVESTIGATIONS
= INVESTIGATE THE CONTENT AND IMPACT OF DATA INCIDENTS

VECTOR SEARCH
= SEARCH CONTENT BY MEANING

CATEGORIZATION
= ORGANIZE IMPACTED DATA BY TYPE AND RISK

EXAMINATION
= ANALYZE CONTENT FOR SECURITY RISKS

SOFT PURGE
= RECOVERABLE DELETION

HARD PURGE
= PERMANENT DELETION

DSPM
= OVERALL DATA SECURITY POSTURE

DATA SECURITY INVESTIGATIONS
= DEEP ANALYSIS OF AFFECTED DATA

CSPM
= CLOUD INFRASTRUCTURE SECURITY POSTURE

EDISCOVERY
= LEGAL AND FORMAL EVIDENCE DISCOVERY
```

---

# 84. Final Mental Model

Imagine an organization manages thousands of personnel files, financial records, contracts, and internal documents.

**Microsoft Purview Information Protection** identifies which documents contain sensitive information.

**Sensitive Information Types** recognize structured information such as identification and account numbers.

**Trainable Classifiers** recognize documents based on their content and characteristics.

**Sensitivity Labels** classify files and can enforce encryption, access restrictions, and other controls.

**Sensitivity Label Policies** determine who receives those labels and how they must be used.

**Data Loss Prevention** monitors and restricts attempts to share sensitive information inappropriately.

**Endpoint DLP** extends protection to activities such as copying files to USB drives or printing confidential documents.

**Insider Risk Management** detects potentially risky internal activity and provides investigation workflows.

**Adaptive Protection** adjusts restrictions based on changing insider risk levels.

**Data Security Posture Management** provides a broad view of where sensitive information exists, how it is protected, and where exposure remains.

**AI Observability** extends that visibility to AI applications and agents.

**Data Security Investigations** helps analysts determine what information was affected when a data-security incident occurs.

Together, these capabilities support one fundamental objective:

**Know your data, protect it appropriately, monitor how it is handled, and respond effectively when it is placed at risk.**

---

# Official Microsoft Learn References

The following pages were verified against the live module on November 23, 2026.

[Module Overview](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-solutions/)

[Introduction](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-solutions/1-introduction)

[Describe Data Classification Capabilities](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-solutions/2-identify-sensitive-data)

[Describe Sensitivity Labels and Policies](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-solutions/3-describe-sensitivity-labels-policies)

[Describe Data Loss Prevention](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-solutions/4-describe-data-loss-prevention)

[Describe Insider Risk Management](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-solutions/5-describe-insider-risk-management)

[Describe Adaptive Protection](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-solutions/6-describe-adaptive-protection)

[Describe Data Security Posture Management](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-solutions/6a-describe-data-security-posture-management)

[Describe Data Security Investigations](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-solutions/6b-describe-data-security-investigations)

[Module Assessment](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-solutions/7-knowledge-check)

[Summary](https://learn.microsoft.com/en-us/training/modules/describe-purview-data-solutions/8-summary)
