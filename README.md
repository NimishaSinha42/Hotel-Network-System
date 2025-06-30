#  Taj Hotel-Network-System

Project Overview

This project involves designing and implementing a multi-floor enterprise network for *Vic Modern Hotel*, using Cisco Packet Tracer. The network infrastructure is segmented across three floors, each containing multiple departments. It incorporates core networking concepts including VLANs, inter-VLAN routing, OSPF protocol, port security, DHCP configuration, and wireless access.

---

## 🗂️ Network Structure

### 🔁 Routers:
- **3 Routers** placed in the Server Room (IT Department - 3rd Floor)
- Connected in a full mesh via **Serial DCE cables**
- IP Links between routers:
  - `10.10.10.0/30`
  - `10.10.10.4/30`
  - `10.10.10.8/30`

### 🖧 Switches & Access:
- **1 Switch per floor**
- Each floor supports:
  - Wired LAN per department
  - Wi-Fi network for laptops and phones
  - 1 Printer per department

---

## 🔒 VLAN Configuration

| Department     | VLAN | Subnet            | Floor |
|----------------|------|-------------------|-------|
| Reception      | 80   | 192.168.8.0/24    | 1st   |
| Store          | 70   | 192.168.7.0/24    | 1st   |
| Logistics      | 60   | 192.168.6.0/24    | 1st   |
| Finance        | 50   | 192.168.5.0/24    | 2nd   |
| HR             | 40   | 192.168.4.0/24    | 2nd   |
| Sales/Marketing| 30   | 192.168.3.0/24    | 2nd   |
| Admin          | 20   | 192.168.2.0/24    | 3rd   |
| IT             | 10   | 192.168.1.0/24    | 3rd   |

---

## ⚙️ Routing & Services

- **Routing Protocol**: OSPF (Single Area)
- **DHCP**: Configured on each router to serve its respective VLANs
- **Connectivity**: All departments and devices can communicate across floors

---

## 🧪 Special Configuration

### 🔐 Port Security (IT Department):
- Port `fa0/1` (on IT floor switch) configured for:
  - **Sticky MAC Address Binding**
  - **Violation Mode: Shutdown**
  - Only allows **Test-PC** for secure remote access testing

---

## 🚀 Tools Used
- **Cisco Packet Tracer**
- **Subnetting and VLAN planning**
- **OSPF routing simulation**
- **DHCP, Port Security, and SSH configuration**

---

## ✅ Outcomes
- Efficient, scalable network layout
- Logical segmentation and security via VLANs
- Smooth inter-floor and inter-departmental communication
- Security enforcement with sticky MAC and remote login testing
