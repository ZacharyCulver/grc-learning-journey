# SC-900 — Section 3, Module 1
# Describe Microsoft Security Copilot

> **Source:** Microsoft Learn — SC-900  
> **Learning Path:** Introduction to Microsoft security solutions  
> **Module:** Describe Microsoft Security Copilot  
> **Verified against current Microsoft Learn content:** November 23, 2026  
> **Duration:** 32 minutes | 8 units | 900 XP  
> **Official Module:** https://learn.microsoft.com/en-us/training/modules/security-copilot-getting-started/

---

# Module Overview

Microsoft Security Copilot is a **cloud-based, generative AI-powered security analysis solution**.

It helps security professionals investigate threats, analyze security information, assess risks, manage security workflows, and respond to incidents more efficiently.

## The Big Idea

Security teams have three major problems:

- **Too many threats:** The volume and sophistication of cyberattacks continue to increase.
- **Too much information:** Organizations collect enormous amounts of security data across numerous systems.
- **Not enough personnel:** Qualified security professionals cannot manually investigate everything at the speed required.

Microsoft Security Copilot helps organizations address these challenges using artificial intelligence.

### ELI5

Imagine you're a cybersecurity analyst responsible for monitoring thousands of devices, accounts, and applications.

An alert indicates suspicious activity.

Normally, you might need to examine several dashboards, read logs, investigate the account, analyze a script, and prepare a report.

Security Copilot can help gather, correlate, summarize, and explain that information using natural-language requests.

Instead of manually assembling every piece of information, you can ask:

> Investigate this incident, identify the affected accounts and devices, summarize the evidence, and recommend the next steps.

**Security Copilot helps the analyst perform the investigation. It does not eliminate the need to verify findings and make appropriate security decisions.**

---

# 1. What Is Microsoft Security Copilot?

Microsoft Security Copilot combines:

**Generative AI + Security Data + Threat Intelligence + Security Tools**

The result is a security-focused AI assistant.

Microsoft Security Copilot uses large language models and Microsoft's security integrations to help security professionals understand and respond to security events.

## Generative AI

Generative artificial intelligence produces new content based on prompts and available information.

Examples include:

- Written summaries
- Explanations
- Investigation reports
- Queries
- Recommended actions
- Analysis of suspicious code

## Large Language Model — LLM

An LLM is an AI model trained to understand and generate language.

Security Copilot uses LLM capabilities provided through Azure OpenAI services.

### Important Distinction

An ordinary LLM can explain what a phishing attack is.

Security Copilot can also use authorized integrations to examine relevant security information from an organization's environment.

This additional context is what makes Security Copilot useful for security operations.

## Natural Language Processing — NLP

Natural Language Processing allows computers to interpret and respond to human language.

### ELI5

You do not necessarily need to write a complicated query.

You can ask a question in normal English:

> Show me the security incidents involving this device over the last seven days.

Security Copilot interprets the request and uses available capabilities to help answer it.

---

# 2. Microsoft Security Copilot Use Cases

Microsoft Learn identifies several major use cases.

## Investigate and Remediate Security Threats

Security Copilot can help analysts:

- Understand an incident
- Correlate security information
- Identify affected entities
- Summarize suspicious activity
- Recommend investigation steps
- Suggest possible remediation actions

### Example

A security alert indicates potential credential theft.

An analyst asks Security Copilot to summarize the incident and identify affected users.

The response can help the analyst decide where to investigate next.

**Memory Trick: Incident → Context → Investigation → Response**

---

## Generate Kusto Query Language Queries

Security professionals frequently use **Kusto Query Language (KQL)** to analyze security data.

KQL appears in services including Microsoft Sentinel and other Microsoft security experiences.

Security Copilot can generate KQL queries from natural-language instructions.

### Example

Instead of writing a query manually, an analyst asks:

> Create a KQL query that identifies repeated failed sign-ins from the same IP address during the last 24 hours.

Security Copilot can help translate the request into query syntax.

### Important Concept

Security Copilot can **generate queries**.

Microsoft Sentinel and other supported services provide the security data and query environment.

Security Copilot does not replace the underlying data platform.

---

## Analyze Suspicious Scripts

Security Copilot can help explain suspicious scripts and code.

Examples include:

- PowerShell scripts
- Command-line commands
- Potentially malicious code
- Obfuscated script behavior

### ELI5

Instead of manually examining a long script line by line, an analyst can ask Security Copilot to explain what the code appears to do.

The analyst must still verify the analysis.

---

## Understand Risks and Security Posture

Security Copilot can help summarize risks across supported security systems.

Examples:

- Security weaknesses
- Potentially exposed resources
- Recommended improvements
- Changes in security posture
- Prioritized risks

### Security Posture

An organization's security posture describes its overall security condition and readiness.

**Security posture = How well protected is the organization?**

---

## Troubleshoot IT Issues

Security Copilot can help administrators examine technical information and identify possible causes of problems.

Examples:

- Authentication failures
- Security policy conflicts
- Configuration issues
- Device-management problems

---

## Define and Manage Security Policies

Security Copilot can assist with policy-related tasks.

Examples:

- Summarize existing policies
- Compare policies
- Identify possible conflicts
- Help develop new policy configurations
- Explain security implications

### Example

An administrator asks:

> Compare these two access policies and explain where their requirements may conflict.

Security Copilot can help analyze the differences.

---

## Configure Secure Lifecycle Workflows

Security Copilot can assist with identity-management configuration tasks, including groups and access parameters.

This connects to the Microsoft Entra content studied earlier.

Examples:

- Employee onboarding
- Employee transfers
- Employee offboarding
- Access configuration guidance

### Remember

**Microsoft Entra Lifecycle Workflows performs lifecycle automation.**

**Security Copilot helps administrators understand and configure supported workflows.**

---

## Develop Stakeholder Reports

Security Copilot can produce reports tailored to different audiences.

### Technical Audience

An analyst might need:

- Indicators of compromise
- Technical findings
- Affected systems
- Investigation evidence
- Recommended remediation

### Executive Audience

A commander, director, or executive might need:

- A short incident summary
- Business impact
- Current risk
- Actions taken
- Remaining decisions

### ELI5

**Same incident. Different audience. Different report.**

This is particularly valuable for communicating cybersecurity risks to leadership.

---

# 3. Standalone vs. Embedded Security Copilot

Microsoft Security Copilot offers two main user experiences.

## Standalone Experience

The standalone experience is accessed through a dedicated Security Copilot interface.

Users interact with Copilot through a natural-language prompt bar.

### Example

An analyst opens Security Copilot and asks:

> Summarize the most critical security incidents affecting our environment.

Copilot uses enabled capabilities and authorized sources to respond.

### Memory Trick

**Standalone = Go directly to Security Copilot**

---

## Embedded Experience

The embedded experience places Security Copilot capabilities inside supported Microsoft security products.

Examples include:

- Microsoft Defender XDR
- Microsoft Sentinel
- Microsoft Entra
- Microsoft Intune
- Microsoft Purview

Specific capabilities depend on the product and integration.

### Example

An analyst opens an incident inside Microsoft Defender XDR.

A Security Copilot feature helps summarize the incident without requiring the analyst to start in the standalone interface.

### Memory Trick

**Embedded = Copilot inside another security product**

---

# 4. Standalone vs. Embedded Comparison

| Feature | Standalone | Embedded |
|---|---|---|
| Where you work | Security Copilot interface | Supported security product |
| Main interaction | Natural-language prompt bar | Product-specific Copilot features |
| Example | Investigate a threat through Copilot | Summarize an incident in Defender XDR |
| Primary benefit | Flexible cross-tool analysis | Assistance within an existing workflow |

Both experiences use Security Copilot capabilities.

**Standalone and embedded describe where the user interacts with Copilot, not two entirely separate AI products.**

---

# 5. Microsoft Security Copilot Terminology

Microsoft Learn identifies several important terms.

These distinctions are central to understanding how Security Copilot operates.

## Session

A **session** is a particular conversation within Security Copilot.

Copilot maintains conversational context during the session.

### ELI5

A session is like a case discussion between an analyst and an assistant.

The analyst can ask an initial question and then follow up.

---

## Prompt

A **prompt** is a specific question or instruction submitted to Security Copilot.

### Example

> Summarize incident 12345.

That individual instruction is a prompt.

**Prompt = The request**

---

## Capability

A **capability** is a specialized function Security Copilot can use to perform a task.

Microsoft also refers to capabilities as **skills**.

Examples include:

- Summarizing incidents
- Analyzing scripts
- Generating KQL queries
- Producing incident reports
- Suggesting guided responses

### Memory Trick

**Capability = What Copilot can do**

---

## Plugin

A **plugin** provides a collection of capabilities associated with a particular resource.

Plugins connect Security Copilot with data sources or external services.

Examples include plugins involving:

- Microsoft Defender XDR
- Microsoft Sentinel
- Microsoft Intune
- Other Microsoft security products
- Supported third-party products
- Custom integrations
- Open-source intelligence sources

### ELI5

Think of a plugin as a toolbox.

Each tool inside that toolbox is a capability.

**Plugin = Collection of tools**

**Capability = Individual tool**

---

# 6. Plugins vs. Capabilities

This relationship is particularly important.

Consider a Microsoft Defender XDR plugin.

The plugin may provide several capabilities:

```text
Microsoft Defender XDR Plugin
│
├── Summarize an incident
├── Analyze a suspicious script
├── Generate KQL queries
├── Provide guided investigation
└── Generate incident reports
```

The plugin provides access to specialized functionality.

The capabilities perform the individual tasks.

## Important Detail

Not every plugin has the same capabilities.

A Defender XDR plugin and a Microsoft Sentinel plugin may offer similar types of analysis, but they work within their supported product contexts.

Some plugins also require additional configuration or authentication.

### Exam Memory Trick

**Plugin = WHERE the functionality comes from**

**Capability = WHAT function it performs**

---

# 7. Promptbooks

A **promptbook** is a collection of predefined prompts organized for a particular task or workflow.

### ELI5

Think of a promptbook as a reusable checklist of questions for an investigation.

Instead of manually writing each prompt, an analyst follows a prepared sequence.

### Example: Incident Investigation Promptbook

```text
Investigate Incident
│
├── Summarize the incident
├── Identify affected accounts
├── Identify affected devices
├── Review relevant evidence
└── Suggest investigation steps
```

Microsoft Learn introduces promptbooks in this module and covers their operation in greater detail in other Security Copilot training.

### Key Distinction

**Prompt = One request**

**Promptbook = A series of prepared prompts**

**Session = The conversation containing requests and responses**

---

# 8. Workspaces

Microsoft Security Copilot supports separate **workspaces** within a tenant.

Workspaces help organizations separate environments, permissions, capacity, and data-handling requirements.

### ELI5

Remember the Microsoft Entra tenant analogy:

**Tenant = House**

**Workspace = Room inside the house**

Different teams can have different rooms.

For example:

```text
Microsoft Entra Tenant
│
├── Security Operations Workspace
│   ├── SOC personnel
│   └── Security investigation activities
│
├── Compliance Workspace
│   ├── Compliance personnel
│   └── Governance and compliance activities
│
└── IT Operations Workspace
    ├── IT administrators
    └── Technical support activities
```

These are illustrative workspace names.

## Workspace Benefits

Workspaces help organizations manage:

- Team separation
- Access permissions
- Compute capacity
- Costs and budgets
- Data storage location
- Regulatory requirements
- Available plugins

## Important Detail

Each workspace requires its own assigned Security Copilot capacity.

Permissions can differ between workspaces.

A user who can access one workspace does not automatically have unrestricted access to every other workspace.

---

# 9. Agents

Microsoft Security Copilot supports AI-powered agents.

Agents can perform specialized security and IT tasks with greater autonomy than a basic question-and-answer interaction.

They can help reduce repetitive work and scale supported security workflows.

### ELI5

A normal Security Copilot interaction might be:

> Analyze this incident.

An agent may be configured to carry out a recurring or more autonomous security workflow within its defined permissions.

## Typical Agent Areas

- Threat protection
- Identity management
- Data security
- Security operations
- IT administration

## Security Principle

Agents must operate within appropriate identity and permission controls.

Autonomy does not mean unlimited access.

### Memory Trick

**Prompt = Ask for a task**

**Agent = AI system designed to perform a task or workflow**

---

# 10. The Orchestrator

The **orchestrator** is Security Copilot's system for combining capabilities to answer a prompt.

### ELI5

Think of the orchestrator as an operations coordinator.

An analyst gives a mission:

> Investigate this suspicious sign-in.

The orchestrator determines which available capabilities may help complete the request.

For example, an investigation might require information from several enabled security sources.

The orchestrator develops a plan and coordinates the available capabilities.

### Memory Trick

**Orchestrator = Plans and coordinates**

**Plugins = Supply tools**

**Capabilities = Perform specialized tasks**

---

# 11. How Security Copilot Processes a Prompt

Microsoft Learn describes a seven-stage process.

## Step 1 — Submit Prompt

The user enters a natural-language request.

Example:

> Summarize incident 12345.

## Step 2 — Orchestrator

The orchestrator interprets the request and determines the initial context.

It constructs a plan using available capabilities.

## Step 3 — Build Context

Security Copilot executes the plan and retrieves relevant context.

## Step 4 — Plugins

Copilot uses enabled plugins and available data sources to analyze relevant information and patterns.

## Step 5 — Compose Response

The LLM combines information and context into a human-readable response.

## Step 6 — Review and Format Response

The response is formatted and reviewed through Microsoft's responsible AI processes.

## Step 7 — Return Response

The user receives the final output.

---

# 12. Prompt Processing Flow

```text
USER SUBMITS PROMPT
         |
         v
ORCHESTRATOR
Interprets request and plans
         |
         v
BUILD CONTEXT
Retrieve relevant information
         |
         v
PLUGINS AND CAPABILITIES
Analyze authorized security data
         |
         v
LLM COMPOSES RESPONSE
Generate understandable explanation
         |
         v
REVIEW AND FORMAT
Responsible AI safeguards
         |
         v
USER RECEIVES RESPONSE
```

### Exam Shortcut

If the question asks:

> What system coordinates the capabilities required to answer a prompt?

Answer:

**Orchestrator**

If the question asks:

> What connects Copilot with a particular security product?

Answer:

**Plugin**

If the question asks:

> What performs an individual specialized task?

Answer:

**Capability**

---

# 13. Process Log

Security Copilot generates a **process log** during prompt processing.

The process log gives users visibility into how the response was produced.

It can show:

- Capabilities used
- Relevant processing steps
- Safety checks applied during response generation

### Why Is This Important?

Security professionals need to understand the basis of AI-generated conclusions.

A process log can help the analyst assess whether appropriate capabilities and sources were involved.

### ELI5

Security Copilot should not simply give you an answer with no indication of how it reached that answer.

The process log helps show which tools were involved.

## Important Limitation

A visible process log does not automatically guarantee the correctness of every conclusion.

Analysts remain responsible for verifying important findings.

### Memory Trick

**Process Log = Transparency into Copilot's processing**

---

# 14. Effective Prompting

Microsoft Learn identifies four elements of an effective prompt.

These are especially worth remembering.

## GOAL

What specific security-related information or result do you want?

Example:

> Analyze recent failed authentication attempts.

## CONTEXT

Why do you need the information, and what situation does it relate to?

Example:

> We are investigating potential password-spray activity affecting administrator accounts during the last 24 hours.

## EXPECTATIONS

How should the answer be formatted, or who will use it?

Example:

> Provide a short executive summary followed by a technical findings table.

## SOURCE

What information or data source should Copilot use?

Example:

> Use the available Microsoft Entra sign-in data.

---

# 15. Four Prompt Elements

| Element | Question |
|---|---|
| Goal | What do I want? |
| Context | Why do I need it? |
| Expectations | How should the result look? |
| Source | Where should the information come from? |

### Memory Trick

**G-C-E-S**

**Goal — Context — Expectations — Source**

---

# 16. Weak Prompt vs. Strong Prompt

## Weak Prompt

```text
Analyze sign-ins.
```

This is too broad.

Copilot may not know:

- Which users
- Which time period
- Which risk criteria
- Which source
- What output format is needed

## Strong Prompt

```text
Goal:
Identify potentially suspicious sign-in activity.

Context:
We are investigating possible account compromise affecting
privileged Microsoft Entra users during the last 24 hours.

Expectations:
Provide a concise incident summary, followed by a table
showing affected accounts, relevant timestamps, risk
indicators, and recommended investigation steps.

Source:
Use available Microsoft Entra sign-in and identity risk data.

Clearly distinguish observed facts from recommendations.
```

The stronger prompt provides a more useful framework for analysis.

---

# 17. Additional Prompting Recommendations

Microsoft Learn recommends several practices.

## Be Specific

Define exactly what you need.

Instead of:

> Investigate an attack.

Try:

> Summarize the indicators of compromise associated with this incident and identify the affected endpoints.

## Provide Context

Include relevant details such as:

- Incident identifier
- Time window
- Affected service
- Audience
- Security objective

## Iterate

Follow up to refine the response.

Example:

> Now summarize those findings for a nontechnical manager.

## Use Positive Instructions

Clearly state what Copilot should do.

Instead of describing only what you do not want, provide the desired output and handling requirements.

## Use Natural Language

You do not need special programming syntax to communicate effectively with Copilot.

Clear instructions are usually more important than complicated wording.

---

# 18. Security Copilot Onboarding

Organizations must configure Security Copilot before users can work with it.

The current Microsoft Learn module identifies four onboarding stages:

**Identify customer category → Provision capacity if required → Configure environment → Assign permissions**

The exact process depends on licensing.

---

# 19. Licensing and Customer Categories

The current module distinguishes between two customer categories.

## Microsoft 365 E5 and E7 Customers

Microsoft Learn describes Security Copilot as included for eligible Microsoft 365 E5 and E7 customers.

For eligible tenants, Microsoft describes automatic, zero-click onboarding.

The current documentation also describes a seven-day advance notification before activation.

### Key Concept

**Eligible E5/E7 customers can have Security Copilot provisioned automatically.**

## Customers Without Included Security Copilot

Organizations without an included entitlement must manually provision Security Copilot capacity.

This generally involves Azure resources and Security Compute Units.

### Important Note

Licensing, service availability, and billing are operational details that can change.

For implementation, always check the current licensing documentation rather than relying solely on older certification notes.

---

# 20. Security Compute Units — SCUs

## Big Idea

Security Copilot uses computing capacity measured in:

**Security Compute Units (SCUs)**

An SCU measures compute capacity available to run Security Copilot workloads.

It supports both standalone and embedded experiences.

### ELI5

Imagine Security Copilot operates using a pool of computing resources.

More complex or frequent workloads require computing capacity.

SCUs represent the provisioned compute resources available to handle that work.

---

# 21. Provisioned Capacity and Overage

For customers using manual capacity provisioning, Microsoft Learn describes:

## Provisioned Capacity

Capacity reserved for regular Security Copilot workloads.

Provisioned capacity is billed hourly.

## Overage Capacity

Additional capacity that can handle demand exceeding the provisioned amount.

Overage is billed based on usage.

### Example

An organization has normal daily Security Copilot demand.

During a major incident, analysts suddenly submit significantly more requests.

Overage capacity can help accommodate the demand spike.

### Memory Trick

**Provisioned SCUs = Planned capacity**

**Overage = Extra capacity for unexpected demand**

---

# 22. SCU Provisioning Requirements

The current Microsoft Learn module describes the following for manual provisioning.

An administrator needs:

- An Azure subscription
- Azure Owner or Contributor permissions at least at the resource-group scope
- Security Administrator or higher privileges in the tenant being onboarded

### Important RBAC Distinction

**Microsoft Entra administrative privileges do not automatically grant Azure resource-management privileges.**

For example, a Microsoft Entra Global Administrator does not automatically have Azure Owner permissions.

This reinforces the distinction studied earlier.

**Microsoft Entra RBAC = Identity and directory administration**

**Azure RBAC = Azure resource permissions**

---

# 23. Provisioning Methods

Microsoft Learn identifies two approaches.

## Provision Through Security Copilot

An administrator uses the Security Copilot setup wizard.

The wizard can guide configuration of:

- Workspace
- Azure subscription
- Resource group
- Region
- Capacity name
- Number of SCUs

Microsoft identifies this as the recommended approach.

## Provision Through Azure

An administrator can also configure Security Copilot resources through the Azure portal.

Both approaches provision the required Azure resources.

### Current Module Figures

For manually provisioned capacity, the module states:

- Minimum: **1 SCU**
- Maximum: **100 SCUs**
- Suggested introductory exploration: **3 SCUs**

These are documented operational details, not universal recommendations for every environment.

---

# 24. Capacity Monitoring

Security Copilot provides a usage-monitoring dashboard.

Capacity owners can monitor:

- SCU consumption
- Workspace usage
- Plugin usage
- Users initiating sessions
- Capacity trends

The current module states that the dashboard can display up to **90 days** of usage information.

### Why It Matters

Organizations can use this information to:

- Monitor costs
- Identify usage patterns
- Adjust provisioned capacity
- Understand which teams consume resources

---

# 25. Configuring the Default Environment

Once capacity is available, administrators configure the Security Copilot environment.

Important settings include:

## Workspace Capacity

Assign appropriate compute capacity to each workspace.

## Data Storage Location

Choose where customer data should be stored.

This matters for:

- Data residency
- Regulatory obligations
- Organizational policies

## Prompt Evaluation Geography

Administrators can configure geographic restrictions on where prompts are evaluated.

## Audit Logging

Security Copilot can integrate with Microsoft Purview for logging supported administrative actions, user actions, and responses.

## Data-Sharing Preferences

Administrators control available options for sharing organizational data with Microsoft for specified product improvement and evaluation purposes.

## Plugin Settings

Administrators determine which plugins and data integrations are available.

---

# 26. Security Copilot Data Privacy

Microsoft Learn emphasizes that organizational Security Copilot data is protected by enterprise security and compliance controls.

The module states that customer data is **not used to train foundational AI models**.

Separate optional data-sharing settings can allow Microsoft to review certain information for product or security AI improvement purposes.

These settings are not the same as allowing customer information to train foundation models.

### ELI5

Using a security AI service does not mean an organization must surrender unrestricted ownership or reuse rights over its information.

Administrators must still understand and configure the applicable privacy, logging, and data-sharing controls.

---

# 27. Security Copilot Role Permissions

Microsoft Security Copilot has two platform-specific roles.

## Copilot Owner

Provides administrative control over supported Security Copilot platform settings and access management.

## Copilot Contributor

Allows authorized use of Security Copilot capabilities without the same platform administration permissions.

### Important Distinction

These are Security Copilot platform roles.

They are not identical to Microsoft Entra directory roles.

They also do not automatically grant access to every connected security product.

---

# 28. Copilot Roles vs. Security Data Permissions

This is one of the most important concepts in the module.

A user may have permission to open Security Copilot.

That does **not** automatically mean the user can read every Microsoft Sentinel incident or Microsoft Intune device record.

Access to underlying security data still requires appropriate permissions.

### Example

A security analyst receives the Copilot Contributor role.

The analyst can use the Security Copilot platform.

However, the analyst wants to investigate Microsoft Sentinel incidents.

They may also need an appropriate Microsoft Sentinel role, such as Sentinel Reader, to access the relevant incident information.

### Memory Trick

**Copilot Role = Permission to use the AI platform**

**Product Role = Permission to access the underlying security data**

---

# 29. On-Behalf-Of Access Model

Microsoft Learn describes how many Microsoft plugins use an:

**On-Behalf-Of (OBO) model**

Under this model, Copilot accesses supported services in the context of the signed-in user's existing access.

### ELI5

Security Copilot does not automatically become a Global Administrator just because an analyst asks it to retrieve information.

The underlying services still apply the relevant identity and authorization permissions.

### Important Principle

**Security Copilot cannot legitimately bypass the permissions enforced by the connected service simply because the request is expressed in natural language.**

Some plugins have separate authentication or configuration requirements.

---

# 30. Least Privilege

Microsoft recommends providing the least-privileged role necessary for each user.

For example:

An analyst who only needs to review incidents should not be granted unnecessarily broad administrative rights.

This reinforces an earlier SC-900 concept:

**Zero Trust — Use Least-Privilege Access**

Security Copilot must be governed using the same security principles as other enterprise systems.

---

# 31. Commonly Confused Products

Security Copilot works alongside Microsoft's security portfolio.

It does not replace those services.

| Product | Primary purpose |
|---|---|
| Microsoft Security Copilot | AI-assisted security analysis and workflows |
| Microsoft Sentinel | SIEM and SOAR |
| Microsoft Defender XDR | Unified detection, investigation, and response |
| Microsoft Defender for Cloud | Cloud security posture and workload protection |
| Microsoft Entra | Identity and access management |
| Microsoft Purview | Data security, governance, risk, and compliance |
| Microsoft Intune | Endpoint and device management |

## Example

Microsoft Sentinel detects and correlates events from multiple sources.

Security Copilot helps an analyst understand those events and investigate them more efficiently.

**Sentinel = Security operations data and SIEM/SOAR functionality**

**Security Copilot = AI assistance for understanding and working with security data**

---

# 32. Security Copilot vs. Microsoft 365 Copilot

These products both use generative AI, but their primary purposes differ.

## Microsoft Security Copilot

Designed for security and IT-related tasks.

Examples:

- Incident investigation
- Threat analysis
- Security posture summaries
- KQL generation
- Security workflow assistance

## Microsoft 365 Copilot

Designed primarily for productivity workflows involving supported Microsoft 365 applications.

Examples:

- Drafting documents
- Summarizing meetings
- Analyzing spreadsheets
- Assisting with email and workplace information

### Memory Trick

**Security Copilot = Security workflows**

**Microsoft 365 Copilot = Productivity workflows**

---

# 33. Security Copilot vs. Security Agents

## Security Copilot

Allows analysts to interact with security information through prompts and supported workflows.

## Security Copilot Agent

Can operate with greater autonomy for designated security or IT tasks.

### Important Principle

Both require appropriate organizational controls, including:

- Permission management
- Oversight
- Secure configuration
- Appropriate data access
- Accountability for automated actions

---

# 34. Practical SC-900 Scenarios

## Scenario 1 — Incident Summary

A security analyst wants a natural-language summary of a complex incident affecting several devices and accounts.

**Solution: Microsoft Security Copilot**

---

## Scenario 2 — Security Data Collection

An organization wants to ingest and correlate logs from multiple Microsoft and third-party security products.

**Solution: Microsoft Sentinel**

Security Copilot can assist with analysis after the data is available.

---

## Scenario 3 — KQL Assistance

An analyst knows what to investigate but does not know how to write the required KQL query.

**Solution: Microsoft Security Copilot's query-generation capability**

---

## Scenario 4 — Response Automation

A SOC needs to automatically carry out predefined security response actions.

**Primary capability: SOAR automation, such as Microsoft Sentinel playbooks**

Security Copilot may assist the analyst, but it is not synonymous with Sentinel's playbook functionality.

---

## Scenario 5 — Natural-Language Investigation

An analyst enters:

> Analyze incident 5678 using Defender XDR data.

Security Copilot must identify the request, coordinate available capabilities, retrieve relevant data, and generate a response.

**Key component: Orchestrator**

---

## Scenario 6 — Add External Security Data

An organization wants Security Copilot to work with information from an additional supported security product.

**Relevant component: Plugin**

---

## Scenario 7 — Reusable Investigation Prompts

A SOC wants a prepared sequence of prompts for recurring investigations.

**Relevant feature: Promptbook**

---

## Scenario 8 — Transparent AI Processing

An analyst wants to examine which capabilities contributed to a Copilot response.

**Relevant feature: Process Log**

---

## Scenario 9 — Restricted Security Data

A user can open Security Copilot but cannot retrieve Microsoft Sentinel incident information.

The user may lack the necessary Microsoft Sentinel permissions.

**Relevant concept: Underlying product authorization still applies**

---

## Scenario 10 — Separate Security Teams

A company wants separate Security Copilot environments with individual capacity assignments and access permissions.

**Relevant capability: Workspaces**

---

# 35. GRC / ISSO Career Connection

The following section provides additional career context. It is not a separate official Microsoft Learn instructional unit.

Security Copilot is relevant to governance, risk, compliance, and information assurance work because many security tasks require gathering evidence, analyzing information, and presenting findings.

## Security Control Assessment

An analyst may use Security Copilot to help summarize security information relevant to the evaluation of implemented controls.

Examples:

- Security configuration findings
- Access-control investigations
- Security posture changes
- Potential policy gaps

The underlying findings still require independent verification.

## Incident Documentation

Security Copilot can help organize:

- Incident timelines
- Affected assets
- Investigation summaries
- Possible remediation activities
- Stakeholder reports

## Risk Communication

An ISSO may need to explain technical findings to nontechnical decision-makers.

Security Copilot can assist with translating supported technical information into clear summaries.

## Audit and Evidence Integrity

AI-generated summaries are not a substitute for original system records.

For compliance work, preserve authoritative evidence from relevant systems and verify that summaries accurately represent it.

### Practical GRC Principle

**Security Copilot can help analyze and communicate evidence. It does not itself establish that a security control is effective or that an organization is compliant.**

---

# 36. High-Value Product Distinctions

| If a question mentions... | Think... |
|---|---|
| AI-powered security analysis | Security Copilot |
| Natural-language security requests | Prompts |
| Conversation context | Session |
| One specialized function | Capability |
| Collection of product-specific functions | Plugin |
| Coordinates capabilities to answer a request | Orchestrator |
| Prepared series of prompts | Promptbook |
| Separate environment within a tenant | Workspace |
| More autonomous AI security workflows | Agent |
| Visible processing steps | Process Log |
| Compute resources for Copilot | SCU |
| Additional capacity beyond provisioned amount | Overage |
| Permission to use Copilot | Copilot platform role |
| Permission to read underlying security data | Connected product role |
| Security Copilot inside Defender XDR | Embedded experience |
| Dedicated Security Copilot interface | Standalone experience |

---

# 37. Final Module 1 Cram Sheet

```text
MICROSOFT SECURITY COPILOT
= AI-POWERED SECURITY ANALYSIS

PRIMARY PURPOSE
= HELP SECURITY PROFESSIONALS ANALYZE,
  INVESTIGATE, AND RESPOND FASTER

GENERATIVE AI
= CREATE CONTENT FROM PROMPTS AND CONTEXT

LLM
= LARGE LANGUAGE MODEL

NLP
= NATURAL LANGUAGE PROCESSING

PROMPT
= A SINGLE USER REQUEST

SESSION
= THE CONVERSATION

CAPABILITY
= AN INDIVIDUAL SPECIALIZED FUNCTION

PLUGIN
= COLLECTION OF CAPABILITIES FROM A SOURCE

PROMPTBOOK
= REUSABLE SERIES OF PROMPTS

ORCHESTRATOR
= PLAN AND COORDINATE CAPABILITIES

WORKSPACE
= SEPARATE COPILOT ENVIRONMENT WITHIN TENANT

AGENT
= AI SYSTEM FOR MORE AUTONOMOUS TASKS

STANDALONE
= DEDICATED SECURITY COPILOT INTERFACE

EMBEDDED
= COPILOT INSIDE A SECURITY PRODUCT

PROCESS LOG
= SHOWS PROCESSING AND CAPABILITIES USED

EFFECTIVE PROMPT
= GOAL + CONTEXT + EXPECTATIONS + SOURCE

SCU
= SECURITY COMPUTE UNIT

PROVISIONED CAPACITY
= PLANNED COMPUTE CAPACITY

OVERAGE
= ADDITIONAL CAPACITY FOR EXTRA DEMAND

COPILOT OWNER
= PLATFORM ADMINISTRATION

COPILOT CONTRIBUTOR
= PLATFORM USE

UNDERLYING PRODUCT ROLE
= PERMISSION TO ACCESS SECURITY DATA

OBO
= ON-BEHALF-OF ACCESS MODEL

SENTINEL
= SIEM + SOAR

DEFENDER XDR
= UNIFIED THREAT DETECTION AND RESPONSE

SECURITY COPILOT
= AI ASSISTANCE FOR SECURITY WORKFLOWS
```

---

# 38. Final Mental Model

Imagine a Security Operations Center investigating a potential compromise.

**Microsoft Sentinel** collects and correlates security events.

**Microsoft Defender XDR** provides unified threat investigation and response across supported Microsoft security domains.

**Microsoft Security Copilot** assists the analyst in understanding the information.

The analyst submits a **prompt**.

The **orchestrator** determines which capabilities are needed.

**Plugins** connect to supported security products.

Individual **capabilities** perform specialized analysis tasks.

The system generates a response using the available data and AI capabilities.

The **process log** provides visibility into relevant processing steps.

The analyst verifies the results and determines the appropriate response.

That is the central concept behind Microsoft Security Copilot.

---

# Official Microsoft Learn References

All links below are from the verified module.

[Module Overview](https://learn.microsoft.com/en-us/training/modules/security-copilot-getting-started/)

[Introduction](https://learn.microsoft.com/en-us/training/modules/security-copilot-getting-started/1-introduction)

[Get Acquainted with Microsoft Security Copilot](https://learn.microsoft.com/en-us/training/modules/security-copilot-getting-started/2-describe-security-copilot)

[Describe Microsoft Security Copilot Terminology](https://learn.microsoft.com/en-us/training/modules/security-copilot-getting-started/3-describe-terminology)

[Describe How Microsoft Security Copilot Processes Prompt Requests](https://learn.microsoft.com/en-us/training/modules/security-copilot-getting-started/4-describe-how-copilot-processes-prompts)

[Describe the Elements of an Effective Prompt](https://learn.microsoft.com/en-us/training/modules/security-copilot-getting-started/5-create-effective-prompts)

[Describe How to Enable Microsoft Security Copilot](https://learn.microsoft.com/en-us/training/modules/security-copilot-getting-started/6-describe-how-to-enable-security-copilot)

[Summary and Resources](https://learn.microsoft.com/en-us/training/modules/security-copilot-getting-started/8-summary)

