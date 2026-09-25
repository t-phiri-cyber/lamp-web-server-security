# HTTP / HTTPS Security Assessment

Documentation and evidence of the HTTP/HTTPS security finding identified during the controlled educational security assessment.

## Finding

The web application was accessed using HTTP rather than HTTPS.

The browser displayed **"Not secure"**, indicating that the connection was not protected by HTTPS/TLS.

The application was also accessed using a direct IP address rather than a configured domain name.

## Security Impact

Using HTTP means traffic between the browser and web server is not protected by TLS encryption.

Depending on the type of information transmitted, unencrypted HTTP traffic may be vulnerable to interception or modification in transit.

Using a direct IP address also provides a less conventional user-facing configuration than accessing the application through a registered domain.

## Evidence

### HTTP Connection

[View HTTP / Not Secure evidence](./01-http-not-secure.png)

The browser address bar shows:

- HTTP rather than HTTPS
- **Not secure** browser warning
- Direct IP-based access

The IP address has been redacted from the public evidence image.

## Recommended Remediation

The recommended remediation was to:

1. Register and configure a suitable domain name.
2. Obtain and install a valid TLS certificate.
3. Configure Apache to serve the application over HTTPS.
4. Redirect HTTP requests to HTTPS.
5. Verify that sensitive traffic is encrypted.
6. Retest the application after TLS implementation.

## Assessment Result

HTTPS/TLS remediation was identified as a required security improvement but was not implemented within the assessment timeframe.

The finding was documented for future remediation rather than being presented as a completed security control.

## Security Skills Demonstrated

- Web security assessment
- HTTP/HTTPS analysis
- Transport security awareness
- Security finding documentation
- Risk identification
- Remediation planning

## Security Context

All testing was performed within a controlled educational environment as part of a Level 2 Cyber Security project.

The assessment was conducted for defensive security assessment and learning purposes.
