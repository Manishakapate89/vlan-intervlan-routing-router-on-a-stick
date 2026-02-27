# VLAN and Inter-VLAN Routing Project (Router-on-a-Stick)

## 📌 Project Overview

This project demonstrates VLAN configuration and Inter-VLAN Routing using the Router-on-a-Stick method in Cisco Packet Tracer.

The objective of this project is to:
- Create multiple VLANs
- Assign switch ports to VLANs
- Configure trunking between switch and router
- Enable communication between VLANs using subinterfaces
- Test connectivity between different departments

---

## 🖥️ Devices Used

- 1 × Cisco ISR4331 Router
- 1 × Cisco 2960 Switch
- 4 × PCs
- Copper Straight-Through Cables

---

## 🗺️ Network Topology

PC1 & PC2 → VLAN 10 (SALES)  
PC3 & PC4 → VLAN 20 (HR)  

All PCs connect to the switch.  
Switch connects to router using trunk link.  
Router performs Inter-VLAN routing.

---

## 🧩 VLAN Configuration

| VLAN ID | VLAN Name | Network Address        |
|----------|------------|------------------------|
| 10       | SALES      | 192.168.10.0/24        |
| 20       | HR         | 192.168.20.0/24        |

---

## 🌐 IP Addressing Scheme

### Router Subinterfaces

- G0/0/0.10 → 192.168.10.1 /24
- G0/0/0.20 → 192.168.20.1 /24

### PCs Configuration

VLAN 10:
- PC1 → 192.168.10.10
- PC2 → 192.168.10.20
- Default Gateway → 192.168.10.1

VLAN 20:
- PC3 → 192.168.20.10
- PC4 → 192.168.20.20
- Default Gateway → 192.168.20.1

---

## ⚙️ Configuration Summary

### Switch Configuration
- VLAN creation (10 & 20)
- Access port assignment
- Trunk port configuration (G0/1)

### Router Configuration
- Subinterface creation
- 802.1Q encapsulation
- IP addressing
- Enabling physical interface

---

## 🧪 Testing & Verification

Commands used for verification:

### On Router:
- show ip interface brief
- show running-config

### On Switch:
- show vlan brief
- show interfaces trunk

### Connectivity Test:
- Ping from VLAN 10 PC to VLAN 20 PC

Successful ping confirms Inter-VLAN routing is working.

---

## 🎯 Learning Outcomes

After completing this project, the following concepts are understood:

- VLAN segmentation
- Access vs Trunk ports
- 802.1Q encapsulation
- Router-on-a-Stick concept
- Inter-VLAN communication
- Basic troubleshooting

---

## 🚀 Future Enhancements

- Add DHCP configuration
- Implement ACL between VLANs
- Add more VLANs
- Convert to Layer 3 Switch design
- Implement Port Security

---

## 📂 Tools Used

- Cisco Packet Tracer
- CLI Configuration (GigabitEthernet interfaces only)

---

## 👨‍💻 Author

MANISHA KAPATE 
CCNA Practice Project  
