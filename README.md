# Cisco Static Routing Lab

## Overview

This project demonstrates the design and configuration of a multi-router network using Cisco Packet Tracer.

The network consists of three Cisco 2911 routers connecting two separate LANs through point-to-point WAN links. Static routing was configured to enable communication between devices on the 192.168.1.0/24 and 192.168.3.0/24 networks.

## Network Topology

The network includes:

- 3 Cisco 2911 routers
- 2 Cisco 2960 switches
- 2 servers
- 1 client PC
- 2 LAN networks
- 2 point-to-point WAN connections

## IP Addressing Scheme

| Network | Subnet | Purpose |
|---|---|---|
| LAN 1 | 192.168.1.0/24 | Server LAN |
| WAN 1 | 10.1.1.0/30 | Router-to-router link |
| WAN 2 | 10.2.2.0/30 | Router-to-router link |
| LAN 2 | 192.168.3.0/24 | Client LAN |

### End Devices

| Device | IP Address |
|---|---|
| Server 1 | 192.168.1.100 |
| Server 2 | 192.168.1.101 |
| Client PC | 192.168.3.5 |

## Static Routing

Static routes were manually configured on the routers to allow communication between networks that are not directly connected.

The edge routers forward traffic destined for the remote LAN toward the intermediate router, which provides connectivity between both sides of the network.

## Connectivity Testing

End-to-end connectivity was tested using ICMP ping.

The client PC on the 192.168.3.0/24 network successfully communicated with:

- 192.168.1.100
- 192.168.1.101

Successful ping tests confirmed that the static routes were correctly forwarding traffic between the two LANs.

## Verification

The following Cisco IOS command was used to verify the routing tables:

`show ip route`

Static routes are identified by the `S` code in the routing table.

## Skills Demonstrated

- Cisco Packet Tracer
- IPv4 addressing
- IPv4 subnetting
- Static routing
- Cisco router configuration
- Basic switch connectivity
- Point-to-point WAN configuration
- Routing table verification
- Network troubleshooting
- ICMP connectivity testing

## Project Files

The `.pkt` file included in this repository contains the complete Cisco Packet Tracer topology and configuration.

It can be opened using Cisco Packet Tracer to inspect, modify, and test the network.
