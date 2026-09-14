# Windows Server

Windows Server is the central infrastructure server of the laboratory.

## Roles

The server provides:

- Active Directory Domain Services (AD DS)
- DNS
- DHCP
- File Server
- Centralized authentication
- Group Policy management

## Network

| Parameter | Value |
|---|---|
| IP Address | 192.168.88.10 |
| Role | Domain Controller / File Server |
| DNS | Windows Server |

## Active Directory

The domain environment includes:

- Organizational Units
- User accounts
- Security groups
- Group Policy Objects
- Windows 11 domain clients

## Security Groups

The following groups are used for role-based access control:

- `Groupe-Informatique`
- `Groupe-RH`

## File Server

Three SMB shares were configured:

- `Commun`
- `IT`
- `RH`

Access is controlled using Active Directory groups and NTFS permissions.

### Access model

| Group | Commun | IT | RH |
|---|---|---|---|
| Groupe-Informatique | ✅ | ✅ | ❌ |
| Groupe-RH | ✅ | ❌ | ✅ |

## Validation

Tests confirmed:

- Domain authentication
- DNS resolution
- DHCP configuration
- GPO application
- SMB connectivity
- NTFS permission enforcement
