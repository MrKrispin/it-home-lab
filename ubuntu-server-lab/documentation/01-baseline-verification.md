# 01 - Baseline System Verification

## Objective

Verify the initial Ubuntu Server configuration by identifying system information, storage and filesystem layout, LVM configuration, and network addressing and routing.

## System Identity

Commands used:

whoami , hostname , hostnamectl , uname -a

### Findings

- Hostname: ubuntu-server
- Logged-in user: kristian
- Operating system: Ubuntu 26.04 LTS
- Kernel: Linux 7.0.0-29-generic
- Architecture: x86-64

### Notes

The commands above were used to confirm the identity of the server, the operating system version, the Linux kernel, and the system architecture.

## Storage and Logical Volume Management

Commands used:

lsblk, df -h, sudo pvs, sudo vgs, sudo lvs

### Findings

- Virtual disk size: /dev/sda - 40 GB
- Boot partition: /dev/sda2 - 2 GB, mounted at /boot
- Root filesystem: /dev/mapper/ubuntu--vg-ubuntu--lv, mounted at /
- LVM physical volume: /dev/sda3 - About 38 GB
- Volume group: ubuntu-vg - About 38 GB
- Logical volume: ubuntu-lv About 19 GB
- Free space in volume group: Approximately 19 GB

### Notes

The commands were used to identify how the virtual disk is partitioned, how the filesystems are mounted, and how LVM manages the storage assigned to the server.

## Network Configuration

Commands used:

ip addr, ip route

### Findings

- Network interface: enp0s3
- IPv4 address: 10.0.2.15
- Prefix length: /24
- Default gateway: 10.0.2.2
- Address assignment: DHCP
- VirtualBox network: Lab NAT

### Notes
The Ubuntu Server VM is connected through the VirtualBox Lab NAT network. The interface enp0s3 received the IPv4 address 10.0.2.15 through DHCP, and outbound traffic is routed through the default gateway 10.0.2.2

## What I Learned
This task helped me understand how to inspect a Linux server before making changes. I practiced identifying the system's OS and kernel information, reading the disk and LVM layout, and determining the server's IP address, subnet, and default gateway.
