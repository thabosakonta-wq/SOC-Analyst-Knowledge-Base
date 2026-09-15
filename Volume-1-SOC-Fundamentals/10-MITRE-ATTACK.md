# SOC Analyst Knowledge Base

A structured cybersecurity handbook designed to document the knowledge, concepts, tools, and methodologies used by Security Operations Center (SOC) Analysts.

This repository combines theory, practical examples, industry frameworks, and Microsoft security technologies to support continuous learning, interview preparation, and real-world SOC operations.

## Who is this for?

* Aspiring SOC Analysts
* Blue Team professionals
* Cybersecurity students
* Microsoft SC-200 learners
* Threat Hunters
* Detection Engineers

---

# MITRE ATT&CK

MITRE ATT&CK is a knowledge base and model for understanding cyber adversary behavior based on real-world observations.

It provides a common language for describing how adversaries operate against systems, networks, identities, applications, and other technology environments.

For SOC Analysts, ATT&CK can help connect:

**Adversary Behavior → Detection → Investigation → Threat Hunting → Response**

ATT&CK is maintained and updated over time as new adversary behaviors and threat intelligence become available.

This chapter uses the current Enterprise ATT&CK terminology and should be treated as a learning reference rather than a permanent snapshot of the entire ATT&CK catalog.

---

# What is MITRE ATT&CK?

MITRE ATT&CK organizes adversary behavior into a structured model.

The major concepts are:

* Tactics
* Techniques
* Sub-techniques
* Procedures
* Groups
* Software
* Mitigations
* Data Sources and Detection-related information

The framework helps security teams understand what adversaries are trying to accomplish and how they may perform those activities.

ATT&CK is not simply a list of malware or indicators.

It focuses primarily on **behavior**.

For example, instead of only asking:

> "Which malware was detected?"

a SOC Analyst can also ask:

> "What behavior did the malware perform?"

That behavioral approach can make detections and investigations more reusable across different tools, malware families, and threat actors.

---

# Tactics

A tactic represents **why** an adversary performs an action.

It describes the adversary's tactical goal.

Examples include:

* Initial Access
* Execution
* Persistence
* Privilege Escalation
* Credential Access
* Discovery
* Lateral Movement
* Collection
* Command and Control
* Exfiltration
* Impact

The current Enterprise ATT&CK model also includes:

* Reconnaissance
* Resource Development
* Stealth
* Defense Impairment

These tactics provide a high-level view of adversary objectives.

A tactic does not describe the exact command or tool used.

It describes the goal behind the activity.

---

# Current Enterprise Tactics

The current Enterprise ATT&CK model contains 15 tactics:

| ID     | Tactic               | General Objective                                   |
| ------ | -------------------- | --------------------------------------------------- |
| TA0043 | Reconnaissance       | Gather information for future operations            |
| TA0042 | Resource Development | Establish resources to support operations           |
| TA0001 | Initial Access       | Gain access to the target environment               |
| TA0002 | Execution            | Run malicious code or actions                       |
| TA0003 | Persistence          | Maintain access to the environment                  |
| TA0004 | Privilege Escalation | Obtain higher-level permissions                     |
| TA0005 | Stealth              | Hide or conceal adversary activity                  |
| TA0112 | Defense Impairment   | Disrupt security mechanisms or defensive visibility |
| TA0006 | Credential Access    | Obtain credentials or authentication material       |
| TA0007 | Discovery            | Learn about the environment                         |
| TA0008 | Lateral Movement     | Move through the environment                        |
| TA0009 | Collection           | Gather information of interest                      |
| TA0011 | Command and Control  | Communicate with compromised systems                |
| TA0010 | Exfiltration         | Remove data from the environment                    |
| TA0040 | Impact               | Manipulate, interrupt, or destroy systems or data   |

Tactics are not necessarily performed in a fixed order.

An adversary may move between tactical objectives depending on the situation, available access, defensive controls, and operational goals.

---

# Techniques

A technique describes **how** an adversary achieves a tactical goal.

For example, an adversary attempting to obtain credentials may use a credential-access technique such as:

* Brute Force
* OS Credential Dumping
* Credentials from Password Stores

Techniques provide more detail than tactics.

A simplified relationship is:

**Tactic = Why**

**Technique = How**

For example:

**Credential Access → OS Credential Dumping**

The tactic describes the objective.

The technique describes the behavior used to pursue that objective.

---

# Sub-Techniques

Sub-techniques provide a more specific description of behavior beneath a parent technique.

For example:

**T1110 — Brute Force**

has sub-techniques including:

* T1110.001 — Password Guessing
* T1110.002 — Password Cracking
* T1110.003 — Password Spraying
* T1110.004 — Credential Stuffing

This level of detail is useful to SOC Analysts because different sub-techniques can produce different telemetry and require different detection logic.

For example, password spraying and password cracking are both associated with brute-force activity, but the observable evidence can be very different.

---

# Procedures

Procedures describe specific implementations or observed examples of how an adversary has used a technique or sub-technique.

This is an important distinction.

A technique is a general behavior.

A procedure describes how a particular adversary, group, or software has actually implemented that behavior.

For example:

**Tactic: Credential Access**

→ **Technique: OS Credential Dumping**

→ **Procedure: An adversary uses a specific tool or method to obtain credentials from a compromised system.**

Procedures therefore provide valuable context for threat intelligence and investigation.

---

# Groups and Software

ATT&CK also contains information about adversary groups and software associated with observed techniques.

### Groups

Groups represent tracked adversary organizations or activity clusters.

A group may be associated with multiple techniques across different tactical objectives.

### Software

Software entries describe malware, tools, and other software associated with adversary operations.

A software entry can also be associated with multiple ATT&CK techniques.

This allows analysts to move between:

**Group → Software → Technique → Procedure**

during threat-intelligence and investigation activities.

---

# MITRE ATT&CK and the SOC

ATT&CK is particularly useful in Security Operations because it provides a common behavioral language.

A SOC Analyst may use ATT&CK to:

* Classify observed activity
* Understand adversary behavior
* Develop detection rules
* Conduct threat hunts
* Investigate alerts
* Map incidents
* Communicate findings
* Identify defensive gaps
* Support threat intelligence
* Improve detection coverage

Instead of documenting an alert only as:

> "Suspicious PowerShell detected"

an analyst can investigate the behavior and determine whether it corresponds to an ATT&CK technique or sub-technique.

This creates additional context around the alert.

---

# SOC Analyst Perspective

When investigating suspicious activity, a SOC Analyst should ask:

1. What happened?
2. Which account or system was involved?
3. What process or application performed the activity?
4. What telemetry supports the observation?
5. What was the apparent objective?
6. Which ATT&CK tactic may apply?
7. Which technique or sub-technique may describe the behavior?
8. Are there related techniques?
9. What additional activity should be investigated?
10. What containment or remediation actions are appropriate?

ATT&CK should support the investigation rather than replace analyst judgment.

The analyst must still validate the evidence.

---

# Detection Engineering and ATT&CK

ATT&CK can help Detection Engineers translate adversary behavior into detection opportunities.

A simplified detection-engineering workflow is:

**Threat Behavior**

↓

**ATT&CK Technique**

↓

**Required Telemetry**

↓

**Detection Logic**

↓

**Alert**

↓

**Investigation**

For example:

**Suspicious PowerShell execution**

may lead a Detection Engineer to investigate:

* PowerShell command-line activity
* Parent and child processes
* User identity
* Host identity
* Script content
* Network connections
* Related authentication activity

The resulting detection can then be mapped to the appropriate ATT&CK technique or sub-technique.

This creates a connection between the behavior being detected and the analytic designed to detect it.

---

# Threat Hunting and ATT&CK

Threat Hunters can use ATT&CK to develop hypotheses.

For example:

> "Could an attacker be using valid accounts to move laterally through the environment?"

The hunter can identify relevant ATT&CK techniques and then search available telemetry for evidence.

Possible telemetry may include:

* Authentication logs
* Windows Security Events
* Microsoft Defender telemetry
* Microsoft Entra sign-in logs
* Network telemetry
* Endpoint process activity
* DNS activity
* Cloud audit logs

The hunt should be evidence-driven.

ATT&CK provides the behavioral framework, while the organization's telemetry provides the evidence.

---

# Investigation and DFIR

ATT&CK can also support investigations and digital forensics.

During an investigation, analysts can map observed behaviors to ATT&CK techniques.

For example:

| Observed Activity                       | Possible ATT&CK Context |
| --------------------------------------- | ----------------------- |
| Repeated failed authentication attempts | Credential Access       |
| Suspicious PowerShell execution         | Execution               |
| New account created unexpectedly        | Persistence             |
| Remote logon to another host            | Lateral Movement        |
| Discovery of domain information         | Discovery               |
| Large outbound data transfer            | Exfiltration            |
| Security tooling disabled               | Defense Impairment      |

The mapping should always be based on evidence.

An analyst should avoid assigning a technique simply because it appears plausible.

---

# MITRE ATT&CK and the Cyber Kill Chain

The Cyber Kill Chain and MITRE ATT&CK are related but serve different purposes.

The Cyber Kill Chain provides a high-level ordered model of an intrusion.

ATT&CK provides a more detailed model of adversary behaviors and tactical objectives.

A simplified comparison is:

| Cyber Kill Chain                            | MITRE ATT&CK                        |
| ------------------------------------------- | ----------------------------------- |
| High-level attack lifecycle                 | Detailed adversary behavior         |
| Seven ordered stages                        | Multiple tactical objectives        |
| Useful for understanding attack progression | Useful for behavioral analysis      |
| Focuses on attack stages                    | Focuses on techniques and behaviors |
| Broad conceptual model                      | Detailed operational knowledge base |

They can therefore be used together.

For example:

**Cyber Kill Chain → Where in the attack lifecycle?**

**ATT&CK → What behavior is the adversary using?**

This distinction is important for SOC Analysts.

---

# Real-World Example — Credential Attack

Consider an attacker attempting to compromise an organization's user accounts.

### Step 1 — Initial Access

The attacker attempts to obtain access using stolen or guessed credentials.

The SOC may observe:

* Failed sign-ins
* Unusual locations
* Multiple accounts targeted
* Unusual authentication patterns

### Step 2 — Credential Access

The attacker attempts to obtain additional credentials.

The SOC may investigate:

* Credential-dumping behavior
* Access to credential stores
* Suspicious processes
* Privileged account activity

### Step 3 — Discovery

The attacker attempts to understand the environment.

The SOC may investigate:

* Account discovery
* Host discovery
* Network discovery
* Domain information queries

### Step 4 — Lateral Movement

The attacker attempts to access another system.

The SOC may investigate:

* Remote authentication
* Administrative connections
* Unusual source and destination hosts
* New authentication relationships

### Step 5 — Collection

The attacker searches for valuable information.

The SOC may investigate:

* File access
* Archive creation
* Database access
* Unusual data staging

### Step 6 — Exfiltration

The attacker attempts to remove data.

The SOC may investigate:

* Large outbound transfers
* Unusual destinations
* Cloud storage activity
* Suspicious encrypted connections

At each stage, ATT&CK provides a way to describe the observed behavior.

---

# ATT&CK Mapping Example

Suppose a SOC Analyst observes:

* A user account experiences repeated authentication failures.
* The failures target multiple users.
* A successful login follows from an unusual location.
* The account then authenticates to several internal systems.

The analyst should not immediately conclude that compromise has occurred.

Instead, the analyst can develop an investigation hypothesis.

Possible areas of ATT&CK relevance include:

**Credential Access**

→ Brute Force

→ Password Spraying

**Initial Access**

→ Valid Accounts

**Lateral Movement**

→ Relevant remote-access or authentication behavior

The analyst then validates these hypotheses against available telemetry.

This demonstrates an important SOC principle:

**ATT&CK mapping supports investigation; evidence establishes what actually happened.**

---

# ATT&CK Coverage

Organizations can use ATT&CK to understand which adversary behaviors their security controls can detect or mitigate.

For example:

| ATT&CK Area         | Possible Defensive Capability                    |
| ------------------- | ------------------------------------------------ |
| Credential Access   | Identity monitoring and authentication analytics |
| Execution           | Endpoint process monitoring                      |
| Discovery           | Endpoint and network telemetry                   |
| Lateral Movement    | Authentication and network monitoring            |
| Command and Control | Network and endpoint analytics                   |
| Exfiltration        | Data-loss and network monitoring                 |
| Impact              | Endpoint, server, and availability monitoring    |

Coverage should be based on organizational risk and relevant threats.

ATT&CK should **not** be treated as a simple requirement to make every technique “green.”

Different organizations face different threats, platforms, technologies, and operational risks.

The objective is meaningful defensive visibility and response capability.

---

# ATT&CK and Microsoft Security Operations

MITRE ATT&CK is particularly useful when working with Microsoft security technologies.

A SOC Analyst may encounter telemetry from:

* Microsoft Defender XDR
* Microsoft Defender for Endpoint
* Microsoft Sentinel
* Microsoft Entra ID
* Windows Security Events
* Sysmon
* Microsoft Defender for Cloud
* Microsoft 365 audit data

An analyst can use ATT&CK to help interpret what the telemetry may represent.

A simplified workflow is:

**Telemetry**

→ **Suspicious Behavior**

→ **ATT&CK Mapping**

→ **Investigation**

→ **Detection or Hunting**

→ **Response**

This is one reason ATT&CK knowledge is valuable for Security Operations Analysts.

---

# ATT&CK and KQL

ATT&CK knowledge can also help an analyst design KQL investigations.

For example, if the investigation concerns suspicious PowerShell activity, the analyst may search endpoint process telemetry for:

* PowerShell processes
* Parent processes
* Command-line arguments
* User accounts
* Device names
* Network connections
* Related alerts

The KQL query provides the technical investigation.

ATT&CK provides the behavioral context.

Neither replaces the other.

---

# Why MITRE ATT&CK Matters

MITRE ATT&CK provides a structured way to understand adversary behavior.

It helps security teams:

* Use consistent terminology
* Understand attacker objectives
* Identify behavioral patterns
* Develop detections
* Conduct threat hunts
* Support incident investigations
* Communicate threat intelligence
* Identify defensive opportunities
* Connect telemetry to adversary behavior

For a SOC Analyst, the greatest value is not memorizing hundreds of technique IDs.

The important skill is being able to recognize behavior and use ATT&CK to organize and communicate what that behavior means.

---

# Limitations of ATT&CK

ATT&CK is powerful, but it has limitations.

### It is not a complete list of every possible attack

ATT&CK documents observed and researched adversary behavior.

New behaviors may exist before they are documented.

### It is not a replacement for evidence

Mapping an alert to a technique does not prove that an attacker performed that technique.

The underlying telemetry must support the conclusion.

### It is not a 100% coverage checklist

Security teams should prioritize relevant threats and techniques instead of attempting to achieve universal coverage.

### It does not replace analyst judgment

Analysts still need to understand:

* The environment
* The user's normal behavior
* The organization's security controls
* Available telemetry
* Threat intelligence
* Incident context

ATT&CK should strengthen analysis rather than replace it.

---

# Summary

MITRE ATT&CK is a knowledge base and model for understanding adversary behavior.

The framework organizes behavior into:

* Tactics
* Techniques
* Sub-techniques
* Procedures

Tactics describe **why** an adversary performs an action.

Techniques describe **how** the adversary achieves a tactical objective.

Sub-techniques provide more specific behavioral descriptions.

Procedures describe specific implementations or observed uses of techniques.

For SOC Analysts, ATT&CK can support:

**Detection → Investigation → Threat Hunting → Incident Response**

ATT&CK also provides an important bridge between security telemetry and adversary behavior.

The goal is not to memorize the entire ATT&CK matrix.

The goal is to understand how to recognize, investigate, map, and communicate adversary behavior.

---

# Key Takeaways

* MITRE ATT&CK is a knowledge base and model for adversary behavior.
* Tactics describe why an adversary performs an action.
* Techniques describe how an adversary achieves a tactical objective.
* Sub-techniques provide more specific descriptions of behavior.
* Procedures describe specific implementations or observed uses.
* ATT&CK can support SOC detection and investigation.
* ATT&CK can support threat hunting.
* ATT&CK can support detection engineering.
* ATT&CK can support DFIR and incident investigations.
* ATT&CK and the Cyber Kill Chain provide different but complementary perspectives.
* ATT&CK mapping should be supported by evidence.
* Analysts should not treat ATT&CK as a simple 100% coverage checklist.
* Understanding behavior is more important than memorizing technique numbers.

---

# Review Questions

1. What is MITRE ATT&CK?
2. What does a tactic represent?
3. What does a technique represent?
4. What is a sub-technique?
5. What is a procedure in ATT&CK?
6. What is the difference between a tactic and a technique?
7. Why are techniques useful to SOC Analysts?
8. How can ATT&CK support detection engineering?
9. How can ATT&CK support threat hunting?
10. How can ATT&CK support DFIR investigations?
11. What is the difference between the Cyber Kill Chain and ATT&CK?
12. Why should ATT&CK mappings be supported by evidence?
13. Why should organizations avoid treating ATT&CK as a 100% coverage checklist?
14. How can Microsoft Sentinel and Defender telemetry support ATT&CK-based investigations?
15. Why is behavioral analysis important in SOC operations?

---

# Further Reading

* MITRE ATT&CK — Enterprise
* MITRE ATT&CK — Get Started
* MITRE ATT&CK — Enterprise Tactics
* MITRE ATT&CK — Enterprise Techniques
* MITRE ATT&CK Data & Tools
* MITRE ATT&CK Navigator
* Microsoft Defender XDR Documentation
* Microsoft Sentinel Documentation

---

# Interview Tip

**Question:** What is MITRE ATT&CK and how is it useful to a SOC Analyst?

**Answer:**

MITRE ATT&CK is a knowledge base and model of adversary behavior based on real-world observations. It organizes activity into tactics, techniques, sub-techniques, and procedures. A SOC Analyst can use ATT&CK to classify observed behavior, understand attacker objectives, develop detection and hunting hypotheses, support investigations, and communicate findings consistently.

A good analyst should also understand that ATT&CK mapping does not replace evidence. The analyst must validate the observed behavior using available telemetry and investigation data.

---

# SC-200 Exam Note

For Microsoft Security Operations Analyst preparation, understand how ATT&CK concepts connect with security operations.

Focus on:

* Security alerts
* Threat detection
* Incident investigation
* Threat hunting
* Endpoint telemetry
* Identity telemetry
* Network telemetry
* Microsoft Defender XDR
* Microsoft Sentinel
* KQL
* Incident response
* Detection engineering

A useful mental model is:

**Telemetry → Behavior → ATT&CK Context → Investigation → Detection/Hunting → Response**

You should be comfortable recognizing suspicious behavior and determining how ATT&CK can provide useful context for investigation and detection.

Do not focus only on memorizing technique IDs.

Focus on understanding the behavior represented by the technique.

---

# Key Terms

| Term                   | Meaning                                                                            |
| ---------------------- | ---------------------------------------------------------------------------------- |
| MITRE ATT&CK           | Knowledge base and model for understanding adversary behavior                      |
| Tactic                 | The adversary's tactical objective or "why"                                        |
| Technique              | The behavior used to achieve a tactical objective or "how"                         |
| Sub-Technique          | A more specific description of adversarial behavior                                |
| Procedure              | A specific implementation or observed use of a technique or sub-technique          |
| TTP                    | Tactics, Techniques, and Procedures                                                |
| ATT&CK Matrix          | Visualization of tactics and associated techniques                                 |
| Enterprise ATT&CK      | ATT&CK domain covering enterprise and cloud technologies                           |
| Threat Hunting         | Proactive search for evidence of malicious activity                                |
| Detection Engineering  | Development and improvement of security detections                                 |
| Telemetry              | Security-related data collected from systems and services                          |
| Behavioral Analysis    | Analysis of activity based on what an adversary or system is doing                 |
| Threat Intelligence    | Information used to understand threats, adversaries, and their activity            |
| MITRE ATT&CK Navigator | Tool for visualizing and working with ATT&CK techniques and coverage               |
| Valid Accounts         | ATT&CK behavior involving use of legitimate credentials for unauthorized activity  |
| Brute Force            | ATT&CK technique involving repeated attempts to obtain or use valid credentials    |
| Lateral Movement       | Adversary activity intended to move through an environment                         |
| Command and Control    | Communication used by adversaries to control compromised systems                   |
| Exfiltration           | Adversary activity intended to remove data from an environment                     |
| Defense Impairment     | Adversary activity intended to disrupt security mechanisms or defensive visibility |

