# Cross-Site Scripting (XSS) Security Assessment

## Overview

A controlled Cross-Site Scripting (XSS) assessment was conducted against the search functionality of the LAMP web application.

The objective was to determine whether user-controlled search input was being safely handled or whether supplied JavaScript could be executed by the application.

## Initial Finding

Testing demonstrated that the search functionality was vulnerable to XSS.

A JavaScript payload was entered through the search field. The application processed the input and executed the script in the user's browser, resulting in a JavaScript popup displaying the test message.

This demonstrated that user-controlled input was being rendered without sufficient input validation or output encoding.

## Security Impact

Successful XSS exploitation may allow an attacker to:

- Execute JavaScript in a user's browser
- Manipulate page content
- Perform actions in the context of the affected user
- Potentially access browser-accessible information
- Conduct phishing or session-related attacks depending on the application's security controls

The actual impact depends on the application's implementation and browser security controls.

## Remediation Status

XSS was identified and tested during the assessment.

Remediation was not completed within the available assessment timeframe.

Recommended controls include:

- Server-side input validation
- Context-appropriate output encoding
- HTML sanitisation where required
- Content Security Policy (CSP)
- Avoiding unsafe rendering of user-controlled input

## Validation

The vulnerability was successfully reproduced during testing by submitting JavaScript through the search functionality.

The application executed the supplied script and displayed the test popup.

No post-remediation validation was performed because the vulnerability was not remediated during the assessment.

## Skills Demonstrated

- XSS vulnerability testing
- Web application security assessment
- Input validation assessment
- Output encoding assessment
- Vulnerability documentation
- Security impact analysis
- Remediation recommendations

## Ethical Scope

All testing was performed against the controlled educational application used for the project.

No unauthorised systems were targeted.
