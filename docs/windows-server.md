# Windows Server Configuration

## 1. Server Installation

A Windows Server virtual machine was deployed using Microsoft Hyper-V.

The server was configured with the static IP address `192.168.88.10`.

**foto 1**

---

## 2. Active Directory Domain Services

Active Directory Domain Services was installed through Server Manager.

The server was then promoted to a Domain Controller and the Active Directory domain was created.

**foto 2**

### Organizational Units

Several Organizational Units were created to organize users and computers according to their roles.

**foto 3**

### Users and Groups

User accounts and security groups were created for the different departments.

The main security groups are:

- `Groupe-Informatique`
- `Groupe-RH`

**foto 4**

---

## 3. DNS

DNS was configured as part of the Active Directory infrastructure.

The Windows Server acts as the DNS server for the domain.

**foto 5**

---

## 4. DHCP

A DHCP scope was configured to provide network configuration to the Windows 11 clients.

**foto 6**

---

## 5. Group Policy

Group Policy Objects were created and linked to the appropriate Organizational Units.

The policies were subsequently tested from the Windows 11 clients.

**foto 7**

---

## 6. File Server

Three SMB shares were created:

- `Commun`
- `IT`
- `RH`

The corresponding directories are:

- `C:\Shares\Commun`
- `C:\Shares\IT`
- `C:\Shares\RH`

**foto 8**

### NTFS Permissions

Access was controlled using Active Directory security groups.

| Group | Commun | IT | RH |
|---|---|---|---|
| Groupe-Informatique | Modify | Modify | Denied |
| Groupe-RH | Modify | Denied | Modify |
| Domain Users | Modify | — | — |

The permissions were validated from the Windows 11 clients.

![File server permissions](../screenshots/windows-server/ntfs-permissions.png)
