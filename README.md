Linux SSH Security Lab

Overview

This project documents my hands-on experience configuring SSH remote access and securing an SSH server using Kali Linux and Xubuntu in a VirtualBox lab environment.

The goal of this lab was to understand how SSH authentication works, how to configure remote access, and how to reduce common security risks.

Lab Environment

Virtualization: Oracle VirtualBox

SSH Client: Kali Linux

SSH Server: Xubuntu 24.04

Tools: OpenSSH, Linux Terminal, Nano

What I Learned

1. SSH Remote Access

Generated SSH public and private keys.

Configured key-based authentication.

Added a public key to the server's authorized_keys file.

Verified remote access using SSH keys.

2. SSH Server Hardening

Implemented and tested four security configurations:

Disable Password Authentication: Restrict password-based SSH logins.

Change Default SSH Port: Change port 22 to 4444 to reduce automated scans targeting the default port.

Disable Root Login: Prevent direct SSH login as root.

Limit Remote Users: Use AllowUsers to restrict SSH access to specific accounts.

3. Troubleshooting and Verification

Tested successful and unsuccessful SSH login attempts.

Verified SSH key authentication.

Troubleshot SSH connection and authentication issues.

Documented commands, screenshots, and results.

Lab Documentation

The complete step-by-step documentation, including commands, explanations, and screenshots, is available here:

View SSH Security Lab Documentation

Key Takeaway

This lab helped me understand that securing an SSH server requires multiple security measures rather than relying on a single configuration.

It also gave me practical experience with Linux administration, SSH authentication, troubleshooting, and technical documentation.
