# Tools & Infrastructure

## Hardware

### ThinkCentre M73
- Dedicated physical firewall and router running pfSense/OPNsense
- Provides inter-VLAN routing, firewall enforcement, and network segmentation
- Serves as the primary gateway between the lab network and the home network/internet
- Hosts VLAN interfaces and their associated gateway addresses

### Dell OptiPlex 3050 SFF
- Primary Proxmox virtualization host
- Hosts Windows Server and other virtual machines supporting the lab's server infrastructure
- Connects to the Cisco managed switch through the Server VLAN
- Used for virtualized infrastructure and network services

### Dell Latitude E6320
- Physical Windows endpoint
- Planned Active Directory domain-joined client
- Used to test endpoint management, Group Policy, and client connectivity across VLANs

### Cisco RV110W-A-NA-K9 V03
- Repurposed as a Guest Access Point
- Provides wireless connectivity for guest devices
- Intended to keep guest wireless access separate from internal company networks

### Cisco WS-C2960C-12PC-L
- Managed Layer 2 switch
- Provides VLAN-based network segmentation and physical device connectivity
- Configured for access ports and 802.1Q trunking
- Connects the firewall, Proxmox host, and physical endpoints

---

## Virtualization & Networking

### Proxmox VE
- Virtualization platform running on the Dell OptiPlex 3050 SFF
- Hosts Windows Server, Windows client, and Linux virtual machines
- Uses virtual bridges (`vmbr0`, `vmbr1`) for virtual network connectivity
- Supports the lab's server infrastructure and virtualized services

### pfSense / OPNsense
- Runs on the dedicated ThinkCentre M73 as the physical firewall and router
- Provides inter-VLAN routing and firewall policy enforcement
- Uses VLAN interfaces with static gateway addresses
- Serves as the primary routing point for segmented lab networks

### Virtual OPNsense
- Previously used as a virtual router and firewall within Proxmox
- Supports virtual networking and isolated lab experiments
- Can be used separately from the physical firewall environment

---

## Operating Systems

- Windows 11
- Windows Server 2022
- Linux distributions for server services and security testing
- pfSense/OPNsense firewall operating system

---

## Identity & Administration

### Active Directory Domain Services (AD DS)
- Centralized identity and authentication for the lab's Windows environment
- Manages domain users, computer accounts, and Organizational Units (OUs)
- Supports separate administrative accounts and domain-based access control
- Provides centralized authentication for domain-joined endpoints

### Group Policy
- Centralized Windows configuration and security management
- Applies security settings and configuration policies to domain-joined computers
- Used to test endpoint hardening and administrative controls

---

## Network Concepts & Technologies

- VLANs and network segmentation
- 802.1Q trunking
- Access ports and VLAN assignment
- Inter-VLAN routing
- Firewall rules and traffic filtering
- DNS and DHCP
- Active Directory and Group Policy
- Physical and virtual networking
- Guest network isolation
- Server, Management, User, Operations, and Security network segmentation
- Network gateway configuration and routing
