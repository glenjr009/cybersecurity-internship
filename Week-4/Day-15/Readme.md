# Day 15 – OWASP Top 10, Web Application Security & Vulnerability Research (Week 4)

**Date:** 23 July 2026  

---

# Objective

To strengthen the understanding of OWASP Top 10 vulnerabilities by solving practical labs on TryHackMe, learning to identify web technologies using Wappalyzer, exploring Exploit Database for known vulnerabilities, and studying common web application security risks through research and practical examples.

---

# Topics Covered

- TryHackMe – OWASP Top 10 Room
- OWASP Top 10 (2025)
- Broken Access Control (A01)
- Cross-Site Scripting (XSS)
- Wappalyzer
- Exploit Database (Exploit-DB)
- Website Technology Enumeration
- A04 – Insecure Design
- A07 – Identification & Authentication Failures
- A08 – Software & Data Integrity Failures
- A10 – Server-Side Request Forgery (SSRF)

---

# TryHackMe – OWASP Top 10

Today's practical session began with the **OWASP Top 10** room on TryHackMe. The room introduced the most critical web application security risks and demonstrated how insecure coding practices can lead to vulnerabilities in modern web applications.

The exercises focused on understanding the impact of these vulnerabilities and the importance of implementing secure development practices.

---

# Wappalyzer

**Wappalyzer** is a technology profiling tool that identifies the technologies used by a website.

It can detect:

- Programming Languages
- Web Frameworks
- CMS Platforms
- JavaScript Libraries
- Analytics Services
- Web Servers
- Operating Systems

### Example

While assessing a website, Wappalyzer may identify:

- WordPress
- PHP
- Apache
- Bootstrap
- jQuery

This information helps security professionals understand the target environment during reconnaissance.

---

# Exploit Database (Exploit-DB)

**Exploit Database** is a public repository containing proof-of-concept exploits and security advisories for known vulnerabilities.

It is commonly used to:

- Research CVEs
- Identify known software vulnerabilities
- Study proof-of-concept exploits
- Verify whether software versions contain publicly disclosed vulnerabilities

> During today's session, Exploit-DB was introduced as a research resource for understanding known vulnerabilities in software and web applications.

---

# OWASP Top 10 Vulnerabilities Discussed

## A01 – Broken Access Control

Occurs when users can access resources or perform actions beyond their intended permissions.

**Example**

A normal user accesses another user's account simply by modifying the user ID in the URL.

---

## Cross-Site Scripting (XSS)

XSS occurs when an application allows malicious scripts to execute inside another user's browser.

### Types of XSS

- Reflected XSS
- Stored XSS
- DOM-Based XSS

**Example**

A comment field accepts JavaScript without validation, causing every visitor's browser to execute the injected script.

---

## A04 – Insecure Design

Applications fail to implement adequate security controls during the design phase.

**Example**

A login page without account lockout or rate limiting allows brute-force attacks.

---

## A07 – Identification & Authentication Failures

Weak authentication mechanisms allow attackers to compromise user accounts.

**Example**

- Weak passwords
- Predictable session IDs
- Missing Multi-Factor Authentication
- Poor session management

---

## A08 – Software & Data Integrity Failures

Occurs when applications trust software updates or data without proper verification.

**Example**

Installing unsigned software updates or executing unverified plugins.

---

## A10 – Server-Side Request Forgery (SSRF)

Allows attackers to force a server to send requests to unintended internal or external resources.

**Example**

A vulnerable image-fetch feature accesses internal cloud metadata instead of public URLs.

---

# Website Research Activity

As part of today's session, we analyzed websites to understand:

- Technologies powering the application
- Server information
- Frameworks and CMS platforms
- Publicly available software details
- Potential attack surface

The activity demonstrated how reconnaissance plays an important role before performing any authorized security assessment.

---

# Practical Activities

### TryHackMe – OWASP Top 10 Room

- Studied common web application vulnerabilities.
- Explored Broken Access Control and Cross-Site Scripting.
- Learned secure authentication practices.
- Understood software integrity risks.
- Explored SSRF attacks conceptually.

### Website Technology Enumeration

- Identified website technologies using **Wappalyzer**.
- Researched publicly known vulnerabilities using **Exploit Database**.
- Analyzed websites to understand their technology stack.

---

# Key Learnings

- Understood the importance of the OWASP Top 10.
- Learned how Broken Access Control remains one of the most critical web vulnerabilities.
- Explored Cross-Site Scripting (XSS) and its impact.
- Learned how Wappalyzer assists during reconnaissance.
- Understood the purpose of Exploit Database for vulnerability research.
- Explored authentication weaknesses and secure authentication practices.
- Learned about Software & Data Integrity Failures and SSRF.
- Strengthened reconnaissance and web application assessment skills.

---

# Reflection

Today's session focused on understanding the most common web application vulnerabilities through both theoretical concepts and practical exercises. Solving the TryHackMe OWASP Top 10 room reinforced how vulnerabilities such as Broken Access Control and Cross-Site Scripting can affect real-world applications. Learning to use tools like Wappalyzer and Exploit Database also highlighted the importance of reconnaissance and vulnerability research before conducting authorized security assessments.

---

# Assignment

- Complete the remaining TryHackMe OWASP Top 10 challenges.
- Revise the OWASP Top 10 (2025).
- Explore additional vulnerabilities on Exploit Database.
- Practice identifying website technologies using Wappalyzer.

---

# Screenshots

Screenshots from today's TryHackMe room and website analysis activities are available in the **`screenshots/`** directory.