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

## Network Equipment

The existing home network uses a Verizon CR1000A router and a Google Nest Wifi Pro mesh system.

The relationship between the router and mesh system will be documented after verifying the current network configuration.

## Network Configuration

| Parameter | Value |
|---|---|
| Kali IP Address | To be documented |
| Network Subnet | To be documented |
| Default Gateway | To be documented |
| Network Interface | To be documented |
| Nest Operating Mode | To be verified |

## Screenshots and Evidence

The following screenshots will be added:

- Kali Linux running inside VirtualBox.
- VirtualBox network adapter configuration.
- Kali network interface configuration.
- Kali routing table.

## Notes

Any installation issues, configuration changes, or troubleshooting performed during the setup process will be documented here.
