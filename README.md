Enterprise Branch Office Network Design (Cisco Packet Tracer)

This repository contains a complete implementation of a small-scale branch office network for a fictional company using Cisco Packet Tracer.
The project demonstrates real-world networking skills including subnetting, VLANs, inter-VLAN routing, DHCP, wireless setup, and network testing.

Project Overview

XYZ Company is setting up a new branch in a village near Bon Alba.
The branch must operate independently from HQ, using only:

1 Cisco Router

1 Cisco Switch

Multiple Wireless Access Points

The branch contains three departments, each with its own VLAN & subnet:

Department	VLAN ID	Subnet (/26)
Admin/IT	10	192.168.1.0/26
Finance/HR	20	192.168.1.64/26
Customer Service	30	192.168.1.128/26

The router performs Inter-VLAN Routing using router-on-a-stick.
DHCP is configured to automatically assign IPs to all devices.

Technologies Used

Cisco Packet Tracer

Subnetting (/24 → /26)

VLANs & Trunking

Router-on-a-stick (Inter-VLAN Routing)

DHCP server (on Router)

Wireless networks (WPA2)

Switch Access & Trunk Port Configuration

ICMP Testing (Ping)

Network Topology

Upload your diagram in the screenshots folder and link it here later.

Subnetting Details
| Subnet | Network ID    | Host Range | Broadcast ID | VLAN |
| ------ | ------------- | ---------- | ------------ | ---- |
| 1      | 192.168.1.0   | 1–62       | 63           | 10   |
| 2      | 192.168.1.64  | 65–126     | 127          | 20   |
| 3      | 192.168.1.128 | 129–190    | 191          | 30   |

VLAN Configuration
| VLAN | Department       | Switch Ports |
| ---- | ---------------- | ------------ |
| 10   | Admin/IT         | Fa0/2–Fa0/4  |
| 20   | Finance/HR       | Fa0/5–Fa0/7  |
| 30   | Customer Service | Fa0/8–Fa0/10 |

Router Configuration (Router-on-a-Stick)
| Subinterface | VLAN | Gateway       |
| ------------ | ---- | ------------- |
| g0/0.10      | 10   | 192.168.1.1   |
| g0/0.20      | 20   | 192.168.1.65  |
| g0/0.30      | 30   | 192.168.1.129 |

Wireless Network Setup
| Department       | SSID         | Password     |
| ---------------- | ------------ | ------------ |
| Admin/IT         | admin-wifi   | admin@123    |
| Finance/HR       | finance-wifi | finance@123  |
| Customer Service | cs-wifi      | customer@123 |


Network Testing

✔ Devices receive IP via DHCP
✔ VLANs communicate through router
✔ Wireless clients connect successfully
✔ Ping tests successful

Folder Structure
/
├── README.md
├── branch-office-network.pkt
├── configs/
│   ├── router-config.txt
│   ├── switch-config.txt
│   └── access-points-config.txt
└── screenshots/
