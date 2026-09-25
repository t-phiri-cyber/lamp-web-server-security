# Fail2Ban SSH Brute-Force Testing

Documentation and evidence from Fail2Ban testing performed during the controlled educational security assessment.

## Assessment

Fail2Ban was configured on the Ubuntu server to monitor repeated failed SSH authentication attempts and automatically ban offending IP addresses.

The objective was to determine whether repeated authentication failures would trigger the configured defensive control.

## Testing Process

The assessment followed these stages:

1. Install and enable Fail2Ban.
2. Configure SSH protection parameters including `bantime`, `findtime`, and `maxretry`.
3. Generate repeated failed SSH authentication attempts within the controlled lab environment.
4. Monitor SSH authentication and Fail2Ban logs.
5. Investigate the initial failure to trigger the expected IP ban.
6. Review configuration and log activity.
7. Retest the control.
8. Verify successful IP banning.

## Evidence

### 1. Fail2Ban Installation

[View installation evidence](./01-fail2ban-installation.png)

Fail2Ban was installed and the service was started on the Ubuntu server.

### 2. Fail2Ban Configuration

[View configuration evidence](./02-fail2ban-configuration.png)

Fail2Ban configuration parameters were reviewed and modified, including:

- `bantime`
- `findtime`
- `maxretry`

### 3. Initial Test and Troubleshooting

[View initial test evidence](./03-fail2ban-initial-test-troubleshooting.png)

The initial brute-force test did not immediately result in the expected IP ban.

The behaviour was investigated through configuration checks and Fail2Ban log analysis.

### 4. SSH Failure Detection

[View SSH detection evidence](./04-ssh-failure-detection.png)

Fail2Ban logs demonstrated repeated SSH authentication failures being detected by the `sshd` jail.

### 5. Successful IP Ban

[View successful ban evidence](./05-fail2ban-successful-ban.png)

Following investigation and retesting, Fail2Ban successfully detected offending SSH activity and applied IP bans.

The logs demonstrate repeated `Found`, `Ban`, and `Unban` events.

## Initial Result

The first test did not immediately produce the expected IP ban.

Rather than treating the test as successful, the behaviour was investigated by reviewing Fail2Ban logs and authentication events.

## Retest Result

Following investigation and configuration checks, the test was repeated.

The subsequent test successfully demonstrated automatic IP banning by Fail2Ban.

This confirmed that the defensive control was functioning as intended under the tested conditions.

## Security Skills Demonstrated

- Linux system administration
- SSH security
- Brute-force attack simulation
- Fail2Ban configuration
- Security control validation
- Log analysis
- Troubleshooting
- Incident detection
- Defensive security controls
- Retesting and verification

## Security Context

All testing was performed within a controlled educational environment as part of a Level 2 Cyber Security project.

The testing was conducted for defensive security assessment and learning purposes.
