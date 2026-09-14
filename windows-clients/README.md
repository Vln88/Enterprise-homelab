# Windows 11 Clients

Two Windows 11 virtual machines are used as domain workstations.

## Configuration

| Client | Role | Address |
|---|---|---|
| Windows 11 Client 01 | Domain workstation | DHCP |
| Windows 11 Client 02 | Domain workstation | DHCP |

## Active Directory

Both clients are joined to the Windows Server domain.

They receive centralized configuration through Group Policy.

## Tests

The clients were used to validate:

- Domain authentication
- DNS resolution
- GPO application
- File server access
- SMB permissions
- Connectivity with Debian
- Network connectivity through OPNsense

## File Server Access

Access was tested using different Active Directory users.

IT users can access:

- `Commun`
- `IT`

RH users can access:

- `Commun`
- `RH`

Unauthorized access is denied through NTFS permissions.
