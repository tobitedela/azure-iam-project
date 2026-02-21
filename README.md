---

# Securing Microsoft 365 with Microsoft Entra ID

## Identity and Access Management (IAM) Implementation Project

---

## Project Overview

Modern cloud environments are identity-driven. In Microsoft 365, identity is the control plane — if identity is compromised, the entire tenant is compromised.

This project demonstrates the implementation of Identity and Access Management (IAM) controls using **Microsoft Entra ID** to strengthen the security posture of a Microsoft 365 environment.

The goal was to simulate real-world identity governance practices including role-based access control (RBAC), external collaboration security, consent governance, audit monitoring, and privilege review.

---

## Objectives

* Implement secure identity provisioning
* Apply least privilege access control
* Govern external (B2B) collaboration
* Strengthen application consent security
* Monitor identity activity through logs
* Review and export privileged role assignments

---

## [Actions Taken](/IAM_Steps_Screenshots_Explanations.pdf)
📄 **Note:** GitHub may not render this PDF inline. Click **Download** to view the full step-by-step walkthrough with screenshots.
---
# Security Controls Implemented
---

## 1️⃣ Identity Provisioning & Role-Based Access Control (RBAC)

### Actions Performed:

* Created three users:

  * DevUser1
  * DevUser2
  * DevUser3
* Assigned **User Administrator** role to DevUser1
* Verified role assignments in Entra ID

### Security Principle Applied:

**Least Privilege**

### Risk Mitigated:

* Overprivileged accounts
* Privilege abuse
* Accidental administrative misconfiguration

---

## 2️⃣ Group-Based Access Management

### Actions Performed:

* Created security group: `AppDevTeam`
* Added DevUser1 and DevUser2 as members

### Why This Matters:

Group-based access reduces:

* Manual access assignment errors
* Orphaned permissions
* Administrative overhead

### Security Impact:

* Centralized access governance
* Simplified access revocation
* Reduced attack surface

---

## 3️⃣ External Collaboration (B2B Access)

### Actions Performed:

* Invited external guest user (personal email)
* Added external user to `AppDevTeam`
* Verified guest sign-in activity

### Risk Considered:

External collaboration introduces:

* Data leakage risk
* Unauthorized tenant access
* Shadow IT behaviors

### Security Benefit:

* Controlled B2B access model
* Centralized monitoring
* Policy-enforced collaboration

---

## 4️⃣ Application Consent Governance

### Actions Performed:

* Reviewed Identity Secure Score recommendations
* Disabled user ability to grant consent to unreliable applications
* Enabled admin consent workflow
* Added DevUser3 as reviewer
* Set request expiry to 2 days

### Why This Is Critical:

Malicious OAuth apps often request:

* Mailbox access
* File access
* Directory read permissions

Without controls, users can unknowingly authorize data exfiltration.

### Risk Mitigated:

* OAuth abuse
* Token theft
* Unauthorized third-party data access

---

## 5️⃣ Monitoring & Audit Logs

### Actions Performed:

* Reviewed Audit Logs
* Reviewed Sign-in Logs
* Confirmed external user authentication activity

### Security Importance:

If you cannot see it, you cannot secure it.

Monitoring enables:

* Suspicious login detection
* Admin activity tracking
* Incident response readiness
* Compliance evidence

---

## 6️⃣ Secure Role Assignment Review

### Actions Performed:

* Navigated to Roles and Administrators
* Exported role assignments

### Governance Value:

* Visibility into privileged accounts
* Detection of excessive permissions
* Supports compliance frameworks (ISO 27001, NIST, SOC 2)

---

# Threat Model Perspective

Identity threats addressed in this project:

* Privilege escalation
* Excessive administrative rights
* OAuth consent abuse
* Guest access misconfiguration
* Lack of identity visibility
* Insider misuse

---

# Security Outcomes

* Implemented structured RBAC model
* Reduced administrative exposure
* Enforced app consent governance
* Established external collaboration controls
* Enabled audit trail monitoring
* Strengthened Microsoft 365 identity posture

---

# Key Takeaways

1. Identity is the primary attack surface in cloud environments.
2. Governance controls must accompany provisioning.
3. Monitoring is as important as configuration.
4. Application permissions are a major overlooked risk vector.
5. Least privilege is non-negotiable in production environments.

---

# Skills Demonstrated

* Microsoft Entra ID Administration
* Identity Governance
* Role-Based Access Control (RBAC)
* OAuth Application Security
* Audit Log Analysis
* Cloud Security Fundamentals
* Microsoft 365 Security Architecture

---

# 📚 References

* Microsoft Entra ID Documentation
* Microsoft Learn – Identity and Access Management
