# Security Limitations and Future Improvements

## Overview

This lab was created for learning and practice purposes. It demonstrates several basic infrastructure administration tasks, but it is not intended to represent a fully hardened production environment.

## Current Limitations

### Firewall Rules

During connectivity troubleshooting, a rule allowing traffic to the Active Directory server with a broad destination port setting was used.

Although this helped verify connectivity, allowing all ports is broader than necessary. The rule should be reviewed and replaced with rules limited to the services and ports required by the lab.

### Ubuntu Domain Integration

The Ubuntu client is connected to the LAN, but it has not yet been joined to the Active Directory domain.

Joining Linux to the domain would be a useful next step for practising centralized authentication across different operating systems.

### Lab Environment

The environment runs in VirtualBox on a personal computer. It is designed for learning and testing, not for production use.

## Future Improvements

Planned improvements include:

- Restricting firewall rules to required ports and services.
- Joining the Ubuntu client to Active Directory.
- Performing additional connectivity and access-control tests.
- Reviewing security settings and documenting any changes.
- Adding further screenshots as new tests are completed.

## Conclusion

This project provided practical experience with Windows domain services, DNS, file permissions, Group Policy and firewall configuration.

Documenting the limitations is part of the process: it shows which settings were used during testing and what could be improved in a future version of the lab.

