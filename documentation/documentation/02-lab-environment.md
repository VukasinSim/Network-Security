# 02 - Lab Environment Setup

## Overview

This section documents the hardware, software, and network configuration used throughout the home network security assessment.

The lab consists of a Windows host machine running a Kali Linux virtual machine, which is connected to the home network through bridged networking.

## Hardware

| Component | Description |
|---|---|
| Host Machine | Windows desktop |
| Router | Verizon CR1000A |
| Wireless Network | Google Nest Wifi Pro |
| Virtualization Host | Windows 11 desktop |

## Software and Tools

| Software | Purpose |
|---|---|
| Windows 11 | Host operating system |
| Kali Linux | Security testing environment |
| Oracle VirtualBox | Virtualization platform |
| Nmap | Network discovery and service identification |
| Wireshark | Network traffic analysis |
| Cisco Packet Tracer | Network simulation |

## Virtual Machine Configuration

| Setting | Configuration |
|---|---|
| Virtualization Platform | Oracle VirtualBox |
| Guest Operating System | Kali Linux |
| Network Adapter | Bridged Adapter |
| Network Connection | Home Local Area Network |

Bridged networking allows the Kali virtual machine to appear as a separate device on the local network.

## Network Infrastructure

The home network uses a Verizon CR1000A router connected directly to a Google Nest Wifi Pro system.

The Verizon router provides the upstream network, while the primary Nest Wifi Pro operates in NAT/router mode and creates a separate internal network.

| Device | Interface | IP Address |
|---|---|---|
| Verizon CR1000A | LAN | 192.168.1.1 |
| Google Nest Wifi Pro | WAN | 192.168.1.152 |
| Google Nest Wifi Pro | LAN | 192.168.86.1 |
| Kali Linux VM | Network | 192.168.1.169 |

The Nest access points operate in bridge mode.

### Initial Finding

The network uses double NAT because both the Verizon CR1000A and the primary Google Nest Wifi Pro perform network address translation.

This configuration creates two separate private IP networks:

- Verizon network: 192.168.1.0/24
- Nest network: 192.168.86.0/24

Further investigation will determine whether this configuration creates unnecessary complexity or security limitations.
