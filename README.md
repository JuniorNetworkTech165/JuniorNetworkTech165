# Lab 1: Basic 2-PC LAN.

## Tools used.
- **Cisco Packet Tracer**

## Network topology.
![Lab 1 topology](https://github.com/JuniorNetworkTech165/1st-Lab-2-PC-LAN/blob/main/Lab1-topology.png?raw=true)

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
- **Generic Ethernet switch.**

## Network topology.
![4-PC LAN Topology](https://github.com/JuniorNetworkTech165/Basic-4-PC-LAN/raw/main/Lab2-topology.png)

## IP Addressing Table.
| Device | Interface | IP Address       | Subnet Mask    | 
| :---   | :---      | :---             | :---           |
| PC1    | ethernet0 | 192.168.10.10    | 255.255.255.0  |
| PC2    | ethernet0 | 192.168.10.11    | 255.255.255.0  |
| PC3    | ethernet0 | 192.168.10.12    | 255.255.255.0  |
| PC4    | ethernet0  | 192.168.10.13    | 255.255.255.0 |

## Verification and Status.
- [x] Network topology created in GNS3.
- [X] All devices powered on.
- [x] IP configuration applied on all VPCS nodes.
- [x] Full connectivity verified via ICMP ping tests across all devices.

---

# 3rd Lab: Troubleshoot incorrect IP addressing.

This lab demonstrate how to identify, troubleshoot, and fix IP addressing misconfiguration in a Local Area Network (LAN).

## Tools & Environment.
* **Emulation Software: GNS3**
* **Device: 3x VPCS, 1x Ethernet switch** 

---

**The table below shows the initial network configuration, which were recorded during the lab setup.**

## 1. Initial Addressing table.

|   Device   |  Interface  |   IP Address      |  Subnet Mask     |
|   :---     |  :---       |   :---            |  :---            |
|   **PC1**  |  ethernet0  |   `192.168.20.10` |  `255.255.255.0` |
|   **PC2**  |  ethernet0  |   `192.168.20.11` |  `255.255.255.0` |
|   **PC3**  |  ethernet0  |   `192.168.30.12` |  `255.255.255.0` |

### Network topology.
![Network Topology](https://github.com/JuniorNetworkTech165/Troubleshoot-incorrect-IP-addressing/blob/main/Network%20topology.png?raw=true)

---

## 2. Problem Statement.

* **PC1**  and **PC2** are configured on the same `192.168.20.0/24` network.

* **PC3** was deliberately misconfigured on the `192.168.30.0/24` network.

* **Result:** Ping requests sent from **PC1** or **PC2** to **PC3** failed, because **PC3** did not belong to the same `192.168.20.0/24` network.

---

## 3. Troubleshooting & Solutions.

1. **Diagnosis:** I tried to ping **PC3** (`192.168.30.12`) from **PC1** and **PC2**, but the connection timed out, because **PC3** did not belong to the same `192.168.20.0/24` network.

2. **Fix:** I corrected **PC3**'s IP configuration, so that it can belong to the same `192.168.20.0/24` network as **PC1** and **PC2**.

### Corrected Addressing Table.

|  Device   |  Interface |  IP Address      |  Subnet Mask       |  Status   |
|  :---     |  :---      |  :---            |  :---              |  :---     |
|  **PC1**  |  ethernet0 |  `192.168.20.10` |  `255.255.255.0`   |  Active   |
|  **PC2**  |  ethernet0 |  `192.168.20.11` |  `255.255.255.0`   |  Active   |
|  **PC3**  |  ethernet0 |  `192.168.20.12` |  `255.255.255.0`   | **Fixed** |


---

## 4. Testing and verification.

* I ran the command `ping 192.168.20.12` from both **PC1** and **PC2**.
* **Results:** The ping test was successful! All ping packets were received with zero packet loss, confirming that all computers can talk to each other.


---

# Lab 4: Custon 5-PC LAN.

## Overview.
This lab project demonstrates a 5-PC Local Area Network (LAN) consisting of five end-user computers connected to a single central switch.

### Tools and components used.
- **Cisco Packet Tracer** (Network Simulation Software)
- 5 x PCs.
- 1 x Switch.
- 5 x Ethernet Copper Straight-Through Cables.

## Network topology.
![Network topology diagram](./<img width="949" height="409" alt="Network-topology" src="https://github.com/user-attachments/assets/bcdec023-ab8e-4d79-b058-257aa5515ab1" />
)

## IP Address Table.

| Host | Interface |  IP Address   |  Subnet Mask    |   Staus    |
| :--- | :---      |  :---         |  :---           |   :---     |
| PC0  |    Fa0    | `192.168.0.1` | `255.255.255.0` | **Active** |
| PC1  |    Fa0    | `192.168.0.2` | `255.255.255.0` | **Active** |
| PC2  |    Fa0    | `192.168.0.3` | `255.255.255.0` | **Active** |
| PC3  |    Fa0    | `192.168.0.4` | `255.255.255.0` | **Active** |
| PC4  |    Fa0    | `192.168.0.5` | `255.255.255.0` | **Active** |

## Status and Verification.
- I successfully configured the IP Address and subnet mask on all the PCs correctly.
- I used the `ping` command utility, to test connectivity between all the PCs.
- **Results:** The ping test results were successful, proving good network connectivity between the PCs.
