# SC-900 — Section 2, Module 4
# Describe the Identity Protection and Governance Capabilities of Microsoft Entra

> **Source:** Microsoft Learn — SC-900  
> **Module:** Describe the identity protection and governance capabilities of Microsoft Entra  
> **Verified against current Microsoft Learn content:** October 20, 2026  
> **Duration:** 44 minutes | 10 units | 1,100 XP  
> **Official module:** https://learn.microsoft.com/en-us/training/modules/describe-identity-protection-governance-capabilities/

---

# Module Overview

Microsoft Entra helps organizations answer two important questions:

**Identity Governance:**
> Should this person still have access, and are we managing that access appropriately?

**Identity Protection:**
> Is this identity potentially compromised, and what should we do about it?

This module covers:

| Capability | Primary purpose |
|---|---|
| Microsoft Entra ID Governance | Manage identities and access throughout their lifecycle |
| Access Reviews | Confirm whether existing access is still needed |
| Entitlement Management | Package, request, approve, and expire access |
| Privileged Identity Management (PIM) | Control privileged access using time limits and activation |
| Microsoft Entra ID Protection | Detect, investigate, and remediate identity risks |
| Microsoft Entra Verified ID | Verify digital credentials while protecting privacy |
| Microsoft Security Copilot Integration | Assist identity administrators with AI-powered investigations and workflows |

## The Five Questions to Remember

1. **Who should have access?** — Identity Governance
2. **Should they still have access?** — Access Reviews
3. **How do they request access?** — Entitlement Management
4. **How do we secure administrative privileges?** — PIM
5. **Is the identity compromised?** — ID Protection

Verified ID adds another question:

**Can this person prove a claim about their identity?**

Security Copilot helps administrators investigate and manage these questions more efficiently.

---

# 1. Microsoft Entra ID Governance

## Big Idea

Microsoft Entra ID Governance helps an organization ensure that:

**The right identities have the right access to the right resources for the right amount of time.**

It supports security, productivity, regulatory compliance, and auditability.

### ELI5

Imagine an Army unit with hundreds of personnel.

Soldiers arrive, change duty positions, receive additional responsibilities, and eventually PCS or ETS.

Their access requirements constantly change.

A Soldier working in the S-3 might need access to operational planning resources.

If that Soldier moves to another section, they may no longer need that access.

If the Soldier leaves the unit, their old permissions should not remain active indefinitely.

**Identity Governance manages that entire process digitally.**

## Four Key Governance Questions

Microsoft Entra ID Governance helps organizations determine:

- Which identities should access which resources?
- How are those identities using their access?
- Are organizational controls managing access effectively?
- Can auditors verify that those controls work?

The last question is especially relevant to GRC.

An organization must be able to demonstrate that access is controlled, not simply claim that it is.

---

# 2. The Identity Lifecycle

The identity lifecycle describes how an identity changes throughout its relationship with an organization.

Microsoft commonly uses:

**Joiner → Mover → Leaver (JML)**

## Joiner

Someone joins the organization.

Typical actions:

- Create an identity
- Provision an account
- Assign required groups
- Grant application access
- Prepare the user for their first working day

### Example

A new employee joins Finance.

Microsoft Entra creates or provisions the employee's identity and grants the access needed for that position.

## Mover

An existing employee changes position, department, or responsibilities.

Typical actions:

- Remove permissions no longer required
- Grant newly required permissions
- Update group memberships
- Change application assignments

### Example

The Finance employee moves to Human Resources.

The employee may need new HR applications but should not automatically retain unnecessary Finance permissions.

**Exam concept: Prevent privilege accumulation.**

## Leaver

Someone leaves the organization.

Typical actions:

- Disable or remove access
- Remove group memberships
- Revoke inappropriate permissions
- Deprovision accounts where appropriate
- Preserve required records and audit evidence

### Example

An employee retires.

Their identity and privileges must be handled according to organizational offboarding policies.

**Memory trick:**

JOIN = Give appropriate access  
MOVE = Adjust access  
LEAVE = Remove access

---

# 3. Identity Lifecycle vs. Access Lifecycle

These concepts are related but different.

## Identity Lifecycle

Focuses on the existence and status of the identity.

Examples:

- Account creation
- Account updates
- Account deactivation
- Account removal

## Access Lifecycle

Focuses on the permissions assigned to the identity.

Examples:

- Group memberships
- Application roles
- SharePoint access
- Administrative permissions
- Periodic access reviews

| Identity Lifecycle | Access Lifecycle |
|---|---|
| Does the account exist? | What can the account access? |
| Is the employee active? | Does the employee need this permission? |
| Has the person left? | Should access be removed? |
| Account provisioning | Permission assignment and review |

An account can remain active while its access requirements change.

That distinction is important.

---

# 4. Identity Governance Capabilities

Microsoft Entra combines several capabilities to automate governance.

## Inbound Provisioning

Identity information can originate from an HR system, such as Workday or SuccessFactors.

Changes in the HR system can initiate identity updates.

### ELI5

HR says:

> We hired a new employee.

The identity system responds:

> Create the employee's account and begin onboarding.

---

## Lifecycle Workflows

Lifecycle Workflows automate tasks triggered by significant identity events.

Examples:

- Before an employee starts
- When an employee becomes active
- When responsibilities change
- When an employee leaves

### Exam Shortcut

**Joiner / Mover / Leaver automation = Lifecycle Workflows**

Lifecycle Workflows are not the same thing as Access Reviews.

A lifecycle workflow responds to an identity event.

An access review asks whether an existing permission should continue.

---

## User Provisioning

Provisioning creates, updates, or removes user accounts in supported applications.

For example:

A new employee may need accounts in Microsoft Entra, an HR platform, and other enterprise applications.

Provisioning helps keep those accounts synchronized.

---

## Dynamic Groups

Dynamic groups determine membership based on identity attributes.

Example rule:

```text
Department = Finance
```

An employee whose department is Finance may be added automatically.

If their department changes, group membership can be reevaluated.

### Important Distinction

**Dynamic Group = Membership based on attributes**

**Lifecycle Workflow = Actions triggered by lifecycle events**

**Entitlement Management = Governed access assignments, requests, approvals, and expiration**

---

# 5. Identity Governance for AI Agents

The current Microsoft Learn module extends identity governance to AI agents.

Microsoft Entra Agent ID provides identities specifically designed for AI agents.

An AI agent may need to interact with enterprise applications and data.

That access must be governed.

## Human Sponsors

Microsoft describes a human sponsor as the person accountable for an agent's purpose and lifecycle.

The sponsor helps ensure that:

- The agent has an appropriate business purpose
- The agent receives appropriate permissions
- The agent's access is reviewed
- Unnecessary access does not remain active

If a sponsor leaves the organization, the module describes automatic sponsorship reassignment to the sponsor's manager.

### ELI5

An AI agent should not receive permanent, unrestricted organizational access simply because it isn't human.

Someone must remain accountable for it.

**Key principle: Least privilege applies to human identities and AI agent identities.**

---

# 6. Access Reviews

## Big Idea

Microsoft Entra Access Reviews help organizations determine:

**Does this identity STILL need this access?**

They support periodic access recertification.

### ELI5

Suppose an employee was granted access to a sensitive application six months ago.

The employee may no longer need it.

An access review asks an authorized reviewer:

> Should this person keep the permission?

The reviewer decides whether to approve or deny continued access.

---

## What Can Be Reviewed?

Access reviews can govern access associated with:

- Groups
- Enterprise applications
- Guest users
- Access packages
- Microsoft Entra administrative roles
- Azure resource roles through supported PIM experiences

## Common Scenarios

### Excessive Administrative Access

A security administrator discovers too many Global Administrators.

Access reviews help determine who still requires those privileges.

### Guest Access

A contractor completed a project but still belongs to sensitive groups.

A review helps determine whether access should be removed.

### Critical Applications

An organization requires quarterly confirmation that users still need access to financial systems.

Access reviews provide the recertification process.

### Policy Exceptions

An organization has granted special access exceptions.

Periodic reviews verify whether those exceptions remain justified.

---

# 7. How Access Reviews Work

A simplified workflow:

1. An administrator creates an access review.
2. The administrator selects the resources or assignments being reviewed.
3. Reviewers are assigned.
4. Reviewers evaluate access.
5. They approve or deny continued access.
6. Decisions are recorded.
7. Changes can be applied when the review is completed.

## Who Can Be a Reviewer?

Depending on configuration:

- Administrators
- Managers
- Group owners
- Resource owners
- Users reviewing their own access

Self-review is also called **self-attestation**.

## Recurring Reviews

Reviews can recur on a schedule, including:

- Weekly
- Monthly
- Quarterly
- Annually

### Memory Trick

**Access Review = Periodic permission inspection**

---

# 8. Applying Review Decisions

An important detail from the current module:

**Review decisions do not immediately change access while the review is in progress.**

After completion, the organization can manually apply decisions or configure automatic application.

However, removal from dynamic groups or groups originating on-premises may require changes through the systems or rules controlling those groups.

## Multi-Stage Access Reviews

Microsoft Entra supports up to **three review stages**.

This allows multiple reviewers to evaluate access sequentially.

Example:

1. Employee's manager reviews access.
2. Application owner reviews the request.
3. Security or compliance reviewer provides another review stage.

These stages help organizations satisfy more complex approval and audit requirements.

## AI-Powered Recommendations

Current Microsoft Learn describes AI-supported access review recommendations based on signals such as:

- Sign-in activity
- Group affiliation
- Contextual identity information
- Access patterns that differ from peers

These recommendations support reviewer decisions.

**They do not eliminate the need for appropriate human oversight.**

---

# 9. Entitlement Management

## Big Idea

Entitlement Management manages:

**Who can request access, who approves it, what they receive, and when it expires.**

It helps organizations manage access at scale.

### ELI5

Think of an access package like an equipment issue bundle.

A person joins a particular mission or project.

Instead of individually requesting every resource, they request a predefined package of everything needed.

---

# 10. Access Packages

An **access package** is a collection of resources and access permissions.

A package can contain access to:

- Security groups
- Microsoft 365 Groups
- Enterprise applications
- SharePoint Online sites

### Example

```text
Access Package: Project Falcon

Resources:
- Project Falcon Microsoft 365 Group
- Project Falcon SharePoint site
- Project management application

Rules:
- Manager approval required
- Access expires after 90 days
- Continued access subject to review
```

An employee requests Project Falcon access.

If the request is approved, the relevant permissions are assigned.

When the assignment expires, the permissions can be removed.

---

# 11. Entitlement Management Policies

Policies control how an access package is assigned.

A policy can determine:

**Who can request access?**

**Who must approve the request?**

**How long should access last?**

**What happens when access expires?**

### Memory Trick

**Access Package = WHAT access is bundled**

**Access Policy = WHO can receive it and under WHAT rules**

Entitlement Management can also use identity attributes for automatic access assignments.

---

# 12. External User Access

Entitlement Management supports users outside the organization.

Example:

A contractor does not yet have a guest identity in the company's tenant.

The contractor requests an access package.

If approved, Microsoft Entra can invite that person into the directory and assign the relevant access.

When the assignment expires, the guest identity may be removed automatically if it has no remaining access package assignments, depending on the configured policy.

### Key Concept

**External access also requires lifecycle management.**

Guest accounts should not remain indefinitely simply because nobody remembers to remove them.

---

# 13. Entitlement Management for AI Agents

Current Microsoft Learn also describes access packages for AI agent identities.

An AI agent may receive a governed set of permissions.

A human sponsor remains responsible for determining whether that access is still needed.

### Example

An automated reporting agent needs access to a specific dataset.

Entitlement Management can support granting the appropriate access for the required period.

The agent should not retain access to unrelated resources.

---

# 14. Microsoft Entra Terms of Use

Terms of Use help an organization ensure users acknowledge legal, regulatory, or organizational requirements before accessing resources.

### ELI5

Before entering a restricted system, the user must agree to the applicable rules.

## Common Scenarios

- Accept a confidentiality agreement
- Acknowledge organizational security policies
- Agree to legal disclaimers
- Periodically reaffirm compliance requirements

Administrators provide the terms in a PDF document.

Microsoft Entra can present these terms to users, including mobile users.

## Connection to Conditional Access

Conditional Access can require a user to accept Terms of Use before access is granted.

### Exam Shortcut

**Require legal disclaimer acceptance before application access = Microsoft Entra Terms of Use**

Do not confuse Terms of Use with Entitlement Management.

Terms of Use concerns acknowledging requirements.

Entitlement Management concerns governing access assignments.

---

# 15. Privileged Identity Management — PIM

## Big Idea

Microsoft Entra Privileged Identity Management controls and monitors:

**Privileged administrative access**

PIM helps organizations reduce unnecessary permanent privileges.

### ELI5

Imagine an employee needs Global Administrator permissions to perform maintenance.

Instead of holding those permissions continuously, the employee requests temporary access.

After completing the task, those elevated permissions expire.

**That is the principle behind PIM.**

---

# 16. Just-in-Time Access

PIM supports **Just-in-Time (JIT)** privileged access.

JIT means:

**Grant elevated permissions only when required.**

This reduces the risks of permanent administrative access.

### Example

A user needs elevated privileges for a scheduled maintenance task.

The privileges activate for a limited period.

Afterward, the privileged access expires.

### Security Benefit

If an attacker compromises the user's account outside the activation window, the account may not have the elevated privileges the attacker wants.

JIT does not eliminate all risk, but it can reduce unnecessary exposure.

---

# 17. PIM Security Controls

PIM provides controls including:

## Time-Limited Activation

Privileges are active only for an approved period.

## Justification

A user provides a reason for requiring privileged access.

## Approval

An authorized reviewer may be required to approve activation.

## MFA

Role activation can require strong authentication.

## Notifications

Relevant administrators can be notified of privileged role activation.

## Auditing

Privileged access assignments and activations can be logged and reviewed.

### Memory Trick

**PIM = Privilege, only when needed, with oversight**

---

# 18. Eligible vs. Active Assignments

This distinction is important.

## Eligible Assignment

The user is eligible to activate the role but does not continuously hold its active privileges.

### Example

A user is eligible for Global Administrator.

They must activate the role before using those administrative permissions.

## Active Assignment

The user already holds the privileges associated with the assignment.

No separate activation is required.

| Eligible | Active |
|---|---|
| Can request or activate privileges | Already has assigned privileges |
| Activation step required | No activation step required |
| Supports JIT administration | Represents active access |

**Eligible does not mean the user already has all the active administrative permissions.**

---

# 19. PIM Workflow

Microsoft describes four major activities:

## Assign

Assign a privileged role.

Important assignment attributes include:

- Identity or principal
- Scope
- Assignment type
- Duration

## Activate

An eligible identity activates the role when privileges are needed.

Depending on configuration, the user may need MFA, justification, and approval.

## Approve or Deny

Designated approvers review activation requests when approval is required.

## Extend or Renew

An existing assignment can be extended before expiration.

An expired assignment may require renewal.

### Memory Trick

**Assign → Activate → Approve/Deny → Extend/Renew**

---

# 20. What Can PIM Manage?

PIM supports privileged access involving:

## Microsoft Entra Roles

Examples:

- Global Administrator
- User Administrator
- Security Administrator

## Azure Roles

Examples include Azure RBAC assignments affecting:

- Management groups
- Subscriptions
- Resource groups
- Azure resources

## PIM for Groups

Provides just-in-time:

- Group membership
- Group ownership

This can govern access to resources controlled through group assignments.

---

# 21. PIM vs. RBAC vs. Access Reviews

These are related but distinct.

| Capability | Main question |
|---|---|
| RBAC | What permissions does a role provide? |
| PIM | When may a privileged identity use those permissions? |
| Access Reviews | Does the identity still need those permissions? |

### Example

**RBAC:** User Administrator can manage specified identity resources.

**PIM:** A particular administrator activates that role temporarily.

**Access Reviews:** Management periodically confirms whether that administrator should remain eligible for the role.

### Critical Concept

**RBAC defines permissions. PIM governs privileged use. Access Reviews reassess continued need.**

---

# 22. Microsoft Entra ID Protection

## Big Idea

Microsoft Entra ID Protection helps organizations:

**Detect, investigate, and remediate identity-based risks.**

It supports risk detection for user identities and workload identities.

### ELI5

An account may successfully authenticate, but something about the activity is suspicious.

For example:

- The credentials appear in a known leak.
- The user signs in from an anonymous IP address.
- Sign-in behavior differs substantially from normal activity.
- The account displays indications of compromise.

ID Protection helps identify those risks.

---

# 23. Sign-In Risk vs. User Risk

This distinction is central to the module.

## Sign-In Risk

Measures the probability that:

**A particular authentication request was not performed by the legitimate identity owner.**

Examples:

- Anonymous IP address
- Atypical travel
- Unfamiliar sign-in properties

### ELI5

> Is THIS login suspicious?

## User Risk

Measures the probability that:

**The identity or account itself is compromised.**

Examples:

- Leaked credentials
- User-reported suspicious activity
- Other evidence of account compromise

### ELI5

> Is THIS ACCOUNT compromised?

| Sign-In Risk | User Risk |
|---|---|
| Particular authentication event | Identity/account |
| Suspicious location or behavior | Evidence of compromised credentials |
| Evaluates a sign-in | Evaluates the user identity |

### Memory Trick

**Sign-In Risk = EVENT**

**User Risk = ACCOUNT**

---

# 24. Three ID Protection Reports

Microsoft Entra ID Protection provides reporting to support investigations.

## Risk Detections

Records individual detected risk signals.

## Risky Sign-Ins

Identifies authentication events associated with detected risk.

## Risky Users

Identifies identities that have risk detections or risky sign-in activity associated with them.

### Memory Trick

**Detection = Signal**

**Risky Sign-In = Suspicious Event**

**Risky User = Potentially Compromised Account**

---

# 25. Responding to Identity Risk

ID Protection supports several approaches.

## Automated Remediation

Risk information can be used with Conditional Access.

Depending on the policy and risk:

- Require stronger authentication
- Require MFA
- Require a secure password change
- Block access when appropriate

Completing the required remediation can resolve certain identity risks.

## Manual Investigation

Administrators can review risk events and determine whether they represent genuine compromise.

Depending on the investigation, administrators can confirm or dismiss risk.

## Export for Investigation

Identity risk data can be exported or integrated with other tools.

Examples include:

- SIEM solutions
- Microsoft Graph APIs
- Log Analytics
- Event Hubs
- Storage accounts
- Microsoft Defender XDR investigation workflows

---

# 26. ID Protection vs. Conditional Access

These capabilities work together but perform different jobs.

## ID Protection

**Detects and evaluates identity risk.**

## Conditional Access

**Applies policy decisions based on conditions and signals.**

### Scenario

ID Protection detects a high-risk sign-in.

Conditional Access evaluates the risk signal.

The policy requires additional authentication or blocks access.

### Memory Trick

**ID Protection = Detect the danger**

**Conditional Access = Enforce the access decision**

---

# 27. ID Protection vs. Password Protection

Do not confuse these products.

## Microsoft Entra ID Protection

Detects risks involving identities and sign-ins.

Examples:

- Leaked credentials
- Suspicious authentication activity
- Risky users

## Microsoft Entra Password Protection

Helps prevent weak or easily guessed passwords.

Examples:

- Microsoft's global banned-password list
- Custom banned-password terms
- Password-spray defense

| Scenario | Capability |
|---|---|
| User credentials appear compromised | ID Protection |
| Suspicious sign-in from anonymous IP | ID Protection |
| Organization wants to ban its name from passwords | Password Protection |
| Block commonly used weak passwords | Password Protection |

---

# 28. Microsoft Entra Verified ID

## Big Idea

Microsoft Entra Verified ID helps organizations verify:

**Claims about someone's identity or qualifications.**

It is a managed service for verifiable digital credentials based on open standards.

### ELI5

Imagine someone says:

> I graduated from this university.

Instead of relying only on a screenshot of a diploma, the person presents a cryptographically verifiable digital credential issued by the university.

The receiving organization can verify that the credential is genuine.

Verified ID supports privacy-preserving verification rather than requiring users to disclose unnecessary information.

---

# 29. Verifiable Credentials

A verifiable credential is digitally issued evidence supporting a claim.

Examples:

- Employment status
- Educational qualification
- Professional qualification
- Identity verification
- Membership or eligibility

These credentials use cryptographic methods so receiving organizations can check their authenticity.

The system follows open standards and decentralized identity principles.

### Decentralized Identity

The goal is to give people greater control over how they present verified information.

A credential does not need to mean the recipient gains unlimited access to the holder's personal information.

---

# 30. The Three Main Verified ID Participants

## Issuer

Creates and issues the verified credential.

Examples:

- University
- Government agency
- Employer
- Identity verification provider

### ELI5

**Issuer = Organization that vouches for the claim**

## Holder

The person or entity that receives and presents the credential.

The holder can manage credentials in a digital wallet.

### ELI5

**Holder = Person carrying the proof**

## Verifier

The organization requesting and checking proof.

Examples:

- Employer
- Airline
- Financial institution

### ELI5

**Verifier = Organization checking the proof**

---

# 31. Verified ID Example

Imagine applying for a cybersecurity position.

```text
University
   |
   | Issues digitally signed qualification
   v
Credential Holder
   |
   | Presents credential
   v
Prospective Employer
   |
   | Verifies authenticity
   v
Trust established
```

The employer verifies the credential using cryptographic trust mechanisms rather than relying solely on an easily altered document.

### Memory Trick

**Issuer = Creates**

**Holder = Presents**

**Verifier = Checks**

---

# 32. Verifiable Data Registry and DIDs

Verified ID uses supporting trust information to help validate credentials.

A verifiable data registry can provide associated metadata, including public-key information.

## Decentralized Identifier — DID

A DID is an identifier used within decentralized identity systems.

The current Microsoft Learn module describes Microsoft's use of:

**did:web**

This associates an issuer's decentralized identifier with a web domain controlled by the organization.

### ELI5

The web domain provides a recognizable foundation for verifying who issued the credential.

## Expiration and Revocation

Verifiable credentials can have expiration and revocation information.

A credential that was valid last year should not necessarily be considered valid forever.

---

# 33. Verified ID and Account Recovery

This is one of the newer and more important additions to the current module.

Verified ID supports Microsoft Entra account recovery.

Consider someone who loses:

- Their phone
- Their Authenticator access
- Their backup authentication methods

The organization must re-establish that the person is the legitimate account owner.

Verified ID can support a high-assurance verification process.

---

# 34. Account Recovery vs. SSPR

These concepts are different.

## Self-Service Password Reset — SSPR

Used when the user needs to reset or recover password access and can complete the configured verification process using registered methods.

## Account Recovery

Designed for situations where the user has lost access to their normal authentication methods and identity must be verified through another trusted process.

### Memory Trick

**SSPR = Reset access using existing verification methods**

**Account Recovery = Re-establish identity when those methods are unavailable**

---

# 35. Verified ID Face Check

The current Microsoft Learn module describes an account recovery process involving:

1. Identity verification through a trusted provider.
2. Verification of government-issued identity documents.
3. Issuance of a verifiable credential.
4. A real-time selfie comparison against document identity information.
5. Issuance of a Temporary Access Pass after successful verification.

## Face Check

Face Check uses Azure AI capabilities to help compare the user's live selfie with identity information.

Microsoft emphasizes sharing verification results rather than unnecessary underlying personal data.

## Temporary Access Pass — TAP

After identity is verified, a Temporary Access Pass can help the user sign in and register new authentication methods.

### Exam Shortcut

**Lost all authentication methods + strong identity verification = Account Recovery / Verified ID**

**Temporary credential for re-registering authentication = TAP**

---

# 36. Verified ID and AI Impersonation

Verified ID can also help establish digital trust in environments where AI-generated impersonation is a concern.

Examples:

- Deepfake identity fraud
- Fraudulent identity claims
- Impersonation during remote verification

Cryptographically verifiable credentials can provide evidence beyond merely trusting an image, video, or claim.

Verified ID does not eliminate identity fraud, but it adds mechanisms for validating claims.

---

# 37. Microsoft Security Copilot Integration

## Big Idea

Microsoft Security Copilot is an AI-powered security assistant.

Microsoft Entra integrates with Security Copilot to help administrators:

- Investigate identity-related risks
- Analyze sign-in and audit information
- Examine permissions and role assignments
- Review governance data
- Identify access-policy gaps
- Troubleshoot identity issues

### ELI5

An identity administrator might normally search several reports and logs manually.

With Security Copilot, the administrator can ask a question using natural language and receive an organized analysis.

---

# 38. Information Security Copilot Can Analyze

The Entra integration can work with supported information such as:

- Users
- Groups
- Sign-in logs
- Audit logs
- Provisioning logs
- Conditional Access policies
- Authentication methods
- Role assignments
- Identity risk reports
- Governance information

### Example Prompts

```text
Show the recent risky sign-ins for this user.

Summarize the identity risk associated with this account.

Find recent changes to this user's permissions.

Show the status of outstanding access reviews.

Identify gaps in existing Conditional Access coverage.
```

These illustrate the types of administrative investigations supported by the integration.

---

# 39. Standalone vs. Embedded Copilot

Microsoft Entra supports two Security Copilot experiences.

## Standalone Experience

Administrators use the dedicated Security Copilot environment.

They can enter natural-language prompts and investigate supported identity information.

### ELI5

**Standalone = Open the Copilot tool and ask questions**

## Embedded Experience

Security Copilot capabilities appear directly inside Microsoft Entra administrative workflows.

Example:

An administrator opens an identity risk report.

Copilot can help summarize relevant findings and suggest remediation options.

### ELI5

**Embedded = Copilot assistance inside the tool you're already using**

---

# 40. Security Copilot Use Cases by Entra Product

| Entra product | Copilot assistance |
|---|---|
| Microsoft Entra ID | User, group, authentication, device, and sign-in analysis |
| ID Protection | Risk summaries, investigations, remediation recommendations |
| ID Governance | Access reviews, entitlements, privileged access, lifecycle workflows |
| Internet Access / Private Access | Global Secure Access traffic and network-log investigation |

### Key Distinction

**Security Copilot assists the administrator.**

It does not replace the underlying Entra products or guarantee that every AI-generated explanation is correct.

Human verification and appropriate authorization remain important.

---

# 41. Microsoft Entra Agents

The current Microsoft Learn module introduces specialized AI agents for identity administration.

These agents can analyze identity environments, recommend changes, and perform supported tasks with controlled permissions.

Agents use distinct identities and are managed in the Microsoft Entra admin center.

---

# 42. Conditional Access Optimization Agent

## Purpose

Analyze Conditional Access configurations and identify opportunities for improvement.

Examples:

- Gaps in policy coverage
- Users not adequately protected
- Applications without appropriate controls
- Overlapping or conflicting policies
- Configurations that depart from Zero Trust recommendations

The current module describes scheduled analysis approximately every 24 hours, with manual triggering also supported.

### Memory Trick

**Conditional Access Optimization Agent = Find gaps in access policies**

---

# 43. Identity Risk Management Agent

The current module also describes the **Identity Risk Management Agent (Preview)**.

## Purpose

Assist administrators with investigations involving identity risk.

Examples:

- Investigate risky users
- Summarize potential compromise
- Identify relevant evidence
- Recommend appropriate response actions

### Memory Trick

**Identity Risk Management Agent = Help investigate risky identities**

Because this capability is identified as Preview, availability and supported behaviors may change.

---

# 44. Microsoft Security Store

Microsoft Security Store provides a centralized environment for discovering supported security agents and solutions.

The current module describes the Security Store being accessible within the Entra administrative experience.

### Exam-Level Concept

**Security Store = Discover and deploy supported security agents and solutions**

Do not confuse it with Microsoft Security Copilot itself.

---

# 45. Security Copilot Limitations

Security Copilot uses AI and machine learning.

AI-generated results may contain errors.

Therefore, an administrator should:

- Verify important findings
- Review recommendations before acting
- Maintain appropriate access permissions
- Apply organizational approval requirements
- Preserve accountability for security decisions

### Important Principle

**AI can assist security decisions without replacing human accountability.**

---

# 46. The Critical Product Distinctions

This table is the most important review material in the module.

| Scenario | Correct capability |
|---|---|
| New employee needs onboarding tasks | Lifecycle Workflows |
| Employee transfers departments | Lifecycle Workflows / provisioning |
| Automatically assign a group based on department | Dynamic Groups |
| User needs a bundle of project resources | Entitlement Management |
| Contractor access should expire | Entitlement Management |
| Determine whether existing access is still necessary | Access Reviews |
| Quarterly administrator permission recertification | Access Reviews |
| Administrator needs temporary elevated permissions | PIM |
| Activate a privileged role with justification | PIM |
| Detect leaked credentials | ID Protection |
| Investigate suspicious sign-in activity | ID Protection |
| Require MFA based on sign-in risk | Conditional Access using risk signals |
| Verify a digitally issued qualification | Verified ID |
| Recover access after all authentication methods are lost | Verified ID-supported account recovery |
| Analyze risky sign-ins using natural language | Security Copilot |
| Find gaps in Conditional Access policies | Conditional Access Optimization Agent |
| Investigate risky identities using a specialized agent | Identity Risk Management Agent |

---

# 47. Commonly Confused Concepts

## Governance vs. Protection

**Governance:** Are permissions appropriate and managed?

**Protection:** Are identities showing signs of compromise?

---

## Access Reviews vs. Entitlement Management

**Access Reviews:** Should existing access continue?

**Entitlement Management:** How is access bundled, requested, assigned, and expired?

---

## PIM vs. Conditional Access

**PIM:** When may an identity activate elevated privileges?

**Conditional Access:** Under what conditions may an identity access a resource?

---

## PIM vs. RBAC

**RBAC:** What permissions belong to a role?

**PIM:** How is privileged use of that role governed?

---

## Lifecycle Workflows vs. Dynamic Groups

**Lifecycle Workflows:** Run tasks because an identity lifecycle event occurs.

**Dynamic Groups:** Determine group membership from attributes.

---

## ID Protection vs. Password Protection

**ID Protection:** Detect compromise-related identity risks.

**Password Protection:** Prevent use of weak and banned passwords.

---

## Verified ID vs. MFA

**Verified ID:** Verify identity claims or credentials.

**MFA:** Authenticate using multiple factors.

---

## Security Copilot vs. ID Protection

**ID Protection:** Produces identity risk detections and reports.

**Security Copilot:** Helps analyze and investigate information from supported systems.

---

# 48. Practical Scenarios

## Scenario 1: Departing Contractor

A contractor finishes a six-month assignment.

Their access package reaches its expiration date.

The organization wants project resources removed.

**Primary solution: Entitlement Management**

---

## Scenario 2: Quarterly Permission Audit

The security team must confirm whether employees still require access to sensitive applications.

Managers should formally approve or deny continued access.

**Primary solution: Access Reviews**

---

## Scenario 3: Temporary Global Administrator

An administrator needs elevated privileges for a short maintenance window.

The organization requires justification and time-limited activation.

**Primary solution: PIM**

---

## Scenario 4: Suspected Compromise

An employee's credentials appear in a known compromise and suspicious authentication activity is detected.

**Primary solution: ID Protection**

Risk-based Conditional Access policies may then enforce appropriate access controls.

---

## Scenario 5: New Hire

HR creates an employment record.

The organization wants an automated sequence of onboarding activities.

**Primary solution: Lifecycle Workflows**

Provisioning can create the necessary accounts.

---

## Scenario 6: University Credential Verification

An employer wants to verify that an applicant holds a qualification issued by a university.

**Primary solution: Verified ID**

---

## Scenario 7: Lost Authenticator and Backup Methods

An employee loses all configured authentication methods.

The organization must re-establish identity before restoring account access.

**Primary solution: Verified ID-supported account recovery**

A Temporary Access Pass can help restore authentication enrollment after identity verification.

---

## Scenario 8: Security Policy Analysis

An administrator wants an AI assistant to examine identity risks and summarize unusual sign-in activity.

**Primary solution: Microsoft Security Copilot integration**

---

# 49. GRC / ISSO Career Connection

The following is additional career context, not a separate Microsoft Learn unit.

This module is particularly relevant to governance, risk, compliance, and information assurance work.

## Account Management

Identity lifecycle management supports keeping accounts current as personnel join, move, and leave.

A related NIST SP 800-53 control is:

**AC-2 — Account Management**

## Least Privilege

PIM and appropriate access assignments help limit unnecessary administrative permissions.

A related control is:

**AC-6 — Least Privilege**

## Separation of Duties

Entitlement Management can help support policies that prevent conflicting access assignments.

A related control is:

**AC-5 — Separation of Duties**

## Access Enforcement

RBAC and Conditional Access support enforcement of authorized access.

A related control is:

**AC-3 — Access Enforcement**

## Auditability

Access reviews, identity logs, and PIM auditing provide evidence that supports ongoing security oversight.

### Practical ISSO Perspective

An ISSO may need to verify not just that a control exists, but that its implementation is functioning and can be demonstrated.

Examples:

- Are accounts disabled when personnel depart?
- Are elevated permissions documented and limited?
- Are permissions periodically reviewed?
- Are suspicious identity events investigated?
- Is access appropriate to assigned responsibilities?

**Governance requires both effective controls and verifiable evidence.**

---

# 50. Final Module 4 Cram Sheet

```text
MICROSOFT ENTRA ID GOVERNANCE
= RIGHT ACCESS, RIGHT PEOPLE, RIGHT TIME

IDENTITY LIFECYCLE
= JOINER / MOVER / LEAVER

LIFECYCLE WORKFLOWS
= AUTOMATE IDENTITY LIFECYCLE TASKS

DYNAMIC GROUPS
= AUTOMATIC MEMBERSHIP BASED ON ATTRIBUTES

ACCESS REVIEWS
= DO YOU STILL NEED THIS ACCESS?

ENTITLEMENT MANAGEMENT
= REQUEST / APPROVE / ASSIGN / EXPIRE ACCESS

ACCESS PACKAGE
= BUNDLE OF RESOURCES AND PERMISSIONS

TERMS OF USE
= ACCEPT REQUIRED AGREEMENT BEFORE ACCESS

PIM
= JUST-IN-TIME PRIVILEGED ACCESS

PIM ELIGIBLE
= CAN ACTIVATE A ROLE

PIM ACTIVE
= PRIVILEGES ALREADY ACTIVE

ID PROTECTION
= DETECT / INVESTIGATE / REMEDIATE IDENTITY RISK

SIGN-IN RISK
= IS THIS AUTHENTICATION EVENT SUSPICIOUS?

USER RISK
= IS THE ACCOUNT COMPROMISED?

CONDITIONAL ACCESS
= APPLY POLICY USING ACCESS AND RISK SIGNALS

VERIFIED ID
= VERIFY DIGITALLY ISSUED IDENTITY CLAIMS

ISSUER
= CREATES THE CREDENTIAL

HOLDER
= PRESENTS THE CREDENTIAL

VERIFIER
= CHECKS THE CREDENTIAL

ACCOUNT RECOVERY
= RESTORE ACCESS WHEN AUTH METHODS ARE LOST

TAP
= TEMPORARY ACCESS PASS FOR AUTHENTICATION SETUP

SECURITY COPILOT
= AI ASSISTANCE FOR IDENTITY ADMINISTRATION

COPILOT STANDALONE
= DEDICATED COPILOT EXPERIENCE

COPILOT EMBEDDED
= ASSISTANCE INSIDE THE ENTRA ADMIN CENTER

CONDITIONAL ACCESS OPTIMIZATION AGENT
= FIND POLICY GAPS

IDENTITY RISK MANAGEMENT AGENT
= HELP INVESTIGATE RISKY IDENTITIES
```

---

# Final Mental Model

Imagine managing an organization's entire workforce.

**Lifecycle Workflows** help onboard people, process changes, and offboard them.

**Entitlement Management** provides the resource bundles they need.

**Access Reviews** periodically confirm whether their permissions remain appropriate.

**PIM** limits when administrators can exercise elevated privileges.

**ID Protection** detects potentially compromised identities and suspicious authentication activity.

**Verified ID** supports trusted, privacy-conscious credential verification and identity recovery.

**Security Copilot** helps administrators analyze information and manage the environment more efficiently.

Together, these capabilities support three fundamental objectives:

**1. Give appropriate access.**

**2. Continuously verify that access remains appropriate.**

**3. Detect and respond when identity security is threatened.**

---

# Official Microsoft Learn References

All links below belong to the verified module or its corresponding instructional units.

1. [Module overview](https://learn.microsoft.com/en-us/training/modules/describe-identity-protection-governance-capabilities/)
2. [Microsoft Entra ID Governance](https://learn.microsoft.com/en-us/training/modules/describe-identity-protection-governance-capabilities/2-describe-identity-governance)
3. [Access Reviews](https://learn.microsoft.com/en-us/training/modules/describe-identity-protection-governance-capabilities/3-describe-what-entitlement-management-access-reviews)
4. [Entitlement Management and Terms of Use](https://learn.microsoft.com/en-us/training/modules/describe-identity-protection-governance-capabilities/3a-describe-entitlement-management-terms-use)
5. [Privileged Identity Management](https://learn.microsoft.com/en-us/training/modules/describe-identity-protection-governance-capabilities/4-describe-privileged-identity-management)
6. [Microsoft Entra ID Protection](https://learn.microsoft.com/en-us/training/modules/describe-identity-protection-governance-capabilities/5-describe-azure)
7. [Microsoft Entra Verified ID](https://learn.microsoft.com/en-us/training/modules/describe-identity-protection-governance-capabilities/5b-describe-entra-verified-id)
8. [Microsoft Security Copilot Integration](https://learn.microsoft.com/en-us/training/modules/describe-identity-protection-governance-capabilities/5c-describe-entra-integration-in-copilot)
