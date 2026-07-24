# Enterprise Homelab Infrastructure & Cybersecurity Lab

> A self-hosted enterprise-style infrastructure and cybersecurity lab built with Proxmox VE, OPNsense, Windows Server, Active Directory, and VLAN segmentation.

## Overview

This project is an ongoing enterprise-style homelab designed to develop hands-on experience in **networking, virtualization, systems administration, Active Directory, and cybersecurity**.

The environment currently includes:

* **Proxmox VE** — Virtualization platform
* **OPNsense** — Router, firewall, and DHCP
* **Windows Server** — Active Directory Domain Controller and DNS
* **Windows 11** — Domain-joined client
* **Active Directory** — Users, Computers, OUs, and administrative accounts
* **VLANs** — Network segmentation currently being implemented



The lab is built incrementally, with the goal of developing a segmented enterprise network and expanding into security hardening, monitoring, and incident response.
The current network is transitioning from an initial management network toward dedicated VLANs for server and client infrastructure.

---

## Network & IP Addressing

The initial lab network uses the `192.168.1.0/24` address space.

* **OPNsense** — Internal gateway: `192.168.1.1`
* **Windows Server** — Static IP for Domain Controller and DNS
* **Windows 11 PC1** — DHCP-assigned client IP
* **Proxmox** — Management infrastructure
* **VLAN 20** — Planned server network

Detailed addressing information is maintained in [`IP-Addressing/`](IP-Addressing/).

---

## Active Directory

**Windows Server** functions as the lab's **Active Directory Domain Controller (DC)** and provides centralized identity and DNS services.

The current Active Directory environment includes:

* Active Directory Domain Services (AD DS)
* DNS
* Organizational Units (OUs)
* User accounts
* Dedicated administrative account
* Active Directory Users and Computers
* Domain-joined Windows 11 client

Windows 11 User PCs use the Domain Controller for DNS and authenticates against the Active Directory domain.


Detailed VLAN information is maintained in [`VLANS/`](VLANS/).

As VLANs are implemented, OPNsense will control traffic between network segments through routing and firewall policies.


* **`Topologies/`** — Network topology diagrams
* **`IP-Addressing/`** — IP assignments and network addressing
* **`Tools/`** — Platforms and technologies used in the lab
* **`VLANS/`** — VLAN architecture and segmentation


## Project Objective

The long-term goal is to evolve this environment into a realistic enterprise-style infrastructure and cybersecurity lab for practicing **network segmentation, identity and access management, firewall administration, Windows Server, Active Directory, security hardening, monitoring, and incident response**.
