# Official SY0-701 objective cross-check

The attached CompTIA Security+ SY0-701 **Exam Objectives Document Version 7.0** is the scope baseline; the [public CompTIA V7 PDF](https://lecbyo.files.cmp.optimizely.com/download/cf25ec24b8a511ef9ecbb69c0f9687be) is linked for readers. The earlier attached Version 5.0 PDF was used for the initial gap fill. Both use the same five domain weights and 28 numbered objectives. A normalized comparison of extracted objective text found the same word inventory after removing PDF bullet/layout artifacts; no substantive objective-scope change was detected. This does not prove identical page layout or guarantee that these study notes cover every possible exam example.

The 28 objective notes now have an **Additional blueprint concepts** section with independently written explanations of previously thin or missing topics. This is a content cross-check, **not proof of exam readiness**, and CompTIA explicitly says its examples are not exhaustive. No official PDF pages or practice questions are reproduced here.

| Domain | Gaps strengthened in the notes | Active validation still needed |
| --- | --- | --- |
| 1 | Control categories and roles; physical sensors; change side effects; certificate and encryption scopes. | Classify controls on two axes and explain PKI and Zero Trust data/control planes without prompts. |
| 2 | Actor motives; image/agentless and social vectors; VM/mobile/supply-chain weakness; network/crypto attack indicators; host mitigation. | Given a log or incident, distinguish vector, vulnerability, attack, indicator and first mitigation. |
| 3 | Architecture dependencies and OT; fail-open/closed, passive/inline, VPN/TLS/IPsec/SD-WAN/SASE; data location; recovery, journaling and power. | Draw zones and permitted flows, justify failure modes, and test data/recovery assumptions. |
| 4 | Wireless/mobile baselines; disposal evidence; contextual vulnerability triage; SCAP, SNMP and NetFlow; filtering; IAM protocols and proofing; automation; forensic preservation. | Choose technologies by function, interpret mixed telemetry, and walk through identity and incident lifecycles. |
| 5 | Privacy and ownership roles; risk cadence and BIA metrics; vendor contracts; compliance consequences; test scope and reconnaissance; behavior-focused training. | Write a risk decision, vendor review or finding with owner, evidence, exception and retest criteria. |

The highest-priority rechecks are [3.2 infrastructure](objectives/domain-3/sy0-701-3-2.md), [4.6 IAM](objectives/domain-4/sy0-701-4-6.md), [4.4 monitoring](objectives/domain-4/sy0-701-4-4.md), [5.2 risk/BIA](objectives/domain-5/sy0-701-5-2.md), and [5.5 audits and testing](objectives/domain-5/sy0-701-5-5.md). For each, explain a new scenario aloud, answer legitimate practice questions without referring to the notes, and record *why* each missed option is wrong. Continue to check all objectives rather than treating this priority list as the whole exam.

## Version 7.0 acronym appendix additions

Compared with the Version 5.0 acronym appendix, Version 7.0 lists these nine additional abbreviations. This is a **delta**, not the complete exam acronym list. Learn their function in context rather than merely their expansion.

| Acronym | Useful distinction | Related note |
| --- | --- | --- |
| 2FA | Two independent authentication factor categories; a subset of MFA. | [4.6 IAM](objectives/domain-4/sy0-701-4-6.md) |
| 3DES | An older symmetric block cipher; recognize it as legacy, not a preferred new design. | [1.4 cryptography](objectives/domain-1/sy0-701-1-4.md) |
| COBO | Corporate-owned, business-only device model; contrast with BYOD, COPE and CYOD. | [4.1 computing resources](objectives/domain-4/sy0-701-4-1.md) |
| DNSSEC | Adds authenticity/integrity checks to DNS answers; it does not encrypt DNS queries. | [3.2 infrastructure](objectives/domain-3/sy0-701-3-2.md) |
| EULA | End-user license terms govern software use, not whether software is secure. | [4.2 asset management](objectives/domain-4/sy0-701-4-2.md) |
| MX | DNS record identifying a domain's mail-exchange destination; not an email-authentication policy. | [4.5 enterprise capabilities](objectives/domain-4/sy0-701-4-5.md) |
| OWASP | A security community and source of application-security guidance, not a security product. | [2.3 vulnerabilities](objectives/domain-2/sy0-701-2-3.md) |
| SMB | Network file-sharing protocol; restrict access and avoid exposing it to untrusted networks. | [3.2 infrastructure](objectives/domain-3/sy0-701-3-2.md) |
| UBA | User behavior analytics surfaces anomalies that require investigation, not automatic attribution. | [4.4 monitoring](objectives/domain-4/sy0-701-4-4.md) |

Continue through the full Version 7.0 acronym appendix in the official PDF; these nine are only the entries absent from the earlier copy.
