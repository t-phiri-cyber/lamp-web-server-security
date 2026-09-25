# Apache Server Hardening Evidence

Documentation of Apache hardening controls implemented and tested during the controlled educational security assessment.

## Objective

The objective was to reduce unnecessary information disclosure and prevent unauthorised directory listing within the Apache web server.

## Controls Implemented

### ServerTokens

The Apache `ServerTokens` configuration was modified to reduce the amount of server information disclosed in HTTP responses.

This reduces unnecessary information that could assist an attacker in identifying the server environment.

### ServerSignature

The Apache `ServerSignature` configuration was modified to prevent unnecessary Apache server information from being displayed in generated error pages and server responses.

### Directory Listing

Apache directory indexing was disabled using:

```text
Options -Indexes
