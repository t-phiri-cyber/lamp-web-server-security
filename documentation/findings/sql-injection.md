# SQL Injection Security Assessment

## Overview

A controlled SQL injection assessment was conducted against the PHP/MySQL customer login functionality within the LAMP web application.

The objective was to determine whether user-controlled input could influence the application's SQL query and bypass the intended authentication controls.

## Initial Finding

Testing demonstrated that the login functionality was vulnerable to SQL injection.

Within the controlled lab environment, malicious input was able to influence the database query and demonstrate authentication bypass before remediation.

### Security Impact

SQL injection can potentially allow an attacker to:

- Bypass authentication
- Access unauthorised database information
- Modify or delete database records
- Compromise application functionality

The actual impact depends on the application's implementation and database permissions.

## Remediation

ModSecurity was implemented as a Web Application Firewall (WAF) to detect and block malicious requests.

The application was then retested using the same controlled testing approach.

## Validation

Following ModSecurity configuration, the malicious SQL injection request was blocked.

The application returned:

**HTTP 403 Forbidden**

This provided evidence that the implemented security control was preventing the tested malicious request.

## Testing Process

1. Identify the authentication endpoint.
2. Establish expected behaviour using valid credentials.
3. Conduct controlled SQL injection testing.
4. Record the initial result.
5. Configure ModSecurity.
6. Repeat the security test.
7. Compare pre- and post-remediation results.
8. Document the outcome.

## Results

| Test Stage | Result |
|---|---|
| Before remediation | SQL injection successfully demonstrated |
| Security control | ModSecurity WAF implemented |
| After remediation | Malicious request blocked |
| HTTP response | 403 Forbidden |

## Skills Demonstrated

- SQL injection testing
- Web application security assessment
- Authentication security
- ModSecurity WAF
- Security-control validation
- Before-and-after testing
- Vulnerability documentation
- Remediation evaluation

## Ethical Scope

All testing was performed against the controlled educational application used for the project.

No unauthorised systems were targeted.
