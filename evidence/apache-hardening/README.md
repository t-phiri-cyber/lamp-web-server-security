# Apache Server Hardening Evidence

Documentation and evidence of Apache security hardening controls implemented and tested during the controlled educational security assessment.

## Objective

The objective was to reduce unnecessary server information disclosure and prevent unauthorised directory listing within the Apache web server.

## Controls Implemented

### ServerTokens

Apache `ServerTokens` was modified to reduce the amount of server information disclosed in HTTP responses.

This reduces unnecessary information that could assist an attacker in identifying the server environment.

### ServerSignature

Apache `ServerSignature` was modified to prevent unnecessary Apache server information from being displayed on generated error pages and server responses.

### Directory Listing

Apache directory indexing was disabled using:

```apache
Options -Indexes
