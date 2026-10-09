# Describe the Function and Identity Types of Microsoft Entra ID

> **Source:** Microsoft Learn — SC-900  
> **Module:** Describe the function and identity types of Microsoft Entra ID  
> **Verified against current Microsoft Learn content:** October 8, 2026

---

# Module Overview

Microsoft Entra ID is Microsoft's cloud-based identity and access management service.

This module covers:

| Topic | Core Idea |
|---|---|
| Microsoft Entra | Microsoft's family of identity and network access products |
| Microsoft Entra ID | Core cloud identity and access management service |
| Tenant and Directory | Organizational identity boundary and identity database |
| User Identities | Identities representing people |
| Workload Identities | Identities representing applications and services |
| Device Identities | Identities representing computers and other devices |
| Agent Identities | Identities specifically designed for AI agents |
| Groups | Manage access for collections of identities |
| Hybrid Identity | One identity across on-premises and cloud environments |
| External ID | Secure access for guests, partners, customers, and consumers |

---

# 1. Microsoft Entra — The Big Picture

## Microsoft Entra Is a Product Family

Do NOT confuse:

**Microsoft Entra**

with:

**Microsoft Entra ID**

Microsoft Entra is the **entire family** of Microsoft identity and network access products.

Microsoft Entra ID is the **foundational identity product inside that family**.

### Memory Trick

**Entra = Family**

**Entra ID = Main identity service**

---

# Microsoft Entra Product Family

Microsoft organizes the Entra family around different access scenarios.

| Access Need | Microsoft Entra Product |
|---|---|
| Core identity and authentication | Microsoft Entra ID |
| Traditional AD features in the cloud | Microsoft Entra Domain Services |
| Private/internal resource access | Microsoft Entra Private Access |
| Internet and SaaS access | Microsoft Entra Internet Access |
| Identity lifecycle and permissions | Microsoft Entra ID Governance |
| Risky users and risky sign-ins | Microsoft Entra ID Protection |
| Verifiable digital credentials | Microsoft Entra Verified ID |
| Customers, partners, and guests | Microsoft Entra External ID |
| Applications and services | Microsoft Entra Workload ID |
| AI agents | Microsoft Entra Agent ID |

---

# Microsoft Entra ID

Microsoft Entra ID is the foundational product in the Microsoft Entra family.

It provides capabilities such as:

- Authentication
- Authorization
- Single Sign-On — SSO
- Access policies
- User management
- Device identity
- Application identity
- Identity protection

### ELI5

**Entra ID = Microsoft's cloud system for figuring out who or what is requesting access and what it should be allowed to access.**

---

# Microsoft Entra Domain Services

Microsoft Entra Domain Services provides traditional Windows Active Directory capabilities for applications that still need them.

It supports older technologies without requiring an organization to deploy and maintain its own domain controllers.

### Exam Cue

If the question mentions:

- Legacy application
- Traditional Active Directory features
- Domain services
- Managed domain
- No domain controllers to manage

Think:

**Microsoft Entra Domain Services**

---

# Microsoft Entra Private Access

Provides secure access to:

- Internal applications
- Private corporate resources
- On-premises resources
- Multicloud private resources

Users can access these resources without relying on a traditional VPN.

### Memory Trick

**Private Access = PRIVATE resources**

---

# Microsoft Entra Internet Access

Secures access to:

- Internet websites
- SaaS applications
- Microsoft 365 resources

It can also provide web content filtering.

### Memory Trick

**Internet Access = INTERNET and SaaS**

---

# Microsoft Entra ID Governance

Helps manage:

- Who gets access
- What access they receive
- When access should begin
- When access should end
- Whether access is still appropriate

Examples include:

- Access requests
- Access assignments
- Access reviews
- Employee onboarding
- Employee offboarding

### Memory Trick

**Governance = Who SHOULD have access?**

---

# Microsoft Entra ID Protection

Detects identity-related risk.

Examples:

- Risky users
- Risky sign-ins
- Suspicious authentication activity

Administrators can respond automatically using tools such as risk-based Conditional Access.

### Memory Trick

**ID Protection = Is this identity RISKY?**

---

# Microsoft Entra Verified ID

Provides verifiable digital credentials.

Example:

A university issues a digital diploma.

An employer can verify:

- Who issued it
- Whether it is valid
- Whether it has been revoked
- When it was issued

### Memory Trick

**Verified ID = Prove something about yourself**

---

# Microsoft Entra External ID

Provides identity services for people outside the organization.

Examples:

- Guests
- Partners
- Vendors
- Customers
- Consumers

Users may authenticate with:

- Another Microsoft Entra organization
- Google
- Facebook
- Other identity providers

### Memory Trick

**External ID = OUTSIDERS**

---

# Microsoft Entra Workload ID

Provides identities for software workloads.

Examples:

- Applications
- Services
- Containers
- Automation
- GitHub Actions

### Memory Trick

**Workload ID = SOFTWARE identity**

---

# Microsoft Entra Agent ID

Provides identities specifically for:

**AI agents**

Agent ID allows organizations to:

- Authenticate agents
- Authorize agents
- Govern agents
- Monitor agents
- Apply least privilege
- Maintain accountability

### Memory Trick

**Agent ID = AI identity**

---

# Entra Product Quick Map

## Who are you?

**Entra ID**

## Are you risky?

**ID Protection**

## Should you still have access?

**ID Governance**

## Are you outside the company?

**External ID**

## Are you software?

**Workload ID**

## Are you AI?

**Agent ID**

## Do you need an internal/private resource?

**Private Access**

## Do you need internet/SaaS access?

**Internet Access**

## Do you need old-school AD features?

**Domain Services**

## Do you need to prove a credential?

**Verified ID**

---

# How Entra Products Work Together

Example: A new employee joins an organization.

## Entra ID

Authenticates the employee and provides SSO.

## ID Governance

Provisions the employee's access based on their role.

## ID Protection

Evaluates sign-ins for identity risk.

## Internet Access

Protects access to internet and cloud resources.

## Private Access

Provides secure access to internal resources.

---

# Microsoft Entra Licensing

For SC-900, focus on the progression:

**Free → P1 → P2**

---

## Entra ID Free

Provides basic identity capabilities.

Examples:

- Users
- Groups
- Basic reporting
- Core identity management

---

## Entra ID P1

Adds capabilities such as:

- Conditional Access
- Hybrid identity
- Advanced group capabilities

### Memory Trick

**P1 = Conditional Access**

---

## Entra ID P2

Adds advanced risk and privileged identity capabilities.

Examples:

- Risk-based Conditional Access
- Entra ID Protection
- Privileged Identity Management — PIM

### Memory Trick

**P2 = Risk + PIM**

---

## Microsoft Entra Suite

Bundles several advanced Microsoft Entra products.

Includes capabilities from products such as:

- Private Access
- Internet Access
- ID Governance
- ID Protection
- Verified ID premium capabilities

Microsoft Entra ID P1 is required.

---

# Microsoft Entra Admin Center

Administrators manage Microsoft Entra products through the:

**Microsoft Entra admin center**

### Exam Cue

If asked where administrators configure Microsoft Entra:

**Microsoft Entra admin center**

---

# 2. Microsoft Entra ID

Microsoft Entra ID connects identities to resources.

It can provide access to:

## Internal Resources

Examples:

- Corporate applications
- Intranet resources
- Organization-developed cloud apps

## External Resources

Examples:

- Microsoft 365
- Azure portal
- SaaS applications

---

# Entra ID Can Work Three Ways

Microsoft Entra ID can be:

## Standalone

Cloud-only identity system.

## Synchronized with Active Directory

On-premises identities synchronize to the cloud.

## Synchronized with Other Directory Services

Other identity systems can also integrate with Entra ID.

---

# Identity Secure Score

Microsoft Entra ID includes:

**Identity Secure Score**

This is a percentage indicating how closely the organization's identity configuration aligns with Microsoft's security recommendations.

It helps organizations:

- Measure identity security posture
- Identify improvements
- Prioritize security actions
- Track improvement over time

### Memory Trick

**Identity Secure Score = Identity security report card**

---

# 3. Important Microsoft Entra Terminology

# Tenant

A Microsoft Entra tenant is:

**An instance of Microsoft Entra ID belonging to an organization**

A tenant contains objects such as:

- Users
- Groups
- Devices
- Applications
- Policies

Each tenant has:

- Unique tenant ID
- Domain name

Example:

`contoso.onmicrosoft.com`

### ELI5

A tenant is your organization's own Microsoft Entra environment.

---

# Tenant as a Boundary

A tenant acts as:

- Security boundary
- Administrative boundary

The organization controls access to its resources inside that tenant.

---

# Directory

A Microsoft Entra directory contains the identity-related objects inside the tenant.

Examples:

- Users
- Groups
- Applications
- Devices

### ELI5

**Tenant = Your organization's Entra environment**

**Directory = The identity database inside it**

---

# Tenant vs. Directory

The terms are often used interchangeably.

For SC-900:

A Microsoft Entra tenant contains:

**one directory**

---

# Multitenant Organization

A multitenant organization has:

**More than one Microsoft Entra tenant**

Reasons might include:

- Separate business units
- Subsidiaries
- Mergers
- Acquisitions
- Geographic requirements
- Data residency requirements

---

# Who Uses Microsoft Entra ID?

## IT Administrators

Use Entra ID to:

- Control access
- Require MFA
- Protect identities
- Implement governance

## Developers

Use Entra ID to:

- Add SSO to applications
- Authenticate users
- Use identity APIs

## Microsoft Cloud Customers

Organizations using:

- Azure
- Microsoft 365
- Dynamics 365

already have Microsoft Entra ID.

---

# 4. Types of Identities

Microsoft Entra ID supports several identity types.

At the highest level, identities can belong to:

1. People
2. Devices
3. Software

AI agents are also represented using specialized agent identities.

---

# User Identities

User identities represent:

**People**

Examples:

- Employees
- Consultants
- Vendors
- Partners
- Customers

---

# Internal vs. External Authentication

## Internal Authentication

The user has an account in the organization's Microsoft Entra tenant.

## External Authentication

The user authenticates using:

- Another Microsoft Entra tenant
- Social identity
- External identity provider

---

# UserType Property

A Microsoft Entra user object can have a UserType of:

**Member**

or

**Guest**

Do NOT assume authentication method and UserType are the same thing.

They describe different characteristics.

---

# Internal Member

Typical employee.

Authentication:

**Internal**

UserType:

**Member**

---

# External Guest

Typical:

- Consultant
- Vendor
- Partner

Authentication:

**External**

UserType:

**Guest**

---

# External Member

Common in organizations with multiple Microsoft Entra tenants.

The user authenticates through another tenant but receives:

**Member-level access**

Authentication:

**External**

UserType:

**Member**

---

# Internal Guest

User has an internal Entra account but is marked:

**Guest**

This is considered more of a legacy scenario.

Modern organizations typically use B2B collaboration instead.

---

# User Identity Quick Table

| Authentication | UserType | Example |
|---|---|---|
| Internal | Member | Employee |
| External | Guest | Partner/vendor |
| External | Member | Member from another organizational tenant |
| Internal | Guest | Legacy guest configuration |

---

# 5. Workload Identities

A workload identity represents:

**Software**

rather than a human.

Examples:

- Applications
- Services
- Virtual machines
- Containers
- Automation processes

A workload identity allows software to:

**Authenticate and access resources**

---

# Microsoft Entra Workload Identity Types

Microsoft Learn identifies:

- Applications
- Service principals
- Managed identities

---

# Application Registration

For an application to use Microsoft Entra ID for authentication and authorization:

**The application must be registered with Entra ID.**

Registration establishes the application in Microsoft's identity platform.

---

# Service Principal

A:

**Service principal**

is essentially the identity of an application within a tenant.

### ELI5

Application registration says:

> This application exists.

Service principal says:

> This is the application's identity in this tenant.

---

# Why Service Principals Matter

Service principals enable applications to:

- Authenticate
- Receive permissions
- Access protected resources

---

# Managed Identity

Managed identities eliminate the need for developers to manually manage application credentials.

Microsoft Entra manages those credentials automatically.

### ELI5

Instead of putting a username/password or secret inside an application:

**Azure manages the application's identity for you.**

---

# Managed Identity Types

There are two:

1. System-assigned
2. User-assigned

---

# System-Assigned Managed Identity

The identity belongs directly to one Azure resource.

Example:

A virtual machine.

Lifecycle:

**Resource created → Identity exists**

**Resource deleted → Identity deleted**

### Memory Trick

**System-assigned dies with the resource**

---

# User-Assigned Managed Identity

The identity exists as a separate Azure resource.

It can be assigned to:

**Multiple resources**

If one of those resources is deleted:

**The identity remains**

It must be explicitly deleted separately.

### Memory Trick

**User-assigned survives independently**

---

# Managed Identity Comparison

| System-Assigned | User-Assigned |
|---|---|
| Attached to one resource | Separate resource |
| Shares resource lifecycle | Independent lifecycle |
| Deleted with resource | Remains until explicitly deleted |
| Usually used by one resource | Can be used by multiple resources |

---

# 6. Agent Identities

Agent identities are specialized identities designed specifically for:

**AI agents**

They are distinct from traditional workload identities.

---

# Why AI Agents Need Their Own Identities

AI agents behave differently from traditional software.

They may:

- Make decisions dynamically
- Adapt to context
- Operate autonomously
- Interact with other systems
- Access business data
- Take actions on behalf of users

This introduces special risks.

---

# AI Agent Security Risks

## Expanded Attack Surface

Agents interact with many systems.

They may also be vulnerable to AI-specific attacks such as:

**Prompt injection**

---

## Excessive Permissions

An AI agent could be granted more access than it actually needs.

This violates:

**Least privilege**

---

## Agent Sprawl

Organizations may create large numbers of AI agents without properly tracking them.

Problems include:

- Forgotten agents
- Excessive permissions
- Poor lifecycle management
- Lack of accountability

---

# Agent Identity Blueprints

Microsoft Entra Agent ID uses:

**Agent identity blueprints**

A blueprint is a reusable template for a type of AI agent.

It can define:

- Agent classification
- Credentials
- Common policies

### ELI5

Blueprint = Template for a class of agents

Example:

**Sales Assistant Agent Blueprint**

---

# Agent Identities

An agent identity is:

**An individual agent instance created from a blueprint**

Each agent identity has:

- Unique identifier
- Display name
- Sponsor

---

# Sponsor

The sponsor is:

**The human user or group accountable for the AI agent**

### Important Concept

AI agents should still have human accountability.

---

# Blueprint vs. Agent Identity

| Blueprint | Agent Identity |
|---|---|
| Template | Individual instance |
| Defines agent type | Represents one actual agent |
| Holds authentication credentials | Uses blueprint to obtain tokens |
| Policies can apply to all instances | Has unique identity |

---

# Agent Authentication Patterns

There are two major scenarios:

## Attended — On Behalf Of

The AI agent acts:

**On behalf of a human user**

It uses permissions delegated by that user.

### Memory Trick

**Attended = Human is involved**

---

## Unattended

The agent acts:

**Autonomously**

It uses its own assigned roles and permissions.

### Memory Trick

**Unattended = Agent works alone**

---

# Agent ID Security Controls

Microsoft Entra Agent ID integrates with:

## Conditional Access

Applies access policies to agents.

## Identity Protection

Detects risky agent activity.

## Identity Governance

Manages agent lifecycle and access.

## Agent Registry

Provides centralized visibility and metadata for registered agents.

---

# Least Privilege for AI Agents

Microsoft limits the ability of AI agents to receive certain powerful roles and permissions.

The goal is to prevent:

- Privilege escalation
- Excessive access
- Unexpected administrative activity

---

# 7. Device Identities

A device identity represents physical hardware.

Examples:

- Laptop
- Desktop
- Mobile phone
- Server
- Printer
- IoT device

Device identities provide information that can be used in access decisions.

---

# Three Device States

Microsoft Entra supports:

1. Microsoft Entra registered
2. Microsoft Entra joined
3. Microsoft Entra hybrid joined

These distinctions are important.

---

# Microsoft Entra Registered

Designed primarily for:

**BYOD / personal devices**

The device belongs to the user but is registered with the organization.

### Memory Trick

**Registered = Personal device**

---

# Microsoft Entra Joined

Device is joined directly to:

**Microsoft Entra ID**

Typically:

**Organization-owned**

The user signs in using their organizational account.

### Memory Trick

**Joined = Company-owned cloud device**

---

# Microsoft Entra Hybrid Joined

Device is joined to:

**On-premises Active Directory**

AND

**Microsoft Entra ID**

### Memory Trick

**Hybrid joined = AD + Entra**

---

# Device Identity Comparison

| Device State | Typical Use |
|---|---|
| Entra Registered | Personal/BYOD |
| Entra Joined | Organization-owned cloud device |
| Entra Hybrid Joined | On-prem AD + Entra environment |

---

# Device Benefits

Registered or joined devices can support:

**Single Sign-On — SSO**

to:

- Cloud resources
- On-premises resources

Organizations can use tools such as:

**Microsoft Intune**

to manage devices.

---

# 8. Groups

Groups simplify access management.

Instead of assigning permissions separately to 100 users:

**Assign permission once to a group.**

Then add the appropriate identities to that group.

---

# Microsoft Entra Group Types

Two major types are:

1. Security groups
2. Microsoft 365 groups

---

# Security Group

Used primarily to:

**Manage access**

Members may include:

- Users
- External users
- Devices
- Other groups
- Service principals
- Agent identities

### Exam Cue

If the purpose is:

**Permissions / security policy / resource access**

Think:

**Security Group**

---

# Microsoft 365 Group

Used primarily for:

**Collaboration**

Can provide access to:

- Shared mailbox
- Calendar
- Files
- SharePoint sites

Membership consists of:

**Users**

including external users.

### Exam Cue

If the purpose is:

**Team collaboration**

Think:

**Microsoft 365 Group**

---

# Group Membership

Membership can be:

## Assigned

Administrator manually chooses members.

## Dynamic

Microsoft Entra automatically adds or removes identities according to rules.

### ELI5

**Assigned = Human picks members**

**Dynamic = Rules pick members**

---

# 9. Hybrid Identity

Many organizations have both:

**On-premises resources**

and

**Cloud resources**

Users still expect one identity that works everywhere.

That is:

**Hybrid Identity**

---

# Hybrid Identity Definition

Hybrid identity provides a common identity for authentication and authorization across:

- On-premises resources
- Cloud resources

### Memory Trick

**Hybrid Identity = One identity, two worlds**

---

# Hybrid Identity Uses Two Important Processes

## Provisioning

Creates an identity in another directory.

Example:

User exists in Active Directory.

That identity is provisioned into Microsoft Entra ID.

---

## Synchronization

Keeps identity information matching between:

- On-premises directory
- Cloud directory

### Memory Trick

**Provision = Create**

**Synchronize = Keep matching**

---

# Microsoft Entra Cloud Sync

Microsoft currently recommends:

**Microsoft Entra Cloud Sync**

for hybrid identity synchronization.

It uses a lightweight:

**Cloud provisioning agent**

deployed in the on-premises or IaaS-hosted environment.

Configuration is stored and managed in Microsoft Entra ID.

---

# Benefits of Cloud Sync

Includes:

- Simpler deployment
- Multiple agents for high availability
- Support for disconnected multi-forest environments
- Cloud-based configuration

---

# Microsoft Entra Connect Sync

Microsoft Entra Connect Sync is the:

**Earlier synchronization technology**

Microsoft is moving development toward:

**Cloud Sync**

### Exam Concept

For new deployments:

**Cloud Sync = recommended**

**Connect Sync = earlier technology**

---

# SCIM

Cloud Sync uses the:

**System for Cross-domain Identity Management — SCIM**

standard.

SCIM helps automate:

- Provisioning users
- Deprovisioning users
- Provisioning groups
- Deprovisioning groups

between identity systems.

### Memory Trick

**SCIM = Standard for automatically exchanging identity information**

---

# 10. External Identities

Organizations often need to give access to people outside the company.

Examples:

- Vendors
- Partners
- Guests
- Customers
- Consumers

Microsoft Entra External ID handles these scenarios.

---

# Bring Your Own Identity

External users can often authenticate using identities they already have.

Examples:

- Their employer's Microsoft Entra identity
- Google
- Facebook
- Other external identity providers

This means the host organization does not necessarily need to create and manage another password for them.

---

# External ID Has Two Major Scenarios

## 1. Collaborate with Business Guests

Use:

**B2B Collaboration**

## 2. Secure Apps for Customers and Consumers

Use:

**Customer Identity and Access Management — CIAM**

---

# Tenant Types for External ID

There are two major tenant configurations:

| Tenant Type | Purpose |
|---|---|
| Workforce Tenant | Employees and organizational resources |
| External Tenant | Customer/consumer-facing applications |

---

# Workforce Tenant

Used for:

- Employees
- Internal business applications
- Organizational resources

External:

- Partners
- Vendors
- Guests

can be invited into a workforce tenant.

---

# External Tenant

Used specifically for:

**Customer and consumer identity scenarios**

It supports applications published to:

- Consumers
- Business customers

---

# B2B Collaboration

Business-to-Business collaboration allows:

**External partners and guests to access organizational resources using their own identities**

Examples:

- Microsoft 365
- SaaS applications
- Line-of-business applications

---

# Important B2B Concept

The guest generally authenticates with:

**Their home identity provider**

The host organization then determines whether the guest is allowed access.

### ELI5

Your company says:

> We trust your company's login, but we decide what you can access here.

---

# B2B Collaboration Exam Cue

If the scenario says:

- Partner
- Vendor
- Guest
- Uses own credentials
- Needs access to company resources

Think:

**External ID B2B Collaboration**

---

# CIAM

CIAM stands for:

**Customer Identity and Access Management**

Used when organizations build applications for:

- Consumers
- Customers
- Business customers

Features include:

- Self-service registration
- Sign-in
- SSO
- Social identities
- Customer account management

### Exam Cue

Customer-facing application:

**External ID / CIAM**

---

# B2B Direct Connect

External ID also supports:

**B2B Direct Connect**

This creates a mutual trust relationship between two Microsoft Entra organizations.

A current example is:

**Microsoft Teams Connect shared channels**

---

# B2B Collaboration vs. B2B Direct Connect

## B2B Collaboration

External user is typically represented as a:

**Guest in your directory**

## B2B Direct Connect

External user:

**Is not added as a guest**

They access the shared resource directly from their home tenant.

---

# B2B Quick Comparison

| B2B Collaboration | B2B Direct Connect |
|---|---|
| Guest access | Direct organizational trust |
| User appears as guest | User stays in home tenant |
| Broad app/resource collaboration | Current major use case: Teams shared channels |

---

# Module 1 Exam Quick Reference

| If the Question Mentions... | Think... |
|---|---|
| Entire Microsoft identity family | Microsoft Entra |
| Core cloud IAM | Microsoft Entra ID |
| Legacy AD capabilities without managing DCs | Entra Domain Services |
| Internal/private apps without VPN | Entra Private Access |
| Internet/SaaS protection | Entra Internet Access |
| Access lifecycle | ID Governance |
| Risky user or risky sign-in | ID Protection |
| Digital credential | Verified ID |
| Guest/customer/partner | External ID |
| Application/service identity | Workload ID |
| AI agent identity | Agent ID |
| Portal to manage Entra | Entra Admin Center |
| Identity security percentage | Identity Secure Score |
| Organization's Entra instance | Tenant |
| Identity/object database | Directory |
| Person | User identity |
| Software | Workload identity |
| App identity inside tenant | Service principal |
| App identity with credentials managed automatically | Managed identity |
| Identity dies with Azure resource | System-assigned managed identity |
| Identity exists independently | User-assigned managed identity |
| AI agent template | Agent identity blueprint |
| Individual AI instance | Agent identity |
| Human accountable for agent | Sponsor |
| Agent works for user | Attended |
| Agent works autonomously | Unattended |
| Personal/BYOD device | Entra registered |
| Organization cloud device | Entra joined |
| AD + Entra device | Hybrid joined |
| Access permissions for many identities | Security group |
| Collaboration | Microsoft 365 group |
| Rules automatically manage membership | Dynamic group |
| One identity across cloud + on-prem | Hybrid identity |
| Create identity in another directory | Provisioning |
| Keep identity data matching | Synchronization |
| Microsoft's recommended sync tool | Entra Cloud Sync |
| Older sync technology | Entra Connect Sync |
| Standard for identity provisioning | SCIM |
| External business partner | B2B Collaboration |
| Customer-facing application | CIAM |
| Direct cross-tenant trust | B2B Direct Connect |

---

# Final Module 1 Cram Sheet

## Microsoft Entra

**Entire product family**

## Microsoft Entra ID

**Core cloud IAM**

---

# Entra Products

**ID = Identity**

**ID Protection = Risk**

**ID Governance = Access lifecycle**

**External ID = Outsiders**

**Workload ID = Software**

**Agent ID = AI**

**Private Access = Internal resources**

**Internet Access = Internet/SaaS**

**Domain Services = Legacy AD**

**Verified ID = Digital proof**

---

# Licensing

**Free = Basic**

**P1 = Conditional Access**

**P2 = Risk + ID Protection + PIM**

---

# Tenant

**Organization's Entra environment**

# Directory

**Identity database inside tenant**

---

# Identity Types

**User = Person**

**Device = Hardware**

**Workload = Software**

**Agent = AI**

---

# Managed Identities

**System-assigned = Dies with resource**

**User-assigned = Independent**

---

# Devices

**Registered = Personal/BYOD**

**Joined = Organization-owned cloud**

**Hybrid Joined = AD + Entra**

---

# Groups

**Security Group = Access**

**Microsoft 365 Group = Collaboration**

**Assigned = Manual**

**Dynamic = Rule-based**

---

# Hybrid Identity

**One identity across cloud + on-prem**

**Provision = Create**

**Synchronize = Keep matching**

**Cloud Sync = Recommended**

**Connect Sync = Earlier**

**SCIM = Provisioning standard**

---

# External ID

**B2B Collaboration = Partners/guests**

**CIAM = Customers/consumers**

**Workforce Tenant = Employees + guests**

**External Tenant = Customer apps**

**B2B Direct Connect = Direct trust without guest account**

---

# AI Agents

**Blueprint = Agent template**

**Agent Identity = Individual agent**

**Sponsor = Human accountable for agent**

**Attended = Acts for user**

**Unattended = Autonomous**

---

# Final Takeaway

Microsoft Entra is Microsoft's entire identity and network access family.

Microsoft Entra ID is the foundational cloud identity service.

For SC-900, the most important skill is recognizing:

1. **What kind of identity is being described?**
2. **Which Microsoft Entra product solves the scenario?**
3. **Is the identity human, device, software, external, or AI?**
4. **Is the environment cloud-only, on-premises, or hybrid?**
5. **Does the scenario involve employees, guests, customers, applications, or agents?**

Do not try to memorize every Microsoft Entra product as an isolated definition.

Instead, associate each product with the problem it solves.
