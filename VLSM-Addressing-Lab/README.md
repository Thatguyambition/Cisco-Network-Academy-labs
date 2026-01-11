Lab: Design and Implement a VLSM Addressing Scheme

Project Objective
  The goal of this lab was to design a Variable Length Subnet Mask (VLSM) addressing scheme to provide the most efficient use of
  address space for a specific network topology. I calculated subnets based on varying host requirements for four LANs and a point-to-point WAN link.

Host Requirements & Design
  I calculated the subnets for a base network of 10.1.1.0/24 starting with the largest host requirement to minimize wasted addresses:

| LAN Name | Hosts Needed | Subnet / CIDR | First Usable | Broadcast |
| :--- | :--- | :--- | :--- | :--- |
| WS-2 | 47 | 10.1.1.0/26 | 10.1.1.1 | 10.1.1.63 |
| ES-2 | 28 | 10.1.1.64/27 | 10.1.1.65 | 10.1.1.95 |
| ES-1 | 11 | 10.1.1.96/28 | 10.1.1.97 | 10.1.1.111 |
| WS-1 | 5 | 10.1.1.112/29 | 10.1.1.113 | 10.1.1.119 |
| WAN Link| 2 | 10.1.1.120/30 | 10.1.1.121 | 10.1.1.123 |

Key Skills Demonstrated
 VLSM Calculation: Effectively dividing a Class C network into subnets of different sizes based on host needs.
 Efficient Addressing: Ensuring zero unused address space between contiguous subnets.
 Router/Switch Management: Implementing the management interface (SVI) for remote switch access.
