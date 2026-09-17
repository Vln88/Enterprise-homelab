# Enterprise Homelab

Enterprise-style virtualized infrastructure laboratory designed to practice
system administration, networking and cybersecurity concepts.

## 🎯 Objectives

- Build an enterprise-like virtual infrastructure
- Configure network routing and firewalling
- Deploy Windows Server services
- Implement Active Directory and centralized authentication
- Configure DNS and DHCP
- Manage Windows clients through Group Policy
- Implement file server permissions
- Deploy and configure a Linux server
- Monitor and test network connectivity and security controls
- Document the complete infrastructure and validation tests

## 🏗️ Architecture

The laboratory is built with Hyper-V.

### Main components

| System | Role | IP |
|---|---|---|
| OPNsense | Firewall / Router | 192.168.88.1 |
| Windows Server | AD DS / DNS / DHCP / File Server | 192.168.88.10 |
| Windows 11 Client 01 | Domain workstation | DHCP |
| Windows 11 Client 02 | Domain workstation | DHCP |
| Debian | Linux server | 192.168.88.20 |

## 🔐 Active Directory

The Windows Server infrastructure includes:

- Active Directory Domain Services
- Organizational Units
- User accounts
- Security groups
- Group Policy Objects
- Centralized authentication
- Windows client domain integration

## 🌐 Network & Security

OPNsense provides:

- Network routing
- Firewalling
- Internet access control
- Traffic logging
- Network monitoring and validation

Firewall and connectivity tests are documented in the `docs/` directory.

## 📂 File Server

The Windows Server provides SMB shares with role-based permissions.

### Shares

- `Commun`
- `IT`
- `RH`

Access is controlled using Active Directory security groups and NTFS permissions.

Example:

- `Groupe-Informatique` → IT share
- `Groupe-RH` → RH share
- `Domain Users` → Commun share

## 🧪 Validation Tests

The infrastructure has been validated through tests including:

- Windows client → Domain Controller
- Windows client → File Server
- Windows client → Debian
- DNS resolution
- DHCP
- Internet connectivity
- Firewall traffic logging
- SMB access control
- NTFS permissions
- User/group authorization

## 🛠️ Technologies

- Microsoft Hyper-V
- OPNsense
- Windows Server
- Windows 11
- Active Directory
- DNS
- DHCP
- Group Policy
- SMB
- NTFS
- Debian Linux

## 📚 Documentation

Detailed documentation will be available in:

- [Windows Server](docs/windows-server.md)
- [OPNsense](docs/OPNsense.md)
- [Windows Clients](docs/windows-clients.md)
- [Debian Linux](docs/debian.md)
- [Tests](docs/tests.md)

## What I Learned

This project allowed me to gain practical experience in designing, deploying and troubleshooting an **small** enterprise-style IT infrastructure.

Thanks to this lab, I learned how to:

- Deploy and manage virtual machines using Microsoft Hyper-V.
- Configure OPNsense as a firewall, gateway and network security.
- Design and configure a local IPv4 network.
- Install and manage Windows Server.
- Deploy and manage Active Directory Domain Services.
- Create and organize Organizational Units, users and security groups.
- Configure DNS for an Active Directory environment.
- Configure DHCP and manage IP address allocation.
- Create and apply Group Policy Objects (GPOs).
- Join Windows 11 clients to an Active Directory domain.
- Configure an SMB file server.
- Manage NTFS permissions and access control using Active Directory security groups.
- Configure a Debian server with a static IP address.
- Troubleshoot network connectivity and DNS issues.
- Analyze firewall traffic and logs using OPNsense.
- Validate network communication between Windows and Linux systems.
- Perform practical troubleshooting when configurations did not work as expected.
- Document an IT infrastructure and its validation process.

### Troubleshooting Experience

During the deployment, I encountered issues related to network configuration, firewall traffic visibility, DNS resolution and file permissions.

These problems helped me develop a more systematic troubleshooting approach:

**Identify the problem -> Analyze the configuration -> Test possible causes -> Apply a solution -> Validate the result.**

This project therefore provided practical experience not only in system administration and networking, but also in troubleshooting and infrastructure security.

## 🚀 Future Improvements

Planned improvements:

- Docker, Docker Compose deployment on Debian
- Network segmentation (VLANs)
- Inter-VLAN routing and firewall rules in OPNsense

 After this immprovements, the lab will be considered as finished.
  

## 👨‍💻 Author

Cybersecurity / Systems & Network Student -> [GitHub](https://github.com/vln88)

This project was built as a hands-on laboratory to develop practical skills
in enterprise infrastructure, networking and cybersecurity.
