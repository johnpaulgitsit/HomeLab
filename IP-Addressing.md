IP Addressing & Device Inventory




The lab uses private IPv4 addressing to organize infrastructure and virtual machines. IP assignments are managed through a combination of **static addressing** for critical infrastructure and **DHCP** for client systems.

Current Network

| Device / System | IP Address    | IP Assignment | Network            | Role                                       |
| --------------- | ------------- | ------------- | ------------------ | ------------------------------------------ |
| OPNsense WAN    | DHCP          | DHCP          | Home Network       | Internet / WAN Gateway                     |
| OPNsense LAN    | `192.168.1.1` | Static        | Management LAN     | Internal Gateway / DHCP                    |
| Windows Server  | TBD           | Static        | Server Network     | Domain Controller / DNS / Active Directory |
| Windows 11 PC1  | DHCP          | DHCP          | User Network       | Domain-Joined Client                       |
| Proxmox Host    | TBD           | Static        | Management Network | Virtualization Host                        |
| Ubuntu Server   | TBD           | Static        | File Server VLAN   | File Server / Storage                      |

> Quick lil Note:          IP addresses marked `TBD` will be updated as the lab's VLAN and IP addressing structure is finalized.

---

Network Addressing Plan

| Network      | Subnet           | Gateway       | Purpose                                     | Status      |
| ------------ | ---------------- | ------------- | ------------------------------------------- | ----------- |
| Management   | `192.168.1.0/24` | `192.168.1.1` | Infrastructure management                   | Active      |
| Servers      | TBD              | TBD           | Domain Controller and server infrastructure | In Progress |
| Users        | TBD              | TBD           | Domain-joined client devices                | In Progress     |
| File Storage | TBD              | TBD           | File and storage services                   | Planned     |

---

IP Assignment Strategy

### Static IP Addresses

Static IP addresses are used for critical infrastructure that must remain consistently reachable.



As VLANs are introduced, the addressing model will transition toward dedicated subnets for management, servers, users, and file storage**, with OPNsense providing the default gateway and controlling inter-VLAN traffic.
