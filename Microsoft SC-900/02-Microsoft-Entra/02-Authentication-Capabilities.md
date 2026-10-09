# Describe the Authentication Capabilities of Microsoft Entra ID

> **Source:** Microsoft Learn — SC-900  
> **Module:** Describe the authentication capabilities of Microsoft Entra ID  
> **Verified against current Microsoft Learn content:** October 8, 2026

---

# Module Overview

This module covers how Microsoft Entra ID verifies users and helps protect authentication.

The current Microsoft Learn module focuses on:

| Topic | Core Idea |
|---|---|
| Authentication Methods | Ways users can prove their identity |
| Passwordless Authentication | Authenticate without using traditional passwords |
| Phishing-Resistant Authentication | Methods designed to resist credential phishing |
| Multifactor Authentication — MFA | Require multiple authentication factors |
| Security Defaults | Baseline Microsoft identity security protections |
| Conditional Access + MFA | Require MFA based on specific conditions |
| Self-Service Password Reset — SSPR | Let users reset passwords without the help desk |
| Account Recovery | Restore access when all normal authentication methods are lost |
| Password Protection | Block weak and commonly attacked passwords |
| Password Spray Protection | Defend against common-password attacks across many accounts |

---

# 1. Authentication

Authentication is the process of verifying:

**Who are you?**

Before Microsoft Entra ID allows access to a:

- Resource
- Application
- Service
- Device
- Network

it verifies that the identity attempting to sign in is legitimate.

### Memory Trick

**Authentication = WHO**

---

# Authentication Factors

Authentication methods generally fall into three categories.

| Factor | Meaning | Examples |
|---|---|---|
| Something you know | Information you know | Password, PIN |
| Something you have | Physical possession | Phone, security key |
| Something you are | Biometric characteristic | Face, fingerprint |

### Memory Trick

**Know — Have — Are**

---

# 2. Passwords

Passwords remain a common authentication method.

However, Microsoft emphasizes that passwords alone have major weaknesses.

Weak passwords are:

- Easy to guess
- Easy to reuse
- Vulnerable to phishing
- Vulnerable to password spray
- Vulnerable if exposed in another breach

Very strong passwords can also:

- Be difficult to remember
- Increase password-reset requests
- Reduce productivity

### Key Concept

Microsoft recommends supplementing or replacing passwords with stronger authentication methods.

---

# 3. Phone Authentication

Microsoft Entra supports phone-based authentication, but Microsoft recommends moving away from SMS and voice toward more modern methods such as:

- Microsoft Authenticator
- Passkeys

---

# SMS Authentication

SMS can be used as:

**Primary authentication**

and as:

**Secondary authentication**

for:

- MFA
- SSPR

Basic process:

1. User enters registered phone number.
2. Microsoft sends a verification code.
3. User enters the code.

### Exam Cue

**SMS = Can be primary OR secondary**

---

# Voice Call Authentication

Voice call verification can be used as a:

**Secondary authentication method**

for:

- MFA
- SSPR

The user receives an automated phone call and confirms the request.

### Important Difference

Voice call is:

**NOT supported as primary authentication**

### Memory Trick

**SMS can start the sign-in**

**Voice cannot**

---

# 4. OATH Tokens

OATH stands for:

**Open Authentication**

OATH can generate:

**Time-Based One-Time Passwords — TOTP**

The code changes periodically.

---

# Software OATH Token

Usually an authentication application.

Examples include:

- Microsoft Authenticator
- Other authenticator apps

A secret key or seed is used to generate the one-time codes.

---

# Hardware OATH Token

A physical device.

Often looks like a:

**Key fob**

It displays a code that changes every:

- 30 seconds
- 60 seconds

---

# OATH Exam Cue

If the question says:

**time-based one-time password**

or

**TOTP**

think:

**OATH**

---

# 5. Other Authentication Methods

Microsoft Entra ID supports several additional authentication methods.

---

# Temporary Access Pass — TAP

A Temporary Access Pass is:

**A time-limited passcode issued by an administrator**

It can help users:

- Sign in initially
- Register authentication methods
- Register passwordless authentication
- Recover access after losing credentials

### Common Scenario

A new employee starts work and has not configured MFA yet.

The administrator gives the employee a:

**Temporary Access Pass**

### Memory Trick

**TAP = Temporary bootstrap credential**

---

# QR Code Authentication

Designed mainly for:

**Frontline workers using shared devices**

The user:

1. Scans a unique QR code.
2. Enters a numeric PIN.

This avoids repeatedly typing long usernames and passwords.

### Exam Cue

**Shared device + frontline worker = QR code authentication**

---

# Email One-Time Passcode — OTP

A verification code sent to the user's email address.

It can be used as a secondary authentication method for:

**SSPR**

It can also support:

**Guest user sign-in**

---

# Platform Credential for macOS

A passwordless, phishing-resistant credential for macOS.

It is backed by the device's:

**Secure Enclave**

It can support:

- Passwordless authentication
- SSO
- Touch ID
- Device password unlock

---

# Authenticator Lite

Authenticator Lite provides authentication features inside applications such as:

**Outlook mobile**

This can allow users to complete MFA without installing the separate Microsoft Authenticator app.

Supports:

- Push notifications
- Time-based one-time passwords

### Memory Trick

**Authenticator Lite = Authenticator functionality inside another Microsoft app**

---

# External Authentication Methods

Organizations can integrate third-party MFA providers with Microsoft Entra ID.

Examples:

- Duo Security
- RSA SecurID

This allows users to satisfy Microsoft Entra MFA requirements using an authentication solution the organization already uses.

---

# 6. Passwordless Authentication

## Big Idea

Passwordless authentication removes the traditional password from the sign-in process.

Instead, authentication can use:

**Something you have**

plus:

**Something you know**

or

**Something you are**

---

# Why Passwordless?

Passwords can be:

- Forgotten
- Phished
- Reused
- Stolen
- Guessed

Passwordless authentication can improve:

**Security**

and

**User experience**

---

# Microsoft Passwordless Methods

Important Microsoft Entra passwordless methods include:

- Windows Hello for Business
- Passkeys — FIDO2
- Microsoft Authenticator
- Certificate-Based Authentication

---

# 7. Windows Hello for Business

Windows Hello for Business replaces passwords with strong authentication tied to a device.

It combines:

**Something you have**

The device

with either:

**Something you know**

PIN

or:

**Something you are**

Biometric

Examples:

- Fingerprint
- Face recognition

---

# Windows Hello Security

The PIN or biometric unlocks a cryptographic credential stored on the device.

The private key:

**Does not leave the device**

### Memory Trick

**Windows Hello = Device + PIN/Biometric**

---

# 8. Passkeys — FIDO2

Passkeys use:

**Public key cryptography**

During registration:

- Public key is registered with Microsoft Entra ID.
- Private key remains securely with the user/device.

Passkeys are based on:

**FIDO2 — Fast Identity Online**

---

# Why Passkeys Are Strong

Passkeys are:

**Phishing resistant**

because they are bound to the legitimate website where they were registered.

A passkey created for:

`login.microsoftonline.com`

cannot simply be reused on a fraudulent look-alike phishing website.

---

# Two Types of Passkeys

## Device-Bound Passkey

Private key remains on:

**One physical device**

Examples:

- FIDO2 USB security key
- Bluetooth security key
- NFC security key
- Passkey stored in Microsoft Authenticator

### Memory Trick

**Device-bound = Stays on one device**

---

## Synced Passkey

Private key is synchronized across a user's devices through a cloud provider.

Examples:

- Apple iCloud Keychain
- Google Password Manager

### Memory Trick

**Synced = Travels across your devices**

---

# 9. Microsoft Authenticator

Microsoft Authenticator supports several authentication scenarios.

---

## Passkey Sign-In

Microsoft Authenticator can store a device-bound passkey.

The user authenticates using:

- Biometric
- Device PIN

---

## Passwordless Sign-In

Instead of entering a password:

1. User enters username.
2. Sign-in page displays a number.
3. User opens Authenticator.
4. User selects/matches the number.
5. User confirms with biometric or PIN.

---

## Push Notification with Number Matching

Used during:

- MFA
- SSPR

The sign-in screen displays a number.

The user must enter that number in Authenticator.

### Why?

This helps reduce:

**MFA fatigue attacks**

---

## OATH Codes

Microsoft Authenticator can also generate:

**OATH verification codes**

---

# 10. Certificate-Based Authentication — CBA

Microsoft Entra Certificate-Based Authentication allows users to authenticate using:

**X.509 certificates**

It provides a cloud-native alternative to some older federated authentication designs.

CBA can support:

**Primary passwordless authentication**

and, when configured:

**Multifactor authentication**

---

# 11. Phishing-Resistant Authentication

Traditional authentication methods such as:

- SMS
- Email codes
- Passwords

can be captured through phishing.

Microsoft recommends phishing-resistant authentication for stronger protection.

---

# Current Microsoft Entra Phishing-Resistant Methods

Microsoft Learn currently identifies:

- Windows Hello for Business
- Platform Credential for macOS
- Synced passkeys — FIDO2
- FIDO2 security keys
- Passkeys in Microsoft Authenticator
- Certificate-Based Authentication

### Core Idea

These methods use cryptography tied to the legitimate site or device.

This makes them difficult to:

- Replay
- Share
- Steal through a fake login page

---

# Phishing-Resistant Memory Sheet

If asked for the strongest modern authentication choices, think:

**Passkeys**

**Windows Hello**

**CBA**

rather than:

**SMS**

or

**Email OTP**

---

# 12. Primary vs. Secondary Authentication

Some authentication methods can begin a sign-in.

Others can only act as an additional verification factor.

---

# Important Current Examples

| Authentication Method | Primary? | Secondary? |
|---|---:|---:|
| Windows Hello for Business | Yes | MFA |
| Platform Credential for macOS | Yes | MFA |
| Passkey — FIDO2 | Yes | MFA |
| Passkey in Microsoft Authenticator | Yes | MFA |
| Synced Passkey | Yes | MFA |
| Certificate-Based Authentication | Yes | MFA |
| Authenticator Passwordless | Yes | No |
| Authenticator Push | Yes | MFA / SSPR |
| Authenticator Lite | No | MFA |
| Hardware OATH | No | MFA / SSPR |
| Software OATH | No | MFA / SSPR |
| External Authentication Method | No | MFA |
| Temporary Access Pass | Yes | MFA |
| SMS Sign-In | Yes | MFA / SSPR |
| Voice Call | No | MFA / SSPR |
| QR Code | Yes | No |
| Email OTP | No | SSPR |
| Password | Yes | No |

Do not try to memorize every table cell immediately.

For SC-900, prioritize recognizing:

- Passwordless methods
- MFA methods
- OATH
- TAP
- SMS vs. voice
- Passkeys
- Authenticator

---

# 13. Multifactor Authentication — MFA

MFA requires:

**Two or more authentication factors**

from different categories.

The categories are:

## Something You Know

Examples:

- Password
- PIN

## Something You Have

Examples:

- Phone
- Security key
- Trusted device

## Something You Are

Examples:

- Fingerprint
- Face

---

# MFA Exam Trap

Password + PIN does NOT necessarily equal true multifactor authentication.

Both are:

**Something you know**

MFA requires factors from different categories.

---

# Why MFA Matters

If an attacker steals a user's password:

Password-only authentication can be compromised.

With MFA, the attacker also needs another factor.

Example:

**Password + physical security key**

---

# Microsoft Entra MFA Verification Methods

Current Microsoft Learn examples include:

- Microsoft Authenticator
- Authenticator Lite
- Windows Hello for Business
- Passkey — FIDO2
- Passkey in Microsoft Authenticator
- Certificate-Based Authentication
- External Authentication Methods
- Temporary Access Pass
- OATH hardware token
- OATH software token
- SMS
- Voice call

---

# 14. Security Defaults

Security defaults are Microsoft's baseline identity-security settings.

They are intended to give organizations:

**Basic protection without complex configuration**

Security defaults are especially useful for:

- Smaller organizations
- Organizations using Entra ID Free
- Organizations without advanced identity-security requirements

---

# Security Defaults Include

## Require MFA Registration

All users must register for MFA.

## Require Administrator MFA

Administrators must use MFA.

## Require MFA When Needed

Users are challenged when Microsoft determines extra verification is needed.

## Block Legacy Authentication

Older authentication protocols that do not support modern security controls are blocked.

## Protect Privileged Activities

Sensitive administrative access receives additional protection.

---

# Important Security Defaults Fact

Security defaults are:

**Enabled by default for new tenants**

---

# Legacy Authentication

Legacy authentication protocols often:

**Do not support MFA**

This makes them a security risk.

### Exam Cue

If a question asks what Microsoft security defaults do with legacy authentication:

**Block it**

---

# MFA Fatigue

MFA fatigue occurs when attackers repeatedly trigger MFA prompts hoping the user eventually approves one.

Microsoft Authenticator:

**Number matching**

helps defend against this attack.

---

# 15. Conditional Access and MFA

Security defaults provide baseline controls.

Organizations needing more precise control use:

**Microsoft Entra Conditional Access**

Conditional Access can require MFA based on conditions such as:

- User
- Location
- Device
- Risk
- Application sensitivity

---

# Example

User signs in from:

**Corporate network + managed device**

Normal authentication may be allowed.

The same user signs in from:

**Unknown country + unmanaged device**

Conditional Access might require:

**MFA**

or block access.

---

# Licensing

Conditional Access requires:

**Microsoft Entra ID P1 or P2**

### Memory Trick

**Free = Security Defaults**

**P1/P2 = Conditional Access**

---

# 16. Self-Service Password Reset — SSPR

SSPR stands for:

**Self-Service Password Reset**

SSPR allows users to:

- Reset forgotten passwords
- Change passwords
- Unlock accounts

without requiring:

- Administrator assistance
- Help desk assistance

---

# Why SSPR Matters

SSPR reduces:

- Help desk workload
- User downtime
- Lost productivity

It also generates audit information that can be sent to a:

**SIEM**

---

# 17. Requirements for SSPR

To use SSPR, a user must:

1. Have an appropriate Microsoft Entra ID license.
2. Be enabled for SSPR by an administrator.
3. Register supported authentication methods.

Microsoft recommends registering:

**Two or more methods**

so users still have another option if one becomes unavailable.

---

# SSPR Memory Trick

**License**

**Enabled**

**Registered**

---

# This Was on Your Practice Assessment

You were asked which actions are required for SSPR.

The correct concepts were:

- Assign an Entra ID license
- Enable SSPR
- Register an authentication method

Creating a custom banned-password list is:

**NOT required for SSPR**

---

# 18. SSPR Authentication Methods

Current Microsoft Learn supports methods including:

- Microsoft Authenticator push notification
- Software OATH token
- Hardware OATH token
- SMS
- Voice call
- Email OTP
- Security questions

---

# Security Questions Retirement

Microsoft currently states that:

**Security questions for SSPR will be retired in March 2027.**

Organizations should migrate users to other authentication methods.

For your October 2026 SC-900 exam:

They still appear in the current Learn material.

---

# Number of SSPR Methods

Administrators can configure users to require:

**One**

or

**Two**

authentication methods to reset or unlock a password.

---

# Administrator Accounts

Administrator accounts have stronger SSPR requirements.

By default, administrators:

**Require two authentication methods**

and:

**Cannot use security questions**

### Memory Trick

**Admins = Two gates**

---

# 19. Registration and Reconfirmation

Organizations can require users to register for SSPR when they sign in.

Users who have not completed registration can continue receiving prompts until they register.

Administrators can also require users to periodically reconfirm their authentication information.

Current Microsoft Learn states the interval can be configured from:

**0 to 730 days**

---

# 20. SSPR Notifications

SSPR can send email notifications.

---

## User Notification

Users can receive an email when:

**Their password is reset**

---

## Administrator Notification

Global administrators can receive an email when:

**Another administrator resets their password using SSPR**

This helps monitor privileged-account activity.

---

# 21. Password Writeback

Hybrid organizations may have users stored in:

**On-premises Active Directory**

and

**Microsoft Entra ID**

When SSPR password writeback is enabled:

A password reset performed in Microsoft Entra ID can be written back to:

**On-premises AD**

---

# Password Writeback Supports

Current Microsoft Learn describes support for users using:

- Federation
- Pass-through authentication
- Password hash synchronization

---

# Password Writeback Memory Trick

**Cloud reset → On-prem password updated**

---

# Account Unlock

Administrators can also allow users to:

**Unlock an on-premises account**

without necessarily:

**Changing the password**

---

# 22. SSPR vs. Account Recovery

This is a newer distinction in the current Microsoft Learn content.

---

# SSPR

Used when:

**The user forgot the password but still has access to at least one registered authentication method**

Example:

User forgot password but still has:

- Authenticator
- Phone
- Security key

---

# Account Recovery

Used when:

**The user has lost access to all normal authentication methods**

Example:

User:

- Lost phone
- Lost security key
- Cannot access registered email
- Does not know password

SSPR alone cannot solve this situation.

---

# SSPR vs. Account Recovery

| SSPR | Account Recovery |
|---|---|
| Forgot password | Lost all authentication methods |
| Uses preregistered methods | Performs identity verification |
| Resets password | Can reset authentication methods |
| Normal recovery | High-assurance identity recovery |

### Memory Trick

**SSPR = I still have one way to prove who I am**

**Account Recovery = I lost everything**

---

# Identity Verification for Account Recovery

Microsoft Entra account recovery can use:

**Identity Verification Providers — IDV**

to establish the user's identity.

Microsoft Learn also describes:

**Microsoft Entra Verified ID with Face Check**

which can compare a live selfie against identification information for stronger identity assurance.

---

# 23. Password Protection

Microsoft Entra Password Protection helps prevent users from choosing:

**Weak passwords**

It uses banned-password lists.

---

# Global Banned Password List

Microsoft maintains a:

**Global banned password list**

It contains commonly used or compromised weak password terms based on Microsoft security telemetry.

Important characteristics:

- Automatically applied
- Applies to all users in the tenant
- Nothing to manually enable
- Cannot be disabled

### Memory Trick

**Global list = Microsoft manages it automatically**

---

# Custom Banned Password List

Organizations can create a custom banned password list for terms specific to their environment.

Examples:

- Company name
- Product name
- Office location
- Internal abbreviation
- Brand name

---

# Example

Company:

**Contoso**

Products:

**ContosoCloud**

Headquarters:

**Seattle**

Those terms could be added to the custom banned-password list.

---

# Custom List Limit

Current Microsoft Learn states:

**Maximum 1,000 custom terms**

The goal is not to upload every bad password imaginable.

Microsoft's fuzzy matching automatically blocks many variations.

---

# Global + Custom Lists

When users change or reset passwords:

Microsoft Entra evaluates the password against:

**Global banned list**

+

**Custom banned list**

---

# 24. How Microsoft Evaluates Passwords

The current Microsoft Learn module explains several stages.

---

# Step 1 — Normalization

Microsoft converts characters into a standardized form.

Examples:

`@` → `a`

`$` → `s`

`1` → `l`

`0` → `o`

This prevents users from bypassing blocked words using obvious character substitutions.

---

# Step 2 — Fuzzy Matching

Microsoft checks variations close to banned words.

This includes:

- One-character substitution
- One-character insertion
- One-character deletion

### ELI5

Changing:

`password`

to:

`passw0rd`

does not magically make it strong.

---

# Step 3 — Substring Matching

Microsoft checks for terms such as:

- User's first name
- User's last name
- Tenant name

Current Microsoft Learn notes this applies to terms at least:

**Four characters long**

---

# Step 4 — Score Calculation

Microsoft calculates a password-strength score.

Current Microsoft Learn states a password must score at least:

**5 points**

to be accepted.

For SC-900, the exact algorithm is less important than understanding:

**Microsoft evaluates variations, names, tenant terms, and overall password strength—not just exact matches.**

---

# 25. Password Spray Attacks

A password spray attack does NOT try thousands of passwords against one user.

Instead:

An attacker tries a few common passwords against:

**Many accounts**

Example:

Try:

`Password123`

against:

- User A
- User B
- User C
- User D
- User E

Then wait and try another common password.

---

# Why Attackers Use Password Spray

Trying many passwords against one account can trigger:

**Account lockout**

Trying a few passwords across many accounts can help attackers avoid lockout thresholds.

---

# Entra Password Protection and Password Spray

Microsoft Entra Password Protection helps defend against password spray because its banned-password lists are informed by:

**Real-world password attack telemetry**

### Exam Cue

**Common passwords against many users = Password spray**

---

# 26. On-Premises Password Protection

Microsoft Entra Password Protection can also protect:

**On-premises Active Directory Domain Services — AD DS**

This uses two major components:

1. Proxy Service
2. DC Agent

---

# Proxy Service

Runs on a domain-joined computer.

It:

- Communicates with Microsoft Entra ID
- Downloads password policies
- Provides policies to domain controllers

### Memory Trick

**Proxy = Bridge to the cloud**

---

# DC Agent

Installed on:

**Domain controllers**

It:

- Receives password validation requests
- Applies Microsoft Entra password-protection rules

### Memory Trick

**DC Agent = Checks the password**

---

# Important Architecture Point

Domain controllers:

**Do NOT need direct internet access**

They communicate through the:

**Proxy Service**

---

# Existing AD Password Policy

Microsoft Entra Password Protection:

**Supplements**

existing AD DS password policy.

It does NOT replace it.

All required password-validation systems must agree before a password is accepted.

---

# Module 2 Exam Quick Reference

| If the Question Mentions... | Think... |
|---|---|
| Verify identity | Authentication |
| Password/PIN | Something you know |
| Phone/security key | Something you have |
| Face/fingerprint | Something you are |
| Two different factor categories | MFA |
| Time-based one-time password | OATH |
| Temporary onboarding credential | TAP |
| Frontline shared device | QR authentication |
| Passwordless Windows login | Windows Hello for Business |
| FIDO2 | Passkey |
| Website-bound credential | Phishing-resistant authentication |
| Number matching | Microsoft Authenticator |
| X.509 certificate | Certificate-Based Authentication |
| Baseline identity protection | Security Defaults |
| New Entra tenant | Security Defaults enabled by default |
| Legacy authentication | Block it |
| Conditional MFA based on risk/location/device | Conditional Access |
| User resets own forgotten password | SSPR |
| SSPR prerequisites | License + enabled + registered method |
| Admin SSPR | Two authentication methods |
| Lost every authentication method | Account Recovery |
| Cloud reset updates AD | Password Writeback |
| Common weak passwords | Global banned-password list |
| Company/product names | Custom banned-password list |
| Same common password against many accounts | Password Spray |
| On-prem Entra password protection | Proxy Service + DC Agent |

---

# Final Module 2 Cram Sheet

## Authentication Factors

**Know = Password / PIN**

**Have = Phone / Key / Device**

**Are = Face / Fingerprint**

---

# MFA

**Two or more different factor categories**

Not:

**Password + PIN**

because both are:

**Something you know**

---

# OATH

**Time-based one-time password — TOTP**

Can be:

**Hardware**

or

**Software**

---

# Passwordless

**Windows Hello = Device + PIN/Biometric**

**FIDO2 Passkey = Public/private key**

**Authenticator = Passwordless + MFA**

**CBA = X.509 certificate**

---

# Phishing Resistant

Think:

**Passkeys**

**Windows Hello**

**Platform Credential for macOS**

**CBA**

---

# TAP

**Temporary administrator-issued passcode**

Useful for:

**Onboarding / Credential recovery**

---

# Security Defaults

**Register MFA**

**Admin MFA**

**User MFA when needed**

**Block legacy authentication**

**Protect privileged activities**

---

# Conditional Access

**IF condition → THEN control**

Examples of conditions:

**Risk**

**Device**

**Location**

**Application**

Can require:

**MFA**

Requires:

**P1 or P2**

---

# SSPR

**Self-Service Password Reset**

Requirements:

**License**

**Enabled**

**Registered authentication method**

Admins:

**Two methods**

---

# SSPR vs. Account Recovery

**SSPR = Forgot password but still have an authentication method**

**Account Recovery = Lost all authentication methods**

---

# Password Writeback

**Cloud password reset → On-prem AD password**

---

# Password Protection

**Global List = Microsoft**

**Custom List = Organization-specific**

Examples:

**Company names**

**Products**

**Locations**

---

# Password Spray

**Few common passwords → Many accounts**

---

# On-Prem Password Protection

**Proxy Service = Cloud communication**

**DC Agent = Password validation**

---

# Final Takeaway

Microsoft Entra authentication is moving away from reliance on passwords toward stronger, passwordless, and phishing-resistant authentication.

For SC-900, the most important distinctions are:

1. **Know / Have / Are**
2. **Single-factor vs. MFA**
3. **Password vs. passwordless**
4. **SMS/OATH vs. phishing-resistant methods**
5. **Security Defaults vs. Conditional Access**
6. **SSPR vs. Account Recovery**
7. **Global vs. Custom banned-password lists**
8. **Password guessing vs. Password Spray**
9. **Cloud-only vs. hybrid password management**

When Microsoft gives you a scenario, first identify:

> Is this an authentication problem, an MFA problem, a password-reset problem, or a password-protection problem?

That usually points directly to the correct Microsoft Entra capability.
