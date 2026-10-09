# SC-900 — Section 1, Module 2
# Describe Identity Concepts

## Module Overview

This module covers the fundamental concepts behind identity and access management.

The main topics are:

| Topic | Core Idea |
|---|---|
| Authentication | Prove who or what you are |
| Authorization | Determine what you are allowed to do |
| Identity as the Security Perimeter | Protect resources based on identity instead of location |
| Identity Providers | Central systems that authenticate users and issue tokens |
| Directory Services | Store and manage identity information |
| Active Directory Domain Services | Traditional on-premises Microsoft directory service |
| Microsoft Entra ID | Microsoft's cloud identity and access service |
| Federation | Trust identities across organizations or domains |

---

# 1. Authentication and Authorization

Authentication and authorization work together, but they are NOT the same thing.

This distinction is extremely important for SC-900.

---

## Authentication

Authentication is the process of proving:

**Who are you?**

Before a system gives you access, it needs evidence that you really are the identity you claim to be.

Examples:

- Username and password
- PIN
- Fingerprint
- Face recognition
- Security key
- Authenticator app

### Simple Meaning

**Authentication = Prove your identity**

---

## Authentication Factors

Authentication factors fall into three major categories.

| Factor | Meaning | Examples |
|---|---|---|
| Something you know | Information you know | Password, PIN |
| Something you have | An object you possess | Phone, smart card, security key |
| Something you are | A physical characteristic | Fingerprint, face |

### Memory Trick

**Know — Have — Are**

---

# Single-Factor Authentication

Single-factor authentication uses only one authentication factor.

Example:

Password only

The problem is that if the password is stolen, the attacker has everything needed to impersonate the user.

---

# Multifactor Authentication — MFA

Multifactor authentication requires two or more authentication factors from different categories.

Example:

Password  
+
Authenticator notification on a phone

This combines:

**Something you know**

with

**Something you have**

---

## Important Exam Concept

Two passwords do NOT count as MFA.

They are both:

**Something you know**

MFA requires factors from different categories.

---

# Authorization

Authorization determines:

**What are you allowed to do?**

Authorization happens AFTER authentication.

Once the system knows who you are, it determines which resources and actions you are permitted to access.

Examples:

- Read a file
- Modify a database
- Access SharePoint
- Delete records
- Manage users
- Administer Azure resources

---

## Authorization May Consider

| Information | Example |
|---|---|
| Role | Administrator vs. employee |
| Permission | Read vs. write |
| Group | Finance department |
| Attribute | Location or job function |

---

# Authentication vs. Authorization

| Authentication | Authorization |
|---|---|
| Who are you? | What can you do? |
| Happens first | Happens after authentication |
| Verifies identity | Verifies permissions |
| Password, MFA, biometrics | Roles, permissions, policies |

### Memory Trick

**Authentication = Identity**

**Authorization = Access**

---

## Simple Example

You walk into a military installation and show your CAC.

Security verifies that you are actually the person identified by the CAC.

That is:

**Authentication**

Your credentials then determine whether you are allowed into a particular secure area.

That is:

**Authorization**

---

# Least Privilege

Authorization should follow the principle of:

**Least Privilege**

Users should receive only the minimum permissions necessary to perform their job.

### Simple Meaning

**Give people what they need — and nothing more.**

Least privilege limits the damage that can occur if:

- An account is compromised
- A user makes a mistake
- Permissions are abused

---

# 2. Identity as the Primary Security Perimeter

## Traditional Security Model

Historically, organizations protected their resources using a network perimeter.

Think:

**Inside the corporate network = trusted**

**Outside the corporate network = untrusted**

Organizations used controls such as:

- Firewalls
- VPN gateways
- Corporate networks

This worked when:

- Employees worked in offices
- Applications were hosted locally
- Employees used company computers
- Data remained inside the organization

---

# Why the Traditional Perimeter Changed

Modern organizations use:

- Cloud services
- SaaS applications
- Remote work
- Hybrid work
- Personal devices
- BYOD
- Contractors
- Partners
- Customers
- IoT devices

Users may access organizational data without ever entering the corporate network.

Because of this, network location alone is no longer enough to determine trust.

---

# Identity Is the New Security Perimeter

Instead of asking:

> Is this person inside our network?

Modern security asks:

> Who or what is requesting access, and should it be trusted?

Every access request begins with an identity.

---

# What Is an Identity?

An identity is a collection of information that describes a person, device, application, or other entity.

Examples of identity information include:

- Username
- Role
- Permissions
- Authentication methods
- Device ID
- Device compliance status

---

# Types of Identities

Modern environments contain multiple kinds of identities.

| Identity Type | Represents |
|---|---|
| Human Identity | Employees, customers, contractors, partners |
| Device Identity | Computers, phones, tablets, IoT devices |
| Workload Identity | Applications, services, containers, automated processes |
| Agent Identity | AI agents acting for users or systems |

---

## Human Identity

Represents a person.

Examples:

- Employee
- Contractor
- Customer
- Partner

---

## Device Identity

Represents hardware.

Examples:

- Laptop
- Smartphone
- Tablet
- IoT device

A device may be evaluated based on things such as:

- Enrollment
- Management status
- Security configuration
- Compliance status

---

## Workload Identity

Represents software rather than a person.

Examples:

- Application
- Service
- Container
- Automated process

A workload may need permission to access:

- APIs
- Databases
- Azure resources

---

## Agent Identity

Represents an AI agent.

AI agents may:

- Act on behalf of users
- Access corporate data
- Perform automated tasks
- Interact with other systems

These agents also require:

- Authentication
- Authorization
- Governance
- Lifecycle management

---

# 3. Four Pillars of Identity Infrastructure

Microsoft organizes identity infrastructure around four pillars:

## Administration

## Authentication

## Authorization

## Auditing

### Memory Trick

**AAAA**

Administration  
Authentication  
Authorization  
Auditing

---

# Administration

Administration is responsible for managing identities throughout their lifecycle.

Examples:

- Create accounts
- Update accounts
- Assign groups
- Assign roles
- Provision users
- Deprovision users
- Remove accounts when employees leave

### Simple Meaning

**Administration = Manage the identity**

---

# Authentication

Authentication verifies that the identity is legitimate.

### Simple Meaning

**Authentication = Prove who you are**

---

# Authorization

Authorization determines what the identity is permitted to do.

### Simple Meaning

**Authorization = Decide what you can access**

---

# Auditing

Auditing tracks identity activity.

Examples:

- Sign-in logs
- Access records
- Activity logs
- Security alerts
- Investigation records

Auditing helps answer:

**Who did what, when, and from where?**

### Simple Meaning

**Auditing = Keep the receipts**

---

# Four Pillars Quick Reference

| Pillar | Question |
|---|---|
| Administration | How do we manage the identity? |
| Authentication | Who are you? |
| Authorization | What can you do? |
| Auditing | What happened? |

---

# 4. Identity Providers

## What Is an Identity Provider?

An identity provider is commonly abbreviated:

**IdP**

An identity provider is a centralized service that manages identities and authentication.

Instead of every application maintaining its own usernames and passwords, applications can trust one identity provider.

### Example

**Microsoft Entra ID** is an identity provider.

---

# Without a Central Identity Provider

Imagine an employee uses:

- Outlook
- Teams
- Salesforce
- ServiceNow
- SharePoint
- Azure

Without a centralized identity provider, each application might require:

- Separate account
- Separate password
- Separate MFA policy
- Separate security configuration

That becomes difficult to manage.

---

# With an Identity Provider

The organization can centralize identity management.

The IdP can:

- Authenticate users
- Apply MFA
- Apply access policies
- Monitor sign-ins
- Disable users
- Issue security tokens

Applications trust the IdP instead of individually authenticating every user.

---

# How an Identity Provider Works

Basic process:

1. User attempts to access an application.
2. Application redirects the user to the identity provider.
3. Identity provider authenticates the user.
4. Identity provider issues a security token.
5. User/application presents the token.
6. Application trusts the token and grants appropriate access.

### ELI5

The identity provider acts like a trusted ID office.

The application does not need to investigate your identity itself.

It trusts the ID office that already verified you.

---

# Security Tokens

After authentication, the identity provider can issue a:

**Security token**

A token is a package of information containing details about an authenticated identity.

---

# Claims

Information inside a token is represented as:

**Claims**

Claims can contain information such as:

- User ID
- Name
- Email address
- Role
- Group membership
- Token expiration
- Permissions

### Simple Meaning

**Claim = A statement about the identity**

Example:

> Zachary belongs to the Finance group.

That can be represented as a claim.

---

# ID Token vs. Access Token

This is an important distinction.

| Token | Purpose |
|---|---|
| ID Token | Authentication |
| Access Token | Authorization |

---

## ID Token

An ID token proves:

**Who the user is**

Think:

**ID token = Identity**

---

## Access Token

An access token specifies:

**What an application can access**

Think:

**Access token = Authorization**

---

# Token Memory Trick

**ID Token = Who**

**Access Token = What**

---

# 5. Authentication Protocols

Identity providers communicate with applications using standard protocols.

The main protocols discussed for SC-900 are:

| Protocol | Main Purpose |
|---|---|
| OpenID Connect — OIDC | Authentication |
| OAuth 2.0 | Authorization |
| SAML | Enterprise authentication/federation |

---

# OpenID Connect — OIDC

OpenID Connect is commonly used for:

**Authentication**

It allows an application to verify a user's identity.

OIDC is built on:

**OAuth 2.0**

### Memory Trick

**OpenID = Identity**

---

# OAuth 2.0

OAuth 2.0 is primarily used for:

**Authorization**

It allows applications to obtain access tokens and access resources on behalf of a user.

### Memory Trick

**OAuth = Access**

---

# SAML

SAML stands for:

**Security Assertion Markup Language**

SAML is commonly used for:

- Enterprise authentication
- Older enterprise applications
- Federation
- SSO scenarios

### Exam Shortcut

If Microsoft asks about:

**modern application authorization**

Think:

**OAuth**

If it asks about:

**modern authentication**

Think:

**OpenID Connect**

If it asks about:

**enterprise federation or older enterprise applications**

Think:

**SAML**

---

# 6. Single Sign-On — SSO

Single Sign-On allows users to:

**Sign in once and access multiple applications**

The user does not need to repeatedly enter separate credentials for every trusted application.

---

## How SSO Works

A simplified process:

1. User signs in to the identity provider.
2. Identity provider authenticates the user.
3. Identity provider issues tokens.
4. Trusted applications accept those tokens.
5. User accesses multiple applications without repeatedly signing in.

---

# Benefits of SSO

## Better User Experience

Users have fewer credentials to remember.

## Better Security

Fewer password prompts reduce opportunities for:

- Phishing
- Password reuse
- Credential theft

## Centralized Control

Disable the user at the identity provider and access to connected applications can be removed centrally.

---

# SSO Exam Cue

If the question says:

> One credential provides access to multiple applications.

Think:

**Single Sign-On — SSO**

---

# 7. Directory Services

## What Is a Directory?

A directory is a structured database containing information about network objects.

Examples:

- Users
- Devices
- Groups
- Applications
- Policies
- Resources

---

# What Is a Directory Service?

A directory service is the software that manages and provides access to directory information.

It helps answer questions such as:

- Who is this user?
- What group are they in?
- What resources can they access?
- What devices belong to them?

---

# 8. Active Directory Domain Services — AD DS

Active Directory Domain Services is Microsoft's traditional on-premises directory service.

Abbreviation:

**AD DS**

It is designed primarily for:

**On-premises Windows domain environments**

---

# Domain Controller

A server running Active Directory Domain Services is called a:

**Domain Controller — DC**

Domain controllers authenticate users and manage domain information.

---

# AD DS Capabilities

AD DS can:

- Manage users
- Manage computers
- Manage groups
- Authenticate users
- Apply Group Policy
- Manage domain resources
- Organize users and computers

---

# Organizational Units — OUs

Active Directory can organize users and computers into:

**Organizational Units — OUs**

OUs make administration easier.

---

# Group Policy

AD DS supports:

**Group Policy**

Group Policy allows administrators to centrally configure settings for domain-joined Windows systems.

---

# Traditional AD Authentication

AD DS commonly uses protocols such as:

- Kerberos
- NTLM

These are strongly associated with traditional on-premises Windows environments.

---

# Limitations of Traditional AD DS

AD DS was designed primarily for on-premises environments.

Modern environments introduced challenges such as:

- SaaS applications
- Cloud services
- Mobile devices
- Remote employees
- Non-Windows devices
- Modern authentication protocols

This led to cloud-focused identity platforms.

---

# 9. Microsoft Entra ID

Microsoft Entra ID is Microsoft's:

**Cloud-based identity and access management service**

It is designed for:

- Cloud applications
- SaaS
- Microsoft 365
- Azure
- Mobile devices
- Remote access
- Modern authentication

---

# AD DS vs. Microsoft Entra ID

Do NOT treat Microsoft Entra ID as simply "Active Directory in the cloud."

They serve related purposes but are different technologies.

| AD DS | Microsoft Entra ID |
|---|---|
| Primarily on-premises | Cloud-based |
| Domain-based | Internet/cloud-based identity |
| Domain controllers | Microsoft-managed cloud service |
| Kerberos / NTLM | Modern authentication protocols |
| Group Policy | Cloud access policies |
| Windows-centric origins | Cross-platform |
| Often requires network/VPN access | Designed for internet access |

---

# Identity as a Service — IDaaS

Microsoft Entra ID operates as:

**Identity as a Service — IDaaS**

Microsoft manages the infrastructure.

Organizations use the service to manage:

- Users
- Devices
- Applications
- Authentication
- Access policies

---

# Hybrid Identity

Organizations do not necessarily have to choose between:

AD DS

and

Microsoft Entra ID

They can use both.

This is called:

**Hybrid Identity**

Identities can be synchronized so users access:

- On-premises resources
- Cloud resources

using the same organizational identity.

### Memory Trick

**Hybrid = On-prem + Cloud**

---

# 10. Federation

## What Is Federation?

Federation allows identities from one organization or identity system to access resources controlled by another.

The two identity systems establish:

**Trust**

---

# ELI5 Federation

Think about a passport.

Your country issues your passport.

Another country did not issue it, but it trusts the issuing government enough to accept the passport as proof of identity.

Federation works similarly.

Organization A trusts Organization B's identity provider.

A user from Organization B authenticates using their normal credentials.

Organization A accepts that authentication because of the trust relationship.

---

# Federation Key Concept

Federation allows users to:

**Use their existing identity across organizational boundaries**

without needing an entirely separate identity and password for every organization.

---

# Federation Example

Company A partners with Company B.

An employee from Company B needs access to Company A's collaboration system.

Instead of Company A creating another independent username and password, Company A can trust Company B's identity provider.

The employee authenticates with Company B.

Company A accepts that identity.

---

# Federation Trust Is NOT Automatically Two-Way

This is an important exam detail.

If:

**Organization A trusts Organization B**

that does NOT automatically mean:

**Organization B trusts Organization A**

Trust relationships can be:

- One-way
- Two-way

A two-way trust must be explicitly established.

---

# Federation Scenarios

Federation can be used for:

## Business-to-Business Collaboration

Partners from another organization use their own identities.

## Social Sign-In

A website allows:

**Sign in with Google**

or

**Sign in with Microsoft**

or

**Sign in with GitHub**

The application trusts the external identity provider.

## Cloud Access from On-Premises Identity

An organization can federate an on-premises identity environment with cloud services.

---

# Active Directory Federation Services — AD FS

AD FS stands for:

**Active Directory Federation Services**

AD FS is a Microsoft server role used to extend identity across organizational or service boundaries.

It can allow on-premises Active Directory users to authenticate to external or cloud applications.

---

# SSO vs. Federation

These concepts are related but different.

| SSO | Federation |
|---|---|
| One sign-in for multiple applications | Trust between separate identity systems |
| Often one identity provider | Usually involves multiple identity providers |
| Reduces repeated sign-ins | Extends identity across boundaries |

### Memory Trick

**SSO = One login, many apps**

**Federation = One identity, multiple organizations**

---

# Identity Concepts Exam Quick Reference

| If the Question Mentions... | Think... |
|---|---|
| Who are you? | Authentication |
| What are you allowed to do? | Authorization |
| Password | Something you know |
| Phone/security key | Something you have |
| Fingerprint/face | Something you are |
| Multiple authentication factor categories | MFA |
| Minimum permissions | Least privilege |
| Users working outside the corporate network | Identity as security perimeter |
| Create/manage/remove identities | Administration |
| Verify identity | Authentication |
| Determine permissions | Authorization |
| Track identity activity | Auditing |
| Central authentication service | Identity Provider |
| Information inside a token | Claims |
| Proof of identity | ID Token |
| Permission to access a resource | Access Token |
| Modern authentication | OpenID Connect |
| Authorization/access tokens | OAuth 2.0 |
| Enterprise federation | SAML |
| One login for many applications | SSO |
| Users/groups/devices repository | Directory Service |
| Traditional on-premises Microsoft directory | AD DS |
| Server running AD DS | Domain Controller |
| Cloud identity service | Microsoft Entra ID |
| On-prem + cloud identities | Hybrid Identity |
| Trust between organizations | Federation |
| Microsoft's federation server role | AD FS |

---

# Module 2 Memory Sheet

## Authentication vs. Authorization

**Authentication = WHO**

**Authorization = WHAT**

Authentication comes first.

Authorization comes second.

---

## Authentication Factors

**Know**

Password / PIN

**Have**

Phone / Security Key

**Are**

Fingerprint / Face

---

## Four Identity Pillars

**Administration**

Manage identities

**Authentication**

Verify identities

**Authorization**

Control access

**Auditing**

Track activity

### Memory Trick

**AAAA**

---

## Tokens

**ID Token = Authentication**

**Access Token = Authorization**

---

## Protocols

**OIDC = Authentication**

**OAuth = Authorization**

**SAML = Enterprise/Federation**

---

## Directory Services

**AD DS = Traditional / On-Prem**

**Microsoft Entra ID = Modern / Cloud**

---

## SSO vs. Federation

**SSO = One login → many apps**

**Federation = One identity → across organizations**

---

# Common SC-900 Traps

## Trap 1

A user successfully signs in.

This is:

**Authentication**

The system decides whether the user may open a confidential document.

This is:

**Authorization**

---

## Trap 2

Username + password + PIN is NOT necessarily MFA.

Password and PIN are both:

**Something you know**

MFA requires factors from different categories.

---

## Trap 3

Microsoft Entra ID and Active Directory Domain Services are NOT the same product.

**AD DS = on-premises/domain-focused**

**Entra ID = cloud identity and access management**

---

## Trap 4

Federation does NOT mean trust is automatically bidirectional.

A trust relationship can be one-way.

---

## Trap 5

SSO and federation are related but not identical.

**SSO = fewer sign-ins**

**Federation = trust between identity systems**

---

## Trap 6

ID Token and Access Token have different jobs.

**ID Token = proves who the user is**

**Access Token = grants permission to access something**

---

# Final Takeaway

Modern security centers on identity.

Before access is granted, systems need to determine:

1. **Who or what is requesting access?**
2. **Can that identity be verified?**
3. **What should that identity be allowed to access?**
4. **Can the activity be monitored and audited?**

Authentication proves identity.

Authorization determines permissions.

Identity providers centralize authentication and issue security tokens.

Directory services store and manage identity information.

Active Directory Domain Services is designed primarily for traditional on-premises environments.

Microsoft Entra ID extends identity management into modern cloud environments.

Federation allows separate identity systems and organizations to trust one another.

For SC-900, focus heavily on recognizing **which identity concept a scenario is describing**.
