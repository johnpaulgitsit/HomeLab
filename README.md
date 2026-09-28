# Enterprise Homelab Infrastructure & Cybersecurity Lab

> A self-hosted, enterprise-style manufacturing company infrastructure and cybersecurity lab built with Proxmox VE, pfSense/OPNsense, Windows Server, Active Directory, and VLAN-based network segmentation.

## Overview

This project is an ongoing enterprise-style homelab designed to develop hands-on experience in **networking, virtualization, systems administration, Active Directory, firewall administration, and cybersecurity**.

The lab simulates the infrastructure of a small manufacturing company with separate network segments for management, servers, operations, IT, guest access, and security.

The environment currently includes:

- **Proxmox VE** — Virtualization platform for hosting servers and virtual machines
- **pfSense/OPNsense** — Physical router and firewall running on a ThinkCentre M73
- **Cisco Catalyst 2960-C** — Managed Layer 2 switch for VLANs and network connectivity
- **Cisco RV110W** — Repurposed as a guest wireless access point
- **Windows Server 2022** — Active Directory Domain Controller and DNS
- **Windows 11** — Domain-joined client for testing endpoint management and Group Policy
- **Active Directory** — Centralized identity management, user accounts, computers, and administrative accounts
- **VLANs** — Network segmentation for separating company departments and infrastructure

The lab is built incrementally, with an emphasis on understanding how enterprise networks are designed, secured, and maintained.

---

## Infrastructure Architecture

The lab uses a dedicated physical firewall to route traffic between VLANs and enforce network access policies.

The Cisco managed switch provides connectivity between the firewall, Proxmox host, and physical endpoints.

Proxmox serves primarily as the virtualization platform for the company's server infrastructure, including Windows Server and other virtual machines.

### Hardware

| Device | Role |
|---|---|
| ThinkCentre M73 | Physical firewall and router |
| Dell OptiPlex 3050 SFF | Proxmox virtualization host |
| Dell Latitude E6320 | Physical Windows client |
| Cisco WS-C2960C-12PC-L | Managed Layer 2 switch |
| Cisco RV110W | Guest wireless access point |

---

## Network & IP Addressing

The network is transitioning from an initial flat management network toward a segmented enterprise-style architecture.

The physical firewall provides gateway interfaces for the VLANs and will enforce traffic restrictions between network segments.

### Planned Network Segments

| VLAN | Department / Network | Purpose |
|---|---|---|
| Management | Management | Restricted access to network infrastructure |
| Servers | Server Infrastructure | Active Directory, DNS, and other server services |
| Operations | Operations | Manufacturing and operational endpoints |
| IT | Information Technology | IT administration and support systems |
| Guest | Guest Network | Internet access for guest devices |
| Security | Security | Security monitoring and analysis systems |

VLAN IDs, subnet assignments, and gateway addresses are documented in [`IP-Addressing/`](IP-Addressing/) and [`VLANS/`](VLANS/).

---

## Firewall & Network Segmentation

The ThinkCentre M73 runs pfSense/OPNsense and serves as the primary physical router and firewall for the lab.

The firewall is used to:

- Route traffic between VLANs
- Enforce access control between network segments
- Restrict access to management interfaces
- Separate guest traffic from internal company networks
- Apply firewall rules based on departmental access requirements

Firewall policies are being developed incrementally and tested against the services currently running in the lab.

---

## Virtualization & Server Infrastructure

### Proxmox VE

Proxmox VE runs on the Dell OptiPlex 3050 SFF and provides the virtualization platform for the lab's server infrastructure.

Current and planned uses include:

- Hosting Windows Server 2022
- Hosting Windows and Linux virtual machines
- Connecting virtual machines to the appropriate network segments
- Supporting future infrastructure and security services

---

## Active Directory

**Windows Server 2022** functions as the lab's Active Directory Domain Controller (DC) and provides centralized identity and DNS services.

The current Active Directory environment includes:

- Active Directory Domain Services (AD DS)
- DNS
- Organizational Units (OUs)
- User accounts
- Dedicated administrative accounts
- Active Directory Users and Computers
- Domain-joined Windows 11 client

Windows clients use the Domain Controller for DNS resolution and authenticate against the Active Directory domain.

The server infrastructure is being organized around a dedicated Server VLAN.

---

## Endpoint Management & Group Policy

Group Policy is used to centrally manage and secure domain-joined Windows endpoints.

Planned and ongoing activities include:

- Applying security policies to domain-joined computers
- Managing user and computer configurations
- Testing administrative restrictions
- Implementing endpoint hardening
- Validating access to internal services across VLANs

---

## Security Monitoring & Future Improvements

The long-term goal is to expand the lab into a more complete enterprise cybersecurity environment.

Planned improvements include:

- **Firewall Policy Development** — Implementing and validating inter-VLAN access controls
- **Network Segmentation** — Isolating departmental networks and restricting unnecessary communication
- **Endpoint Hardening** — Applying Windows security configurations through Group Policy
- **Security Monitoring** — Deploying Security Onion for log analysis and network monitoring
- **Incident Response** — Simulating security events and investigating activity across the network
- **Infrastructure Security** — Restricting management access and improving administrative security
- **Remote Access** — Exploring secure VPN connectivity for remote administration

These features will be introduced as the underlying infrastructure becomes operational.

---

## Repository Structure

```text
.
├── Topologies/
│   └── topo2.png
├── IP-Addressing/
├── Tools/
├── VLANS/
└── README.md
