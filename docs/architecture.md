# Architecture du laboratoire
# Lab Architecture

## Overview

This lab simulates a small enterprise IT environment using VirtualBox. It combines network segmentation, a firewall, a Windows domain controller, a Windows client and a Linux client.

## Virtualization Environment

- **Host OS:** Windows 10 Pro
- **Hypervisor:** Oracle VirtualBox 7.2.16

## Virtual Machines

| Virtual Machine | Operating System | Role |
|---|---|---|
| OPNsense-Firewall | OPNsense | Firewall and network routing |
| SRV-AD01 | Windows Server 2025 Standard Evaluation | Active Directory Domain Services and DNS |
| WIN11-CLIENT01 | Windows 11 Pro | Domain-joined Windows workstation |
| Ubuntu-Client-LAN | Ubuntu | Linux client and network testing |

## Network Segmentation

| Network | Subnet | Gateway |
|---|---|---|
| LAB-LAN | `10.10.10.0/24` | `10.10.10.1` |
| LAB-SERVERS | `10.10.20.0/24` | `10.10.20.1` |
| LAB-DMZ | `10.10.30.0/24` | `10.10.30.1` |

OPNsense provides the firewall and routing functions between the lab networks. Its WAN interface uses VirtualBox NAT.

## Key IP Addresses

| Device | IP Address |
|---|---|
| OPNsense LAN gateway | `10.10.10.1` |
| Windows 11 client | `10.10.10.20` |
| Active Directory server | `10.10.20.10` |
| Ubuntu LAN interface | `10.10.10.10` |

The Windows client uses the Active Directory server (`10.10.20.10`) as its DNS server.

## Architecture Diagram

```text
                  Internet
                     |
              VirtualBox NAT
                     |
              OPNsense Firewall
               /      |      \
              /       |       \
         LAB-LAN  LAB-SERVERS  LAB-DMZ
        10.10.10.0 10.10.20.0 10.10.30.0
            |          |
       Windows 11   SRV-AD01
       Ubuntu       AD DS / DNS
```

## Notes

The Ubuntu client is configured on the LAN, but joining it to the Active Directory domain remains a planned improvement. Firewall rules will also be reviewed to restrict access to only the required services.
