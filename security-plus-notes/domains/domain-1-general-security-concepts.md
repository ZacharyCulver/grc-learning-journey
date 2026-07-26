# Domain 1 - General Security Concepts
**Goal of Domain 1:**
Understand core security principles, security controls, risk management basics, cryptography fundamentals, and physical security.
This domain sets the foundation for everything else in cybersecurity.

## *1.1 Security Control Types and Categories* 

**What is a Security Control?**
- A security control is any safeguard or measure that reduces risk to assets.
- Think of it like defenses in a castle: walls, guards, moats, alarms -- all are controls protecting valuables.

**Categories of Controls (by implementation type)**
1. Technical (Logical)
   - Technology-based controls.
   - Examples:
      - Firewalls
      - Anti-virus software
      - Encryption
      - Intrusion Detection Systems (IDS)

2. Administrative (or Managerial)
   - Policies and procedures implemented by humans that must be followed.
   - Examples:
      - Security policies (like Acceptable Use Policy)
      - Hiring practices (background checks)
      - Training programs (security awareness)
    
3. Physical
   - Controls you can physically touch.
   - Examples:
      - Locked doors
      - Security cameras
      - Fences
      - Biometrics at doors (i.e., fingerprint access)
    
---

**Functional Types of Controls**
1. Preventive
   - _Prevents_ an incident before it happens.
   - Examples:
      - Firewalls blocking unauthorized traffic
      - Password policies requiring strong passwords
      - Locked doors

2. Detective
   - _Detects_ an incident as it happens or afterward.
   - Examples:
      - Security alarms
      - Intrusion Detection Systems (IDS)
      - Audit logs

3. Corrective
   - _Fixes_ the damage after an incident.
   - Examples:
      - Backup restoration after ransomware attack
      - Antivirus removing malware
      - Patching a vulnerability after a breach
    
4. Deterrent
   - _Discourages_ attacks by increasing perceived risk.
   - Examples:
      - Warning signs ("This area under surveillance")
      - Visible security guards
    
5. Compensating
   - _Alternative_ controls when the primary control isn't feasible.
   - Examples:
      - If you can't encrypt an old system's hard drive, use strict physical security (locked room) instead
      - Multi-factor authentication (MFA) when full role-based access controls are not feasible by the organization
    
6. Directive
   - _Directs_ people toward correct actions
   - Examples:
      - Signs ("No Tailgating")
      - Security awareness training

---

## *1.2 Core Security Principles* 

**CIA Triad**
- The three fundamental goals of cybersecurity:

**Confidentiality**
- Ensuring only authorized people can access information.
- Techniques: encryption, access controls, authentication.
- Example: Encrypting sensitive email to prevent eavesdropping.

**Integrity**
- Ensuring data remains accurate and unaltered.
- Techniques: hashing, digital signatures, file permissions.
- Example: A checksum on a downloaded file verifies it wasn't tampered with.

**Availability**
- Ensuring systems and data are accessible when needed.
- Techniques: redundant systems, DDoS protection, backups.
- Example: A redundant pwoer supply keeps a server online during power failures.

---

**Non-Repudiation**
- Guarantee that a sender cannot deny having sent a message and the recipient cannot deny having received it.
- Techniques: Digital signatures (proving identity and integrity), logging systems
- Example: An email digitally signed with a private key ensures proof of origin.

---

## *1.3 AAA - Authentication, Authorization, Accounting*

**Authentication**
- Proving who you are. Examples:
   - username + password
   - Biometrics (fingerprint, face)
   - Smartcards
   - OTP (one-time password) apps

MFA (Multi-Factor Authentication) uses two or more different types:
- Something you know (password)
- Something you have (smartcard)
- Something you are (fingerprint)

**Authorization**
- Defining what you can do once authenticated.
- Permissions, rights, access levels
- Example: A user may authenticate into a network but be authorized only to access their own files.

**Accounting**
- Tracking actions.
   - Logging user activies
   - Monitoring access attempts
   - Reviewing logs
- Example: Audit logs showing who logged into the database and when.

**Think:**
* Authentication -- "Who are you?"
* Authorization -- "What can you do?"
* Accounting -- "What _did_ you do?"

---

## *1.4 Security Posture Assessment*

**Gap Analysis**
- Compare current security posture against desired/best practices.
- Find "gaps" (weaknesses).
- Leads to action plans to fix gaps.

**Zero Trust Architecture**
- Principle: Never trust, always verify.
- No implicit trust inside or outside the network.
- Every access request must be authenticated, authorized, and encrypted.

---

## *1.5 Physical Security and Safety*

**Physical Controls:**
- Fences
- Locked doors
- Biometrics (finterprint/face access)
- Mantraps (two doors; traps intruders)
- Bollards (posts preventing vehicle access)
- Surveillance cameras (CCTV)
- Alarm systems
- Access badges

**Environmental Controls:**
- HVAC systems (cool servers)
- Fire suppression (gas-based systems for server rooms)
- Water detection sensors
- Temperature/humidity monitors

**Remember that protecting people, facilities, and equipment is as important as protecting data!**

---

## *1.6 Deception and Disruption Techniques*

**Honeypots and Honeynets**
- Honeypot: A fake system/device to lure attackers.
- Honeynet: A fake network of multiple honeypots.
- Honeyfiles: Fake sensitive files (like "passwords.txt") to detect unauthorized access.

Goal:
- Detects attackers
- Study attack methods
- Waste attacker time

Honeypots = detection + research tools, <u>NOT</u> real asset protection.

---

## *1.7 Change Management*

**Why Change Management?**
Goal: Prevent security incidents caused by careless/uncontrolled changes.

**Change Control Process Steps**
1. Request change.
2. Analyze impact (risk assessment).
3. Get approvals.
4. Test in safe environment.
5. Schedule deployment (usually during low-usage windows).
6. Deploy with rollback plans ready.
7. Document everything.

Real-world example:
A firewall rule change accidentally opens a vulnerable port.
Proper change management would catch this during risk analysis & testing.

---

## *1.8 Basic Cryptographic Solutions*

**Encryption**
- Scrambles data so unauthorized people can't read it.

Two types:

1. Symmetric encryption:
   - Same key used to encrypt and decrypt.
   - Examples: AES, DES
  
2. Asymmetric encryption:
   - Two keys: public and private.
   - Examples: RSA, ECC.
  
**Public Key Infrastructure (PKI)**

Key concepts:
   - Certificates (prove identity)
   - Certificates Authorities (trusted issuers)
   - Certificate Revocation (CRL, OSCP)

**Hashing**
   - One way function to create a unique fingerprint of data.
   - Used for integrity checks.
   - Examples: SHA-256, SHA-3.

**Digital Signatures**
   - Use asymmetric encryption + hashing.
   - They prove:
      - Data integrity
      - Sender authenticity
      - Non-repudiation
    
**Blockchain basics**
   - A decentralized ledger
   - Uses hashing and chaining of blocks
   - Common in cryptocurrency, but useful for tamper-evident systems

---

## *Domain 1 Summary*

- Categories of security controls (technical/logical, admin/managerial, physical)
- Functional types of controls (preventive, detective, corrective, deterrent, compensating, directive)
- CIA triad + non-repudiation
- AAA (authentication, authorization, accounting)
- Zero trust principles
- Physical and environmental security measures
- Honeypots, honeynets, honeyfiles
- Change management process
- Basic cryptography concepts (symmetric/asymmetric encryption, PKI, hashing, digital signatures)
