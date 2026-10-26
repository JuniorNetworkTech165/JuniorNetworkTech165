<div align="center">

  <h1>👨‍💻 BOITUMELO VILAKAZI 💻</h1>
  
  <h3>🌐 NETWORKING 🌐</h3>

  <p><b>Learning · Building · Troubleshooting</b></p>

  <p>
    <!-- Combined Portfolio & Alias Badge on Top -->
    <a href="https://github.com/JuniorNetworkTech165">
      <img src="https://img.shields.io/badge/PORTFOLIO-JUNIORNETWORKTECH165-00FF66?style=for-the-badge&logo=cisco&logoColor=white" />
    </a>
  </p>

  <p>
    <!-- Networking Badge Underneath Alone -->
    <a href="https://github.com/JuniorNetworkTech165">
      <img src="https://img.shields.io/badge/NETWORKING-blue?style=for-the-badge&logo=gns3&logoColor=white" />
    </a>
  </p>

</div>

---

# Lab 1: Basic 2-PC LAN.

## Tools used.
- **Cisco Packet Tracer**

## Network topology.
<img width="946" height="285" alt="Lab1-topology" src="https://github.com/user-attachments/assets/59953406-ba5e-43e7-82ec-af5658f98aa0" />

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
<img width="926" height="561" alt="Lab2-topology" src="https://github.com/user-attachments/assets/bdba781a-94ce-4b52-8a0c-031e1f13ec07" />

## IP Addressing Table.
| Device | Interface | IP Address       | Subnet Mask   | 
| :---   | :---      | :---             | :---          |
| PC1    | ethernet0 | 192.168.10.10    | 255.255.255.0 |
| PC2    | ethernet0 | 192.168.10.11    | 255.255.255.0 |
| PC3    | ethernet0 | 192.168.10.12    | 255.255.255.0 |
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
<img width="943" height="544" alt="Network topology" src="https://github.com/user-attachments/assets/20020bd9-aada-4577-a512-dda7039c02de" />

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

# Lab 4: Custom 5-PC LAN.

## Overview.
This lab project demonstrates a 5-PC Local Area Network (LAN) consisting of five end-user computers connected to a single central switch.

### Tools and components used.
- **Cisco Packet Tracer** (Network Simulation Software)
- 5 x PCs.
- 1 x Switch.
- 5 x Ethernet Copper Straight-Through Cables.

## Network topology.
<img width="949" height="409" alt="Network-topology" src="https://github.com/user-attachments/assets/585d1b71-938e-46b0-b837-812eedcbf425" />

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
