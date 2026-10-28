# Active Directory Configuration

## Overview

The goal of this part of the lab was to set up a Windows domain and manage users, groups and computers in a small enterprise-style environment.

The domain controller runs Windows Server 2025 Standard Evaluation.

## Domain Information

- **Domain name:** `ad.lab.test`
- **NetBIOS name:** `AD`
- **Domain controller:** `SRV-AD01`
- **Server IP address:** `10.10.20.10`
- **Services:** Active Directory Domain Services (AD DS) and DNS

## Organizational Units

I created the following Organizational Units (OUs) to keep the directory organized:

- `Utilisateurs`
- `Groupes`
- `Ordinateurs`
- `Serveurs`

The Windows 11 client was joined to the domain and its computer account was moved into the `Ordinateurs` OU.

## Users and Security Groups

Three domain users were created for different departments:

| User | Department | Security Group |
|---|---|---|
| `alice.compta` | Accounting | `GG_Comptabilite` |
| `paul.info` | IT | `GG_Informatique` |
| `sophie.direction` | Management | `GG_Direction` |

Security groups were used to organize users according to their department and to help manage access to shared resources.

## Domain Client

The Windows 11 workstation, `WIN11-CLIENT01`, was successfully joined to the `ad.lab.test` domain.

I tested domain logins using the three user accounts to verify that the accounts could authenticate on the workstation.

## DNS Configuration

The domain controller also provides DNS services. The Windows 11 client uses `10.10.20.10` as its DNS server so it can locate the domain controller and other domain services.

## Screenshots

Relevant screenshots are available in `../screenshots/02-active-directory/`.

## What I Learned

This part of the lab helped me practise domain setup, user and group management, Organizational Units and domain authentication.
