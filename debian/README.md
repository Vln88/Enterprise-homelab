# Debian Server

Debian is used as the Linux server of the laboratory.

## Network

| Parameter | Value |
|---|---|
| IP Address | 192.168.88.20 |
| Netmask | 255.255.255.0 |
| Gateway | 192.168.88.1 |
| DNS | 192.168.88.10 |

The server uses a static IP configuration.

## Connectivity Tests

The following tests were successfully performed:

- Debian → OPNsense
- Debian → Windows Server
- Debian → Internet
- DNS resolution

## Planned Services

Docker and Docker Compose will be installed on this server as part of the final improvements of the laboratory.

## Future VLAN Integration

The Debian server will also be used to validate network segmentation and firewall policies after VLAN implementation.
