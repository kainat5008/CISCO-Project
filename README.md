# 🖧 Computer Network Design & Implementation

This project demonstrates the design and configuration of a complex computer network using Cisco Packet Tracer. It covers topology planning, subnetting, routing, DHCP, NAT, ACLs, and an SMTP mail server—all configured to simulate a functional enterprise-level network.

---

## 📘 Project Overview

The project follows a structured, step-by-step approach:

- Designing the network topology
- Performing subnetting for efficient IP allocation
- Configuring dynamic IP allocation via DHCP
- Implementing multiple routing protocols (OSPF, EIGRP, RIP)
- Setting up NAT for internal-to-external communication
- Securing traffic using Access Control Lists (ACLs)
- Configuring an internal SMTP mail server with test accounts

---

## 🛠️ Technologies Used

- **Cisco Packet Tracer**
- **Routing Protocols**: OSPF (multi-area), EIGRP, RIP
- **IP Addressing**: VLSM and CIDR
- **DHCP, NAT, ACL**
- **SMTP Email Configuration**

---

## 🗺️ Network Topology

- Multi-router setup with switches, PCs, smartphones, and servers
- Labelled networks: A–K, with varying size and function
- WAN connections using `/30` subnets
- Efficient IP planning using VLSM to avoid waste

---

## 📑 Subnetting Overview

| Network | Hosts Needed | Subnet Mask | Network Address | Usable IP Range           |
|---------|--------------|-------------|------------------|----------------------------|
| G       | 94145        | /15         | 203.0.0.0        | 203.0.0.1 – 203.1.255.254  |
| F       | 83034        | /15         | 203.2.0.0        | 203.2.0.1 – 203.3.255.254  |
| D       | 61812        | /16         | 203.4.0.0        | 203.4.0.1 – 203.4.255.254  |
| C, B, A, K, I, H, E, J | ...         | See table above  | ...                        |

Full subnet plan includes:
- Proper allocation of network/broadcast addresses
- Wildcard masks for ACLs
- Serial link planning between routers using `/30`

---

## 🔄 Routing Configuration

| Protocol | Usage Area                |
|----------|---------------------------|
| OSPF     | Area 1 & 2 (hierarchical) |
| EIGRP    | Dynamic and scalable zone |
| RIP      | Legacy/legacy-compatible  |

Each router configured based on its network region and protocol compatibility.

---

## 🌐 DHCP Setup

- Central DHCP server with defined pools for each subnet
- Ensured automatic and correct IP assignment to all hosts
- Excluded IPs reserved for static devices (e.g., routers, servers)

---

## 🔁 NAT Configuration

- **Dynamic NAT**: For internal hosts to share public IPs
- **Static NAT**: For servers requiring fixed mappings
- Ensured outbound internet access for internal networks

---

## 🔐 Access Control Lists (ACLs)

Security policies implemented using standard/extended ACLs:

- Blocked a PC from Network A from accessing the Web Server
- Denied smartphones in Network E and J Web Server access
- Prevented all devices in Network D from reaching the Web Server
- ACLs were applied to the correct interfaces and directions

---

## 📧 SMTP Mail Server

- Internal mail server setup using SMTP protocol
- Created and tested multiple email accounts
- Verified mail delivery across the internal network

---

## ✅ Final Testing

| Feature           | Status        |
|-------------------|---------------|
| End-to-end ping   | ✅ Successful |
| DHCP assignment   | ✅ Validated  |
| Routing protocols | ✅ Verified   |
| NAT translation   | ✅ Working    |
| ACL restrictions  | ✅ Enforced   |
| Mail server       | ✅ Operational|

---

## 📌 Conclusion

This project demonstrates a full-cycle network deployment, integrating core concepts of IP addressing, routing, DHCP, NAT, ACLs, and server configuration. It highlights the importance of planning, execution, and testing in building reliable and secure network infrastructures.

---



