# SC-900 — Section 2, Module 3
# Describe Access Management Capabilities of Microsoft Entra

> **Source:** Microsoft Learn — SC-900  
> **Module:** Describe access management capabilities of Microsoft Entra  
> **Verified against current Microsoft Learn content:** October 16, 2026

---

# Module Overview

Microsoft Entra does more than authenticate identities.

It also determines:

**Who or what should be allowed to access a resource, under what conditions, and with what permissions.**

This module focuses on three major areas:

| Topic | Core Idea |
|---|---|
| Conditional Access | Make access decisions based on signals and conditions |
| Global Secure Access | Apply Zero Trust controls to network access |
| Microsoft Entra RBAC | Control administrative permissions using roles |

---

# 1. Conditional Access

## Big Idea

Microsoft Entra Conditional Access is Microsoft's:

**Zero Trust policy engine**

It evaluates signals about an access request and decides what should happen.

### ELI5

Think:

> IF this happens, THEN require this.

Example:

> IF a user signs in from an unfamiliar location, THEN require MFA.

---

# Authentication Happens First

Conditional Access is evaluated:

**After first-factor authentication**

This is important.

Conditional Access does NOT replace authentication.

The basic flow is:

1. User attempts to sign in.
2. First-factor authentication succeeds.
3. Conditional Access evaluates the request.
4. Microsoft decides whether additional requirements should apply.
5. Access is allowed, restricted, or blocked.

### Memory Trick

**Authenticate first → Conditional Access second**

---

# Conditional Access Is Not a Firewall

Conditional Access is designed to make:

**Access decisions**

It is not intended to be the organization's primary defense against attacks such as:

- Denial-of-Service — DoS
- DDoS

It can, however, use security and risk signals when making access decisions.

---

# Conditional Access Policy Structure

A Conditional Access policy has two main components:

## Assignments

**When should this policy apply?**

## Access Controls

**What should happen when it applies?**

### Memory Trick

**Assignments = IF**

**Access Controls = THEN**

---

# 2. Conditional Access Assignments

Assignments define the:

**Who**

**What**

**Where**

**When**

of the policy.

If multiple assignments are configured, they are logically combined.

The configured conditions must be satisfied for the policy to trigger.

---

# Users

Policies can target:

- All users
- Specific users
- Groups
- Directory roles
- External guests
- Workload identities
- Agent identities

### Current Concept

Microsoft also supports Conditional Access scenarios involving:

**AI agent identities**

This extends Zero Trust access controls beyond human users.

---

# Target Resources

Policies can target resources such as:

- Microsoft 365
- Microsoft Entra registered applications
- Cloud applications
- User actions
- Authentication context
- Global Secure Access traffic profiles

---

# Network

Conditional Access can consider where the connection originates.

Examples:

- Trusted network
- Trusted IP range
- Named location
- Compliant network

### Example

IF:

User signs in from outside a trusted network

THEN:

Require MFA

---

# Conditions

Conditional Access can evaluate multiple signals.

Important examples include:

## Sign-In Risk

How suspicious is this specific authentication attempt?

## User Risk

How likely is it that the user's account has been compromised?

## Insider Risk

Risk information can come from Microsoft Purview.

## Device Platform

Examples:

- Windows
- macOS
- iOS
- Android

## Client Application

Examples:

- Browser
- Mobile app
- Desktop client

## Device Filters

Policies can target devices based on attributes.

---

# Sign-In Risk vs. User Risk

Do not confuse these.

## Sign-In Risk

**Is this particular sign-in suspicious?**

## User Risk

**Is this user's identity likely compromised overall?**

### Memory Trick

**Sign-in risk = Event**

**User risk = Account**

---

# 3. Conditional Access Controls

Once the assignments match, Conditional Access applies:

**Access Controls**

These determine what happens next.

---

# Block Access

The most restrictive option.

### Meaning

**Do not allow access.**

---

# Grant Access

Microsoft can allow access with no additional requirement or require additional controls.

Examples include:

- Require MFA
- Require a specific authentication strength
- Require a compliant device
- Require a Microsoft Entra hybrid joined device
- Require an approved client application
- Require an app protection policy
- Require a password change
- Require acceptance of terms of use

---

# Conditional Access Example

IF:

A user attempts to access a sensitive application

AND:

The device is not compliant

THEN:

Require a compliant device

OR:

Block access

---

# Session Controls

Conditional Access can also control:

**What users are allowed to do during a session**

Examples:

- Block downloads
- Prevent copying
- Prevent printing
- Require sensitivity labels
- Limit session duration
- Control sign-in frequency

### ELI5

Normal access control asks:

> Can you get in?

Session control can also ask:

> What can you do once you're inside?

---

# 4. Authentication Strengths

Conditional Access can require particular levels of authentication security.

Microsoft currently provides three built-in authentication strength categories.

---

# Multifactor Authentication Strength

Allows authentication combinations that meet standard MFA requirements.

Examples:

- Password + SMS
- Password + voice call
- Password + Authenticator
- Password + OATH token

### Meaning

**Any acceptable MFA combination**

---

# Passwordless MFA Strength

Requires MFA-capable methods that do not depend on a traditional password.

Examples:

- Microsoft Authenticator phone sign-in
- FIDO2 security keys
- Windows Hello for Business
- Platform credentials

### Meaning

**MFA without a password**

---

# Phishing-Resistant MFA Strength

Requires authentication methods designed to resist phishing.

Examples:

- Windows Hello for Business
- FIDO2 security keys / passkeys
- Certificate-Based Authentication

### Meaning

**Strongest built-in authentication-strength category**

---

# Authentication Strength Memory Sheet

| Strength | Think |
|---|---|
| MFA Strength | Standard MFA |
| Passwordless MFA | MFA without passwords |
| Phishing-Resistant MFA | Strong authentication resistant to phishing |

---

# Conditional Access and AI

The current Microsoft Learn module includes protecting generative AI services such as:

- Microsoft 365 Copilot
- Microsoft Security Copilot

Policies can require controls such as:

- Phishing-resistant MFA
- Compliant devices
- Blocking access based on elevated insider risk

### Key Concept

AI services can be protected using the same:

**Zero Trust Conditional Access principles**

used for other applications.

---

# Conditional Access Licensing

Conditional Access requires:

**Microsoft Entra ID P1**

or

**Microsoft Entra ID P2**

Organizations using the free tier can instead use:

**Security Defaults**

for baseline protection.

### Memory Trick

**Free = Security Defaults**

**P1/P2 = Conditional Access**

---

# 5. Global Secure Access

## Big Idea

Global Secure Access is Microsoft's:

**Security Service Edge — SSE**

solution.

It applies Zero Trust concepts to network access.

---

# Zero Trust Principles

Global Secure Access follows:

**Verify explicitly**

**Use least privilege**

**Assume breach**

---

# Why Global Secure Access Exists

Traditional security often relied heavily on:

**VPNs**

A VPN can create broad network access.

If an attacker compromises a VPN session, they may gain opportunities for:

**Lateral movement**

Global Secure Access moves toward:

**Identity-aware, per-resource access**

rather than broad network access.

---

# Security Service Edge — SSE

SSE brings network security services closer to users and cloud resources.

Global Secure Access combines capabilities including:

- Microsoft Entra Internet Access
- Microsoft Entra Internet Access for Microsoft Services
- Microsoft Entra Private Access
- Microsoft Defender for Cloud Apps integration

### ELI5

Instead of saying:

> You're connected to our network, so you can move around.

SSE says:

> Tell me who you are, what device you're using, where you're going, and whether you're allowed to access that specific resource.

---

# Global Secure Access Client

The Global Secure Access client runs on end-user devices.

It helps route selected network traffic through Microsoft's security service.

This allows Microsoft to evaluate signals including:

- Identity
- Device
- Location
- Application
- Risk

and integrate them with:

**Conditional Access**

---

# 6. Microsoft Entra Internet Access

Microsoft Entra Internet Access secures:

- Internet traffic
- SaaS applications
- Web access

It functions as an identity-aware:

**Secure Web Gateway — SWG**

---

# Secure Web Gateway — SWG

A Secure Web Gateway protects users when accessing internet resources.

### ELI5

**SWG = Security checkpoint between the user and the internet**

---

# Internet Access Capabilities

Current Microsoft Learn includes capabilities such as:

## Web Content Filtering

Control websites based on:

- Categories
- Domains

Example:

Block gambling websites.

---

## Universal Conditional Access

Conditional Access can be applied to internet destinations even if those applications are not directly federated with Microsoft Entra ID.

### Key Idea

**Conditional Access beyond Entra-integrated apps**

---

## TLS Inspection

Encrypted network traffic can be:

- Decrypted
- Inspected
- Evaluated for threats

Then securely handled according to policy.

---

## Threat Intelligence

Known malicious:

- Domains
- IP addresses

can be blocked using Microsoft threat intelligence.

---

## Prompt Injection Protection

Internet Access can detect and block malicious prompts targeting AI systems.

### Prompt Injection

An attacker attempts to manipulate an AI system using malicious instructions.

---

## Continuous Access Evaluation — CAE

Microsoft Entra and applications continuously evaluate whether access should remain valid.

If something changes, such as:

- User location
- Security risk
- Account status

access can be adjusted or revoked quickly.

### Memory Trick

**CAE = Don't only check at login — keep checking**

---

# 7. Microsoft Entra Internet Access for Microsoft Services

This component focuses specifically on Microsoft services.

Examples include:

- Exchange Online
- SharePoint Online
- Microsoft Teams
- Microsoft 365 workloads

---

# Compliant Network Check

Conditional Access can require users to connect through:

**Global Secure Access**

before accessing protected applications.

---

# Universal Tenant Restrictions

Helps prevent users from moving organizational data into:

- Unauthorized tenants
- Personal accounts
- Unapproved environments

### ELI5

**Keep company data inside approved Microsoft environments**

---

# Source IP Restoration

Traffic passing through a security proxy can normally make everyone appear to come from the proxy's IP.

Source IP restoration preserves the user's original IP information.

This helps maintain accurate:

- Sign-in logs
- Location-based Conditional Access
- Risk detections

---

# Enriched Microsoft 365 Logs

Provides more detailed network traffic information for Microsoft 365 traffic.

---

# Licensing

Microsoft Entra Internet Access for Microsoft Services is included with:

**Microsoft Entra ID P1**

or

**Microsoft Entra ID P2**

---

# 8. Microsoft Entra Private Access

Microsoft Entra Private Access provides secure access to:

**Private corporate resources**

Examples:

- Internal applications
- On-premises resources
- Private cloud resources
- Multicloud resources

---

# Private Access vs. Traditional VPN

Traditional VPN:

**Connect user to a network**

Private Access:

**Connect user to the specific application or resource they are authorized to use**

This is:

**Zero Trust Network Access — ZTNA**

### Memory Trick

**VPN = Network access**

**Private Access = Per-app access**

---

# Zero Trust Network Access — ZTNA

ZTNA grants access based on:

- Identity
- Device state
- Policy
- Specific resource

instead of trusting a user because they are connected to the corporate network.

---

# Quick Access

Administrators define private resources using things such as:

- FQDN
- IP address
- IP range
- Ports

Multiple resources can be grouped together.

### ELI5

**Quick Access = Group several private resources into one access definition**

---

# Per-App Access

Each private application can receive its own:

- Resource definitions
- User assignments
- Conditional Access policies

### ELI5

**Per-App = Fine-grained control for each application**

---

# App Discovery

Global Secure Access can discover private applications being accessed by users.

This helps administrators identify:

- Unknown resources
- Resources needing protection
- Applications that should be moved under Private Access policies

---

# 9. Global Secure Access Dashboard

The Microsoft Entra admin center contains a:

**Global Secure Access dashboard**

Administrators can monitor information such as:

- Network traffic
- Users
- Devices
- Cross-tenant access
- Web filtering
- Device status

---

# Global Secure Access and AI

Current Microsoft Learn also includes network protection for AI workloads.

Examples:

## Prompt Injection Protection

Detect malicious instructions aimed at manipulating AI models.

## Shadow AI Discovery

Identify unauthorized or unmanaged AI applications.

### Memory Trick

**Shadow AI = AI tools employees use without organizational approval**

## Network Controls for AI Agents

AI agent traffic can be subject to the same:

- Identity controls
- Access policies
- Network policies

as human users.

---

# Global Secure Access Quick Map

| Scenario | Think |
|---|---|
| Secure internet/SaaS traffic | Entra Internet Access |
| Secure Microsoft 365 traffic | Internet Access for Microsoft Services |
| Secure private/internal applications | Entra Private Access |
| Replace broad VPN access | Private Access / ZTNA |
| Internet content filtering | Internet Access |
| AI prompt injection filtering | Internet Access |
| Unauthorized AI apps | Shadow AI discovery |
| Continuous access reevaluation | CAE |

---

# 10. Microsoft Entra Roles and RBAC

## RBAC

RBAC stands for:

**Role-Based Access Control**

Instead of assigning every permission individually, permissions are grouped into:

**Roles**

Those roles are then assigned to:

- Users
- Groups
- Other identities

### ELI5

Instead of saying:

> Zachary can do action A, B, C, D, and E.

You say:

> Zachary is a User Administrator.

The role already contains the required permissions.

---

# Microsoft Entra RBAC

Microsoft Entra RBAC controls access to:

**Microsoft Entra resources**

Examples:

- Users
- Groups
- Applications

---

# Built-In Roles

Microsoft provides roles with predefined sets of permissions.

Examples include:

## Global Administrator

Has access to essentially all administrative capabilities in Microsoft Entra.

The person who initially creates the tenant automatically becomes a:

**Global Administrator**

---

## User Administrator

Can manage:

- Users
- Groups

and related administrative functions.

---

## Billing Administrator

Can manage:

- Purchases
- Subscriptions
- Billing-related activities

---

# Built-In Role Important Concept

Built-in roles contain:

**Fixed permission sets**

You cannot change the permissions inside a built-in role.

---

# Custom Roles

A custom role lets the organization choose:

**Exactly which permitted actions should belong to the role**

This supports:

**Least privilege**

---

# Creating a Custom Role

Two basic steps:

## Step 1

Create the:

**Role definition**

This defines the permissions.

## Step 2

Create a:

**Role assignment**

This gives the role to a user or group.

### Memory Trick

**Definition = What can the role do?**

**Assignment = Who gets the role?**

---

# Role Assignment

A role assignment combines:

**Security principal + Role + Scope**

The assignment determines:

- Who receives permissions
- Which permissions they receive
- Where those permissions apply

---

# Scope

Scope defines:

**Where the permissions apply**

A role may apply:

- Across the organization
- To a specific object
- To a specific application

### Example

User A:

User Administrator across the entire organization

User B:

Custom role only for the Contoso Expense application

---

# Custom Role Licensing

Custom Microsoft Entra roles require:

**Microsoft Entra ID P1**

or

**Microsoft Entra ID P2**

---

# 11. Least Privilege and Roles

Microsoft recommends assigning:

**The least privilege necessary**

Example:

If someone only manages users:

Assign:

**User Administrator**

Do NOT assign:

**Global Administrator**

unless they genuinely require global administrative capabilities.

### Why?

A compromised Global Administrator account creates much greater risk.

---

# Least Privilege and AI

Current Microsoft Learn emphasizes least privilege for AI as well.

If an AI tool operates using an overprivileged identity, it may potentially access much more organizational data than necessary.

### Core Idea

**Human or AI — grant only the access required**

---

# 12. Categories of Microsoft Entra Roles

Microsoft Entra roles fall into broad categories.

---

# Microsoft Entra-Specific Roles

Manage resources inside Microsoft Entra.

Examples:

- User Administrator
- Application Administrator
- Groups Administrator

---

# Service-Specific Roles

Manage a specific Microsoft 365 service.

Examples:

- Exchange Administrator
- Intune Administrator
- SharePoint Administrator
- Teams Administrator

---

# Cross-Service Roles

Permissions span multiple Microsoft services.

Examples:

- Security Administrator
- Compliance Administrator

---

# 13. Microsoft Entra RBAC vs. Azure RBAC

This distinction is VERY important for SC-900.

Both use:

**Role-Based Access Control**

But they control different things.

---

# Microsoft Entra RBAC

Controls access to:

**Microsoft Entra resources**

Examples:

- Users
- Groups
- Applications

### Think

**Identity resources**

---

# Azure RBAC

Controls access to:

**Azure resources**

Examples:

- Virtual machines
- Storage accounts
- Azure infrastructure

### Think

**Cloud infrastructure/resources**

---

# Entra RBAC vs. Azure RBAC

| Microsoft Entra RBAC | Azure RBAC |
|---|---|
| Identity administration | Azure resource administration |
| Users | Virtual machines |
| Groups | Storage |
| Applications | Azure resources |
| Entra roles | Azure roles |

### Memory Trick

**Entra RBAC = WHO**

**Azure RBAC = WHAT YOU BUILT IN AZURE**

---

# SC-900 Exam Quick Reference

| If the Question Mentions... | Think... |
|---|---|
| IF condition → THEN control | Conditional Access |
| Zero Trust policy engine | Conditional Access |
| Evaluated after first-factor authentication | Conditional Access |
| User / resource / network / condition | Conditional Access assignment |
| MFA / compliant device / block | Access control |
| Standard acceptable MFA methods | MFA authentication strength |
| MFA without passwords | Passwordless MFA strength |
| FIDO2 / Hello / CBA only | Phishing-resistant MFA |
| P1/P2 | Conditional Access |
| Microsoft's SSE solution | Global Secure Access |
| Secure Web Gateway | Entra Internet Access |
| Internet/SaaS protection | Entra Internet Access |
| Private corporate application | Entra Private Access |
| Replace broad VPN access | ZTNA / Private Access |
| Microsoft 365 traffic security | Internet Access for Microsoft Services |
| Reevaluate access continuously | CAE |
| Unauthorized AI apps | Shadow AI |
| Manage Entra users/groups/apps | Microsoft Entra RBAC |
| Manage Azure VMs/storage | Azure RBAC |
| Fixed Microsoft permissions | Built-in role |
| Choose specific permissions | Custom role |
| What permissions a role contains | Role definition |
| Who receives the role | Role assignment |
| Where permissions apply | Scope |
| Minimum permissions necessary | Least privilege |

---

# Final Module 3 Cram Sheet

## Conditional Access

**Microsoft's Zero Trust policy engine**

**IF → THEN**

Assignments:

**WHO / WHAT / WHERE / WHEN**

Access Controls:

**BLOCK / GRANT / REQUIRE**

---

## Order

**Authentication first**

**Conditional Access second**

---

## Authentication Strength

**MFA = Standard MFA**

**Passwordless MFA = No password**

**Phishing-resistant MFA = FIDO2 / Hello / CBA**

---

## Licensing

**Free = Security Defaults**

**P1/P2 = Conditional Access**

---

# Global Secure Access

**Microsoft's SSE solution**

Built on:

**Verify explicitly**

**Least privilege**

**Assume breach**

---

## Internet Access

**Internet + SaaS**

Think:

**Secure Web Gateway**

---

## Internet Access for Microsoft Services

**Microsoft 365 traffic**

Think:

**Exchange + SharePoint + Teams**

---

## Private Access

**Private/internal resources**

Think:

**ZTNA**

**Per-app instead of VPN-wide access**

---

## CAE

**Continuously reevaluate access**

---

## AI Network Security

**Prompt Injection Protection**

**Shadow AI Discovery**

**Agent Network Controls**

---

# RBAC

**Role-Based Access Control**

---

## Built-In Role

**Microsoft defines permissions**

## Custom Role

**Organization chooses permissions**

---

## Role Definition

**WHAT permissions**

## Role Assignment

**WHO gets them**

## Scope

**WHERE they apply**

---

# Critical Difference

## Microsoft Entra RBAC

Controls:

**Users**

**Groups**

**Applications**

## Azure RBAC

Controls:

**Virtual Machines**

**Storage**

**Azure Resources**

---

# Least Privilege

**Give only the permissions needed to perform the job**

Do not use:

**Global Administrator**

when:

**User Administrator**

is sufficient.

---

# Final Takeaway

Access management answers three basic questions:

**Should this identity be allowed in?**

Conditional Access answers that using identity, device, location, risk, and other signals.

**How should this identity securely reach the resource?**

Global Secure Access applies Zero Trust controls to internet, Microsoft, and private network traffic.

**What is this identity allowed to administer?**

Microsoft Entra RBAC assigns permissions through roles and scopes.

For SC-900, the highest-value distinctions in this module are:

**Conditional Access = IF / THEN**

**Assignments = WHEN the policy applies**

**Access Controls = WHAT happens**

**Internet Access = Internet/SaaS**

**Private Access = Internal/private apps**

**Entra RBAC = Identity resources**

**Azure RBAC = Azure resources**

**Least privilege = Never grant more access than necessary**
