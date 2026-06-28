# Corporate Network Design and Security Policy Implementation

This repository contains the undergraduate thesis project developed at **Ege University, Department of Computer Engineering**.

The project focuses on designing, implementing, and validating a secure enterprise network architecture in the **EVE-NG simulation environment**. The network was modeled as a multi-location corporate/banking infrastructure consisting of a headquarters site, a main retail branch, two satellite branches, and a remote worker segment.

The main goal of the project was not only to provide network connectivity, but also to enforce security policies, segment critical resources, control inter-site communication, and validate both allowed and intentionally restricted traffic flows.

## Project Overview

The implemented topology includes the following network locations:

* **Headquarters (HQ):** Central network site, core services, DMZ, monitoring, and VPN hub
* **Main Retail Branch:** Branch office with local users, ATM, CCTV, guest network, and branch security controls
* **Satellite Branch 1:** Router-based branch network with teller, ATM, and CCTV segments
* **Satellite Branch 2:** Router-based branch network with teller, ATM, VoIP, printer, and CCTV segments
* **Remote Worker:** Remote access segment for external staff connectivity

All locations are connected through a simulated WAN/Internet environment and secured using VPN tunnels and access control policies.

## Technologies and Concepts Used

* EVE-NG
* Cisco ASA
* Router and Layer 2/Layer 3 switching
* Site-to-Site IPsec VPN / VTI
* OSPF dynamic routing
* VLAN segmentation
* ACL-based access control
* NAT and NAT exemption
* DMZ design and isolation
* Syslog-based centralized monitoring
* Positive and negative security testing
* Network troubleshooting and validation

## Security Architecture

The project was designed according to secure enterprise networking principles such as:

* **Network segmentation:** Separating teller, ATM, CCTV, guest, voice, printer, management, DMZ, and server networks
* **Least privilege:** Allowing only required traffic between network zones
* **Defense-in-depth:** Combining VPN, firewall rules, VLANs, ACLs, NAT policies, and monitoring
* **DMZ isolation:** Separating public-facing services from internal corporate resources
* **Guest and ATM restrictions:** Preventing untrusted or sensitive endpoint groups from reaching unauthorized internal networks
* **Centralized logging readiness:** Using Syslog architecture for monitoring security-relevant events

## Validation and Testing

The project was validated through multiple layers of testing, including:

* Interface and VLAN verification
* Endpoint-to-gateway connectivity tests
* Headquarters-to-branch reachability tests
* Branch-to-branch communication tests through HQ
* IPsec VPN tunnel verification
* OSPF neighbor and route propagation checks
* ACL and firewall rule validation
* DMZ access and isolation tests
* Negative security tests for intentionally blocked traffic flows

During implementation, several troubleshooting cases were analyzed and documented, such as NAT route-lookup behavior on Cisco ASA, CEF forwarding issues in the EVE-NG environment, ACL-related branch communication problems, and duplicate IP conflicts in the DMZ network.

## Repository Structure

The repository currently includes the following project files:

- `FKG_BANK_THESIS_REPORT.pdf` — Final thesis report
- `FKG_BANK_THESIS_REPORT.docx` — Editable thesis report
- `JURI_SUNUM_DOSYASI.pptx` — Jury presentation file
- `THESIS_POSTER.pdf` — Thesis poster
- `README.md` — Project documentation

## Project Outcome

As a result of this project, a secure, scalable, and manageable enterprise network architecture was designed and validated in a simulation environment. The final design demonstrates secure inter-branch communication, controlled access between network zones, isolated critical services, and a structured approach to network security validation.

## Authors

- Kutlu Çağan Akın
- Furkan İyem
- Gülnaz Karaca

## Supervisor

**Prof. Dr. Orhan Dağdeviren**

## Keywords

EVE-NG, Cisco ASA, IPsec VPN, OSPF, VLAN, ACL, NAT, DMZ, Syslog, Network Security, Enterprise Network Design, Cybersecurity
