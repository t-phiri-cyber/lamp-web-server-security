# Cross-Site Scripting (XSS) Evidence

Evidence and documentation from the controlled educational assessment demonstrating the identification of a Cross-Site Scripting (XSS) vulnerability.

## Assessment

XSS testing was performed against the search functionality of the LAMP web application.

A JavaScript payload was entered into the search field. The application processed the input and executed the supplied script in the browser.

The test produced a JavaScript popup containing the test message:

> Haha, you have been hacked

This demonstrated that user-controlled input was being rendered without sufficient input validation or output encoding.

## Result

**Finding:** XSS vulnerability identified

**Location:** Application search functionality

**Test result:** JavaScript executed successfully

**Remediation status:** Not completed during the assessment timeframe

## Security Impact

Successful XSS exploitation can potentially allow an attacker to:

- Execute JavaScript in a user's browser
- Manipulate web page content
- Perform actions in the context of the affected user
- Access information available to browser-side scripts, depending on application controls
- Conduct phishing or session-related attacks depending on the application's security configuration

## Recommended Remediation

Recommended controls include:

- Server-side input validation
- Context-appropriate output encoding
- HTML sanitisation where required
- Content Security Policy (CSP)
- Secure handling of user-supplied search input
- Retesting after remediation

## Evidence Limitation

No screenshots were captured for the XSS test during the assessment.

The finding is documented based on the test performed during the controlled educational assessment and is therefore recorded as an identified vulnerability rather than a remediated control.

## Scope

Testing was performed only against the controlled educational application used for the project.

No unauthorised systems were targeted.
