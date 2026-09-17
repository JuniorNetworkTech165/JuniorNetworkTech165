# Lab 1: Basic 2-PC LAN.

## Tools used.
- **Cisco Packet Tracer**

## Network topology.
![Lab 1 topology](Lab1-topology.png)

## IP Configuration.
- **PC0:** `192.168.1.10/24`
- **PC1:** `192.168.1.11/24`

## Status.
- [X] Switch connection active.
- [X] Ping verified between PC0 and PC1.

---

# Lab 2: Basic 4-PC LAN.

## Overview.
This lab demonstrates a basic Local Area Network (LAN) layout connecting four Virtual PC Simulators (VPCS) to a single Ethernet switch using GNS3.

## Tools used.
- **GNS3 (Graphical Network Simulator-3)**
- **VPCS (Virtual PC Simulator)**
- **Generic Ethernet switch**

## Network topology.
![4-PC LAN Topology](Lab2-topology.png)

## IP Addressing Table.
| Device | Interface | IP Address       | Subnet Mask   | 
| :---   | :---      | :---             | :---          |
| PC1    | ethernet0 | 192.168.10.10    | 255.255.255.0 |
| PC2    | ethernet0 | 192.168.10.11    | 255.255.255.0 |
| PC3    | ethernet0 | 192.168.10.12    | 255.255.255.0 |
| PC4    | ethernet  | 192.168.10.13    | 255.255.255.0 |

## Verification and Status
- [x] Network topology created in GNS3.
- [X] All devices powered on.
- [x] IP configuration applied on all VPCS nodes.
- [x] Full connectivity verified via ICMP ping tests across all devices.
