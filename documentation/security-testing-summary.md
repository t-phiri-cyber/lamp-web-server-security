# Security Testing Summary

## Project Scope

Security assessment and hardening of a LAMP-based web application hosted on Ubuntu 22.04.

Testing was conducted within a controlled educational lab environment.

## Security Testing Methodology

Testing followed a structured process:

1. Identify the security objective
2. Establish the expected result
3. Conduct the security test
4. Record the actual result
5. Implement remediation where required
6. Retest the security control
7. Evaluate the outcome

## Key Findings

| Area | Finding | Remediation / Outcome |
|---|---|---|
| SQL Injection | SQL injection was demonstrated against a PHP/MySQL customer login | ModSecurity was implemented and subsequent malicious requests returned HTTP 403 Forbidden |
| XSS | XSS was demonstrated through the search functionality during application testing | Remediation was not completed, input and output-encoding improvements were recommended |
| Server Information Disclosure | Apache exposed unnecessary server information | `ServerTokens` and `ServerSignature` were modified to reduce information disclosure |
| Directory Listing | Apache directory contents were accessible | `Options -Indexes` was implemented and access returned HTTP 403 Forbidden |
| SSH Brute Force | Repeated failed SSH authentication attempts were tested against Fail2Ban | Fail2Ban behaviour was investigated, logs analysed and successful IP banning verified during retesting |
| HTTPS | The application was observed using HTTP during the assessment  | SSL/TLS implementation was identified as a future remediation requirement |

## Security Controls Evaluated

### ModSecurity

ModSecurity was configured as a Web Application Firewall (WAF).

SQL injection testing was performed before and after implementation. Following configuration, malicious requests were blocked and returned an HTTP 403 Forbidden response.

### Fail2Ban

Fail2Ban was configured to detect repeated SSH authentication failures.

Initial testing did not immediately produce the expected IP ban. The behaviour was investigated and the control was subsequently retested successfully.

Fail2Ban logs were analysed to identify authentication failures and Ban/Unban events.

### Apache Hardening

Apache configuration was hardened to reduce unnecessary information disclosure and directory exposure.

Controls included:

- `ServerTokens`
- `ServerSignature`
- `Options -Indexes`

The controls were subsequently tested to verify their effect.

## Log Analysis

The project included analysis of:

- Apache logs
- ModSecurity audit logs
- Fail2Ban logs

Log analysis was used to investigate security events and validate the behaviour of implemented controls.

## Project Outcome

The assessment demonstrated practical experience in:

- Vulnerability identification
- Web application security testing
- SQL injection testing
- XSS identification
- Security-control validation
- Apache hardening
- ModSecurity WAF configuration
- Fail2Ban testing
- Security log analysis
- Before-and-after testing
- Remediation evaluation
- Security documentation

## Scope and Ethics

All testing was performed within a controlled educational environment.

No unauthorised systems were targeted.
