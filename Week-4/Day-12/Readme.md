# Day 12 – OWASP Top 10 & Web Application Security (Week 4)

**Date:** 20 July 2026

---

# Objective

To understand the fundamentals of Web Application Penetration Testing (WAPT), explore the OWASP Top 10 (2025), learn access control mechanisms, and identify common web application vulnerabilities through theory and practical labs.

---

# Topics Covered

- Web Application Penetration Testing (WAPT)
- OWASP Foundation
- OWASP Top 10 (2025)
- OWASP Mobile Top 10
- A01: Broken Access Control
- CIA Triad (Revision)
- IDOR (Insecure Direct Object Reference)
- Privilege Escalation
- RBAC, MAC & DAC
- Website Security Checker
- Gobuster (Revision)
- Hydra (Revision)
- Thunder Cipher Lab – **DeleteMe**

---

# What is WAPT?

**Web Application Penetration Testing (WAPT)** is the process of identifying security vulnerabilities in web applications before attackers can exploit them.

**Example:** Testing whether a normal user can access or modify administrator-only resources.

---

# OWASP Top 10 (2025)

| Vulnerability | Description | Example |
|---------------|-------------|---------|
| **A01 – Broken Access Control** | Users can perform actions beyond their permissions. | Accessing another user's account by changing the user ID. |
| **A02 – Cryptographic Failures** | Sensitive data is not properly protected. | Passwords stored without encryption. |
| **A03 – Injection** | Malicious input is executed as commands or queries. | SQL Injection bypassing login. |
| **A04 – Insecure Design** | Security flaws caused by poor application design. | Missing rate limiting on login pages. |
| **A05 – Security Misconfiguration** | Unsafe default or incorrect server settings. | Directory listing enabled. |
| **A06 – Vulnerable Components** | Using outdated software or libraries. | Running an application with vulnerable dependencies. |
| **A07 – Identification & Authentication Failures** | Weak authentication or session handling. | Weak passwords or predictable session IDs. |
| **A08 – Software & Data Integrity Failures** | Trusting unverified software or updates. | Installing unsigned plugins. |
| **A09 – Security Logging & Monitoring Failures** | Lack of proper logging and alerting. | Failed login attempts are not monitored. |
| **A10 – Server-Side Request Forgery (SSRF)** | Server makes unauthorized requests on behalf of an attacker. | Accessing internal cloud metadata through the server. |

---

# Access Control Concepts

## IDOR (Insecure Direct Object Reference)

Allows users to access another user's resources by modifying an identifier.

**Example**

```
/profile?id=101
```

Changing it to

```
/profile?id=102
```

may expose another user's information.

---

## Privilege Escalation

A user gains permissions beyond their intended role.

**Example:** A standard user obtains administrator privileges.

---

## RBAC (Role-Based Access Control)

Permissions are assigned according to user roles.

**Example**

- Admin → Full Access
- Manager → Edit
- Employee → Read Only

---

## DAC (Discretionary Access Control)

The resource owner decides who can access the resource.

**Example:** Sharing a Google Drive file with selected users.

---

## MAC (Mandatory Access Control)

Access is enforced by predefined security policies.

**Example:** Classified government documents accessible only to users with the required clearance.

---

# CIA Triad (Revision)

- **Confidentiality** – Protect information from unauthorized access.
- **Integrity** – Ensure information remains accurate and unaltered.
- **Availability** – Ensure systems remain accessible to authorized users.

---

# Tool Revision

## Gobuster

**Gobuster** is a directory and file enumeration tool used to discover hidden resources on a web server.

**Example:** Finding hidden directories such as `/admin`, `/backup`, or `/uploads` using a wordlist.

---

## Hydra

**Hydra** is a password auditing tool used to test login credentials against various network services.

**Example:** Testing SSH or FTP login credentials in an authorized penetration testing environment using a predefined wordlist.

---

# Practical Activity

- Learned the OWASP Top 10 (2025) vulnerabilities.
- Studied access control mechanisms and authorization flaws.
- Revised Gobuster and Hydra.
- Solved the **Thunder Cipher DeleteMe Lab**, demonstrating **Broken Access Control** and **IDOR** in a controlled environment.

---

# Key Learnings

- Understood the importance of secure access control.
- Learned the OWASP Top 10 vulnerabilities with practical examples.
- Differentiated between RBAC, DAC, and MAC.
- Revised the use of Gobuster for enumeration and Hydra for password auditing.
- Applied authorization concepts through the DeleteMe lab.

---

# Reflection

Today's session strengthened my understanding of web application security by focusing on common vulnerabilities and access control mechanisms. The practical DeleteMe lab demonstrated how Broken Access Control and IDOR can lead to unauthorized actions, while revisiting Gobuster and Hydra reinforced the importance of proper enumeration and credential testing during authorized security assessments.

---

# Assignment

- Revise the OWASP Top 10 (2025).
- Practice identifying Broken Access Control and IDOR in safe lab environments.
- Complete additional Thunder Cipher and PortSwigger Web Security Academy labs.
- Solve lab on TryHackMe called LinPrivSec

---

# Screenshots

Screenshots from today's session and the DeleteMe lab are available in the `screenshots/` directory.