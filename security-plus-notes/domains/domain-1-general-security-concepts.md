# Domain 1 - General Security Concepts

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

### CIA Triad
The three fundamental goals of cybersecurity:

#### Confidentiality
- Ensuring only authorized people can access information.
- Techniques: encryption, access controls, authentication.
- Example: Encrypting sensitive email to prevent eavesdropping.

#### Integrity
- Ensuring data remains accurate and unaltered.
- Techniques: hashing, digital signatures, file permissions.
- Example: A checksum on a downloaded file verifies it wasn't tampered with.

#### Availability
- Ensuring systems and data are accessible when needed.
- Techniques: redundant systems, DDoS protection, backups.
- Example: A redundant pwoer supply keeps a server online during power failures.

---

## Non-Repudiation
- Guarantee that a sender cannot deny having sent a message and the recipient cannot deny having received it.
- Techniques: Digital signatures (proving identity and integrity), logging systems
- Example: An email digitally signed with a private key ensures proof of origin.

---

