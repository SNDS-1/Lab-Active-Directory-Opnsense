# File Shares and Permissions

## Overview

In this part of the lab, I configured shared folders on the Windows Server to simulate file access for different departments.

The goal was to understand how SMB sharing and Windows permissions can be used to control access to files.

## Shared Folders

Three department shares were configured:

| Share | Intended Department |
|---|---|
| `Comptabilite` | Accounting |
| `Informatique` | IT |
| `Direction` | Management |

The shares were configured on the server and made available over the network.

## Access Control

Share permissions and NTFS permissions were configured to control access to the folders.

The access model follows the department structure:

- Accounting users should access the `Comptabilite` share.
- IT users should access the `Informatique` share.
- Management users should access the `Direction` share.

The corresponding security groups are `GG_Comptabilite`, `GG_Informatique` and `GG_Direction`.

## Testing

I tested access using the different domain accounts and checked both authorized and unauthorized access.

The tests helped verify whether the permissions matched the intended department access.

## Security Considerations

Windows evaluates both share permissions and NTFS permissions when a user accesses a folder over the network. The effective access is determined by the combined permissions.

Permissions should be assigned to security groups where possible, rather than managed separately for every user.

## Screenshots

Relevant screenshots are available in `../screenshots/03-shares/`.

## What I Learned

This exercise helped me understand the difference between shared-folder permissions and NTFS permissions, and how security groups can simplify access management.
