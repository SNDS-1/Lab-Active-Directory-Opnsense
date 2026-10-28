# Active Directory & OPNsense Lab

Virtualized IT infrastructure lab built with VirtualBox, Windows Server, Windows 11, Ubuntu and OPNsense.

## Overview

This project demonstrates the setup and administration of a small enterprise-style IT environment, including a Windows domain, network segmentation, user and group management, file sharing and security policies.

## Environment

- **Virtualization:** VirtualBox
- **Firewall:** OPNsense
- **Server:** Windows Server 2025
- **Client:** Windows 11 Pro
- **Linux:** Ubuntu
- **Domain:** `ad.lab.test`

## Implemented Features

- Active Directory Domain Services and DNS
- Organizational Units, domain users and security groups
- Windows client joined to the domain
- SMB file shares with access permissions
- Group Policy security settings
- Segmented virtual networks using OPNsense
- Connectivity and access-permission tests

## Documentation

- [Network Architecture](docs/architecture.md)
- [Active Directory](docs/active-directory.md)
- [Shares and Permissions](docs/shares-permissions.md)
- [Group Policy](docs/gpo.md)
- [Tests and Results](docs/tests-results.md)
- [Security Limitations and Improvements](docs/security-limitations.md)

## Screenshots

Screenshots documenting the lab configuration and tests are available in the [`screenshots/`](screenshots/) directory.

## Future Improvements

- Join the Ubuntu client to the Active Directory domain
- Restrict firewall rules to only the required ports and services

