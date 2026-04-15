# Secure Multi-Router Network Design & Implementation

A comprehensive network security project demonstrating the architecture and configuration of a segmented enterprise network. This project focuses on isolating departmental traffic using VLANs and enforcing security policies via Access Control Lists (ACLs).

## Project Overview
The goal of this project was to move away from a flat network architecture to a secure, hierarchical design. By implementing logical segmentation, the network reduces the blast radius of potential internal threats and ensures that sensitive departments (like Management) are protected from unauthorized access.

## Technical Implementation
* **Network Segmentation:** Divided the organization into four functional VLANs (IT, HR, Sales, Management).
* **Inter-VLAN Routing:** Configured **Router-on-a-Stick** on Cisco routers to facilitate communication between authorized segments.
* **Dynamic Routing:** Implemented **OSPF (Open Shortest Path First)** to ensure efficient and scalable routing across three different routers.
* **Access Control Lists (ACLs):** Configured and deployed ACLs to enforce the **Principle of Least Privilege**, specifically restricting access to the Management VLAN to only authorized IT endpoints.
* **Trunking & Encapsulation:** Used IEEE 802.1Q encapsulation for trunk links between switches and routers.

## Network Topology
The infrastructure consists of:
- **3 Cisco Routers** (R1, R2, R3)
- **3 Catalyst Switches**
- **6 End-Devices** (PCs/Laptops) representing different departments.

## Key Configurations Demonstrated
1. **VLAN Assignment:** `VLAN 11 (IT)`, `VLAN 12 (HR)`, `VLAN 31 (Sales)`, `VLAN 32 (Management)`.
2. **Security Policy:** An ACL was applied to ensure only `Laptop1` in the IT VLAN can reach `VLAN 32`.
3. **Verification:** Validated connectivity via ICMP (ping) and confirmed MAC address table accuracy across all switches.

## Files in this Repository
* `Project-2 packet tracer.pkt`: The original Cisco Packet Tracer lab file.
* `Project_Documentation.pdf`: Detailed walkthrough and screenshots of the configuration.

## How to Run
1. Download and install [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer).
2. Clone this repository.
3. Open the `.pkt` file to view the topology and configuration.
