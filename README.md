markdown
# Motswana Auto Electrical - Network Design Project

**Student:** Musa Prince Sithoza  
**Student Number:** 45500207  
**Location:** Taung  
**Module:** CMG 325 - Computer Networks

---

## Project Overview

This repository contains the complete design documentation and implementation for a secure and scalable enterprise network for Motswana Auto Electrical. The network connects three departments—**Admin**, **Workshop**, and **Sales**—using a Hub-and-Spoke topology with a central Main Router.

The project was designed and tested in **Cisco Packet Tracer**.

---

## Repository Structure
NETWOKING/
│
├── Milestone1_Design/
│ ├── Physical_Topology.pkt
│ ├── Logical_Topology.pkt
│ └── Milestone1_Design_Document.docx
│
├── Milestone2_Implementation/
│ ├── Motswana_Network_Final.pkt
│ └── Milestone2_Implementation_Report.pdf
│
├── screenshots/
│ ├── ping_routers.png
│ ├── ping_pcs.png
│ ├── show_ip_route.png
│ └── show_ospf_neighbors.png
│
└── README.md

text

---

## Milestone 1: Client Design Review

**Status:** ✅ Complete

**Deliverables:**
- Client requirements analysis
- Physical topology design (Hub-and-Spoke)
- Logical topology design (VLANs 10, 20, 30, 40)
- IP addressing plan
- Initial GitHub repository

**Design Justification:**
- **Star (Hub-and-Spoke) topology** for centralized management and fault isolation
- **VLAN segmentation** to separate departments and improve security
- **/30 subnets** for WAN links to conserve IP addresses
- **/24 subnets** for LANs to allow future growth

---

## Milestone 2: Implementation and Testing

**Status:** ✅ Complete

**Implemented Features:**
- VLANs (10 – Admin, 20 – Workshop, 30 – Sales, 40 – Servers)
- Inter-VLAN routing on the Admin Router using sub-interfaces
- OSPF dynamic routing across all four routers
- DHCP for automatic IP address assignment in all departments
- Trunk ports between switches and routers
- WAN serial links between the Main Router and department routers
- Server configuration in the Admin department
- IP Phones connected in each department

**Testing Results:**

| Test | Result |
|------|--------|
| Admin PC → Admin Router (192.168.10.1) | ✅ 0% packet loss |
| Admin PC → Workshop Router (192.168.20.1) | ✅ 0% packet loss |
| Admin PC → Sales Router (192.168.30.1) | ✅ 0% packet loss |
| Admin PC → Workshop PC (192.168.20.3) | ✅ 0% loss (after ARP) |
| Admin PC → Sales PC (192.168.30.4) | ✅ 0% loss (after ARP) |
| OSPF neighbors (all routers) | ✅ FULL state |

---

## IP Addressing Plan

| Network | VLAN | Subnet | Gateway |
|---------|------|--------|---------|
| Admin | 10 | 192.168.10.0/24 | 192.168.10.1 |
| Workshop | 20 | 192.168.20.0/24 | 192.168.20.1 |
| Sales | 30 | 192.168.30.0/24 | 192.168.30.1 |
| Servers | 40 | 192.168.40.0/24 | 192.168.40.1 |
| WAN 1 (Admin) | – | 10.1.1.0/30 | – |
| WAN 2 (Workshop) | – | 10.1.2.0/30 | – |
| WAN 3 (Sales) | – | 10.1.3.0/30 | – |

---

## Technologies Used

- Cisco Packet Tracer 9.0.1
- Cisco 2911 Routers
- Cisco 2960 Switches
- OSPF (Open Shortest Path First) routing protocol
- VLANs (802.1Q) for network segmentation
- DHCP for automatic IP assignment

---

## Contact

**Musa Prince Sithoza**  
Student Number: 45500207  
Location: Taung, South Africa

---

*This project was completed as part of the CMG 325 - Computer Networks module.*
