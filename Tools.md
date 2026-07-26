# Tools & Infrastructure

## Hardware

### Dell OptiPlex 3050 SFF
- Primary Proxmox virtualization host
- Runs virtual machines and network services
- Hosts the virtual lab environment

### Dell Latitude E6320
- Physical Windows endpoint
- Planned Active Directory domain-joined client
- Used for testing endpoint management and Group Policy

### Cisco RV110W-A-NA-K9 V03
- Planned physical router/firewall
- Provides routing and network connectivity for the physical lab
- Intended to replace or supplement the virtual OPNsense router during physical networking labs

### Cisco WS-C2960C-12PC-L
- Planned managed Layer 2 switch
- Used for VLAN configuration, access ports, trunking, and physical network segmentation
- Provides physical connectivity between lab devices and the Proxmox host

---

## Virtualization & Networking

### Proxmox VE
- Virtualization platform running on the Dell OptiPlex 3050 SFF
- Hosts Windows and Linux virtual machines
- Uses virtual bridges (`vmbr0`, `vmbr1`) for network connectivity

### OPNsense
- Virtual router and firewall
- Provides routing, firewalling, and network services for the virtual lab
- Used for VLAN and network segmentation experiments

---

## Operating Systems

- Windows 11
- Windows Server 2022
- Linux distributions as needed for lab services and security testing

---

## Identity & Administration

### Active Directory Domain Services (AD DS)
- Centralized identity and authentication
- Organizational Units (OUs)
- User and computer accounts
- Administrative accounts
- Group Policy management

### Group Policy
- Centralized Windows configuration and security management
- Used to apply policies to domain-joined computers

---

## Network Concepts & Technologies

- VLANs
- 802.1Q Trunking
- Access Ports
- Inter-VLAN Routing
- DNS
- DHCP
- Active Directory
- Group Policy
- Network Segmentation
- Virtual Networking
