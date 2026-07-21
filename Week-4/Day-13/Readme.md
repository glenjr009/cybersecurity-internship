# Day 13 – Access Control & Linux Privilege Escalation (Week 4)

**Date:** 21 July 2026

**Duration:** 6:30 PM – 8:30 PM

---

# Objective

To strengthen the understanding of access control vulnerabilities, privilege escalation techniques, and secure authorization mechanisms through theory and hands-on labs using TryHackMe and PortSwigger Web Security Academy.

---

# Topics Covered

- IAAA Security Model
- Access Control Vulnerabilities
- Broken Access Control (Revision)
- Linux Privilege Escalation
- Referer-Based Access Control
- GTFOBins
- TryHackMe – Linux PrivEsc Room
- PortSwigger Lab – Referer-Based Access Control

---

# IAAA Security Model

The IAAA model defines the core principles used to secure systems and manage user access.

### Identification

The process of claiming an identity.

**Example:** Entering a username such as `glen123`.

---

### Authentication

Verifying that the claimed identity is genuine.

**Example:** Logging in using a password, OTP, or fingerprint.

---

### Authorization

Determining what an authenticated user is allowed to access.

**Example:** An administrator can manage users, while a normal user can only view their own profile.

---

### Accounting (Auditing)

Recording user activities for monitoring and investigation.

**Example:** Logging successful logins, failed login attempts, and file modifications.

---

# Access Control Vulnerabilities

Access control vulnerabilities occur when applications fail to properly restrict users from accessing resources or performing actions beyond their permissions.

Common causes include:

- Missing authorization checks
- Improper role validation
- Direct object reference vulnerabilities
- Client-side access control

---

# Broken Access Control (Revision)

Broken Access Control occurs when users can access resources or perform actions outside their intended permissions.

### Example

A regular user changes:

```
/profile?id=1001
```

to

```
/profile?id=1002
```

and gains access to another user's profile.

This is one of the most critical vulnerabilities in the OWASP Top 10.

---

# Linux Privilege Escalation

Privilege escalation is the process of obtaining higher privileges on a system after initial access.

Common techniques include:

- Exploiting SUID binaries
- Weak file permissions
- Misconfigured services
- Cron job abuse
- Kernel vulnerabilities

**Example**

A low-privileged user exploits a vulnerable SUID binary to gain root privileges.

---

# Referer-Based Access Control

Some applications rely on the **Referer** HTTP header to authorize requests.

Since HTTP headers can be modified, relying solely on the Referer header is insecure.

### Example

A web application only allows administrators to access:

```
/admin/deleteUser
```

by checking whether the request comes from:

```
/admin
```

An attacker can manually modify the Referer header using Burp Suite and bypass this protection if no server-side authorization exists.

---

# GTFOBins

**GTFOBins** is a curated collection of Unix binaries that can be abused to perform privilege escalation, bypass restrictions, transfer files, or spawn shells.

It is widely used during Linux privilege escalation assessments.

### Example

Using the `find` binary to spawn a shell:

```bash
find . -exec /bin/sh \; -quit
```

This works only when the binary can be executed with elevated privileges.

---

# Practical Activities

### TryHackMe – Linux Privilege Escalation

During the lab, we explored:

- Linux enumeration
- SUID binaries
- File permissions
- Privilege escalation techniques
- Identifying common Linux misconfigurations

---

### PortSwigger Lab – Referer-Based Access Control

The lab demonstrated how applications relying solely on the Referer header for authorization can be bypassed.

Using Burp Suite, the HTTP request was modified to manipulate the Referer header and successfully access restricted functionality in the controlled lab environment.

---

# Key Learnings

- Understood the IAAA security model.
- Learned how broken access control occurs.
- Explored Linux privilege escalation concepts.
- Understood why Referer headers should never be trusted for authorization.
- Learned how GTFOBins assists during Linux privilege escalation.
- Completed practical labs on TryHackMe and PortSwigger.

---

# Reflection

Today's session emphasized the importance of implementing proper authorization and secure privilege management. The hands-on labs demonstrated how seemingly small security misconfigurations can lead to privilege escalation or unauthorized access. Learning about GTFOBins also highlighted the importance of understanding native Linux utilities during security assessments.

---

# Assignment

- Complete additional Linux Privilege Escalation rooms on TryHackMe.
- Explore more GTFOBins examples.
- Practice PortSwigger access control labs.
- Revise the IAAA security model and authorization concepts.

---

# Screenshots

Screenshots from today's labs are available in the `screenshots/` directory.