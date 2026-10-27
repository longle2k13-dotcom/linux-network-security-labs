# SSH Remote Access & Server Hardening Lab

## Overview

This project documents my hands-on experience configuring secure SSH remote access and hardening an SSH server using Kali Linux and Xubuntu in an Oracle VirtualBox environment.

The objective was to understand SSH authentication, implement security controls, and verify their effectiveness through practical testing and troubleshooting.

## Lab Environment

- **Virtualization:** Oracle VirtualBox
- **SSH Client:** Kali Linux
- **SSH Server:** Xubuntu 24.04
- **Tools:** OpenSSH, Linux Terminal, Nano

## Technical Implementation

### 1. SSH Remote Access

- Generated SSH public and private key pairs.
- Configured SSH key-based authentication.
- Added the public key to the server's `authorized_keys` file.
- Verified remote access using SSH keys.

### 2. SSH Server Hardening

Implemented and tested four security configurations:

- **Disable Password Authentication:** Restricted password-based SSH logins.
- **Change Default SSH Port:** Changed the listening port from 22 to 4444 to reduce exposure to automated scans targeting the default port.
- **Disable Root Login:** Prevented direct SSH authentication as root.
- **Limit Remote Users:** Configured `AllowUsers` to restrict SSH access to authorized accounts.

### 3. Troubleshooting and Verification

- Tested successful and unsuccessful SSH login attempts.
- Verified SSH key-based authentication.
- Investigated SSH connectivity and authentication issues.
- Documented commands, screenshots, observations, and troubleshooting results.

## Lab Documentation

[View Complete SSH Security Lab Report](./SSH-Security-Lab.pdf)

The PDF contains the step-by-step implementation, terminal commands, screenshots, explanations, and verification results.

## Key Takeaways

This lab demonstrated that SSH security requires multiple complementary controls rather than relying on a single configuration.

It strengthened my practical skills in Linux administration, SSH authentication, server hardening, troubleshooting, and technical documentation.
