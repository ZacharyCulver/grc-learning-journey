# SC-900 — Section 3, Module 2
# Describe Core Infrastructure Security Services in Azure

> **Source:** Microsoft Learn — SC-900  
> **Learning Path:** Introduction to Microsoft security solutions  
> **Module:** Describe core infrastructure security services in Azure  
> **Verified against current Microsoft Learn content:** November 23, 2026  
> **Duration:** 29 minutes | 10 units | 1,100 XP  
> **Official Module:** https://learn.microsoft.com/en-us/training/modules/describe-basic-security-capabilities-azure/

---

# Module Overview

Microsoft Azure provides several security services that help organizations protect their cloud infrastructure.

These services protect different parts of an environment, including:

- Network availability
- Network traffic
- Web applications
- Virtual networks and subnets
- Virtual machines
- Passwords, secrets, encryption keys, and certificates

## The Big Idea

**Different Azure security services solve different security problems.**

No single service protects an entire environment.

Organizations combine multiple services to create **defense in depth**.

### ELI5

Imagine protecting a military installation.

One system prevents large crowds from overwhelming the entrance.

Another controls which vehicles can enter or leave.

Another protects a specific facility against specialized attacks.

Other controls divide the installation into restricted areas, manage access to equipment, and safeguard sensitive credentials.

Azure security services work in a similar way.

## The Seven Core Services

| Service | Primary purpose |
|---|---|
| Azure DDoS Protection | Protect service availability against distributed denial-of-service attacks |
| Azure Firewall | Centrally filter network and application traffic |
| Web Application Firewall (WAF) | Protect web applications against common exploits |
| Azure Virtual Network (VNet) | Provide private networking and segmentation |
| Network Security Group (NSG) | Apply network traffic filtering rules |
| Azure Bastion | Provide secure RDP and SSH access to virtual machines |
| Azure Key Vault | Securely manage secrets, encryption keys, and certificates |

### Master Memory Trick

**DDoS = Availability**

**Firewall = Traffic Control**

**WAF = Web Application Protection**

**VNet = Private Network**

**NSG = Network Rules**

**Bastion = Secure VM Access**

**Key Vault = Secrets and Keys**

---

# 1. Azure DDoS Protection

## Big Idea

Azure DDoS Protection helps organizations maintain the availability of applications and services during distributed denial-of-service attacks.

## What Is a DDoS Attack?

**DDoS = Distributed Denial of Service**

A DDoS attack attempts to overwhelm a system with traffic or requests until legitimate users cannot access the service.

### ELI5

Imagine a military installation with one main gate.

Thousands of vehicles arrive simultaneously, creating an enormous traffic jam.

Authorized personnel cannot enter because the gate is overwhelmed.

A DDoS attack does something similar to a network or application.

The attacker wants to make the target unavailable.

## CIA Triad Connection

Recall the three cybersecurity objectives:

| Objective | Meaning |
|---|---|
| Confidentiality | Prevent unauthorized disclosure |
| Integrity | Prevent unauthorized modification |
| Availability | Ensure authorized users can access resources |

DDoS attacks primarily threaten:

**AVAILABILITY**

### Exam Shortcut

**Distributed attack overwhelming a service = DDoS**

---

# 2. Three Major Categories of DDoS Attacks

Microsoft Learn describes three common categories.

## Volumetric Attacks

These attacks overwhelm network bandwidth by generating enormous amounts of traffic.

### Example

An attacker sends large volumes of traffic toward a public-facing application.

The network connection becomes saturated.

Legitimate traffic cannot reach the destination.

**Memory Trick: Volumetric = Too much traffic**

---

## Protocol Attacks

These attacks exploit or exhaust resources associated with network and transport protocols.

Common examples include:

- TCP SYN floods
- Other attacks that exhaust connection-handling resources
- Malicious traffic targeting Layer 3 or Layer 4 operations

### ELI5

Instead of simply sending enormous amounts of data, an attacker abuses how network connections are established or managed.

The server becomes overwhelmed trying to process the requests.

**Memory Trick: Protocol = Abuse network/transport behavior**

---

## Application-Layer Attacks

These attacks target the application itself.

An example is an HTTP flood that overwhelms a website with application requests.

### Important Distinction

The Azure infrastructure DDoS service primarily operates at network Layers 3 and 4.

Application-layer DDoS protection requires appropriate Layer 7 protection, such as Web Application Firewall.

---

# 3. Azure DDoS Protection and the OSI Model

Azure DDoS Protection focuses on:

**Layer 3 — Network**

**Layer 4 — Transport**

Web Application Firewall focuses on:

**Layer 7 — Application**

| OSI layer | Typical concern | Relevant Azure protection |
|---|---|---|
| Layer 3 — Network | Network-layer floods | Azure DDoS Protection |
| Layer 4 — Transport | Protocol and connection floods | Azure DDoS Protection |
| Layer 7 — Application | HTTP floods, SQL injection, XSS | WAF |

### Memory Trick

**DDoS Protection = L3/L4**

**WAF = L7**

These products complement each other.

Neither should be considered a universal defense against every possible attack.

---

# 4. Is Azure DDoS Protection Enabled by Default?

This distinction is particularly important.

## Default Infrastructure Protection

Azure provides baseline infrastructure-level DDoS protection automatically.

Customers receive this underlying protection without separately enabling an enhanced DDoS Protection tier.

However, the baseline service:

- Uses broader platform-level thresholds
- Does not provide application-specific tuning
- Does not provide the enhanced DDoS telemetry and alerting described for paid protection

### ELI5

Azure protects the overall cloud infrastructure against large attacks.

But a volume of traffic that Azure's platform can withstand might still overwhelm a particular customer's application.

---

## Enhanced Azure DDoS Protection

Organizations can enable additional dedicated protection for their resources.

These enhanced offerings provide:

- Application-specific traffic monitoring
- Adaptive mitigation thresholds
- Attack telemetry
- Metrics and alerting
- Additional protection capabilities

### Exam Shortcut

**Baseline infrastructure protection = Automatic**

**DDoS Network Protection = Must be enabled**

---

# 5. Azure DDoS Protection Tiers

Microsoft Learn currently describes two enhanced service tiers.

## DDoS IP Protection

Uses a:

**Pay-per-protected-public-IP model**

This provides core DDoS mitigation capabilities for selected public IP addresses.

It includes core protection engineering but does not include all value-added services available with Network Protection.

### ELI5

Protect specific public IP addresses.

---

## DDoS Network Protection

Designed for protection associated with Azure virtual networks.

It provides enhanced capabilities and value-added services.

Examples include:

- Adaptive DDoS mitigation
- Application-specific traffic profiling
- Monitoring and alerts
- DDoS rapid response assistance
- Additional cost-protection benefits
- Eligible WAF-related discounts

### ELI5

Provide more comprehensive DDoS protection for the organization's virtual network environment.

---

# 6. DDoS Protection Tier Comparison

| Feature | Default infrastructure | IP Protection | Network Protection |
|---|---|---|---|
| Basic infrastructure-level DDoS mitigation | Yes | Yes | Yes |
| Dedicated resource protection | No | Yes | Yes |
| Application-specific traffic tuning | No | Yes | Yes |
| Enhanced attack telemetry | No | Yes | Yes |
| Alerting and analytics | Not included | Yes | Yes |
| DDoS Rapid Response team | No | No | Yes |
| Enhanced cost-protection benefits | No | No | Yes |

### Memory Trick

**Default = Infrastructure baseline**

**IP Protection = Specific public IPs**

**Network Protection = VNet-focused enhanced protection**

---

# 7. Azure DDoS Protection Capabilities

## Always-On Traffic Monitoring

Azure continuously monitors traffic patterns associated with protected resources.

When an attack is detected, the service can automatically mitigate malicious traffic.

Legitimate traffic is forwarded toward its intended destination.

---

## Adaptive Real-Time Tuning

The service learns normal application traffic patterns.

Protection thresholds can adjust as traffic changes.

### ELI5

A normal traffic level for a small business website may be very different from that of a major online retailer.

Adaptive tuning helps distinguish the application's expected traffic from abnormal attacks.

---

## Attack Analytics

Azure DDoS Protection provides information about detected attacks.

The current module describes:

- Reports at five-minute intervals during attacks
- Post-attack summary reports
- Mitigation flow logs
- Attack metrics
- Alerting capabilities

## Azure Monitor Integration

Azure Monitor can collect DDoS-related metrics and generate alerts.

Logs can also be integrated with services such as:

- Azure Monitor Logs
- Azure Event Hubs
- Azure Storage
- Microsoft Sentinel

### GRC Connection

Attack logs and mitigation reports can support incident investigations, security monitoring, and compliance evidence.

---

# 8. DDoS Rapid Response

Organizations using DDoS Network Protection can access Microsoft's:

**DDoS Rapid Response (DRR) team**

DRR specialists can assist with:

- Investigating an active attack
- Understanding mitigation activity
- Supporting the response to complex attacks
- Conducting post-attack analysis

### Important Distinction

Automated DDoS mitigation and expert response assistance are related but separate capabilities.

---

# 9. DDoS Protection: Three Exam Traps

These are especially relevant because they resemble the DDoS questions encountered during your SC-900 exam.

## Does Azure DDoS Protection prevent Man-in-the-Middle attacks?

**No.**

A Man-in-the-Middle (MitM) attack involves intercepting or manipulating communication between parties.

Controls such as proper TLS certificate validation and secure communications help protect against MitM attacks.

DDoS Protection primarily protects availability.

---

## Is DDoS Network Protection enabled automatically?

**No.**

Azure provides baseline infrastructure protection by default.

Enhanced Network Protection must be enabled and configured.

---

## Does Azure DDoS Protection mitigate protocol attacks?

**Yes.**

Protocol attacks targeting Layers 3 and 4 fall within the service's protection scope.

### Remember

**MitM = Interception**

**DDoS = Availability**

**Protocol Flood = DDoS Protection**

**HTTP Application Flood = Layer 7 / WAF**

---

# 10. Azure Firewall

## Big Idea

Azure Firewall is a:

**Managed, cloud-based, stateful network security service.**

It helps organizations centrally control network and application traffic.

### ELI5

Imagine a security checkpoint controlling traffic entering and leaving a military installation.

Personnel can configure rules defining:

- Which sources are permitted
- Which destinations are permitted
- Which ports and protocols may be used
- Which destinations should be blocked

Azure Firewall performs comparable filtering for Azure network traffic.

---

# 11. Stateful Firewall

A stateful firewall tracks information about active network connections.

This helps it evaluate traffic in the context of an established communication session.

### Example

An internal resource initiates an authorized connection to an external service.

The firewall tracks the connection and can recognize legitimate return traffic.

### Memory Trick

**Stateful = Remembers connection state**

---

# 12. Azure Firewall Capabilities

## Centralized Network Protection

Azure Firewall can be deployed in a central virtual network.

Traffic from other virtual networks and connected on-premises networks can be routed through it.

This allows an organization to manage traffic filtering from a centralized point.

### ELI5

Instead of maintaining separate security checkpoints for every building, establish a central checkpoint through which selected traffic flows.

---

## Built-In High Availability

Azure Firewall is designed for high availability.

It can also use availability zones to improve resilience.

An availability zone is a physically separate datacenter grouping within an Azure region.

---

## Network-Level Filtering

Rules can evaluate properties such as:

- Source IP address
- Destination IP address
- Port
- Protocol

### Example

Allow authorized administrative traffic to a designated service while blocking unwanted connections.

---

## Application-Level Filtering

Azure Firewall supports application rules involving supported protocols and destinations.

A key capability is filtering based on:

**Fully Qualified Domain Names — FQDNs**

Example:

```text
updates.contoso.com
```

### Exam Concept

**Centralized network filtering + application destination filtering = Azure Firewall**

---

# 13. Network Address Translation — NAT

Azure Firewall supports:

**Source Network Address Translation (SNAT)**

and:

**Destination Network Address Translation (DNAT)**

## SNAT

Changes the source IP address.

### Example

A virtual machine with a private IP address accesses the internet.

The firewall translates the source address to an appropriate public IP.

**SNAT = Change the source address**

---

## DNAT

Changes the destination IP address.

### Example

Traffic arrives at a public-facing address.

The firewall translates the destination to a private resource behind the firewall.

**DNAT = Change the destination address**

---

# 14. Azure Firewall Threat Intelligence

Azure Firewall can integrate with Microsoft threat intelligence.

It can identify traffic involving known malicious:

- IP addresses
- Domains

Supported configurations can alert or deny matching traffic.

### Important Distinction

**Threat intelligence = Information about known threats**

**Firewall enforcement = Apply traffic filtering using configured rules**

---

# 15. Azure Firewall Tiers

Microsoft Learn currently identifies three Azure Firewall tiers.

## Basic

Designed for smaller environments with simpler security requirements.

The module describes:

- Essential firewall protection
- Fixed-scale backend
- Threat intelligence in alert mode
- Approximately 250 Mbps recommended throughput scenario

## Standard

Provides broader enterprise firewall capabilities.

The module identifies:

- Layer 3 through Layer 7 filtering
- Microsoft threat intelligence integration
- Alerting and blocking of known malicious destinations
- Suitable enterprise network protection

## Premium

Adds advanced security capabilities for sensitive environments.

The module emphasizes:

**Intrusion Detection and Prevention System — IDPS**

IDPS uses signatures to detect and help prevent certain attack patterns.

Examples include threats associated with:

- Malware
- Exploits
- Suspicious traffic
- Known malicious patterns

### Memory Trick

**Basic = Essential**

**Standard = Enterprise filtering**

**Premium = Advanced IDPS protection**

---

# 16. Azure Firewall Manager

Azure Firewall Manager provides centralized management of multiple Azure Firewall deployments.

Organizations can use it to apply common firewall policies across:

- Virtual networks
- Azure subscriptions
- Multiple regions
- Virtual WAN environments

### ELI5

Instead of separately configuring every firewall, an organization can manage shared policies centrally.

**Firewall = Enforces traffic rules**

**Firewall Manager = Centrally manages firewall policies**

---

# 17. Azure Firewall and Security Copilot

The current Microsoft Learn module describes integration with Microsoft Security Copilot.

Security Copilot can assist analysts in investigating supported Azure Firewall security information through natural-language prompts.

For this integration, the module discusses requirements such as:

- Appropriate structured firewall logs
- A Log Analytics workspace
- Appropriate Azure RBAC permissions
- An enabled Azure Firewall plugin

### Example

An analyst asks Security Copilot to help investigate suspicious traffic detected by Azure Firewall.

Copilot analyzes information available through the configured integration.

### Important Distinction

**Azure Firewall blocks or filters traffic.**

**Security Copilot helps analyze firewall-related security information.**

---

# 18. Web Application Firewall — WAF

## Big Idea

A Web Application Firewall protects web applications against common application-layer attacks.

It works at:

**OSI Layer 7 — Application**

### ELI5

A traditional network firewall checks where traffic comes from and where it is going.

A WAF examines requests targeting web applications to identify malicious behavior.

A WAF understands web attack patterns that ordinary network filtering rules might not detect.

---

# 19. Common Attacks WAF Protects Against

## SQL Injection — SQLi

An attacker places malicious SQL instructions into application input.

The goal may be to:

- Access information
- Modify database records
- Delete records
- Bypass application security controls

### Exam Shortcut

**Malicious SQL in application input = WAF**

---

## Cross-Site Scripting — XSS

An attacker injects malicious scripts into web content that another user views.

Possible effects include:

- Session theft
- Credential theft
- Unauthorized actions
- Exposure of sensitive information

### Memory Trick

**XSS = Malicious script in web content**

---

## HTTP Floods

An attacker sends excessive HTTP requests to overwhelm a web application.

This is an application-layer DDoS attack.

### Important Distinction

**Network/transport flood = Azure DDoS Protection**

**HTTP application flood = WAF protection**

---

## Remote File Inclusion — RFI

An attacker manipulates a web application into including or executing a malicious remote file.

A WAF can help detect and block known attack patterns.

---

# 20. OWASP and WAF

**OWASP = Open Worldwide Application Security Project**

OWASP publishes widely used web application security resources.

WAF implementations can use managed rule sets based on OWASP attack-detection rules.

### Important Concept

A WAF helps protect applications from common web exploits.

However, a WAF does not eliminate the need for:

- Secure coding
- Application patching
- Vulnerability management
- Secure configuration
- Appropriate monitoring

**WAF is a security layer, not a replacement for application security.**

---

# 21. Azure WAF Deployment Options

The current Microsoft Learn module identifies four deployment options.

## Azure Application Gateway

Provides regional web application protection.

Useful for applications that need Layer 7 routing and WAF capabilities within an Azure region.

## Azure Application Gateway for Containers

Provides application delivery and WAF capabilities for supported containerized workloads.

## Azure Front Door

Provides global application delivery and WAF capabilities.

It can help protect globally distributed web applications closer to the origin of malicious traffic.

## Azure Content Delivery Network — CDN

The module also identifies Azure CDN as a supported WAF deployment option.

### Memory Trick

**Application Gateway = Regional**

**Front Door = Global**

**WAF = Application attack protection**

---

# 22. WAF and Security Copilot

The current module describes Microsoft Security Copilot integration with Azure WAF.

Security Copilot can assist with:

- Investigating WAF events
- Analyzing supported WAF logs
- Understanding attack patterns
- Summarizing related security findings

An enabled and configured Azure WAF plugin is required.

### Distinction

**WAF = Detect and block supported web attacks**

**Security Copilot = Assist analysis of WAF findings**

---

# 23. Azure Firewall vs. WAF vs. DDoS Protection

This is one of the most important comparisons in the entire module.

| Service | Primary protection | Typical scenario |
|---|---|---|
| Azure Firewall | Centralized network and application traffic filtering | Control access by IP, port, protocol, or supported application destination |
| WAF | Web application attacks | Block SQL injection or XSS |
| Azure DDoS Protection | Network and transport availability | Mitigate network floods or protocol attacks |

### Practical Example

A company hosts a public-facing online application.

It might use:

**Azure DDoS Protection** to help mitigate network floods.

**Azure Firewall** to filter appropriate network traffic.

**WAF** to protect the website from common application-layer attacks.

These services can work together.

---

# 24. Network Segmentation in Azure

## Big Idea

Network segmentation means dividing a network into smaller, controlled sections.

Organizations use segmentation to:

- Group related resources
- Isolate sensitive systems
- Apply different security policies
- Reduce the impact of compromised systems
- Limit unauthorized lateral movement

### ELI5

Imagine dividing a military installation into separate areas:

- Motor pool
- Headquarters
- Barracks
- Communications facility
- Ammunition storage

Not every person or vehicle should have unrestricted access to every area.

Network segmentation applies comparable boundaries to digital resources.

---

# 25. Network Segmentation and Zero Trust

Segmentation supports the Zero Trust principle:

**Assume Breach**

Organizations should not assume that everything inside a network is trustworthy.

If one system becomes compromised, segmentation can help prevent an attacker from moving freely to unrelated systems.

### Lateral Movement

Lateral movement occurs when an attacker moves from one system or resource to another after gaining an initial foothold.

### Security Benefit

Segmentation can reduce the attacker's ability to move throughout the environment.

**Memory Trick: Segmentation = Contain the breach**

---

# 26. Azure Virtual Network — VNet

## Big Idea

An Azure Virtual Network is the fundamental building block of private networking in Azure.

A VNet is a logically isolated network environment in which Azure resources can communicate.

### ELI5

A VNet is like creating a private organizational network in Microsoft Azure.

You decide how the network is organized and which resources can communicate.

---

# 27. VNet Capabilities

An Azure VNet supports:

## Communication Between Azure Resources

Resources in the same VNet can communicate using private networking.

## Internet Communication

Resources can communicate with internet destinations, subject to their networking configuration and applicable rules.

Public inbound access requires appropriate exposure and configuration.

## On-Premises Connectivity

VNets can connect to on-premises environments through services including:

- Site-to-site VPN
- Point-to-site VPN
- Azure ExpressRoute

## Traffic Filtering

VNets can use:

- Network Security Groups
- Azure Firewall

to control traffic.

## Traffic Routing

Azure provides routing between network resources.

Organizations can also configure custom routing rules.

---

# 28. VNet vs. VPN

These are different concepts.

## VNet

The private network environment inside Azure.

## VPN

A method for creating an encrypted network connection between locations or clients.

### Example

An organization operates a datacenter and an Azure VNet.

A site-to-site VPN can securely connect the on-premises network to the Azure VNet.

### Memory Trick

**VNet = The network**

**VPN = A secure connection to a network**

---

# 29. Azure Subnets

A **subnet** is a smaller network segment inside a VNet.

Organizations can use subnets to divide resources by purpose.

### Example

```text
Azure Virtual Network
│
├── Web Subnet
│   └── Web Servers
│
├── Application Subnet
│   └── Application Servers
│
└── Database Subnet
    └── Database Servers
```

Security rules can control communication between segments.

### Practical Scenario

Web servers must communicate with application servers.

Application servers need limited database access.

Web servers should not directly access the database subnet unless specifically required.

Subnet-level controls can enforce these requirements.

### Memory Trick

**VNet = Entire private network**

**Subnet = Section inside the network**

---

# 30. VNet Peering

**VNet peering** connects two Azure virtual networks.

Peered networks can communicate through Microsoft's Azure backbone network.

This does not require sending the traffic over the public internet.

## Global VNet Peering

Connects virtual networks located in different Azure regions.

### ELI5

Two private Azure networks need to communicate.

Peering establishes a connection between them.

### Important Detail

Peering does not automatically eliminate all traffic restrictions.

Routing, security rules, and other network controls still matter.

### Memory Trick

**VNet Peering = Connect two VNets**

---

# 31. Network Security Groups — NSGs

## Big Idea

Network Security Groups filter inbound and outbound network traffic associated with Azure resources.

NSGs use security rules.

Rules determine whether traffic should be:

**ALLOWED**

or

**DENIED**

### ELI5

An NSG is like a traffic-control checklist for a subnet or network interface.

The rules might say:

> Allow this connection.

> Deny that connection.

> Permit communication using a particular port.

---

# 32. Where Can NSGs Be Applied?

NSGs can be associated with:

- Azure subnets
- Network interfaces (NICs)

A subnet or network interface can have one associated NSG.

The same NSG can be reused across multiple subnets or interfaces.

### Exam Shortcut

**Subnet/NIC traffic filtering = NSG**

---

# 33. NSG Rule Properties

An NSG rule can evaluate several properties.

| Property | Purpose |
|---|---|
| Name | Identify the rule |
| Priority | Determine processing order |
| Source | Where traffic originates |
| Source port | Port used by the source |
| Destination | Where traffic is going |
| Destination port | Target port |
| Protocol | TCP, UDP, ICMP, or Any |
| Direction | Inbound or outbound |
| Action | Allow or deny |

Rules can use IP addresses, ranges, service tags, and application security groups.

---

# 34. NSG Rule Priority

This is a high-value exam concept.

**LOWER priority numbers are processed FIRST.**

Example:

```text
Priority 100 — Allow TCP 443
Priority 200 — Deny TCP 443
Priority 300 — Allow TCP 80
```

If matching traffic satisfies the rule with priority 100, Azure applies that rule.

It does not continue evaluating lower-priority rules for that traffic.

### ELI5

Think of an ordered list of instructions.

Azure reads the first matching instruction and follows it.

### Memory Trick

**Smaller number = Higher priority**

---

# 35. Worked NSG Priority Scenario

An administrator configures:

| Priority | Rule | Action |
|---|---|---|
| 100 | TCP 443 from approved subnet | Allow |
| 200 | TCP 443 from any source | Deny |
| 300 | TCP 80 from any source | Allow |

## Scenario A

An approved system connects using TCP port 443.

The traffic matches priority 100.

**Result: Allowed**

## Scenario B

An unapproved system connects using TCP port 443.

It does not match priority 100.

It matches priority 200.

**Result: Denied**

## Scenario C

An unapproved system connects using TCP port 80.

It does not match the TCP 443 rules.

It matches priority 300.

**Result: Allowed**

### Important Concept

**Rules are evaluated in priority order until a match is found.**

---

# 36. Default NSG Rules

Azure creates default inbound and outbound rules.

There are three default inbound rules and three default outbound rules.

These rules cannot be removed, but custom rules with higher priority can override their behavior.

## Default Inbound Rules

| Rule | Purpose |
|---|---|
| AllowVNetInBound | Allow traffic from the VirtualNetwork service tag |
| AllowAzureLoadBalancerInBound | Allow Azure Load Balancer traffic |
| DenyAllInBound | Deny remaining inbound traffic |

## Default Outbound Rules

| Rule | Purpose |
|---|---|
| AllowVNetOutBound | Allow traffic within the VirtualNetwork service tag |
| AllowInternetOutBound | Allow outbound internet traffic |
| DenyAllOutBound | Deny remaining outbound traffic |

### Important Distinction

Default inbound rules are more restrictive regarding internet-originated traffic.

Default outbound rules allow certain outbound connections unless overridden.

---

# 37. Service Tags

A service tag represents a group of Azure-related IP address prefixes.

Instead of manually maintaining many individual IP addresses, administrators can reference an appropriate service tag in network rules.

### ELI5

Instead of writing a long list of IP addresses, use a Microsoft-maintained label representing a defined group of addresses.

---

# 38. Application Security Groups — ASGs

An **Application Security Group** helps administrators organize virtual machines based on application roles.

Examples:

- WebServers
- AppServers
- DbServers

### Example

```text
Application Security Groups
│
├── WebServers
├── AppServers
└── DbServers
```

NSG rules can then reference those groups.

### Why This Matters

If a new application server is deployed, it can be added to the AppServers group.

Existing rules referencing the group can apply without manually adding the server's individual IP address.

### Memory Trick

**ASG = Group resources by application role**

**NSG = Apply network filtering rules**

---

# 39. NSG vs. Azure Firewall

These services overlap in some capabilities but have different purposes.

## NSG

Provides distributed network traffic filtering at subnet and NIC boundaries.

Useful for local network segmentation and controlled resource access.

## Azure Firewall

Provides centralized, stateful network and application-level filtering.

Useful for broader traffic inspection and control across VNets and subscriptions.

| NSG | Azure Firewall |
|---|---|
| Distributed traffic filtering | Centralized firewall service |
| Subnet or NIC association | Centrally deployed and routed through |
| IP, port, protocol rules | Network and application rules |
| Allow/deny controls | Stateful filtering, NAT, threat intelligence |
| Supports network segmentation | Supports broader network protection |

### Important Principle

**NSG and Azure Firewall can be used together.**

This is defense in depth.

---

# 40. Azure Bastion

## Big Idea

Azure Bastion provides secure remote access to Azure virtual machines.

It supports:

**Remote Desktop Protocol — RDP**

and

**Secure Shell — SSH**

without requiring a public IP address on the target VM.

### ELI5

An administrator needs to manage a server remotely.

Traditionally, they might expose a management port to the internet.

That increases the attack surface.

Azure Bastion provides a managed access point so the administrator can connect without exposing those management ports directly.

---

# 41. Why Exposed RDP and SSH Ports Are Risky

Common remote administration protocols include:

| Protocol | Typical purpose | Common port |
|---|---|---|
| RDP | Remote graphical desktop | TCP 3389 |
| SSH | Secure command-line access | TCP 22 |

Exposing these services directly to the internet increases opportunities for:

- Port scanning
- Credential attacks
- Exploitation attempts
- Unauthorized remote access

Azure Bastion reduces the need to expose these management ports publicly.

---

# 42. How Azure Bastion Works

Azure Bastion is a:

**Fully managed Platform-as-a-Service (PaaS) offering**

It is deployed within an Azure VNet.

Administrators can connect through the Azure portal using a browser-based interface.

The connection uses:

**Transport Layer Security — TLS**

The current module describes browser connections using HTTPS/TLS on port 443.

### Simplified Flow

```text
Administrator
      |
      | HTTPS / TLS
      v
Azure Portal / Bastion
      |
      | Private RDP or SSH connection
      v
Azure Virtual Machine
      |
      └── No public IP required on VM
```

### Memory Trick

**Bastion = Secure bridge to a VM**

---

# 43. Azure Bastion Benefits

## No Public IP Required on the VM

The administrator connects to the VM through its private IP.

## Secure Browser-Based Access

Administrators can open remote sessions through the Azure portal.

## No Agent Required on the Target VM

The VM does not need a special Bastion agent.

## Reduced Public Management Exposure

RDP and SSH do not need to be exposed directly to the internet.

## Managed Service

Microsoft manages and maintains the Bastion service infrastructure.

## VNet-Based Deployment

Bastion supports access to VMs in the deployed VNet and supported peered VNets.

---

# 44. Azure Bastion Tiers

The current module identifies four service tiers.

## Developer

- Free shared infrastructure
- Development and testing
- One VM connection at a time
- Limited regional availability

## Basic

- Dedicated deployment
- Core Bastion capabilities
- Suitable for production environments with moderate needs

## Standard

Includes additional capabilities such as:

- Scaling options
- Native client support
- Shareable links
- Custom ports
- File transfer
- IP-based connection capabilities

## Premium

Adds advanced features including:

- Session recording
- Private-only deployment
- Enhanced suitability for stringent security and compliance requirements

### Memory Trick

**Developer = Testing**

**Basic = Core access**

**Standard = Advanced connectivity**

**Premium = Recording and private-only deployment**

---

# 45. Bastion vs. PIM vs. VPN

These concepts are different.

| Capability | Main purpose |
|---|---|
| Azure Bastion | Secure remote VM administration |
| Microsoft Entra PIM | Time-limited privileged role activation |
| VPN | Encrypted connection between network endpoints |

### Scenario

An administrator needs temporary elevated Azure permissions to manage a VM.

PIM can govern activation of the relevant privileged role.

Bastion can provide secure RDP or SSH connectivity to the VM.

Both capabilities can be used together.

### Memory Trick

**PIM = WHEN you can exercise privileges**

**Bastion = HOW you securely connect to a VM**

---

# 46. Azure Key Vault

## Big Idea

Azure Key Vault is a cloud service for securely storing and managing:

**Secrets**

**Cryptographic Keys**

**Certificates**

### ELI5

An application needs a password or API key to communicate with another system.

Instead of placing that credential inside the application's source code, the organization stores it in a secure vault.

Authorized applications retrieve it when needed.

This reduces the risk of accidentally exposing credentials.

---

# 47. Secrets Management

A **secret** is sensitive information that must be protected.

Examples include:

- Passwords
- API keys
- Authentication tokens
- Connection strings

### Example

An application requires database credentials.

Rather than storing the credentials directly in application code, the developer stores them in Azure Key Vault.

The application retrieves the secret using appropriate authentication and authorization.

### Security Benefit

Secrets can be managed centrally and access can be restricted.

---

# 48. Cryptographic Key Management

Azure Key Vault can store and manage cryptographic keys.

These keys support operations involving data encryption and other cryptographic functions.

### ELI5

Encryption protects information.

Cryptographic keys determine how protected information can be encrypted or decrypted.

Key management controls who can use those keys.

### Important Distinction

**Encryption = Protect the data**

**Key Vault = Securely manage the keys and related secrets**

---

# 49. Certificate Management

Azure Key Vault can manage supported certificates.

Certificates are used in scenarios such as:

- TLS/SSL communications
- Server identity verification
- Secure application connections
- Certificate lifecycle management

Key Vault can help automate supported certificate-management operations, including renewal.

### Memory Trick

**Secret = Sensitive value**

**Key = Cryptographic material**

**Certificate = Digital identity/trust credential**

---

# 50. Why Use Azure Key Vault?

## Centralized Storage

Keep sensitive information in controlled locations rather than distributing secrets across multiple applications.

## Authentication and Authorization

Require appropriate identity verification and permissions.

## Logging and Monitoring

Monitor access to secrets, keys, and certificates.

## High Availability

Azure provides replication and resilience capabilities.

## Secret Separation

Different applications can be restricted to the secrets and operations they require.

## Zero Trust

Key Vault supports:

**Verify Explicitly**

and

**Use Least-Privilege Access**

---

# 51. Key Vault Authentication vs. Authorization

These concepts reinforce earlier SC-900 material.

## Authentication

Determines:

**Who are you?**

Azure Key Vault uses Microsoft Entra ID for authentication.

## Authorization

Determines:

**What are you allowed to do?**

Key Vault supports authorization through:

- Azure Role-Based Access Control (Azure RBAC)
- Key Vault access policies

### Example

An application authenticates through Microsoft Entra ID.

Key Vault checks whether the application's identity has permission to retrieve the requested secret.

### Memory Trick

**Entra ID = Authenticate the caller**

**Azure RBAC / Access Policy = Authorize the operation**

---

# 52. Key Vault and Least Privilege

Suppose an application needs to read one secret.

It should not automatically receive permission to:

- Delete every secret
- Modify unrelated keys
- Manage all certificates
- Administer the entire vault

Permissions should be limited to the application's actual operational needs.

### GRC Connection

This reflects:

**Least Privilege**

and

**Separation of Duties**

The organization should avoid giving unnecessary authority to identities or applications.

---

# 53. Azure Key Vault Integrations

The current Microsoft Learn module identifies several Azure integrations.

## Azure Disk Encryption

Supports management of keys used for virtual machine disk encryption scenarios.

## Azure SQL Database and SQL Server

Supports key management for supported database encryption scenarios.

## Azure App Service

Applications can retrieve sensitive connection information and secrets at runtime.

## Certificate Management

Supports certificate provisioning, management, and automated renewal for supported certificate scenarios.

---

# 54. Azure Key Vault Tiers

Microsoft Learn describes two tiers.

## Standard

Uses software-protected keys.

Appropriate for typical business scenarios.

## Premium

Provides:

**Hardware Security Module — HSM**

protected keys.

### What Is an HSM?

An HSM is a specialized hardware device designed to securely generate, protect, and perform operations involving cryptographic keys.

It provides stronger hardware-based protection for certain cryptographic operations.

### Memory Trick

**Standard = Software-protected keys**

**Premium = HSM-protected keys**

---

# 55. Key Vault vs. HSM

An HSM is not simply another name for Azure Key Vault.

**Azure Key Vault** is the cloud service.

**HSM** describes specialized hardware-based cryptographic protection.

Azure Key Vault Premium provides HSM-protected key capabilities.

### Important Concept

Organizations with demanding cryptographic security and compliance requirements may need HSM-based protection.

---

# 56. Infrastructure Security: Complete Scenario

Imagine a company deploying a three-tier business application in Azure.

The application contains:

- Public web servers
- Internal application servers
- Database servers
- Stored application credentials

The company wants strong infrastructure protection.

## Step 1 — Create the Network

Use an:

**Azure Virtual Network**

## Step 2 — Divide Resources

Create separate:

**Subnets**

for web, application, and database workloads.

## Step 3 — Control Traffic Between Segments

Use:

**Network Security Groups**

to enforce permitted traffic patterns.

## Step 4 — Centrally Control Network Traffic

Use:

**Azure Firewall**

for centralized network/application filtering.

## Step 5 — Protect the Public Application

Use:

**Web Application Firewall**

against supported web attack patterns.

## Step 6 — Protect Availability

Use:

**Azure DDoS Protection**

to help defend against network and transport floods.

## Step 7 — Provide Secure Administration

Use:

**Azure Bastion**

for secure RDP and SSH connections to virtual machines.

## Step 8 — Protect Secrets

Use:

**Azure Key Vault**

for passwords, API keys, cryptographic keys, and certificates.

### Final Architecture

```text
                 INTERNET
                     |
                     v
           Azure DDoS Protection
                  (L3/L4)
                     |
                     v
          Web Application Firewall
                    (L7)
                     |
                     v
           Azure Virtual Network
                     |
          +----------+----------+
          |          |          |
          v          v          v
      Web Subnet  App Subnet  DB Subnet
          |          |          |
       NSG Rules   NSG Rules  NSG Rules
          |          |          |
          +----------+----------+
                     |
              Azure Firewall
          (Centralized traffic control)

      Azure Bastion
          |
          +--> Secure VM administration

      Azure Key Vault
          |
          +--> Secrets, keys, certificates
```

**Note:** This is a conceptual diagram showing the role of each service, not a prescribed Azure network deployment or exact traffic-routing topology.

The important concept is that multiple controls address different threats.

---

# 57. The Most Common Exam Confusions

## DDoS Protection vs. WAF

**DDoS Protection = Network and transport availability**

**WAF = Web application protection**

---

## Azure Firewall vs. NSG

**Azure Firewall = Centralized managed firewall**

**NSG = Subnet/NIC traffic filtering**

---

## VNet vs. VPN

**VNet = Private network**

**VPN = Encrypted network connection**

---

## VNet vs. Subnet

**VNet = Entire Azure private network**

**Subnet = Segment inside that VNet**

---

## NSG vs. ASG

**NSG = Filtering rules**

**ASG = Logical grouping of application resources**

---

## Bastion vs. PIM

**Bastion = Secure remote connection**

**PIM = Govern privileged role activation**

---

## Key Vault vs. Encryption

**Encryption = Cryptographic protection**

**Key Vault = Management of keys and secrets**

---

## Key Vault Standard vs. Premium

**Standard = Software-protected keys**

**Premium = HSM-protected keys**

---

# 58. GRC / ISSO Career Connection

The following section provides additional career context rather than reproducing a separate Microsoft Learn unit.

Understanding these services helps an ISSO evaluate whether an organization's infrastructure security controls are appropriately designed and operating.

## NIST SP 800-53 Relationships

These are illustrative control relationships, not claims that deploying a service automatically satisfies the control.

| Azure capability | Related NIST SP 800-53 control | Security objective |
|---|---|---|
| DDoS Protection | SC-5 — Denial-of-Service Protection | Maintain availability |
| Azure Firewall | SC-7 — Boundary Protection | Control communications at boundaries |
| NSGs | AC-4 — Information Flow Enforcement | Enforce permitted traffic flows |
| Network Segmentation | SC-7 — Boundary Protection | Separate security domains |
| Azure Bastion | AC-17 — Remote Access | Control remote administrative access |
| Azure Key Vault | SC-12 — Cryptographic Key Establishment and Management | Protect cryptographic keys |
| Firewall and DDoS Logs | AU-2 — Event Logging | Support security monitoring and accountability |

### Example ISSO Questions

**DDoS Protection**

Does the organization have appropriate protection for internet-facing critical services?

**Azure Firewall**

Are network traffic rules reviewed and approved?

**NSGs**

Are subnets properly isolated, and are unnecessary ports blocked?

**Azure Bastion**

Are remote administrative connections protected from direct public exposure?

**Azure Key Vault**

Are secrets and cryptographic keys restricted to authorized users and applications?

**Monitoring**

Are security events being logged, retained, and investigated?

### Practical GRC Principle

**Deploying a security tool does not automatically establish compliance.**

An assessor must verify:

- Configuration
- Scope of protection
- Assigned responsibilities
- Operating effectiveness
- Monitoring
- Supporting evidence

---

# 59. SC-900 Exam Quick Reference

| If the question mentions... | Think... |
|---|---|
| Distributed network flood | Azure DDoS Protection |
| Layer 3 and Layer 4 attack | Azure DDoS Protection |
| Protocol exhaustion | Azure DDoS Protection |
| Automatically included baseline protection | Azure infrastructure DDoS protection |
| Enhanced virtual network DDoS protection | DDoS Network Protection |
| Pay-per-protected-public-IP | DDoS IP Protection |
| DDoS incident expert assistance | DDoS Rapid Response |
| SQL injection | WAF |
| Cross-site scripting | WAF |
| HTTP flood | WAF |
| OWASP rules | WAF |
| Regional WAF deployment | Azure Application Gateway |
| Global WAF deployment | Azure Front Door |
| Centralized stateful firewall | Azure Firewall |
| SNAT/DNAT | Azure Firewall |
| Threat intelligence traffic filtering | Azure Firewall |
| Premium intrusion detection/prevention | Azure Firewall Premium |
| Central firewall policy management | Azure Firewall Manager |
| Azure private network | VNet |
| Smaller network segment | Subnet |
| Connect two VNets | VNet Peering |
| Encrypted on-premises network connection | VPN |
| Filter subnet traffic | NSG |
| Filter network interface traffic | NSG |
| Lower-numbered rule evaluated first | NSG priority |
| Organize VMs by application role | ASG |
| Secure RDP/SSH without VM public IP | Azure Bastion |
| Browser-based VM administration | Azure Bastion |
| Secure application passwords | Azure Key Vault |
| Protect cryptographic keys | Azure Key Vault |
| Manage TLS certificates | Azure Key Vault |
| HSM-protected keys | Key Vault Premium |

---

# 60. Final Module 2 Cram Sheet

```text
AZURE INFRASTRUCTURE SECURITY
= DEFENSE IN DEPTH

DDOS PROTECTION
= PROTECT AVAILABILITY

DDOS LAYERS
= LAYER 3 + LAYER 4

VOLUMETRIC ATTACK
= OVERWHELM BANDWIDTH

PROTOCOL ATTACK
= EXHAUST NETWORK/TRANSPORT RESOURCES

APPLICATION-LAYER ATTACK
= TARGET WEB APPLICATION REQUESTS

DEFAULT DDOS PROTECTION
= AUTOMATIC INFRASTRUCTURE BASELINE

DDOS NETWORK PROTECTION
= ENHANCED VNET-FOCUSED PROTECTION

DDOS IP PROTECTION
= PAY PER PROTECTED PUBLIC IP

DDOS RAPID RESPONSE
= EXPERT ASSISTANCE DURING ATTACKS

AZURE FIREWALL
= CENTRALIZED STATEFUL TRAFFIC FILTERING

SNAT
= TRANSLATE SOURCE ADDRESS

DNAT
= TRANSLATE DESTINATION ADDRESS

FIREWALL BASIC
= ESSENTIAL FIREWALL PROTECTION

FIREWALL STANDARD
= ENTERPRISE NETWORK/APPLICATION FILTERING

FIREWALL PREMIUM
= ADVANCED IDPS

FIREWALL MANAGER
= CENTRALIZE FIREWALL POLICIES

WAF
= PROTECT WEB APPLICATIONS

WAF LAYER
= LAYER 7

SQL INJECTION
= MALICIOUS SQL INPUT

XSS
= MALICIOUS SCRIPT IN WEB CONTENT

APPLICATION GATEWAY
= REGIONAL APPLICATION PROTECTION

FRONT DOOR
= GLOBAL APPLICATION PROTECTION

NETWORK SEGMENTATION
= DIVIDE NETWORK AND CONTAIN ATTACKS

VNET
= AZURE PRIVATE NETWORK

SUBNET
= SMALLER SEGMENT INSIDE A VNET

VNET PEERING
= CONNECT TWO VNets

VPN
= ENCRYPTED NETWORK CONNECTION

NSG
= ALLOW/DENY NETWORK TRAFFIC

NSG PRIORITY
= LOWER NUMBER PROCESSED FIRST

ASG
= GROUP RESOURCES BY APPLICATION ROLE

BASTION
= SECURE RDP/SSH TO VMs

RDP
= REMOTE DESKTOP PROTOCOL

SSH
= SECURE SHELL

BASTION CONNECTION
= TLS / PORT 443

BASTION PREMIUM
= SESSION RECORDING AND PRIVATE-ONLY OPTION

KEY VAULT
= SECRETS + KEYS + CERTIFICATES

SECRET
= PASSWORD / API KEY / TOKEN

KEY
= CRYPTOGRAPHIC MATERIAL

CERTIFICATE
= DIGITAL TRUST CREDENTIAL

KEY VAULT AUTHENTICATION
= MICROSOFT ENTRA ID

KEY VAULT AUTHORIZATION
= AZURE RBAC OR ACCESS POLICIES

KEY VAULT STANDARD
= SOFTWARE-PROTECTED KEYS

KEY VAULT PREMIUM
= HSM-PROTECTED KEYS
```

---

# 61. Final Mental Model

Imagine securing an Azure-hosted business application.

**Azure DDoS Protection** helps keep the application available when attackers flood the network.

**Azure Firewall** controls network and application traffic through centralized rules.

**Web Application Firewall** protects the web application from common attacks such as SQL injection and cross-site scripting.

**Azure Virtual Network** provides the private network environment.

**Subnets** divide the network into separate areas.

**Network Security Groups** determine which traffic can enter and leave those areas.

**Application Security Groups** organize resources according to application roles.

**Azure Bastion** allows administrators to securely connect to virtual machines without exposing management ports directly to the internet.

**Azure Key Vault** protects the sensitive credentials, cryptographic keys, and certificates required by applications.

Together, these services support:

**Confidentiality**

**Integrity**

**Availability**

and the Zero Trust principle:

**Assume Breach**

No single Azure service solves every security problem.

**The goal is to combine appropriate controls to reduce the likelihood and impact of compromise.**

---

# Official Microsoft Learn References

All instructional-unit links below were checked against the live module.

[Module Overview](https://learn.microsoft.com/en-us/training/modules/describe-basic-security-capabilities-azure/)

[Introduction](https://learn.microsoft.com/en-us/training/modules/describe-basic-security-capabilities-azure/1-introduction)

[Describe Azure DDoS Protection](https://learn.microsoft.com/en-us/training/modules/describe-basic-security-capabilities-azure/2-describe-azure-ddos-protection)

[Describe Azure Firewall](https://learn.microsoft.com/en-us/training/modules/describe-basic-security-capabilities-azure/3-describe-what-azure-firewall)

[Describe Web Application Firewall](https://learn.microsoft.com/en-us/training/modules/describe-basic-security-capabilities-azure/4-describe-web-application-firewall)

[Describe Network Segmentation in Azure](https://learn.microsoft.com/en-us/training/modules/describe-basic-security-capabilities-azure/5-describe-network-segmentation)

[Describe Azure Network Security Groups](https://learn.microsoft.com/en-us/training/modules/describe-basic-security-capabilities-azure/6-describe-azure-network-security-groups)

[Describe Azure Bastion](https://learn.microsoft.com/en-us/training/modules/describe-basic-security-capabilities-azure/7-describe-azure-bastion-just-in-time-access)

[Describe Azure Key Vault](https://learn.microsoft.com/en-us/training/modules/describe-basic-security-capabilities-azure/8-describe-ways-azure-encrypts-data)

[Summary and Resources](https://learn.microsoft.com/en-us/training/modules/describe-basic-security-capabilities-azure/10-summary-resources)
