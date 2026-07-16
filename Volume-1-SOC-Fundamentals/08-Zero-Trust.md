# Real-World Example

An employee attempts to sign in from a new country using an unmanaged device.

Zero Trust policies:

1. Detect the unusual sign-in.
2. Require Multi-Factor Authentication (MFA).
3. Evaluate device compliance.
4. Assess the user's sign-in risk.
5. Block or restrict access if the calculated risk exceeds organizational policy.
6. Generate an alert for the Security Operations Center (SOC).

The SOC Analyst investigates the event by reviewing authentication logs, device information, user activity, and related alerts to determine whether the sign-in is legitimate or malicious.

If the activity is confirmed to be malicious, the analyst escalates the incident, revokes active sessions, resets the user's credentials, and documents the investigation according to the organization's incident response procedures.

---

# Benefits of Zero Trust

Implementing a Zero Trust security model provides several advantages:

- Stronger identity protection
- Reduced attack surface
- Continuous verification of users and devices
- Improved visibility across the environment
- Faster threat detection and response
- Better protection against credential theft
- Reduced impact of compromised accounts
- Support for regulatory and compliance requirements

---

# Summary

Zero Trust replaces the traditional "trust but verify" model with a "never trust, always verify" approach. By continuously validating users, devices, applications, and access requests, organizations can reduce their attack surface, limit the impact of compromised accounts, and improve their overall cybersecurity posture.

---

# Key Takeaways

- Never trust any user, device, or application by default.
- Verify every access request before granting access.
- Apply the principle of least privilege.
- Assume attackers may already be present within the environment.
- Continuously monitor identities, devices, and network activity.
- Zero Trust strengthens an organization's overall security posture.

---

# Review Questions

1. What is the primary principle of the Zero Trust security model?
2. Explain the principle of least privilege.
3. Why does Zero Trust operate under the assumption of breach?
4. Name at least three technologies commonly used to implement Zero Trust.
5. How does Zero Trust improve the work of a SOC Analyst?

---

# Further Reading

- Microsoft Zero Trust Guidance
- NIST SP 800-207: Zero Trust Architecture
- Microsoft Security Documentation
- Microsoft Entra ID Documentation

---

> **Interview Tip**
>
> Employers frequently ask:
>
> "What are the three principles of Zero Trust?"
>
> A strong answer is:
>
> - Verify explicitly
> - Use least privilege access
> - Assume breach

---

> **SC-200 Exam Note**
>
> Understand how Microsoft Entra ID, Conditional Access, Microsoft Defender XDR, and Microsoft Sentinel work together to implement Zero Trust principles. Expect scenario-based questions that require selecting the most appropriate security controls.

---

# Key Terms

- Zero Trust
- Multi-Factor Authentication (MFA)
- Conditional Access
- Least Privilege
- Assume Breach
- Device Compliance
- Identity Protection
- Risk-Based Access
