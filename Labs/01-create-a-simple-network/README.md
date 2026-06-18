# Packet Tracer Lab: Create a Simple Network

## Overview

This lab demonstrates a basic home network built in Cisco Packet Tracer. The network includes a wired PC, a wireless laptop, a wireless router, a cable modem, an internet cloud, and a server named `cisco.srv`.

## Objectives

- Build a simple network in Packet Tracer
- Connect a PC using Ethernet
- Connect a laptop using wireless
- Use DHCP to assign IP addresses
- Verify connectivity to `cisco.srv`

## Topology

![Network Topology](/Labs/01-create-a-simple-network/screenshots/Topology.png)

## Devices Used

| Device | Purpose |
|---|---|
| PC | Wired end device |
| Laptop | Wireless end device |
| Wireless Router | DHCP server and default gateway |
| Cable Modem | Connects local network to ISP/internet |
| Internet Cloud | Simulated ISP network |
| cisco.srv | Remote server used for connectivity testing |

## Cabling

| From | Interface | To | Interface | Cable Type |
|---|---|---|---|---|
| PC | FastEthernet0 | Wireless Router | Ethernet 1 | Copper straight-through |
| Wireless Router | Internet | Cable Modem | Port 1 | Copper straight-through |
| Cable Modem | Port 0 | Internet Cloud | Coaxial 7 | Coaxial |

## Configuration Summary

### PC

- Connected to the wireless router using Ethernet
- DHCP enabled
- Received an IPv4 address in the `192.168.0.0/24` network

### Laptop

- Ethernet module removed
- Wireless WPC300N module installed
- Connected to the wireless network `HomeNetwork`
- Received an IPv4 address using DHCP

## Verification

| Test | Result |
|---|---|
| PC received DHCP address | Successful |
| PC pinged `cisco.srv` | Successful |
| Laptop joined `HomeNetwork` | Successful |
| Laptop accessed `cisco.srv` in browser | Successful |

## Addressing Table

| Device | IPv4 Address | Subnet Mask | Default Gateway |
|---|---|---|---|
| PC | 192.168.0.___ | 255.255.255.0 | 192.168.0.1 |
| Laptop | 192.168.0.___ | 255.255.255.0 | 192.168.0.1 |

## What I Learned

- How to build a basic network topology in Cisco Packet Tracer
- How DHCP assigns IP addresses automatically
- How wired and wireless clients connect to the same local network
- How to test network connectivity using `ping`
- How a default gateway allows local devices to reach outside networks

## Files

- `create-a-simple-network.pkt` - Packet Tracer project file
- `screenshots/` - Lab screenshots and verification evidence
