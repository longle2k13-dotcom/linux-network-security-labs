
# Linux & Network Security Labs

## Overview

This repository showcases my hands-on experience with Linux system administration, SSH security, firewall configuration, and network troubleshooting.

These projects were completed in a virtualized lab environment using Kali Linux, Xubuntu, and OPNsense.

My objective is to develop practical cybersecurity and networking skills through configuring security controls, testing their behavior, troubleshooting issues, and documenting the results.

## Lab Projects

### 01 — SSH Remote Access & Server Hardening

**Technologies:** Kali Linux, Xubuntu, OpenSSH, Oracle VirtualBox

Configured and secured SSH remote access between Linux virtual machines.

**Key Implementations:**
- Generated SSH key pairs and configured key-based authentication.
- Disabled password-based SSH authentication.
- Changed the default SSH port from 22 to 4444.
- Restricted direct root login.
- Limited SSH access to authorized users using `AllowUsers`.
- Tested authentication behavior and troubleshot connection issues.

**Skills Demonstrated:** Linux Administration, SSH Security, Access Control, Authentication, Troubleshooting

[View SSH Security Lab](./01-SSH-Security/)

---

### 02 — Firewall & Network Security (UFW + OPNsense)

**Technologies:** Xubuntu, Kali Linux, UFW, OPNsense 26.7, Oracle VirtualBox

Configured host-based and network-based firewall security controls in a virtualized networking environment.

**Key Implementations:**
- Configured UFW default-deny incoming traffic policies.
- Created SSH (TCP/22) and HTTP (TCP/80) firewall exceptions.
- Tested firewall rule precedence using conflicting allow and deny rules.
- Installed and configured an OPNsense virtual firewall.
- Assigned WAN and LAN interfaces using MAC address verification.
- Connected Xubuntu to an isolated internal network.
- Troubleshot network connectivity and verified successful ICMP communication.
- Created an inbound WAN firewall rule permitting TCP destination port 443.

**Skills Demonstrated:** Firewall Administration, Network Segmentation, TCP/IP, Access Control, Virtual Networking, Troubleshooting

[View Firewall & Network Security Lab](./02-Firewall-Security/)

---

## Lab Environment

| Component | Technology |
|---|---|
| Virtualization | Oracle VirtualBox |
| Operating Systems | Kali Linux, Xubuntu 24.04, OPNsense 26.7 |
| Remote Access | OpenSSH |
| Host-Based Firewall | UFW |
| Network Firewall | OPNsense |
| Network Configuration | NAT, Internal Networks, WAN/LAN |
| Testing Tools | SSH, ping, curl, Linux CLI |

## Technical Skills Developed

- Linux system administration and command-line operations
- SSH authentication and server hardening
- Firewall policy configuration and rule management
- Network segmentation and interface assignment
- TCP/IP networking and connectivity verification
- Security troubleshooting and root cause investigation
- Technical documentation and evidence-based verification

## Documentation Approach

Each lab includes a dedicated README and a detailed PDF report containing configuration steps, screenshots, testing results, and troubleshooting observations.

The documentation distinguishes between successfully verified outcomes and configuration steps that were not independently tested.

## Project Development

This repository will continue to expand as I complete additional Linux, networking, and cybersecurity labs.

My focus is on developing practical technical skills and maintaining a documented portfolio that demonstrates my learning progress and hands-on experience.

