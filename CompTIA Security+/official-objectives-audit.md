# Official SY0-701 objective cross-check

The attached CompTIA Security+ SY0-701 *Exam Objectives Version 5.0* provided a more granular checklist than the earlier summary notes. The [public CompTIA objectives PDF](https://lecbyo.files.cmp.optimizely.com/download/cf25ec24b8a511ef9ecbb69c0f9687be) linked in this repository identifies itself as **Exam Objectives Document Version 7.0**. Both identify SY0-701, the same five domain weights and objective IDs 1.1 through 5.6. They are different document revisions; this review did not establish that every line of wording is identical. Use the version CompTIA currently provides when making a final exam checklist.

The 28 objective notes now have an **Additional blueprint concepts** section with independently written explanations of previously thin or missing topics. This is a content cross-check, **not proof of exam readiness**, and CompTIA explicitly says its examples are not exhaustive. No official PDF pages or practice questions are reproduced here.

| Domain | Gaps strengthened in the notes | Active validation still needed |
| --- | --- | --- |
| 1 | Control categories and roles; physical sensors; change side effects; certificate and encryption scopes. | Classify controls on two axes and explain PKI and Zero Trust data/control planes without prompts. |
| 2 | Actor motives; image/agentless and social vectors; VM/mobile/supply-chain weakness; network/crypto attack indicators; host mitigation. | Given a log or incident, distinguish vector, vulnerability, attack, indicator and first mitigation. |
| 3 | Architecture dependencies and OT; fail-open/closed, passive/inline, VPN/TLS/IPsec/SD-WAN/SASE; data location; recovery, journaling and power. | Draw zones and permitted flows, justify failure modes, and test data/recovery assumptions. |
| 4 | Wireless/mobile baselines; disposal evidence; contextual vulnerability triage; SCAP, SNMP and NetFlow; filtering; IAM protocols and proofing; automation; forensic preservation. | Choose technologies by function, interpret mixed telemetry, and walk through identity and incident lifecycles. |
| 5 | Privacy and ownership roles; risk cadence and BIA metrics; vendor contracts; compliance consequences; test scope and reconnaissance; behavior-focused training. | Write a risk decision, vendor review or finding with owner, evidence, exception and retest criteria. |

The highest-priority rechecks are [3.2 infrastructure](objectives/domain-3/sy0-701-3-2.md), [4.6 IAM](objectives/domain-4/sy0-701-4-6.md), [4.4 monitoring](objectives/domain-4/sy0-701-4-4.md), [5.2 risk/BIA](objectives/domain-5/sy0-701-5-2.md), and [5.5 audits and testing](objectives/domain-5/sy0-701-5-5.md). For each, explain a new scenario aloud, answer legitimate practice questions without referring to the notes, and record *why* each missed option is wrong. Continue to check all objectives rather than treating this priority list as the whole exam.
