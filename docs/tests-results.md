# Tests and Results

## Overview

After configuring the lab, I performed several tests to check domain authentication, network configuration and file access.

The tests focused on verifying the main features rather than measuring performance.

## Test Results

| Test | Expected Result | Result |
|---|---|---|
| Windows client IP configuration | Correct IP, gateway and DNS settings | Verified |
| Domain controller discovery | Client can locate the domain controller | Verified |
| Domain login with `alice.compta` | User can authenticate | Successful |
| Domain login with `paul.info` | User can authenticate | Successful |
| Domain login with `sophie.direction` | User can authenticate | Successful |
| Department share access | Access follows configured permissions | Tested |
| Group Policy configuration | GPO and settings are configured | Verified |

## Network Configuration

The Windows 11 client uses the following configuration:

- **IP address:** `10.10.10.20`
- **Default gateway:** `10.10.10.1`
- **DNS server:** `10.10.20.10`

The DNS server points to the domain controller so that the workstation can locate domain services.

## File Access Tests

I tested the department shares with different domain users. Both authorized and unauthorized access were checked to confirm that the configured permissions behaved as intended.

## Notes

The firewall configuration was tested to allow communication between the LAN and the Active Directory server. During troubleshooting, a rule using a broad destination port setting was required for the tested connectivity.


## Screenshots

Relevant screenshots are available in `../screenshots/05-tests/`.

## Conclusion

The main lab components were configured and tested: domain authentication, DNS, department shares and Group Policy settings.

The lab also highlighted the importance of validating network access and reviewing firewall rules after troubleshooting.
