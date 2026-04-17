# Day 16 - Ip Commands in Linux

## Objective

To understand and apply the Linux ip command for inspecting and managing network interfaces, IP addressing, routing, and connectivity. This exercise focuses on practical usage of key ip command objects and their role in troubleshooting network-related issues.

---

## What I Learned

1. What the ip Command Really Is

The Linux ip command is part of the iproute2 package and serves as the modern replacement for older tools like:

ifconfig
route
netstat

Core Responsibility:

It is the central command-line utility for managing networking in Linux systems.
- Uses an object-based structure (link, address, route, neighbour)
- Supports both IPv4 and IPv6
- Provides real-time and detailed network insights

#### Key ip Command Objects
- ip addr → View and manage IP addresses
- ip link → Manage network interfaces
- ip route → Control routing tables
- ip neighbour → View ARP (IP-to-MAC mapping)
- ip monitor → Real-time network changes

---

## What I Built / Practiced

- Inspected network interfaces and IP configurations
`ip addr show`

- Checked link-layer details and interface status
`ip link`

- Assigned an IP address to an interface
`sudo ip addr add 192.168.1.100/24 dev eth0`

- Brought a network interface up and down
`sudo ip link set eth0 up`
`sudo ip link set eth0 down`

- Viewed and modified routing tables
`ip route`
`sudo ip route add default via 192.168.1.254 dev eth0`

- Monitored network interface statistics
`ip -s link show eth0`

Observed real-time network changes
`ip monitor`

---

## Key Takeaways

- The ip command is essential for modern Linux networking
- Networking issues are often infrastructure-related, not application-related
- Understanding routing and interfaces is critical for:
    - Data pipelines
    - Distributed systems
    - Cloud environments
- Real-time monitoring (ip monitor, ip -s) is powerful for troubleshooting
---

## Resources

- https://www.geeksforgeeks.org/linux-unix/ip-command-in-linux-with-examples/

---

## Output
