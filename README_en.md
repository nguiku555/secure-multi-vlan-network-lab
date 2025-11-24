# Secure Multi-VLAN Network Lab
*Small Enterprise Network Lab*

A lab project configured using Cisco Packet Tracer to implement foundational enterprise networking and security practices.

---

## Key Features

* **Multi-VLAN Design:** 4 distinct VLANs (1F, 2/F, 3/F, Management) for logical segmentation.
* **Layer 3 Backbone:** OSPF routing configured across the core switches and router.
* **Security & Policy Implementation:**
    * **ACL Enforcement:** Extended ACLs enforce inter-VLAN isolation and least privilege access.
    * **Anti-Reconnaissance:** ICMP blocked to internal router interfaces and DMZ subnets.
    * **Management Control:** Dedicated VLAN with controlled access policies.
    * **Port Security:** Enabled on all access ports.
* **Internet Access:** NAT (Overload) configured.
* **DMZ:** Isolated zone for servers.

---

## Design Intent and Objectives

This lab simulates the network of a three-story small enterprise with the following design goals:

* **Security Design:** VLANs are separated per floor, with a dedicated Management VLAN isolated from external networks.
* **Access Control:** Extended ACLs enforce inter-segment access restrictions and allow DMZ access.
* **Redundancy and Connectivity:** OSPF routing ensures stable and fault-tolerant inter-floor communication.
* **Cost Efficiency:** Router and L2 switch on 1/F; L3 switches on 2/F and 3/F.
* **Operational Management:** Port Security, PortFast, and BPDU Guard are configured to improve security and operational efficiency.
* **Remote Access:** All devices are managed exclusively via SSH.
* **NAT Configuration:** NAT Overload is applied for VLANs connecting to external networks.

---

## Technologies Used

VLANs, SVI, Inter-VLAN Routing, OSPFv2, ROAS, DHCP, SSH, NTP, NAT (Overload), Standard/Extended ACLs, Port Security.

---

## Device Access / Passwords

All devices in this lab are configured with passwords for security purposes:  
- **Username:** `admin`  
- **Password / Secret:** `1234`  
- **Enable / Privileged EXEC:** `abcd`  

Please ensure you use these credentials when accessing the devices in Cisco Packet Tracer.

---

## File Contents

* [topology.jpg](topology.jpg) – Network diagram  
* [lab.pkt](lab.pkt) – Packet Tracer project file  
* [Configs/](Configs/) – Device configuration output

---

## Notes

* **Configuration Source:** The configuration files in the `/configs` folder are the direct `show running-config` output from the virtual devices, ensuring accuracy.
* **File Requirement:** The `.pkt` file must be opened using **Cisco Packet Tracer** software.
* **ACL Naming:** ACLs are functionally descriptive for clarity (e.g., SSH ACL is named `SSH`).
* **Purpose:** This lab is for practice and demonstration purposes.




