# Group Policy Configuration

## Overview

Group Policy was used to apply basic security settings to domain computers.

The goal was to centralize some workstation settings instead of configuring each computer individually.

## Group Policy Object

- **GPO name:** `GPO_Securite_Postes`
- **Linked OU:** `Ordinateurs`

The GPO was linked to the OU containing the Windows workstation computer account.

## Configured Settings

The following settings were configured and verified:

- **Audit logon events:** success and failure
- **Audit account logon events:** success and failure
- **Guest account:** disabled
- **Interactive logon inactivity limit:** 600 seconds

These settings provide basic workstation security and help record authentication-related events.

## Verification

I checked the GPO configuration and its link to the `Ordinateurs` OU.

The Windows 11 client was used for domain and workstation testing.

## Why Group Policy Is Useful

Group Policy allows administrators to apply consistent settings across domain computers. It also makes it easier to update security settings centrally.

## Screenshots

Relevant screenshots are available in `../screenshots/04-gpo/`.

## What I Learned

This part of the lab helped me practise creating and linking a GPO, configuring security settings and checking its configuration.

## Possible Improvements

A future step would be to expand the policy with additional settings and continue testing their application on domain computers.
