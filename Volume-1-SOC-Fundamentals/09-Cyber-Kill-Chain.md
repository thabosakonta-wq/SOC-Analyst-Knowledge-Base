# Cyber Kill Chain

The Cyber Kill Chain is a model used to describe the stages of a cyber attack. It helps Security Operations Center (SOC) Analysts understand how attackers progress from initial reconnaissance through actions on their objectives.

Understanding the Cyber Kill Chain helps analysts identify where an attack may be detected, disrupted, contained, or investigated.

The traditional Cyber Kill Chain consists of seven stages:

1. Reconnaissance
2. Weaponization
3. Delivery
4. Exploitation
5. Installation
6. Command and Control
7. Actions on Objectives

---

# 1. Reconnaissance

Reconnaissance is the stage where an attacker gathers information about the target.

Information may include:

* Domain names
* IP addresses
* Email addresses
* Publicly exposed services
* Employee information
* Technology platforms
* Network infrastructure

Attackers may obtain information from publicly available sources or through active scanning.

### SOC Analyst Perspective

Security teams can monitor for unusual scanning activity, suspicious network reconnaissance, and attempts to identify exposed services.

---

# 2. Weaponization

Weaponization is the stage where an attacker prepares a malicious payload or tool to use against the target.

Examples include:

* Malicious documents
* Exploitation tools
* Malware
* Scripts
* Credential-stealing tools
* Malicious macros

The attacker combines the delivery method with the malicious capability needed to compromise the target.

### SOC Analyst Perspective

Weaponization may occur outside the organization's environment, meaning the SOC may not directly observe this stage. However, threat intelligence, malware analysis, and indicators associated with known campaigns can help defenders prepare detection capabilities.

---

# 3. Delivery

Delivery is the stage where the attacker attempts to deliver the malicious payload to the target.

Common delivery methods include:

* Phishing emails
* Malicious attachments
* Malicious links
* Compromised websites
* Removable media
* Exploitation of exposed services

### SOC Analyst Perspective

Delivery can provide important detection opportunities.

Analysts may investigate:

* Suspicious emails
* Malicious URLs
* Unexpected file attachments
* Unusual inbound connections
* Security gateway alerts
* Endpoint protection alerts

---

# 4. Exploitation

Exploitation occurs when the attacker takes advantage of a vulnerability or weakness to execute malicious activity.

Examples include:

* Exploiting an unpatched vulnerability
* Exploiting a vulnerable application
* Exploiting a malicious document
* Exploiting weak security controls
* Exploiting stolen credentials

### SOC Analyst Perspective

Analysts may investigate:

* Exploit alerts
* Unusual process creation
* Suspicious application behavior
* Unexpected command execution
* Authentication anomalies
* Endpoint security alerts

The analyst should determine whether the activity represents a successful compromise or a blocked attempt.

---

# 5. Installation

Installation occurs when the attacker establishes malicious software or another mechanism that allows continued access to the compromised environment.

Examples include:

* Malware installation
* Persistence mechanisms
* Malicious services
* Scheduled tasks
* Startup mechanisms
* Unauthorized accounts

### SOC Analyst Perspective

Analysts can investigate endpoint telemetry for:

* New processes
* New services
* Scheduled tasks
* Suspicious files
* Registry modifications
* Unexpected user accounts
* Persistence activity

Successful installation can indicate that the attacker has moved beyond an initial compromise and established a foothold.

---

# 6. Command and Control

Command and Control (C2) is the stage where a compromised system communicates with infrastructure controlled by the attacker.

C2 communication may allow an attacker to:

* Send commands
* Receive information
* Download additional tools
* Maintain access
* Control compromised systems

Common communication methods may include:

* HTTP or HTTPS
* DNS
* Other network protocols
* Remote access mechanisms

### SOC Analyst Perspective

Network and endpoint telemetry can provide valuable detection opportunities.

Analysts may investigate:

* Connections to suspicious IP addresses
* Suspicious domains
* Unusual DNS queries
* Repeated outbound connections
* Unusual network destinations
* Unexpected processes making network connections

This stage connects directly with network traffic analysis and threat-hunting activities.

---

# 7. Actions on Objectives

Actions on Objectives is the stage where the attacker performs the intended activity after gaining access to the environment.

Examples include:

* Data theft
* Data destruction
* Credential theft
* Financial fraud
* System disruption
* Unauthorized changes
* Deployment of ransomware

### SOC Analyst Perspective

This stage may involve significant business impact and therefore requires rapid investigation and response.

Analysts may investigate:

* Large data transfers
* Suspicious file access
* Privilege escalation
* Unauthorized administrative activity
* Data modification or deletion
* Ransomware indicators
* Account misuse

The analyst should determine the scope and impact of the incident and initiate the appropriate incident response procedures.

---

# Real-World Example

Consider a phishing attack against an organization.

The attacker:

1. Performs reconnaissance on the organization.
2. Prepares a malicious document.
3. Delivers the document through a phishing email.
4. Exploits a vulnerability or tricks the user into executing the payload.
5. Installs malicious software on the endpoint.
6. Establishes communication with attacker-controlled infrastructure.
7. Attempts to steal sensitive organizational information.

The SOC Analyst may detect activity at several stages.

For example:

* Email security may detect the phishing message.
* Endpoint security may detect malicious execution.
* Windows Event Logs may show suspicious process activity.
* Network monitoring may identify communication with a suspicious destination.
* Threat hunting may identify related activity across additional endpoints.
* Incident response procedures may be initiated once malicious activity is confirmed.

This demonstrates why understanding the attack lifecycle is important for SOC Analysts.

---

# Detection Opportunities

The Cyber Kill Chain provides defenders with multiple opportunities to detect and disrupt attacks.

| Kill Chain Stage      | Example Detection Opportunity                      |
| --------------------- | -------------------------------------------------- |
| Reconnaissance        | Network scanning and unusual discovery activity    |
| Weaponization         | Threat intelligence and malware analysis           |
| Delivery              | Phishing and malicious attachment detection        |
| Exploitation          | Exploit and suspicious process detection           |
| Installation          | Persistence and endpoint activity                  |
| Command and Control   | Suspicious DNS and network connections             |
| Actions on Objectives | Data access, theft, destruction, or account misuse |

A SOC Analyst should not wait until the final stage before responding.

Earlier detection can reduce the potential impact of an attack.

---

# Benefits of the Cyber Kill Chain

Understanding the Cyber Kill Chain provides several advantages:

* Helps analysts understand attacker behavior
* Provides a structured way to analyze attacks
* Identifies potential detection opportunities
* Supports incident investigation
* Helps security teams identify defensive gaps
* Supports threat hunting
* Helps prioritize security monitoring
* Improves incident response decisions
* Provides a common language for discussing attack activity

---

# Summary

The Cyber Kill Chain describes seven stages commonly associated with a cyber attack:

**Reconnaissance → Weaponization → Delivery → Exploitation → Installation → Command and Control → Actions on Objectives**

SOC Analysts can use the model to understand how an attack progresses and identify opportunities to detect, investigate, contain, and disrupt malicious activity.

The model is particularly useful when analyzing an incident because it encourages analysts to consider both the activity already observed and the possible next stages of an attack.

---

# Key Takeaways

* The Cyber Kill Chain describes seven stages of a cyber attack.
* Reconnaissance involves gathering information about the target.
* Weaponization involves preparing the malicious capability.
* Delivery involves sending or introducing the malicious payload.
* Exploitation takes advantage of a vulnerability or weakness.
* Installation establishes malicious software or persistence.
* Command and Control enables communication with attacker-controlled infrastructure.
* Actions on Objectives represents the attacker's intended outcome.
* SOC Analysts can identify detection opportunities throughout the attack lifecycle.
* Earlier detection can reduce the impact of an incident.

---

# Review Questions

1. What is the purpose of the Cyber Kill Chain?
2. Name the seven stages of the Cyber Kill Chain.
3. What happens during the reconnaissance stage?
4. Why may weaponization be difficult for a SOC to observe directly?
5. Give two examples of delivery methods.
6. What is exploitation?
7. Why is installation important to an attacker?
8. What is Command and Control (C2)?
9. Give three examples of suspicious network activity that may indicate C2.
10. What types of activity may occur during Actions on Objectives?
11. At which stages can a SOC Analyst potentially detect malicious activity?
12. Why is early detection important during an attack?

---

# Further Reading

* Lockheed Martin Cyber Kill Chain
* MITRE ATT&CK
* NIST Cybersecurity Framework
* Microsoft Security Documentation
* Microsoft Defender XDR Documentation
* Microsoft Sentinel Documentation

---

> **Interview Tip**
>
> Employers may ask:
>
> "What is the Cyber Kill Chain?"
>
> A strong answer is:
>
> "The Cyber Kill Chain is a model that describes seven stages of a cyber attack, from reconnaissance through actions on objectives. It helps security teams understand attacker behavior and identify opportunities to detect and disrupt attacks."

---

> **SC-200 Exam Note**
>
> Understand how attack activity can generate security telemetry across endpoints, identities, applications, and networks.
>
> Be able to connect suspicious activity with investigation and response activities using Microsoft Defender XDR and Microsoft Sentinel.
>
> Pay particular attention to how security alerts, endpoint activity, authentication events, network connections, and threat intelligence can help analysts identify different stages of an attack.

---

# Key Terms

* Cyber Kill Chain
* Reconnaissance
* Weaponization
* Delivery
* Exploitation
* Installation
* Command and Control (C2)
* Actions on Objectives
* Malware
* Persistence
* Phishing
* Threat Intelligence
* Threat Hunting
* Incident Response
* Security Monitoring
* Endpoint Detection
* Network Monitoring

