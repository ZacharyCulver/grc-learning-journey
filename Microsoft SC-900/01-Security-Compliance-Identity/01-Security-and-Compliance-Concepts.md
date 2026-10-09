# Describe Security and Compliance Concepts

## Module Overview

This module covers the foundational security and compliance concepts used throughout Microsoft security products.

The main topics are:

| Topic | Core Idea |
|---|---|
| Shared Responsibility | Who is responsible for security in the cloud |
| Defense in Depth | Using multiple layers of security |
| Zero Trust | Never trust automatically; always verify |
| Encryption and Hashing | Protecting data and verifying integrity |
| GRC | Governance, Risk, and Compliance |

---

# 1. Shared Responsibility Model

## Big Idea

Moving to the cloud does **not** mean Microsoft becomes responsible for everything.

Security responsibilities are divided between:

**Microsoft — the cloud provider**

and

**The customer — the organization using the cloud**

The exact division depends on the type of cloud service being used.

---

## On-Premises

If an organization owns and operates everything itself, the organization is responsible for essentially everything.

The organization manages:

| Responsibility |
|---|
| Physical datacenter |
| Physical servers |
| Networking |
| Operating systems |
| Applications |
| Identities |
| Accounts |
| Data |

### Memory Trick

**On-premises = You own everything, so you secure everything.**

---

## Infrastructure as a Service — IaaS

Microsoft manages the physical cloud infrastructure.

The customer still manages much of the software environment.

Examples include Azure virtual machines.

| Microsoft | Customer |
|---|---|
| Physical datacenter | Operating system |
| Physical servers | Applications |
| Physical networking | Identities |
| Hardware | Accounts |
|  | Data |

### Memory Trick

**IaaS = Microsoft provides the hardware; you manage the computer running on it.**

---

## Platform as a Service — PaaS

Microsoft manages both the infrastructure and much of the platform.

The customer mainly focuses on applications, identities, and data.

### Memory Trick

**PaaS = Microsoft manages the platform; you manage what you build on it.**

---

## Software as a Service — SaaS

Microsoft manages nearly the entire technical platform.

Examples include Microsoft 365.

The customer is still responsible for important areas such as:

| Customer Responsibility |
|---|
| User identities |
| Access permissions |
| Accounts |
| Data |
| Security configuration |

### Important Exam Concept

Even with SaaS, the customer is **not completely free of security responsibilities**.

The customer must still protect identities, configure access correctly, and protect organizational data.

### Memory Trick

**SaaS = Microsoft runs the software, but you still control your users and data.**

---

# 2. Defense in Depth

## Big Idea

Defense in depth means using **multiple layers of security** instead of relying on one security control.

If one layer fails, another layer can still protect the organization.

Think of a castle:

An attacker may get past the outer wall, but there are still gates, guards, doors, and locks behind it.

---

## Defense-in-Depth Layers

A common model moves from the outside toward the data:

| Layer | Purpose |
|---|---|
| Physical Security | Protect buildings, datacenters, and hardware |
| Identity and Access | Verify users and control permissions |
| Perimeter | Protect the boundary of the network |
| Network | Control traffic between network resources |
| Compute | Protect servers, virtual machines, and endpoints |
| Application | Protect software and applications |
| Data | Protect the actual information |

---

## Data Is the Final Layer

The **data layer** protects the information itself.

Examples include:

Encryption

Access controls

Data classification

Data Loss Prevention

### Exam Cue

If a question asks which layer protects information **regardless of where it is stored**, think:

**DATA**

---

# 3. Zero Trust Model

## Big Idea

Traditional security often assumed:

> If you are inside the corporate network, you can probably be trusted.

Zero Trust assumes:

> Nobody should automatically be trusted simply because of where they are located.

Every access attempt should be evaluated.

---

## Three Zero Trust Principles

| Principle | Meaning |
|---|---|
| Verify Explicitly | Always verify identity and access conditions |
| Use Least Privilege | Give only the minimum access necessary |
| Assume Breach | Design security as though attackers may already be inside |

---

## Verify Explicitly

Access decisions should use available information.

This may include:

Identity

Location

Device

Application

Risk level

Authentication method

### Simple Meaning

**Prove who you are before getting access.**

---

## Least Privilege

Users should receive only the permissions they actually need.

A user should not receive administrator privileges simply because they might need them someday.

### Simple Meaning

**Give people the minimum access necessary to do their job.**

---

## Assume Breach

Organizations should operate as if an attacker could already be inside the environment.

Security teams should:

Limit access

Segment systems

Monitor activity

Detect suspicious behavior

Protect important data

### Simple Meaning

**Plan as if someone has already gotten in.**

---

# 4. Encryption and Hashing

## Encryption

Encryption transforms readable data into unreadable data.

Encrypted information can later be converted back into readable information using the appropriate key.

### Purpose

**Confidentiality**

Encryption prevents unauthorized people from reading information.

---

## Symmetric Encryption

Symmetric encryption uses the **same key** for encryption and decryption.

### Memory Trick

**Symmetric = Same key**

---

## Asymmetric Encryption

Asymmetric encryption uses a **key pair**:

| Key |
|---|
| Public Key |
| Private Key |

One key can encrypt information and the corresponding key can decrypt it.

### Memory Trick

**Asymmetric = A pair of different keys**

### Exam Cue

If the question mentions:

> public key + private key

The answer is:

**Asymmetric encryption**

---

# Hashing

Hashing converts data into a fixed-length value called a **hash**.

Hashing is designed to be **one-way**.

You do not normally reverse a hash to recover the original information.

---

## Primary Purpose of Hashing

Hashing is commonly used to verify:

**Integrity**

If the original data changes, the resulting hash changes.

---

## Encryption vs. Hashing

| Encryption | Hashing |
|---|---|
| Reversible with the correct key | Designed to be one-way |
| Protects confidentiality | Helps verify integrity |
| Uses encryption keys | Produces a hash value |
| Original data can be recovered | Original data is not intended to be recovered |

### Memory Trick

**Encryption = Hide it**

**Hashing = Check it**

---

# 5. Governance, Risk, and Compliance — GRC

GRC stands for:

**Governance**

**Risk**

**Compliance**

These three concepts help organizations manage security in a structured way.

---

## Governance

Governance defines how an organization makes decisions and establishes rules.

Governance includes things such as:

Policies

Standards

Procedures

Roles

Responsibilities

Oversight

### Simple Meaning

**Governance = What rules do we follow and who is responsible?**

---

## Risk

Risk is the possibility that a threat could cause harm to an organization.

Organizations identify risks, evaluate them, and decide how to respond.

### Simple Meaning

**Risk = What could go wrong, and how bad would it be?**

---

## Common Risk Responses

| Response | Meaning |
|---|---|
| Avoid | Stop doing the risky activity |
| Mitigate | Reduce the likelihood or impact |
| Transfer | Shift some risk to another party |
| Accept | Acknowledge the risk and live with it |

---

## Compliance

Compliance means meeting required rules or requirements.

Requirements can come from:

Laws

Regulations

Industry standards

Contracts

Internal policies

### Simple Meaning

**Compliance = Are we following the rules we are required to follow?**

---

# Security vs. Compliance

Security and compliance are related, but they are not identical.

| Security | Compliance |
|---|---|
| Protects systems, identities, and data | Demonstrates adherence to requirements |
| Focuses on reducing threats and risk | Focuses on laws, regulations, policies, and standards |
| Can exceed minimum requirements | Often establishes required minimums |

### Important Concept

An organization can technically be compliant with a requirement and still have security weaknesses.

Good security usually goes beyond simply checking compliance boxes.

---

# Core Security Concepts

## Confidentiality

Only authorized people should be able to view information.

Think:

**Who can see it?**

Encryption helps support confidentiality.

---

## Integrity

Information should not be changed without authorization.

Think:

**Has the data been altered?**

Hashing can help verify integrity.

---

## Availability

Systems and information should be accessible when authorized users need them.

Think:

**Can I access it when I need it?**

---

# CIA Triad

The three fundamental security objectives are:

| Letter | Meaning | Question |
|---|---|---|
| C | Confidentiality | Who can see the data? |
| I | Integrity | Has the data been changed? |
| A | Availability | Can authorized users access it? |

### Memory Trick

**CIA = Confidentiality, Integrity, Availability**

---

# Identity as the Security Perimeter

Traditional security focused heavily on protecting the corporate network.

Modern organizations use:

Cloud applications

Remote work

Mobile devices

Bring Your Own Device — BYOD

Software as a Service — SaaS

Users may access company resources without ever being physically connected to the corporate network.

Because of this, **identity becomes a primary security perimeter**.

### Simple Meaning

Security increasingly asks:

> Who are you?

rather than:

> Are you inside our building or network?

---

# Authentication vs. Authorization

These concepts are easy to confuse.

## Authentication

Authentication proves **who you are**.

Examples:

Password

MFA

Biometrics

Security key

### Memory Trick

**Authentication = Who are you?**

---

## Authorization

Authorization determines **what you are allowed to do**.

Examples:

Read a file

Modify a database

Access SharePoint

Administer users

### Memory Trick

**Authorization = What are you allowed to do?**

---

## Example

A user enters a password and successfully signs in.

That is:

**Authentication**

Microsoft then determines whether that user can open a confidential SharePoint site.

That is:

**Authorization**

---

# SC-900 Exam Quick Reference

| If the Question Mentions... | Think... |
|---|---|
| Minimum necessary permissions | Least privilege |
| Never automatically trust | Zero Trust |
| Explicit identity verification | Verify explicitly |
| Plan as if attacker is already inside | Assume breach |
| Multiple security layers | Defense in depth |
| Public + private key | Asymmetric encryption |
| Same key encrypts and decrypts | Symmetric encryption |
| Protecting confidentiality | Encryption |
| Checking whether data changed | Hashing / Integrity |
| Laws and regulations | Compliance |
| Policies and organizational direction | Governance |
| What could go wrong | Risk |
| Who are you? | Authentication |
| What can you access? | Authorization |
| Who can see the data? | Confidentiality |
| Has the data changed? | Integrity |
| Can users access it? | Availability |

---

# Module 1 Memory Sheet

## Zero Trust

**Verify Explicitly**

**Least Privilege**

**Assume Breach**

---

## CIA Triad

**Confidentiality**

**Integrity**

**Availability**

---

## Encryption

**Symmetric = Same key**

**Asymmetric = Public + Private key**

**Encryption = Confidentiality**

---

## Hashing

**One-way**

**Integrity**

**Hash changes if data changes**

---

## Identity

**Authentication = Who are you?**

**Authorization = What can you do?**

---

## GRC

**Governance = Rules and direction**

**Risk = What could go wrong**

**Compliance = Are we following required rules**

---

# Final Takeaway

The main idea of this module is that modern security does not rely on one tool or one network boundary.

Organizations divide security responsibilities with cloud providers, use multiple layers of protection, follow Zero Trust principles, protect data with encryption and hashing, and manage organizational security through governance, risk, and compliance.

For SC-900, focus on recognizing **which concept Microsoft is describing in a scenario** rather than memorizing long definitions.
