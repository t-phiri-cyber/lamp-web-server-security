# LAMP Web Server Security Assessment & Hardening

## 📌 Project Overview

This project involved the security assessment, vulnerability testing and hardening of a LAMP-based web application hosted on Ubuntu Linux.

The objective was to identify common web application and server security weaknesses, test defensive controls, and implement security improvements to reduce the identified risks.

## 🖥️ Environment

### Hardware
- Raspberry Pi 4 Model B
- Cisco Meraki Router
- Netgear 8-Port Switch

### Operating System & Software
- Ubuntu 22.04 LTS
- Apache
- MySQL
- PHP
- Python
- Flask

### Security Tools & Controls
- ModSecurity
- Fail2ban
- HTTPS/TLS assessment
- Apache security configuration

## 🔎 Security Testing

The application was assessed for several common security weaknesses within a controlled lab environment.

### SQL Injection

Testing identified a SQL injection vulnerability within the application's search functionality.

**Finding:**  
User-supplied search input was not adequately protected against SQL injection.

**Remediation:**  
ModSecurity rules were implemented to detect and block malicious SQL injection patterns.

**Result:**  
The test request was blocked and redirected to a forbidden response.

---

### Cross-Site Scripting (XSS)

The application was tested for reflected XSS by submitting JavaScript through user-controlled input.

**Finding:**  
The application was capable of processing malicious script input.

**Risk:**  
Successful XSS could allow malicious JavaScript to execute in a user's browser.

**Recommendation:**  
Implement appropriate input validation, output encoding and secure application development practices.

---

### Authentication Security

Customer and administrative login functionality was assessed for password security.

**Finding:**  
Weak password practices were identified.

**Recommendations:**
- Enforce stronger password requirements
- Implement multi-factor authentication
- Apply account lockout/rate-limiting controls
- Store passwords using secure hashing mechanisms

---

## 🛡️ Server Hardening

Several Apache security controls were implemented.

### Server Banner Removal

Apache server information was restricted to reduce unnecessary information disclosure.

### Directory Listing

Directory listing was disabled to prevent users from browsing directory contents that should not be publicly accessible.

### ModSecurity

ModSecurity was configured as a web application firewall to help detect and block malicious requests.

### Fail2ban

Fail2ban was configured to detect repeated authentication failures and provide automated IP banning.

Testing identified that the banning response was not immediate during initial testing, highlighting the importance of validating security controls after deployment.

## 🌐 HTTPS

The application initially operated over HTTP rather than HTTPS.

**Recommendation:**

Implement TLS certificates and configure HTTPS to protect data transmitted between users and the web server.

## 📊 Security Objectives

The project included the following security objectives:

- Regular security software checks
- Security updates within 24 hours where appropriate
- Strong password policies
- Multi-factor authentication
- Secure server configuration
- Protection against common web application attacks
- Compliance considerations relating to data protection

## 🧠 Key Learning Outcomes

This project provided practical experience in:

- Linux server administration
- Apache configuration
- Web application security testing
- Vulnerability identification
- SQL injection testing
- XSS testing
- Web application firewall configuration
- Intrusion prevention
- Server hardening
- Security documentation
- Risk mitigation

## ⚠️ Ethical & Legal Scope

All security testing described in this repository was performed within a controlled environment for educational and defensive security purposes.

No unauthorised systems were targeted.

## 🚀 Future Improvements

Potential future improvements include:

- Full HTTPS implementation
- Two-factor authentication
- Improved password policies
- Centralised security logging
- Additional network monitoring
- Improved physical security controls
- Data Protection Officer review where required
- Microsoft security tooling integration
