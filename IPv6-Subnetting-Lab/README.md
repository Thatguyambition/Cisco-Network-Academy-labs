Lab: Implement a Subnetted IPv6 Addressing Scheme

Project Objective
  The goal of this lab was to design a contiguous IPv6 subnetting scheme and implement it across a dual-router topology.
  I calculated five unique /64 subnets based on a starting prefix of 2001:db8:acad:00c8::/64.

Addressing Table & Calculation
  I incremented the subnet ID consecutively by one for each network requirement:

| Device | Interface | IPv6 Address | Link-Local |
| :--- | :--- | :--- | :--- |
| **R1** | G0/0 | 2001:db8:acad:00c8::1/64 | fe80::1 |
| **R1** | G0/1 | 2001:db8:acad:00c9::1/64 | fe80::1 |
| **R1** | S0/0/0 | 2001:db8:acad:00cc::1/64 | fe80::1 |
| **R2** | G0/0 | 2001:db8:acad:00ca::1/64 | fe80::2 |
| **R2** | G0/1 | 2001:db8:acad:00cb::1/64 | fe80::2 |
| **R2** | S0/0/0 | 2001:db8:acad:00cc::2/64 | fe80::2 |

Key Concepts Applied
  Hexadecimal Subnetting:** Correctly incrementing the 4th hextet (00c8, 00c9, 00ca, etc.).
  Link-Local Addressing:** Manually assigning `fe80` addresses for consistent gateway identification.
  SLAAC:** Configuring router advertisements so PCs could auto-configure their own addresses.
