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

# CIA Triad

The CIA Triad is a fundamental cybersecurity model consisting of three core security principles:

1. Confidentiality
2. Integrity
3. Availability

These principles help organizations understand what security controls and protections are required to protect information systems and data.

For a SOC Analyst, the CIA Triad provides a useful way to understand the potential impact of security incidents.

---

# What is the CIA Triad?

The CIA Triad describes three objectives that information security controls commonly aim to protect.

### Confidentiality

Confidentiality means protecting information from unauthorized access or disclosure.

Examples include:

* Access controls
* Authentication
* Authorization
* Encryption
* Data classification
* Multi-factor authentication

A confidentiality breach occurs when information is accessed or disclosed by someone who is not authorized to access it.

### Integrity

Integrity means maintaining the accuracy, consistency, and trustworthiness of information.

Examples include:

* Hashing
* Digital signatures
* File integrity monitoring
* Access controls
* Change management
* Audit logging

An integrity violation occurs when information is changed, deleted, corrupted, or manipulated without appropriate authorization.

### Availability

Availability means ensuring that authorized users can access systems, services, and information when required.

Examples include:

* Backups
* Redundancy
* Disaster recovery
* High-availability systems
* System monitoring
* Capacity management

An availability incident may occur when ransomware, denial-of-service activity, system failure, or another event prevents legitimate users from accessing required resources.

---

# CIA Triad in SOC Operations

The CIA Triad helps SOC Analysts understand the potential security impact of an incident.

| Principle       | Security Concern                     | Example SOC Investigation                              |
| --------------- | ------------------------------------ | ------------------------------------------------------ |
| Confidentiality | Unauthorized access or disclosure    | Investigating stolen credentials or data exfiltration  |
| Integrity       | Unauthorized modification            | Investigating altered files, configurations, or logs   |
| Availability    | Loss of access or service disruption | Investigating ransomware or denial-of-service activity |

A single incident can affect more than one CIA principle.

For example, a ransomware attack may primarily affect availability, while data theft associated with the same attack may also affect confidentiality.

---

# Security Controls and the CIA Triad

Security controls can support one or more elements of the CIA Triad.

Examples include:

| Security Control            | Confidentiality | Integrity | Availability |
| --------------------------- | :-------------: | :-------: | :----------: |
| Encryption                  |        ✓        |           |              |
| Access Control              |        ✓        |     ✓     |              |
| Hashing                     |                 |     ✓     |              |
| Digital Signatures          |                 |     ✓     |              |
| Backups                     |                 |     ✓     |       ✓      |
| Redundancy                  |                 |           |       ✓      |
| Multi-Factor Authentication |        ✓        |           |              |
| File Integrity Monitoring   |                 |     ✓     |              |
| Disaster Recovery           |                 |           |       ✓      |

The purpose of this model is not to place every control into only one category. Many security controls contribute to multiple security objectives.

---

# SOC Analyst Perspective

When investigating a security alert, a SOC Analyst should consider how the activity could affect:

* Confidentiality
* Integrity
* Availability

For example, if a compromised account is suspected of accessing sensitive information, the analyst may investigate:

* Which account was used
* Which systems were accessed
* What information was accessed
* Whether data was downloaded or transferred
* Whether unauthorized changes occurred
* Whether other accounts or systems were affected

This helps the analyst understand both the technical activity and its potential security impact.

---

# Real-World Example — Ransomware

A ransomware attack encrypts company files.

### Confidentiality

Sensitive information may be exposed if attackers also access or steal company data.

### Integrity

Files are modified and encrypted, meaning their original state has been changed.

### Availability

Employees cannot access business systems and files while the affected resources are unavailable.

The SOC investigates the incident, isolates affected devices, restores backups, and improves security controls.

This demonstrates that one security incident can affect multiple elements of the CIA Triad.

---

# CIA Triad and Incident Response

The CIA Triad can also help analysts understand incident-response priorities.

For example:

* A **confidentiality** incident may require investigation of unauthorized access and possible data exposure.
* An **integrity** incident may require determining what information or systems were modified.
* An **availability** incident may require restoring affected services and limiting operational disruption.

During incident response, the analyst should collect evidence that helps determine which security objectives were affected.

The impact assessment can then support containment, eradication, recovery, and post-incident activities.

---

# Why the CIA Triad Matters

The CIA Triad provides a simple framework for thinking about cybersecurity risk.

It helps security teams:

* Identify what needs to be protected
* Understand the impact of security incidents
* Design appropriate security controls
* Prioritize security requirements
* Communicate security risks
* Support incident investigation
* Improve security monitoring

For SOC Analysts, the CIA Triad is particularly useful when explaining **why an alert matters**, not only what technical activity occurred.

---

# Key Takeaways

* The CIA Triad consists of Confidentiality, Integrity, and Availability.
* Confidentiality protects information from unauthorized access or disclosure.
* Integrity protects the accuracy and trustworthiness of information.
* Availability ensures authorized users can access systems and information when required.
* Security controls can support one or more CIA principles.
* A single security incident can affect multiple CIA principles.
* Ransomware can affect availability and integrity, and may also affect confidentiality when data is accessed or stolen.
* The CIA Triad helps SOC Analysts understand the potential impact of security incidents.

---

# Review Questions

1. What does the CIA Triad stand for?
2. What is confidentiality?
3. What is integrity?
4. What is availability?
5. Give two examples of confidentiality controls.
6. How does hashing support integrity?
7. Why are backups important for availability?
8. How can ransomware affect the CIA Triad?
9. Can one security incident affect more than one CIA principle? Explain.
10. How does the CIA Triad help SOC Analysts understand security incidents?

---

# Further Reading

* NIST Cybersecurity Framework
* Microsoft Security Documentation
* CIS Critical Security Controls

---

# Interview Tip

**Question:** What is the CIA Triad and why is it important to a SOC Analyst?

**Answer:**

The CIA Triad represents confidentiality, integrity, and availability. It provides a fundamental framework for understanding information-security objectives and assessing the potential impact of security incidents. A SOC Analyst can use these principles to understand what was affected during an incident and help prioritize investigation and response activities.

---

# SC-200 Exam Note

When studying for the Microsoft Security Operations Analyst certification, connect the CIA Triad to practical security operations.

Important areas include:

* Security monitoring
* Identity and access protection
* Data protection
* Endpoint security
* Incident investigation
* Threat detection
* Incident response
* Recovery and remediation

A useful way to think about the relationship is:

**Security telemetry → Detection → Investigation → Impact Assessment → Response**

The CIA Triad helps provide context for the **impact assessment** part of this process.

---

# Key Terms

| Term              | Meaning                                                                                    |
| ----------------- | ------------------------------------------------------------------------------------------ |
| CIA Triad         | Confidentiality, Integrity, and Availability                                               |
| Confidentiality   | Protection of information from unauthorized access or disclosure                           |
| Integrity         | Protection of information from unauthorized modification or destruction                    |
| Availability      | Ensuring authorized access to systems, services, and information                           |
| Encryption        | A method used to protect information by transforming it into an encoded form               |
| Hashing           | A process that produces a fixed-length value used to help verify data integrity            |
| Authentication    | Verification of an identity                                                                |
| Authorization     | Determining what an authenticated user or system is permitted to access                    |
| Backup            | A copy of data or systems that can be used for restoration                                 |
| Redundancy        | Use of additional resources or components to improve resilience and availability           |
| Data Exfiltration | Unauthorized transfer of data from an environment                                          |
| Ransomware        | Malicious software that can prevent access to data or systems, commonly by encrypting data |

