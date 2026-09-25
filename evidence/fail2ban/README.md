# Fail2Ban SSH Brute-Force Testing

Documentation of the Fail2Ban testing performed during the controlled educational security assessment.

## Assessment

Fail2Ban was configured to monitor repeated failed SSH authentication attempts on the Ubuntu server.

The objective was to determine whether repeated authentication failures would trigger the configured protection and result in the source IP address being banned.

## Testing Process

The assessment followed these steps:

1. Configure Fail2Ban to monitor SSH authentication failures.
2. Generate repeated failed SSH authentication attempts within the controlled lab environment.
3. Monitor the relevant authentication and Fail2Ban logs.
4. Check whether the source IP address was banned.
5. Investigate the behaviour when the expected ban did not occur immediately.
6. Retest the control after investigating the configuration and logs.
7. Verify successful IP banning during retesting.

## Initial Result

Initial testing did not immediately produce the expected IP ban.

The behaviour was investigated by reviewing Fail2Ban logs and authentication events to determine why the expected action had not occurred.

## Retest Result

Following investigation and configuration checks, the test was repeated.

The retest successfully demonstrated IP banning by Fail2Ban.

This confirmed that the defensive control was functioning as intended under the tested conditions.

## Log Analysis

The assessment included analysis of:

- SSH authentication failures
- Fail2Ban logs
- Ban and unban events

Log analysis was used to investigate the initial unexpected behaviour and validate the operation of the security control.

## Skills Demonstrated

- Linux security administration
- SSH security testing
- Brute-force detection
- Fail2Ban configuration
- Security log analysis
- Troubleshooting security controls
- Control validation
- Before-and-after testing
- Security documentation

## Evidence Limitation

No dedicated screenshots were captured for the Fail2Ban testing.

The finding is documented based on the testing and investigation performed during the controlled educational assessment.

## Scope

All testing was performed against the controlled educational environment used for the project.

No unauthorised systems were targeted.
