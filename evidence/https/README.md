# HTTPS / SSL-TLS Assessment

Documentation of the HTTPS and SSL/TLS security assessment performed during the controlled educational project.

## Finding

The web application was observed operating over HTTP rather than HTTPS during the assessment.

This meant that communications between the client and web server were not protected by TLS.

## Security Impact

Using HTTP without TLS can expose network communications to risks including:

- Interception of transmitted data
- Exposure of credentials or other sensitive information
- Man-in-the-middle attacks
- Loss of confidentiality and integrity of web traffic

The actual risk depends on the network environment and the type of information transmitted by the application.

## Assessment Result

The use of HTTP was identified as a security weakness during the assessment.

SSL/TLS implementation was identified as a required future remediation.

HTTPS was not implemented within the available assessment timeframe.

## Recommended Remediation

Recommended controls include:

- Obtain a valid TLS certificate.
- Configure Apache to support HTTPS.
- Redirect HTTP traffic to HTTPS.
- Disable insecure HTTP access where appropriate.
- Configure modern TLS protocols and secure cipher suites.
- Verify certificate validity and configuration.
- Retest the application after implementation.

## Evidence Limitation

No separate screenshot was captured specifically for the HTTPS finding.

The finding is documented based on the application behaviour observed during the controlled educational assessment.

## Scope

All testing was performed against the controlled educational environment used for the project.

No unauthorised systems were targeted.
