# Day 16 – SQL Injection, XSS, SSRF & Cryptographic Failures (Week 4)

**Date:** 24 July 2026  
---

# Objective

To gain practical experience in identifying and understanding common web application vulnerabilities by solving hands-on labs from PortSwigger Web Security Academy and TryHackMe. Today's session focused on SQL Injection, Cross-Site Scripting (XSS), Server-Side Request Forgery (SSRF), and Cryptographic Failures.

---

# Topics Covered

- PortSwigger Web Security Academy
- SQL Injection (SQLi)
- SQL Injection Authentication Bypass
- Burp Suite Repeater
- Cross-Site Scripting (XSS)
- Reflected XSS
- Server-Side Request Forgery (SSRF)
- TryHackMe – Cryptographic Failures
- Secure Input Validation
- Secure Authentication
- Secure Cryptographic Practices

---

# SQL Injection (SQLi)

**SQL Injection (SQLi)** is a web vulnerability that occurs when an application improperly validates user input before using it in SQL queries. Attackers may manipulate database queries to retrieve or modify unintended information.

### Types of SQL Injection

- Authentication Bypass
- Union-Based SQL Injection
- Error-Based SQL Injection
- Blind SQL Injection

### Example

Instead of validating user input safely, a vulnerable application may directly include user input in a database query, allowing the query's behavior to be altered.

---

# Practical Activity – SQL Injection Authentication Bypass

The session began with a **PortSwigger Web Security Academy** lab demonstrating a vulnerable login page.

Using **Burp Suite Repeater**, I analyzed the HTTP requests sent by the application and observed how user input was processed by the backend. The exercise demonstrated how insecure handling of database queries can lead to authentication bypass in intentionally vulnerable training environments.

The lab emphasized:

- Intercepting requests with Burp Suite
- Analyzing HTTP parameters
- Understanding authentication logic
- Recognizing insecure database query handling

---

# Burp Suite Repeater

**Burp Suite Repeater** allows security testers to resend and modify HTTP requests in a controlled environment.

It is commonly used to:

- Inspect application responses
- Modify request parameters
- Validate vulnerabilities
- Understand application behavior

During today's session, Repeater was used to inspect requests sent to the vulnerable login page and observe how different inputs affected server responses.

---

# Cross-Site Scripting (XSS)

Cross-Site Scripting (XSS) occurs when an application allows untrusted input to be executed as client-side JavaScript within another user's browser.

### Types of XSS

- Reflected XSS
- Stored XSS
- DOM-Based XSS

### Practical Understanding

Using intentionally vulnerable lab environments, I studied how insufficient input validation can result in reflected XSS. The session also examined the application's source code to understand how user input was processed and why proper output encoding and input validation are essential for preventing XSS attacks.

---

# Server-Side Request Forgery (SSRF)

**Server-Side Request Forgery (SSRF)** is a vulnerability that allows a web server to make requests to unintended internal or external resources on behalf of an attacker.

### Example

A web application that fetches remote images may be manipulated into requesting internal network resources if proper validation is not implemented.

### Practical Activity

Completed a **basic SSRF** lab to understand:

- How SSRF vulnerabilities occur
- Why user-controlled URLs are dangerous
- The importance of server-side validation and request filtering

---

# TryHackMe – Cryptographic Failures

The second practical exercise involved the **Cryptographic Failures** room on TryHackMe.

The room focused on understanding how improper cryptographic implementations can expose sensitive information.

Topics explored included:

- Weak encryption practices
- Insecure password storage
- Sensitive data exposure
- Secure transmission of information
- Importance of modern cryptographic standards

The room highlighted that many security incidents occur because organizations use outdated or improperly implemented cryptographic mechanisms rather than flaws in the encryption algorithms themselves.

---

# Secure Development Practices

Today's labs reinforced several secure coding principles:

- Validate and sanitize user input.
- Use parameterized queries to prevent SQL Injection.
- Encode user output to mitigate XSS.
- Never trust user-controlled URLs without validation.
- Implement strong authentication and authorization controls.
- Protect sensitive information using modern cryptographic standards.
- Regularly test applications for common OWASP Top 10 vulnerabilities.

---

# Practical Activities

### PortSwigger Web Security Academy

Completed practical labs on:

- SQL Injection Authentication Bypass
- Reflected Cross-Site Scripting (XSS)
- Basic Server-Side Request Forgery (SSRF)

### TryHackMe

Completed the **Cryptographic Failures** room to understand how weak cryptographic implementations can compromise application security.

---

# Key Learnings

- Understood how SQL Injection affects authentication mechanisms.
- Learned to analyze HTTP requests using Burp Suite Repeater.
- Explored Reflected Cross-Site Scripting and secure input validation.
- Understood the fundamentals of Server-Side Request Forgery.
- Learned the importance of secure cryptographic implementation.
- Strengthened practical web application testing skills through hands-on labs.
- Reinforced multiple OWASP Top 10 concepts using real-world training environments.

---

# Reflection

Today's session combined multiple web application security concepts into practical exercises. Working through PortSwigger labs improved my understanding of how vulnerabilities such as SQL Injection, XSS, and SSRF arise due to insecure application design and improper input handling. Completing the TryHackMe Cryptographic Failures room highlighted the importance of protecting sensitive information through strong encryption and secure implementation practices. Overall, the combination of theory and hands-on practice strengthened my understanding of secure web application development and penetration testing methodologies.

---

# Assignment

- Complete additional PortSwigger SQL Injection labs.
- Practice more XSS and SSRF scenarios in controlled environments.
- Revise the OWASP Top 10 (2025) vulnerabilities.
- Continue exploring secure cryptographic implementations and best practices.

---

# Screenshots

The screenshots for today's session demonstrate:

- **SQL Injection authentication bypass** lab on PortSwigger Web Security Academy.
- **Burp Suite Repeater** used for analyzing and modifying HTTP requests.
- **DVWA Reflected XSS** lab for understanding client-side input validation issues.
- **Source code review** illustrating how improper input handling can introduce XSS vulnerabilities.

All screenshots are available in the **`screenshots/`** directory.