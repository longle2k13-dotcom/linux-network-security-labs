
# Firewall & Network Security Lab — UFW and OPNsense

## Overview

This project documents my hands-on experience configuring host-based and network-based firewalls using UFW on Xubuntu and OPNsense in an Oracle VirtualBox environment.

The objective was to understand firewall traffic filtering, rule precedence, network segmentation, and interface configuration through practical testing and troubleshooting.

## Lab Environment

- **Virtualization:** Oracle VirtualBox
- **Operating Systems:** Kali Linux, Xubuntu 24.04, OPNsense 26.7
- **Firewall Technologies:** UFW (Uncomplicated Firewall), OPNsense
- **Network Tools:** Linux Terminal, OpenSSH, ping, curl
- **Network Configuration:** VirtualBox NAT and Internal Networks

## Network Configuration

| Device | Interface | IP Address | Network |
|---|---|---|---|
| OPNsense | WAN (em1) | 172.30.1.22/24 (DHCP) | Testing |
| OPNsense | LAN (em2) | 192.168.1.1/24 | InsideFirewall |
| Xubuntu | enp0s9 | 192.168.1.107/24 | InsideFirewall |

## Technical Implementation

### Part A — UFW Host-Based Firewall

Configured and tested UFW rules on Xubuntu to control incoming network connections.

**1. Default Firewall Policies**

- Enabled UFW and verified its operational status.
- Configured the default policy to deny incoming connections and allow outgoing traffic.
- Confirmed that ICMP ping traffic remained functional while incoming SSH connections were blocked.

**2. SSH and HTTP Firewall Exceptions**

- Allowed inbound SSH traffic on TCP port 22.
- Allowed inbound HTTP traffic on TCP port 80.
- Verified successful SSH remote access from Kali Linux.
- Confirmed HTTP service availability using `curl -I` and received an HTTP 200 OK response.

**3. Firewall Rule Precedence**

- Created conflicting allow and deny rules for SSH.
- Observed that an earlier matching allow rule permitted SSH connections despite a later deny rule.
- Removed the earlier allow rule and verified that SSH connectivity was blocked.
- Reconfigured UFW to permit SSH and HTTP while maintaining the default deny-incoming policy.

### Part B — OPNsense Network Firewall

Installed and configured OPNsense as a dedicated virtual firewall to separate network segments.

**1. OPNsense Installation**

- Created an OPNsense virtual machine using Oracle VirtualBox.
- Completed the installation and configured the virtual disk.
- Removed the installation ISO to prevent the VM from booting back into the installer.
- Verified successful boot into the OPNsense console.

**2. WAN and LAN Interface Assignment**

- Identified network interfaces by matching MAC addresses with VirtualBox adapter settings.
- Assigned `em1` to the WAN interface connected to the Testing network.
- Assigned `em2` to the LAN interface connected to the InsideFirewall network.
- Verified the assigned IP addresses through the OPNsense console.

**3. Internal Network Connectivity**

- Connected the Xubuntu virtual machine to the InsideFirewall network.
- Verified its assigned IPv4 address using `ip -br addr`.
- Tested connectivity to the OPNsense LAN interface using ICMP ping.
- Resolved an initial connectivity issue by rebooting the OPNsense virtual machine.
- Confirmed successful connectivity with 0% packet loss.

**4. WAN Firewall Rule Configuration**

- Accessed the OPNsense web management interface.
- Navigated to the WAN firewall rules.
- Created an IPv4 TCP pass rule for HTTPS destination port 443.
- Verified that the rule appeared in the WAN firewall rules table.

## Troubleshooting Experience

This project involved identifying and resolving several practical configuration issues:

- **SSH connectivity blocked:** Investigated UFW default policies and configured appropriate inbound exceptions.
- **Conflicting firewall rules:** Examined rule ordering and removed an earlier allow rule to enforce the intended deny policy.
- **OPNsense installation loop:** Identified a mounted installation ISO as the cause and removed it.
- **LAN connectivity failure:** Verified subnet configuration and UFW status before restoring connectivity by rebooting OPNsense.

## Key Takeaways

This lab demonstrated the difference between host-based firewall protection and network-level traffic filtering.

UFW provided control over traffic entering an individual Linux system, while OPNsense introduced dedicated WAN/LAN interfaces and network segmentation.

I also gained practical experience verifying firewall behavior, identifying interfaces through MAC addresses, testing network connectivity, and troubleshooting configuration issues.

The project reinforced the importance of establishing reliable network connectivity before implementing firewall policies.

## Lab Documentation

The complete lab report includes configuration steps, terminal commands, screenshots, troubleshooting observations, and verification results.

[View Firewall & Network Security Lab Documentation](./OPNsense_Firewall_Lab.pdf)
