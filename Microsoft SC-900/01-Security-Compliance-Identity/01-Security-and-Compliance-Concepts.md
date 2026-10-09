# Describe Security and Compliance Concepts

> **Source:** Microsoft Learn — SC-900  
> **Verified against current Microsoft Learn content:** October 8, 2026

---

# Module Overview

This module covers foundational security and compliance concepts used throughout Microsoft security products and services.

The current Microsoft Learn module focuses on:

| Topic | Core Idea |
|---|---|
| Shared Responsibility | Who is responsible for securing what |
| Defense in Depth | Protect resources with multiple security layers |
| CIA Triad | Confidentiality, Integrity, and Availability |
| Zero Trust | Trust no one automatically; continuously verify |
| Encryption | Protect data from unauthorized viewing |
| Hashing | Verify data integrity and protect stored passwords |
| GRC | Governance, Risk, and Compliance |
| Data Residency | Where data is physically stored |
| Data Sovereignty | Which country's laws apply to data |
| Data Privacy | Appropriate handling of personal information |

---

# 1. Shared Responsibility Model

## Big Idea

Using cloud services does **not** mean Microsoft becomes responsible for all security.

Security responsibility is divided between:

**The cloud provider**

and

**The customer**

The exact split depends on the type of service being used.

---

# On-Premises

In a traditional on-premises environment, the organization manages and secures the entire technology stack.

The organization is responsible for:

- Buildings
- Physical servers
- Networking equipment
- Operating systems
- Applications
- Identities
- Access
- Endpoints
- Data

### ELI5

**On-premises = You own it, run it, and secure it.**

---

# Infrastructure as a Service — IaaS

With IaaS, the cloud provider manages the underlying physical infrastructure.

Examples include cloud-hosted virtual machines.

## Cloud Provider Typically Manages

- Physical datacenter
- Physical servers
- Physical networking
- Host infrastructure

## Customer Typically Manages

- Operating systems
- Applications
- Configured network controls
- Identities and access
- Data

### ELI5

**IaaS = Microsoft owns the computer; you manage what runs inside it.**

---

# Platform as a Service — PaaS

With PaaS, the cloud provider also manages the operating system and runtime environment.

## Cloud Provider Typically Manages

- Physical infrastructure
- Networking hardware
- Host systems
- Operating system
- Runtime/platform

## Customer Typically Manages

- Application code
- Application configuration
- Access controls
- Data

### ELI5

**PaaS = Microsoft manages the platform; you manage your application and data.**

---

# Software as a Service — SaaS

With SaaS, the cloud provider manages almost the entire application stack.

Examples include Microsoft 365 services.

The customer still manages important security responsibilities.

## Customer Responsibilities Include

- Access management
- User identities
- Permissions
- Organizational data
- Tenant configuration

### ELI5

**SaaS = Microsoft runs the software; you still control your users, settings, and data.**

---

# As You Move Toward SaaS...

Think:

**On-Prem → IaaS → PaaS → SaaS**

As you move to the right:

**The provider manages more.**

But the customer never gives up all responsibility.

---

# Responsibilities the Customer Always Retains

Microsoft Learn emphasizes four areas that remain customer responsibilities regardless of cloud service model.

## Data

You decide:

- What data is collected
- How sensitive it is
- Who can access it
- How long it is retained
- How it should be protected
- How compliance requirements are met

### Memory Cue

**Your data = your responsibility**

---

## Identities and Access

You manage:

- User accounts
- Authentication methods
- Access permissions
- MFA
- Least privilege

A perfectly secured cloud platform cannot protect you if an attacker successfully uses a compromised authorized account.

---

## Endpoints

Organizations remain responsible for devices connecting to cloud resources.

Examples:

- Laptops
- Phones
- Tablets
- Desktops

Security measures include:

- Patching
- Device management
- Threat detection
- Security configuration

---

## Configuration Choices

The customer controls many security settings inside the cloud environment.

Examples:

- Permissions
- Access policies
- Network rules
- Storage configuration
- Tenant settings

A secure cloud service can still become exposed through bad configuration.

### Exam Concept

**Cloud provider security does not protect against customer misconfiguration.**

---

# Shared Responsibility and AI

The shared responsibility model also applies to AI workloads.

Microsoft Learn describes an AI-enabled application using three layers:

| Layer | Meaning |
|---|---|
| AI Platform | Infrastructure, model, and built-in safety controls |
| AI Application | Application using the AI platform |
| AI Usage | How people use the AI system |

---

## AI Platform

The provider typically handles areas such as:

- Physical infrastructure
- AI model hosting
- Underlying compute
- Platform-level safety controls
- Operational security of the AI service

---

## AI Application

The organization controls things such as:

- Application configuration
- Connected data sources
- Plugins
- Integrations
- Access configuration

---

## AI Usage

The organization is responsible for:

- What users enter into AI systems
- Acceptable use policies
- User training
- Monitoring
- Oversight

---

# Customer Responsibilities for AI

Even when Microsoft secures the underlying AI platform, the customer remains responsible for:

## Protecting Data

Control what business and sensitive data the AI system can access.

## Identity and Access Management

Control:

- Who can use AI applications
- What they are allowed to do

## Safe Configuration

Control:

- External connectors
- Data sources
- Logging
- Retention
- Access settings

## AI-Specific Risks

One example is:

**Prompt injection**

Prompt injection occurs when malicious instructions are placed into prompts or external data in an attempt to manipulate AI behavior.

## User Training

Users influence AI systems through their prompts and inputs.

Organizations therefore need:

- Training
- Policies
- Monitoring
- Clear acceptable-use expectations

---

# Shared Responsibility Memory Sheet

## On-Premises

**Customer manages everything**

## IaaS

**Provider = hardware**

**Customer = OS and above**

## PaaS

**Provider = infrastructure + OS/platform**

**Customer = application + data**

## SaaS

**Provider = application stack**

**Customer = identities + access + data + configuration**

---

# 2. Defense in Depth

## Big Idea

Defense in depth means using **multiple overlapping security layers**.

Do not depend on one firewall, one password, or one security tool.

If one security layer fails, another layer should still protect the organization.

### ELI5

Think of protecting a vault with:

- Building security
- Cameras
- Guards
- Badge reader
- Locked door
- Vault
- Locked container inside the vault

Getting past one control does not give the attacker everything.

---

# Seven Defense-in-Depth Layers

From outermost toward the protected data:

1. Physical Security
2. Identity and Access
3. Perimeter
4. Network
5. Compute
6. Application
7. Data

---

## 1. Physical Security

Protects physical infrastructure.

Examples:

- Locked facilities
- Security guards
- Badge readers
- Surveillance cameras

### Simple Meaning

**Keep unauthorized people away from the hardware.**

---

## 2. Identity and Access

Ensures users are authenticated and authorized.

Examples:

- MFA
- Role-Based Access Control — RBAC
- Conditional Access
- Least privilege

### Simple Meaning

**Make sure the right person gets the right access.**

---

## 3. Perimeter Security

Protects the outer boundary of the network.

Examples:

- Firewalls
- DDoS protection

### Simple Meaning

**Protect the front door of the network.**

---

## 4. Network Security

Controls communication between resources.

Examples:

- Network segmentation
- Network Security Groups — NSGs
- Traffic restrictions

### Simple Meaning

**Even if someone gets inside, don't let them freely move everywhere.**

---

## 5. Compute Security

Protects systems performing computing work.

Examples:

- Virtual machines
- Containers
- Servers

Controls include:

- Patching
- Closing unnecessary ports
- Restricting administrator access
- Monitoring abnormal behavior

---

## 6. Application Security

Protects software applications.

Examples:

- Secure development
- Input validation
- Authentication
- Authorization
- Security testing

Application security helps prevent attacks such as:

- SQL injection
- Cross-site scripting — XSS

---

## 7. Data Security

The innermost layer.

Protects the information itself.

Examples:

- Encryption
- Access controls
- Classification

### Exam Cue

If asked what ultimately needs to be protected:

**DATA**

---

# Why Defense in Depth Matters

Any individual security control can fail because of:

- Vulnerabilities
- Misconfiguration
- Human mistakes
- Business exceptions

Multiple security layers make it harder for one failure to become a full breach.

---

# CIA Triad

The three fundamental security goals are:

**Confidentiality**

**Integrity**

**Availability**

### Memory Trick

**CIA**

---

# Confidentiality

Confidentiality means:

**Only authorized people should be able to see protected information.**

Examples of confidential information:

- Passwords
- Customer records
- Financial information
- Private communications
- Intellectual property

Controls include:

- Encryption
- Access controls
- Secure transmission

### Exam Question

**Who can see the data?**

= Confidentiality

---

# Integrity

Integrity means:

**Data remains accurate, complete, and unchanged except through authorized actions.**

Threats to integrity include:

- Unauthorized modification
- Data corruption
- Malicious tampering
- Unauthorized deletion

Controls include:

- Hashing
- Digital signatures
- Audit logs
- Database controls

### Exam Question

**Has the data been changed?**

= Integrity

---

# Availability

Availability means:

**Authorized users can access systems and data when they need them.**

Threats include:

- DDoS
- Ransomware
- Hardware failure
- Software failure
- Natural disaster

Controls include:

- Redundancy
- Load balancing
- Failover
- Backups
- Recovery plans
- DDoS protection

### Exam Question

**Can authorized users access it when needed?**

= Availability

---

# CIA Attack Examples

| Attack | Security Goal Affected |
|---|---|
| Stealing confidential records | Confidentiality |
| Changing database records | Integrity |
| Taking a website offline | Availability |

---

# 3. Zero Trust

## Big Idea

Zero Trust is a **security strategy**, not one Microsoft product.

Core idea:

**Trust no one automatically. Verify everything.**

Being inside the organization's network does not automatically make a user, device, or application trustworthy.

---

# Traditional Security

Traditional network security often operated like a castle:

**Outside = untrusted**

**Inside = trusted**

Modern computing broke this model because users now work from:

- Home
- Public networks
- Cloud environments
- Personal devices
- Mobile devices
- Third-party applications

An attacker who steals credentials may also bypass the traditional network perimeter.

---

# Three Zero Trust Principles

## 1. Verify Explicitly

Always authenticate and authorize using all available information.

Signals can include:

- User identity
- Location
- Device
- Device compliance
- Application
- Data sensitivity
- Risk
- Unusual activity

### Simple Meaning

**Don't assume. Check.**

---

## 2. Use Least-Privileged Access

Give users and systems:

**Only the access they need**

and

**Only for as long as they need it**

Microsoft Learn specifically discusses:

### Just-in-Time — JIT

Access is granted only when needed and removed afterward.

### Just-Enough-Access — JEA

Only the exact permissions required are granted.

### Memory Trick

**JIT = WHEN**

**JEA = HOW MUCH**

---

## 3. Assume Breach

Design security as if an attacker may eventually get through your defenses.

This means:

- Segment access
- Encrypt data
- Monitor activity
- Detect threats
- Limit attacker movement
- Reduce damage

### Simple Meaning

**Plan as though the bad guy may already be inside.**

---

# Seven Zero Trust Pillars

The current Microsoft model uses seven interconnected pillars:

1. Identities
2. Devices
3. Applications
4. Data
5. Infrastructure
6. Networks
7. Visibility, Automation, and Orchestration

---

## 1. Identities

Identities can include:

- Users
- Services
- Devices

Identity controls include:

- Strong authentication
- Least privilege
- Risk evaluation

### Key Idea

**Identity is a primary control plane in modern security.**

---

## 2. Devices

Every device accessing organizational resources can become an attack point.

Organizations evaluate:

- Device health
- Compliance
- Management status
- Signs of compromise

A risky device can be:

- Blocked
- Restricted
- Required to meet additional controls

---

## 3. Applications

Applications are how users consume data.

Organizations need visibility into:

- Approved applications
- Unapproved applications
- Permissions
- Application access

### Shadow IT

Applications employees use without formal organizational approval are often called:

**Shadow IT**

---

## 4. Data

Data should be:

- Classified
- Labeled
- Protected
- Encrypted

Protection should remain with the data even when it leaves the organization's direct control.

---

## 5. Infrastructure

Infrastructure can include:

- On-premises systems
- Cloud systems
- Servers
- Virtual machines

Zero Trust applies controls such as:

- Continuous assessment
- Configuration compliance
- Monitoring
- JIT administration

---

## 6. Networks

Networks should be segmented.

### Microsegmentation

Creates smaller security boundaries inside the network.

Goal:

**Compromise of one network area should not give access to everything else.**

Controls include:

- Segmentation
- Encryption
- Monitoring
- Threat protection

---

## 7. Visibility, Automation, and Orchestration

This pillar ties the others together.

It collects and correlates security information across the environment.

Important technologies include:

### SIEM

**Security Information and Event Management**

Collects and correlates security signals.

### SOAR

**Security Orchestration, Automation, and Response**

Automates actions based on detected threats.

You will study SIEM and SOAR in more detail later in SC-900.

---

# Zero Trust Memory Sheet

## Three Principles

**Verify explicitly**

**Use least privilege**

**Assume breach**

## Seven Pillars

**Identity**

**Devices**

**Applications**

**Data**

**Infrastructure**

**Networks**

**Visibility / Automation / Orchestration**

---

# 4. Encryption and Hashing

# Encryption

Encryption makes information unreadable to unauthorized users.

Encrypted data must be:

**Decrypted**

using the correct:

**Key**

### Main Security Goal

**Confidentiality**

---

# Symmetric Encryption

Symmetric encryption uses:

**The same key for encryption and decryption**

Advantages:

- Fast
- Efficient for large amounts of data

Challenge:

**How do you securely share the secret key?**

### Memory Trick

**Symmetric = Same key**

---

# Asymmetric Encryption

Asymmetric encryption uses a key pair:

**Public Key**

and

**Private Key**

The keys are mathematically related.

Data encrypted with the public key can be decrypted using the corresponding private key.

### Advantages

The public key can be shared openly while the private key remains secret.

### Memory Trick

**Asymmetric = A pair of different keys**

---

# Public and Private Key Exam Cue

If the question says:

> public key + private key

Think:

**Asymmetric encryption**

---

# Digital Signatures

Asymmetric cryptography also enables:

**Digital signatures**

A sender signs information using their:

**Private key**

Others can verify the signature using the sender's:

**Public key**

Digital signatures help verify:

## Authenticity

Did this information actually come from the expected sender?

## Integrity

Was the information changed after it was signed?

### Memory Trick

**Digital signature = WHO sent it + WAS it changed?**

---

# Encryption by Data State

Microsoft Learn identifies three data states:

1. Data at rest
2. Data in transit
3. Data in use

---

# Data at Rest

Data stored somewhere.

Examples:

- Hard drive
- Database
- Storage account

Encryption protects stored information if the storage is stolen or accessed improperly.

### Memory Trick

**At rest = sitting somewhere**

---

# Data in Transit

Data moving between locations.

Examples:

- Across the internet
- Between cloud services
- Across a private network

Common protection:

**TLS**

Example:

**HTTPS**

### Memory Trick

**In transit = moving**

---

# Data in Use

Data actively being processed.

Examples:

- Data in RAM
- Data being processed by the CPU

Traditional systems usually need to decrypt data before processing it.

This creates a potential exposure point.

---

# Confidential Computing

Confidential computing can protect:

**Data in use**

It uses protected execution environments sometimes called:

**Secure enclaves**

These environments help process data while shielding it from other parts of the system.

---

# Key Management

Encryption is only effective if encryption keys remain secure.

Key management includes:

- Generating keys
- Storing keys
- Protecting keys
- Rotating keys
- Retiring keys

---

# Key Management Best Practices

## Store Keys Separately

Do not store the encryption key beside the data it protects.

## Protect Keys with Dedicated Hardware

A:

**Hardware Security Module — HSM**

is a specialized tamper-resistant device used to protect cryptographic keys.

## Rotate Keys

Change keys periodically.

## Restrict Access

Only authorized users and systems should access keys.

Apply:

- Strong authentication
- Least privilege

---

# Azure Key Vault

Azure Key Vault is a managed cloud service used to store and manage things such as:

- Encryption keys
- Certificates
- Secrets

### Exam Cue

If asked which Azure service protects:

**keys, secrets, certificates**

Think:

**Azure Key Vault**

---

# Hashing

Hashing converts input into a fixed-length value called a:

**Hash**

or

**Digest**

Hashing is designed to be:

**One-way**

You should not be able to reverse the hash and recover the original information.

---

# Hashing vs. Encryption

| Encryption | Hashing |
|---|---|
| Reversible with the correct key | One-way |
| Uses keys | Does not use encryption keys |
| Protects confidentiality | Often verifies integrity |
| Original data can be recovered | Original data is not meant to be recovered |

### Memory Trick

**Encryption = Hide it**

**Hashing = Fingerprint it**

---

# Hashing and Integrity

Changing the original data causes its hash to change.

This makes hashing useful for checking:

**Integrity**

Example:

You download software and compare its hash to the publisher's expected hash.

If they match, the file probably has not been changed.

---

# Password Hashing

Secure systems generally should not store passwords in plain text.

Instead:

1. User creates a password
2. System hashes the password
3. System stores the hash
4. User signs in later
5. Entered password is hashed
6. New hash is compared with stored hash

If the hashes match:

**Authentication succeeds**

---

# Rainbow Tables

Basic password hashing can still be attacked using precomputed hash collections.

These may be used in:

- Rainbow table attacks
- Dictionary attacks

This is why secure password hashing uses:

**Salting**

---

# Salting

A salt is a:

**Unique random value added to a password before hashing**

Because each user gets a different salt:

Two users with the same password will still produce different stored hashes.

This makes precomputed rainbow tables far less useful.

### Memory Trick

**Salt = Random extra ingredient before hashing**

---

# Encryption and Hashing Memory Sheet

## Symmetric

**Same key**

## Asymmetric

**Public + Private key**

## Digital Signature

**Private key signs**

**Public key verifies**

## Encryption

**Confidentiality**

## Hashing

**Integrity**

## Data States

**At rest = stored**

**In transit = moving**

**In use = processing**

## HSM

**Specialized hardware that protects cryptographic keys**

## Azure Key Vault

**Keys + Secrets + Certificates**

## Salt

**Random value added before password hashing**

---

# 5. Governance, Risk, and Compliance — GRC

GRC stands for:

**Governance**

**Risk**

**Compliance**

GRC provides a structured way for organizations to manage:

- Security decisions
- Organizational risk
- Laws
- Regulations
- Standards
- Accountability

---

# Governance

Governance is the system of:

- Rules
- Practices
- Processes

that an organization uses to direct and control its activities.

Security governance can include:

- Data classification policies
- Data retention policies
- Identity standards
- Access management standards
- Privileged access approval
- Security control ownership
- Accountability
- Security strategy

### ELI5

**Governance = Who makes the rules, what are the rules, and who is responsible?**

---

# Risk

Risk management is the process of understanding potential events that could negatively affect:

- Systems
- Data
- Operations
- Organizational objectives
- Customer trust

The goal is **not** to eliminate every possible risk.

The goal is to:

**Understand risk well enough to make informed decisions.**

---

# Internal and External Risks

## External Risk Examples

- Cyberattacks
- Natural disasters
- Economic disruption
- Regulatory changes
- Third-party supplier problems

## Internal Risk Examples

- Employee mistakes
- Insider threats
- Fraud
- Weak security processes

---

# Four-Step Risk Management Process

Microsoft Learn presents the process as:

1. Identify
2. Assess
3. Respond
4. Monitor

---

## 1. Identify

Discover potential risks.

Sources can include:

- Interviews
- Vulnerability assessments
- Audit findings
- Monitoring

### Question

**What could go wrong?**

---

## 2. Assess

Evaluate:

- Likelihood
- Impact

This can produce a risk score used to prioritize risks.

### Question

**How likely is it, and how bad would it be?**

---

## 3. Respond

Choose how to handle the risk.

Common responses:

| Response | Meaning |
|---|---|
| Accept | Live with the risk |
| Mitigate | Reduce likelihood or impact |
| Transfer | Shift some risk to another party |
| Avoid | Stop the activity creating the risk |

### Memory Trick

**Accept — Mitigate — Transfer — Avoid**

---

## 4. Monitor

Continue tracking:

- Risk
- Controls
- Changes
- Effectiveness

Risk management is continuous.

---

# Compliance

Compliance means following the:

- Laws
- Regulations
- Standards
- Policies

that apply to an organization.

Requirements may depend on:

- Industry
- Geography
- Type of data handled

---

# Compliance Examples

Microsoft Learn provides examples including:

## HIPAA

U.S. requirements involving protection and handling of health information.

## ISO 27001

International standard for information security management systems.

## SOC 2

Auditing standard commonly relevant to service organizations processing or storing customer data.

---

# Compliance Is NOT the Same as Security

This is an important exam concept.

## Compliance

Focuses on meeting required rules and minimum standards.

## Security

Is broader.

Security includes all measures used to protect:

- Data
- Identities
- Systems
- Applications
- Infrastructure

### Important Point

An organization can be:

**Compliant**

and still:

**Have security vulnerabilities**

because compliance may represent only the minimum required standard.

---

# Data Residency

Data residency refers to requirements about:

**Where data is physically stored**

and sometimes:

- Where it can be processed
- Where it can be transferred
- Where it can be accessed

### Exam Question

**Where is the data physically located?**

= Data Residency

---

# Data Sovereignty

Data sovereignty means:

**Data is subject to the laws and regulations of the country or region where it is collected, stored, or processed.**

Data may interact with several jurisdictions.

Example:

- Collected in Country A
- Stored in Country B
- Processed in Country C

Multiple legal requirements may apply.

### Exam Question

**Whose laws apply to this data?**

= Data Sovereignty

---

# Residency vs. Sovereignty

| Concept | Key Question |
|---|---|
| Data Residency | Where is the data located? |
| Data Sovereignty | Which laws apply to the data? |

### Memory Trick

**Residency = Residence**

**Sovereignty = Sovereign laws**

---

# Data Privacy

Data privacy concerns the appropriate handling of:

**Personal data**

Personal data can include:

- Names
- Email addresses
- Phone numbers
- Location history
- Browsing activity
- Other information linked to an identifiable person

---

# Privacy Requirements May Include

Organizations may need to:

- Explain what personal information they collect
- Explain how it is used
- Obtain consent
- Protect the information
- Allow individuals to access their data
- Allow individuals to correct their data
- Allow individuals to delete certain data

### ELI5

**Privacy = How personal information about people is collected, used, protected, and controlled.**

---

# GRC Memory Sheet

## Governance

**Rules + Direction + Accountability**

## Risk

**What could go wrong?**

Process:

**Identify → Assess → Respond → Monitor**

## Compliance

**Are we following required laws, regulations, standards, and policies?**

## Data Residency

**WHERE is the data?**

## Data Sovereignty

**WHOSE LAWS apply?**

## Data Privacy

**HOW is personal information handled?**

---

# SC-900 Exam Quick Reference

| If the Question Mentions... | Think... |
|---|---|
| Customer vs. cloud provider duties | Shared responsibility |
| Moving from IaaS → PaaS → SaaS | Provider takes more responsibility |
| Data, identities, endpoints, configuration | Customer responsibility |
| AI platform infrastructure/model hosting | Provider responsibility |
| AI prompts, access, connectors, policies | Customer responsibility |
| Multiple overlapping security layers | Defense in depth |
| Protecting information from unauthorized viewing | Confidentiality |
| Ensuring data was not changed | Integrity |
| Ensuring systems remain accessible | Availability |
| Trust nobody automatically | Zero Trust |
| Evaluate multiple signals | Verify explicitly |
| Minimum permissions | Least privilege |
| Access only when needed | JIT |
| Only permissions needed | JEA |
| Design as if attacker is already inside | Assume breach |
| Unapproved apps | Shadow IT |
| Public + private key | Asymmetric encryption |
| Same key encrypts/decrypts | Symmetric encryption |
| Verify sender and unchanged data | Digital signature |
| Stored data | Data at rest |
| Moving data | Data in transit |
| Data being processed | Data in use |
| Protected execution environment | Confidential computing |
| Tamper-resistant key hardware | HSM |
| Keys, secrets, certificates | Azure Key Vault |
| One-way fingerprint | Hash |
| Random value added before password hashing | Salt |
| Policies and organizational direction | Governance |
| Likelihood + impact | Risk assessment |
| Accept / Mitigate / Transfer / Avoid | Risk response |
| Laws and regulations | Compliance |
| Physical location of data | Data residency |
| Laws applying based on location | Data sovereignty |
| Handling personal information | Data privacy |

---

# Final Module 1 Cram Sheet

## Shared Responsibility

**On-Prem = Customer does everything**

**IaaS = Provider handles infrastructure**

**PaaS = Provider also handles OS/platform**

**SaaS = Provider handles application stack**

Customer always retains responsibility for:

**Data**

**Identity/access**

**Endpoints**

**Configuration**

---

## Defense in Depth

Seven layers:

**Physical**

**Identity & Access**

**Perimeter**

**Network**

**Compute**

**Application**

**Data**

---

## CIA

**Confidentiality = Who can see it?**

**Integrity = Was it changed?**

**Availability = Can I access it?**

---

## Zero Trust

**Verify Explicitly**

**Least Privilege**

**Assume Breach**

Seven pillars:

**Identity**

**Devices**

**Applications**

**Data**

**Infrastructure**

**Networks**

**Visibility / Automation / Orchestration**

---

## Cryptography

**Symmetric = Same key**

**Asymmetric = Public + Private**

**Encryption = Confidentiality**

**Hashing = Integrity**

**Digital signature = Authenticity + Integrity**

**At Rest = Stored**

**In Transit = Moving**

**In Use = Processing**

**HSM = Protect cryptographic keys**

**Key Vault = Keys + Secrets + Certificates**

**Salt = Random input added before password hashing**

---

## GRC

**Governance = Rules**

**Risk = What could go wrong**

**Compliance = Follow requirements**

Risk process:

**Identify → Assess → Respond → Monitor**

Risk responses:

**Accept**

**Mitigate**

**Transfer**

**Avoid**

Data concepts:

**Residency = WHERE**

**Sovereignty = WHOSE LAWS**

**Privacy = PERSONAL DATA HANDLING**

---

# Final Takeaway

This module establishes the security concepts used throughout the rest of SC-900.

Modern cloud security depends on:

1. Understanding what the customer and provider are each responsible for.
2. Protecting systems with multiple security layers.
3. Protecting confidentiality, integrity, and availability.
4. Applying Zero Trust continuously instead of automatically trusting users or devices.
5. Using encryption and hashing appropriately.
6. Managing encryption keys securely.
7. Governing organizational security through structured risk and compliance practices.
8. Understanding where data resides, which laws govern it, and how personal information must be handled.

For the SC-900 exam, focus on recognizing the concept being described in a scenario rather than memorizing long definitions.
