# CompTIA Security+ Practice Exam 1
40 Questions, Multiple Choice

---

1. In which type of cloud computing model does the customer have the least control over the infrastructure?
<details>
<summary>A. Software as a Service (SaaS)</summary>
Correct. In a SaaS model, the provider manages the entire infrastructure and software. The customer only has access to the application itself, offering them the least amount of control.
</details>
<details>
<summary>B. Platform as a Service (PaaS)</summary>
Incorrect. PaaS provides a platform for development and deployment, giving customers control over applications but not the underlying infrastructure like operating systems or hardware.
</details>
<details>
<summary>C. Private Cloud</summary>
Incorrect. A private cloud offers the highest level of control as the infrastructure is dedicated to a single organization.
</details>
<details>
<summary>D. Infrastructure as a Service (IaaS)</summary>
Incorrect. IaaS provides customers with the most control over the operating systems and applications, as they manage the virtualized hardware resources.
</details>


2. Which type of encryption is used for securing data in transit?
<details>
<summary>A. Symmetric encryption</summary>
Incorrect. Symmetric encryption uses the same key for both encryption and decryption and is often used for data at rest, though it can be part of a hybrid system for data in transit. Asymmetric encryption is primarily used to establish the secure channel.
</details>
<details>
<summary>B. Asymmetric encryption</summary>
Correct. Asymmetric encryption (using a public/private key pair) is fundamental to protocols like TLS/SSL, which are used to establish a secure channel and protect data in transit over a network.
</details>
<details>
<summary>C. Salted encryption</summary>
Incorrect. Salting is a technique used to protect stored passwords, not for encrypting data in transit. A salt is added to a password before hashing.
</details>
<details>
<summary>D. Hashing</summary>
Incorrect. Hashing is a one-way function used to verify data integrity, not to encrypt and decrypt data in transit.
</details>


3. Which protocol is essential for secure web browsing?
<details>
<summary>A. FTP</summary>
Incorrect. FTP (File Transfer Protocol) is used for transferring files but is inherently insecure as it transmits data in cleartext.
</details>
<details>
<summary>B. HTTP</summary>
Incorrect. HTTP (Hypertext Transfer Protocol) is the foundation of data communication for the World Wide Web, but it is not secure.
</details>
<details>
<summary>C. SFTP</summary>
Incorrect. SFTP (SSH File Transfer Protocol) is used for secure file transfers, not for general web browsing.
</details>
<details>
<summary>D. HTTPS</summary>
Correct. HTTPS (Hypertext Transfer Protocol Secure) encrypts the communication between a web browser and a web server, ensuring confidentiality and integrity for web browsing.
</details>


4. What is the primary purpose of a digital certificate?
<details>
<summary>A. User authentication</summary>
Incorrect. While digital certificates can be used for user authentication, their primary purpose is to validate the ownership of a public key.
</details>
<details>
<summary>B. Email encryption</summary>
Incorrect. Digital certificates are a component used in email encryption (like S/MIME), but their main function is key validation, not encryption itself.
</details>
<details>
<summary>C. Validate ownership of a public key</summary>
Correct. A digital certificate, issued by a Certificate Authority (CA), binds a public key to a specific entity (like a person or a server), thereby validating its ownership and authenticity.
</details>
<details>
<summary>D. Provide secure wireless connection</summary>
Incorrect. While certificates can be used in the authentication process for some secure wireless networks (like WPA2-Enterprise), this is not their primary purpose.
</details>


5. Which technology is essential for building a secure network perimeter?
<details>
<summary>A. VLAN</summary>
Incorrect. VLANs (Virtual Local Area Networks) are used for segmenting a network internally, not for securing the perimeter.
</details>
<details>
<summary>B. Proxy server</summary>
Incorrect. A proxy server can be part of a perimeter defense, but a firewall is the most essential component.
</details>
<details>
<summary>C. Load balancer</summary>
Incorrect. A load balancer distributes traffic across multiple servers to improve availability and performance, which is not its primary security role.
</details>
<details>
<summary>D. Firewall</summary>
Correct. A firewall is a fundamental network security device that monitors and controls incoming and outgoing network traffic based on predetermined security rules, forming the core of a secure perimeter.
</details>


6. Which type of firewall inspects the state of active connections?
<details>
<summary>A. Stateful firewall</summary>
Correct. A stateful firewall monitors the state of active connections and uses this context to make decisions about which network packets to allow or block.
</details>
<details>
<summary>B. Next-generation firewall</summary>
Incorrect. While a next-generation firewall (NGFW) is stateful, this answer is less precise. The defining feature described is stateful inspection itself.
</details>
<details>
<summary>C. Web application firewall</summary>
Incorrect. A WAF (Web Application Firewall) operates at the application layer to protect web applications, which is a more specific function than stateful inspection.
</details>
<details>
<summary>D. Packet-filtering firewall</summary>
Incorrect. A packet-filtering firewall is a stateless firewall that inspects packets individually and does not track the state of connections.
</details>


7. What is the main function of a SIEM system?
<details>
<summary>A. Security information and event management</summary>
Correct. SIEM stands for Security Information and Event Management. Its main function is to collect, correlate, and analyze security data from various sources to detect threats and manage incidents.
</details>
<details>
<summary>B. Network traffic analysis</summary>
Incorrect. While a SIEM does perform traffic analysis, its function is broader, encompassing log management, event correlation, and reporting.
</details>
<details>
<summary>C. Intrusion prevention</summary>
Incorrect. An Intrusion Prevention System (IPS) is designed to actively block attacks, whereas a SIEM is primarily for detection, analysis, and alerting.
</details>
<details>
<summary>D. Data loss prevention</summary>
Incorrect. Data Loss Prevention (DLP) tools are specifically focused on preventing sensitive data from leaving the organization, which is a different function from a SIEM.
</details>


8. Which two factors contribute to a strong security posture?
<details>
<summary>A. Regular security audits</summary>
Correct. Audits systematically evaluate an organization's security controls and practices, helping to identify weaknesses and ensure compliance, which strengthens security posture.
</details>
<details>
<summary>B. Continuous monitoring</summary>
Correct. Continuous monitoring provides real-time visibility into the security state of systems and networks, allowing for rapid detection and response to threats.
</details>
<details>
<summary>C. Frequent password changes</summary>
Incorrect. Modern security guidance (like NIST) de-emphasizes frequent forced password changes, as they can lead to weaker passwords and do not necessarily improve security.
</details>
<details>
<summary>D. Single sign-on implementation</summary>
Incorrect. While SSO can improve user experience and centralize authentication management, it can also create a single point of failure if not implemented securely. It does not inherently guarantee a strong posture.
</details>


9. Which type of attack involves bombarding a DNS server with traffic to overwhelm it?
<details>
<summary>A. DNS poisoning</summary>
Incorrect. DNS poisoning (or cache spoofing) involves corrupting a DNS cache to redirect users to malicious sites.
</details>
<details>
<summary>B. DNS spoofing</summary>
Incorrect. DNS spoofing involves an attacker providing a false DNS response to a user's query.
</details>
<details>
<summary>C. DNS tunneling</summary>
Incorrect. DNS tunneling involves encoding data of other programs or protocols in DNS queries and responses, often to exfiltrate data.
</details>
<details>
<summary>D. DNS amplification attack</summary>
Correct. A DNS amplification attack is a type of Distributed Denial of Service (DDoS) attack where an attacker uses open DNS resolvers to flood a target with a large volume of DNS response traffic.
</details>


10. Which cryptographic algorithm is commonly used for secure wireless communication?
<details>
<summary>A. AES</summary>
Correct. AES (Advanced Encryption Standard) is the encryption standard used in the WPA2 and WPA3 security protocols to protect wireless network traffic.
</details>
<details>
<summary>B. MD5</summary>
Incorrect. MD5 is a hashing algorithm used for integrity checks, not for encryption. It is also considered insecure for cryptographic purposes.
</details>
<details>
<summary>C. DES</summary>
Incorrect. DES (Data Encryption Standard) is an older and weaker encryption algorithm that has been superseded by AES.
</details>
<details>
<summary>D. RSA</summary>
Incorrect. RSA is an asymmetric algorithm often used for key exchange or digital signatures, but AES (a symmetric algorithm) is used for the bulk encryption of the wireless data itself.
</details>


11. Which attack involves overwhelming a system with traffic to make it unavailable?
<details>
<summary>A. Phishing attack</summary>
Incorrect. A phishing attack is a form of social engineering used to deceive users into revealing sensitive information.
</details>
<details>
<summary>B. Buffer overflow attack</summary>
Incorrect. A buffer overflow attack exploits a vulnerability by writing data beyond the boundaries of a fixed-length buffer, potentially allowing arbitrary code execution.
</details>
<details>
<summary>C. Distributed Denial of Service (DDoS) attack</summary>
Correct. A DDoS attack uses multiple compromised systems (a botnet) to generate a flood of traffic, overwhelming a target's resources and making it unavailable to legitimate users.
</details>
<details>
<summary>D. Man-in-the-middle attack</summary>
Incorrect. A Man-in-the-middle (MitM) attack involves an attacker secretly intercepting and relaying communications between two parties.
</details>


12. Identify two common methods used in multifactor authentication.
<details>
<summary>A. Security tokens</summary>
Correct. A security token (something you have), which can be a hardware device or a software application that generates a one-time code, is a common MFA factor.
</details>
<details>
<summary>B. Biometrics</summary>
Correct. Biometrics (something you are), such as a fingerprint or facial scan, provide a unique inherence factor for authentication in MFA.
</details>
<details>
<summary>C. Passwords</summary>
Incorrect. A password is a single factor (something you know). MFA requires the use of two or more different types of factors.
</details>
<details>
<summary>D. Usernames</summary>
Incorrect. A username is an identifier, not an authentication factor.
</details>


13. What is the main goal of an incident response plan?
<details>
<summary>A. Preventing security incidents</summary>
Incorrect. While prevention is a goal of overall security, an incident response plan specifically deals with what to do *after* an incident has occurred.
</details>
<details>
<summary>B. Training employees on security practices</summary>
Incorrect. This is the goal of a security awareness program, not an incident response plan.
</details>
<details>
<summary>C. Encrypting sensitive data</summary>
Incorrect. Data encryption is a security control used to protect data, not the main goal of an incident response plan.
</details>
<details>
<summary>D. Responding effectively to security incidents</summary>
Correct. The primary goal of an incident response plan is to provide a structured, organized, and effective approach to handling security incidents, thereby minimizing damage and reducing recovery time.
</details>


14. Identify two characteristics of a DDoS attack.
<details>
<summary>A. Overwhelms a target's resources</summary>
Correct. The primary goal of any Denial of Service attack, including a DDoS attack, is to exhaust the resources (like bandwidth, CPU, or memory) of the target system.
</details>
<details>
<summary>B. Originates from a single source</summary>
Incorrect. This describes a Denial of Service (DoS) attack. The first 'D' in DDoS stands for 'Distributed', meaning it originates from multiple sources.
</details>
<details>
<summary>C. Utilizes multiple compromised systems</summary>
Correct. A DDoS attack leverages a network of compromised computers (a botnet) to launch the attack from many different locations simultaneously.
</details>
<details>
<summary>D. Targets multiple systems</summary>
Incorrect. A DDoS attack typically focuses its combined traffic on a single target system or service to maximize its impact.
</details>


15. Select two protocols commonly used for securing email communication.
<details>
<summary>A. S/MIME</summary>
Correct. S/MIME (Secure/Multipurpose Internet Mail Extensions) is a standard for public key encryption and signing of email encapsulated in MIME.
</details>
<details>
<summary>B. SMTP</summary>
Incorrect. SMTP (Simple Mail Transfer Protocol) is the standard protocol for sending email, but it does not inherently include encryption.
</details>
<details>
<summary>C. FTP</summary>
Incorrect. FTP (File Transfer Protocol) is used for transferring files, not for securing email.
</details>
<details>
<summary>D. PGP</summary>
Correct. PGP (Pretty Good Privacy) is an encryption program that provides cryptographic privacy and authentication for data communication, commonly used for securing emails.
</details>


16. Select two primary goals of a security awareness training program.
<details>
<summary>A. Educate employees about security policies</summary>
Correct. A key goal of security awareness training is to ensure all employees understand the organization's security policies and their role in upholding them.
</details>
<details>
<summary>B. Train employees on using new software</summary>
Incorrect. This is a function of general employee training or IT training, not specifically security awareness.
</details>
<details>
<summary>C. Improve hardware maintenance skills</summary>
Incorrect. This is a technical skill unrelated to security awareness training.
</details>
<details>
<summary>D. Increase awareness about social engineering attacks</summary>
Correct. One of the most important goals of security awareness training is to teach employees how to recognize and respond to social engineering tactics like phishing, vishing, and tailgating.
</details>


17. What does PKI stand for in network security?
<details>
<summary>A. Public Key Infrastructure</summary>
Correct. PKI is a framework of hardware, software, policies, and procedures needed to create, manage, distribute, use, store, and revoke digital certificates and manage public-key encryption.
</details>
<details>
<summary>B. Public Key Interface</summary>
Incorrect. This is not a standard cybersecurity term.
</details>
<details>
<summary>C. Private Key Integration</summary>
Incorrect. This is not a standard cybersecurity term.
</details>
<details>
<summary>D. Protected Key Interface</summary>
Incorrect. This is not a standard cybersecurity term.
</details>


18. What is the primary function of RAID technology?
<details>
<summary>A. Provide data encryption</summary>
Incorrect. RAID does not inherently provide data encryption. Encryption must be implemented separately.
</details>
<details>
<summary>B. Enhance data security</summary>
Incorrect. While redundancy from RAID can protect against data loss from a drive failure (which is a form of availability), its primary purpose isn't security in the sense of confidentiality or integrity against attacks.
</details>
<details>
<summary>C. Increase storage capacity</summary>
Incorrect. Some RAID levels (like RAID 0) can increase performance and capacity, but the overarching function across most RAID levels is redundancy.
</details>
<details>
<summary>D. Improve data redundancy and performance</summary>
Correct. RAID (Redundant Array of Independent Disks) combines multiple physical disk drives into one or more logical units for the purposes of data redundancy, performance improvement, or both.
</details>


19. Which two are essential components of a security incident response plan?
<details>
<summary>A. Incident identification</summary>
Correct. A core part of any incident response plan is the process for detecting and validating that a security incident has occurred.
</details>
<details>
<summary>B. Incident escalation</summary>
Correct. The plan must define procedures for escalating an incident to the appropriate personnel or teams based on its severity and type.
</details>
<details>
<summary>C. Regular data backup</summary>
Incorrect. Data backup is a preventative and recovery control, but it is not a component of the incident response plan itself, although the plan may refer to using backups during the recovery phase.
</details>
<details>
<summary>D. Data encryption</summary>
Incorrect. Data encryption is a security control to protect data, not a component of the response process.
</details>


20. Select two common cryptographic algorithms used in hashing.
<details>
<summary>A. MD5</summary>
Correct. MD5 (Message Digest 5) is a widely known hashing algorithm, though it is now considered insecure for cryptographic purposes due to vulnerabilities.
</details>
<details>
<summary>B. RSA</summary>
Incorrect. RSA is an asymmetric algorithm used for encryption and digital signatures, not for hashing.
</details>
<details>
<summary>C. SHA</summary>
Correct. SHA (Secure Hash Algorithm) is a family of cryptographic hash functions, including SHA-1, SHA-256, and SHA-3, which are the modern standard for hashing.
</details>
<details>
<summary>D. DES</summary>
Incorrect. DES (Data Encryption Standard) is a symmetric encryption algorithm, not a hashing algorithm.
</details>


21. Which term describes unauthorized access to data, applications, services, or networks?
<details>
<summary>A. Attack</summary>
Incorrect. An attack is the action or attempt to gain unauthorized access; a breach is the successful result of that attack.
</details>
<details>
<summary>B. Breach</summary>
Correct. A security breach is an incident that results in confirmed unauthorized access to, and potential exposure of, sensitive or protected data.
</details>
<details>
<summary>C. Phishing</summary>
Incorrect. Phishing is a specific type of attack method, not the outcome of unauthorized access itself.
</details>
<details>
<summary>D. Exploit</summary>
Incorrect. An exploit is a piece of code or technique used to take advantage of a vulnerability, which may lead to a breach.
</details>


22. Which security concept ensures that data is not altered or tampered with?
<details>
<summary>A. Integrity</summary>
Correct. Integrity is one of the core principles of the CIA triad (Confidentiality, Integrity, Availability) and refers to maintaining the consistency, accuracy, and trustworthiness of data.
</details>
<details>
<summary>B. Non-repudiation</summary>
Incorrect. Non-repudiation provides proof of the origin of data and ensures that the sender cannot deny having sent the message.
</details>
<details>
<summary>C. Confidentiality</summary>
Incorrect. Confidentiality ensures that sensitive information is not disclosed to unauthorized individuals.
</details>
<details>
<summary>D. Availability</summary>
Incorrect. Availability ensures that systems and data are accessible to authorized users when needed.
</details>


23. Identify two key components of risk management in cybersecurity.
<details>
<summary>A. Risk mitigation</summary>
Correct. Risk mitigation involves implementing controls and countermeasures to reduce the likelihood or impact of identified risks.
</details>
<details>
<summary>B. Purchasing insurance</summary>
Incorrect. Purchasing insurance is a form of risk transference, which is one strategy within risk management, but risk assessment and mitigation are more fundamental components of the process.
</details>
<details>
<summary>C. Risk assessment</summary>
Correct. Risk assessment is the process of identifying, analyzing, and evaluating risks to organizational assets. It is a foundational component of risk management.
</details>
<details>
<summary>D. Installing antivirus software</summary>
Incorrect. Installing antivirus software is a specific example of a risk mitigation technique, not a high-level component of the overall risk management process.
</details>


24. Which type of security testing involves testers having no prior knowledge of the network infrastructure?
<details>
<summary>A. Grey box testing</summary>
Incorrect. In grey box testing, testers have partial knowledge of the system, such as user-level credentials or network diagrams.
</details>
<details>
<summary>B. Penetration testing</summary>
Incorrect. This is a broad term for security testing. Black box, white box, and grey box are different methodologies within penetration testing.
</details>
<details>
<summary>C. White box testing</summary>
Incorrect. In white box testing, testers have full knowledge of the system, including source code and administrative access.
</details>
<details>
<summary>D. Black box testing</summary>
Correct. Black box testing simulates an attack from an external actor with no inside knowledge of the target system. Testers must discover vulnerabilities from the outside, just as a real attacker would.
</details>


25. Which security principle involves having more than one person required to perform a task?
<details>
<summary>A. Least privilege</summary>
Incorrect. The principle of least privilege dictates that users should only be given the minimum level of access required to perform their job functions.
</details>
<details>
<summary>B. Job rotation</summary>
Incorrect. Job rotation is a policy of moving employees between different roles to prevent fraud and detect irregularities.
</details>
<details>
<summary>C. Dual control</summary>
Correct. Dual control is a security principle that requires two individuals to be present to perform a single, critical task, preventing any single person from acting alone.
</details>
<details>
<summary>D. Separation of duties</summary>
Incorrect. Separation of duties is a related but distinct concept where a single critical task is divided into multiple parts, and each part is performed by a different person. Dual control requires two people for the same task at the same time.
</details>


26. In a security context, what does 'AAA' stand for?
<details>
<summary>A. Authentication, Analysis, and Auditing</summary>
Incorrect. While these are all security concepts, they are not the correct expansion of the AAA acronym.
</details>
<details>
<summary>B. Authentication, Authorization, and Accounting</summary>
Correct. AAA is a security framework for controlling access to resources. Authentication verifies who a user is, Authorization determines what they are allowed to do, and Accounting tracks what they did.
</details>
<details>
<summary>C. Access, Authentication, and Audit</summary>
Incorrect. While these are all security concepts, they are not the correct expansion of the AAA acronym.
</details>
<details>
<summary>D. Analysis, Authorization, and Access</summary>
Incorrect. While these are all security concepts, they are not the correct expansion of the AAA acronym.
</details>


27. What is the main purpose of a VPN?
<details>
<summary>A. Filter web content</summary>
Incorrect. While some VPN services offer content filtering, the primary purpose of the underlying technology is to encrypt traffic.
</details>
<details>
<summary>B. Manage network devices</summary>
Incorrect. Network management protocols like SNMP are used for managing devices, not VPNs.
</details>
<details>
<summary>C. Encrypt data transmission</summary>
Correct. A Virtual Private Network (VPN) creates a secure, encrypted tunnel over a public network (like the internet), protecting the confidentiality and integrity of the data transmitted within it.
</details>
<details>
<summary>D. Increase internet speed</summary>
Incorrect. Using a VPN typically adds a small amount of overhead that can slightly decrease internet speed due to the encryption process. It does not increase speed.
</details>


28. Which two network devices are used for traffic management and segmentation?
<details>
<summary>A. Router</summary>
Correct. A router operates at Layer 3 and is used to connect different networks and make decisions on how to forward traffic between them, effectively segmenting them.
</details>
<details>
<summary>B. Modem</summary>
Incorrect. A modem (modulator-demodulator) is used to convert digital signals from a computer into analog signals for transmission over a phone line or cable, and vice versa. It does not manage or segment traffic.
</details>
<details>
<summary>C. Switch</summary>
Correct. A switch operates at Layer 2 and creates separate collision domains for each port. More advanced switches can create VLANs (Virtual LANs) to logically segment the network.
</details>
<details>
<summary>D. Hub</summary>
Incorrect. A hub is a Layer 1 device that simply repeats all incoming traffic to all other ports. It cannot segment traffic and creates a single collision domain.
</details>


29. In cybersecurity, what does 'IAM' stand for?
<details>
<summary>A. Internet Application Mode</summary>
Incorrect. This is not a standard cybersecurity term.
</details>
<details>
<summary>B. Identity and Access Management</summary>
Correct. IAM is the security discipline and framework that enables the right individuals to access the right resources at the right times for the right reasons.
</details>
<details>
<summary>C. Integrated Asset Monitoring</summary>
Incorrect. This is not a standard cybersecurity term.
</details>
<details>
<summary>D. Intrusion Alert Mechanism</summary>
Incorrect. This is not a standard cybersecurity term.
</details>


30. What is the primary purpose of data classification in an organization?
<details>
<summary>A. Protecting sensitive information</summary>
Correct. Data classification is the process of categorizing data based on its sensitivity (e.g., Public, Internal, Confidential). This allows an organization to apply the appropriate level of security controls to protect sensitive information.
</details>
<details>
<summary>B. Improving data access speed</summary>
Incorrect. Data classification is not related to the speed of data access.
</details>
<details>
<summary>C. Securing the network</summary>
Incorrect. While data classification supports overall security, its direct purpose is to protect the data itself, not the network infrastructure.
</details>
<details>
<summary>D. Organizing files by type</summary>
Incorrect. Data classification is based on sensitivity and business impact, not simply the file type (e.g., .pdf, .docx).
</details>


31. In network security, what does a WAF protect against?
<details>
<summary>A. Windows authentication</summary>
Incorrect. A WAF is not related to Windows authentication mechanisms.
</details>
<details>
<summary>B. WAN intrusion</summary>
Incorrect. This is too general. A firewall or IPS might protect against WAN intrusion, but a WAF is more specific.
</details>
<details>
<summary>C. Wireless access</summary>
Incorrect. Wireless Access Points (WAPs) and related protocols handle wireless security.
</details>
<details>
<summary>D. Web application attacks</summary>
Correct. A WAF (Web Application Firewall) is specifically designed to protect web applications by filtering and monitoring HTTP traffic between a web application and the Internet, guarding against attacks like SQL injection and cross-site scripting (XSS).
</details>


32. What type of attack involves intercepting legitimate communication and forging a fictitious response to the sender?
<details>
<summary>A. Man-in-the-middle attack</summary>
Correct. A Man-in-the-middle (MitM) attack places the attacker between two communicating parties. The attacker intercepts traffic and can alter, relay, or forge responses while both sides believe they're communicating directly with each other.
</details>
<details>
<summary>B. Phishing attack</summary>
Incorrect. A phishing attack tricks a victim into revealing information through fraudulent messages.
</details>
<details>
<summary>C. Denial of service attack</summary>
Incorrect. A denial of service (DOS) attack overwhelms resources to make a service unavailable.
</details>
<details>
<summary>D. SQL injection attack</summary>
Incorrect. A SQL injection attack injects malicious SQL commands into a database query.
</details>


33. In which type of attack does the attacker disguise as a trusted entity to steal sensitive information?
<details>
<summary>A. SQL injection attack</summary>
Incorrect. A SQL injection attack targets a database through a vulnerable application.
</details>
<details>
<summary>B. DDoS attack</summary>
Incorrect. A DDoS attack is designed to make a service unavailable, not to steal information by impersonation.
</details>
<details>
<summary>C. Phishing attack</summary>
Correct. Phishing is a social engineering attack where an attacker sends fraudulent communications that appear to come from a reputable source, with the goal of tricking the victim into revealing sensitive information.
</details>
<details>
<summary>D. Man-in-the-middle attack</summary>
Incorrect. A MitM attack involves intercepting communication, not necessarily disguising oneself to trick a user into handing over information.
</details>


34. Which malware type is specifically designed to take advantage of a known vulnerability?
<details>
<summary>A. Exploit</summary>
Correct. An exploit is a piece of code, a sequence of commands, or a set of data that takes advantage of a bug, flaw, or vulnerability in a software application or system to cause unintended or unanticipated behavior.
</details>
<details>
<summary>B. Worm</summary>
Incorrect. A worm is a standalone malware that replicates itself to spread to other computers, often using a vulnerability, but the code that targets the vulnerability is the exploit.
</details>
<details>
<summary>C. Trojan</summary>
Incorrect. A Trojan is malware disguised as legitimate software. It relies on tricking the user into running it.
</details>
<details>
<summary>D. Virus</summary>
Incorrect. A virus is a type of malware that attaches itself to another program and spreads when that program is executed.
</details>


35. Choose two types of malware that typically require user interaction to activate.
<details>
<summary>A. Trojan</summary>
Correct. A Trojan horse disguises itself as legitimate software and relies on a user to execute it, thereby activating the malware.
</details>
<details>
<summary>B. Virus</summary>
Correct. A classic virus requires a user to run the infected program or open the infected file to activate and spread.
</details>
<details>
<summary>C. Rootkit</summary>
Incorrect. A rootkit is designed to gain and maintain privileged control over a computer system without being detected, and it often does not require direct user interaction to run once installed.
</details>
<details>
<summary>D. Worm</summary>
Incorrect. A worm is specifically designed to spread across networks without needing user interaction, often by exploiting software vulnerabilities automatically.
</details>


36. Which type of security control is a security awareness training?
<details>
<summary>A. Physical</summary>
Incorrect. Physical controls are items like locks, fences, and security guards that deter physical access.
</details>
<details>
<summary>B. Technical</summary>
Incorrect. Technical controls are implemented using technology, such as firewalls, antivirus software, and encryption.
</details>
<details>
<summary>C. Legal</summary>
Incorrect. Legal is not a standard category of security control. It would fall under administrative or regulatory.
</details>
<details>
<summary>D. Administrative</summary>
Correct. Administrative (or managerial) controls are security measures that focus on policies, procedures, and training. Security awareness training is a prime example of an administrative control.
</details>


37. Which term describes a flaw or weakness in a system's design or implementation that could be exploited?
<details>
<summary>A. Exploit</summary>
Incorrect. An exploit is the tool or technique used to take advantage of a vulnerability.
</details>
<details>
<summary>B. Threat</summary>
Incorrect. A threat is a potential for a vulnerability to be exploited by a threat actor.
</details>
<details>
<summary>C. Vulnerability</summary>
Correct. A vulnerability is a weakness or flaw in a system, process, or control that can be exploited by a threat.
</details>
<details>
<summary>D. Risk</summary>
Incorrect. Risk is the intersection of a threat and a vulnerability (Risk = Threat x Vulnerability). It is the potential for loss or damage when a threat exploits a vulnerability.
</details>


38. What is a honeypot primarily used for in network security?
<details>
<summary>A. Managing user access</summary>
Incorrect. Identity and Access Management (IAM) systems are used for managing user access.
</details>
<details>
<summary>B. Filtering spam</summary>
Incorrect. Email gateways and spam filters are used for filtering spam.
</details>
<details>
<summary>C. Encrypting data</summary>
Incorrect. Encryption protocols and algorithms are used for encrypting data.
</details>
<details>
<summary>D. Detecting and analyzing attacks</summary>
Correct. A honeypot is a decoy system set up to be an attractive target for attackers. Its purpose is to lure them in so that their attack methods and tools can be monitored and analyzed in a safe environment.
</details>


39. In cybersecurity, what is the principle of least privilege?
<details>
<summary>A. Providing users with only the access necessary to perform their jobs</summary>
Correct. The principle of least privilege is a fundamental security concept that dictates a user or process should only have the minimum set of permissions, rights, or access required to perform their specific task.
</details>
<details>
<summary>B. Regularly updating user privileges</summary>
Incorrect. While regularly reviewing privileges is a good practice (called access review), it is not the definition of the principle itself.
</details>
<details>
<summary>C. Requiring two or more forms of identification for access</summary>
Incorrect. This describes multifactor authentication (MFA), not the principle of least privilege.
</details>
<details>
<summary>D. Separating user data from application data</summary>
Incorrect. This describes data segregation, which is a good security practice but is not the principle of least privilege.
</details>


40. Which protocol is used for securely accessing remote servers?
<details>
<summary>A. SNMP</summary>
Incorrect. SNMP (Simple Network Management Protocol) is used for managing and monitoring network devices, not for secure remote access sessions.
</details>
<details>
<summary>B. FTP</summary>
Incorrect. FTP (File Transfer Protocol) is used for file transfers and is insecure. Its secure counterpart is SFTP or FTPS.
</details>
<details>
<summary>C. HTTPS</summary>
Incorrect. HTTPS is for securing web traffic, not for general-purpose remote server access (like a command-line shell).
</details>
<details>
<summary>D. SSH</summary>
Correct. SSH (Secure Shell) is a cryptographic network protocol used for operating network services securely over an unsecured network. Its most notable applications are remote login and command-line execution.
</details>
