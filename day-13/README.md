# Day 13 - Linux Networking (ip Command)

## Objective

To understand how to use the ip command to manage and inspect network interfaces, IP addresses, and routing in Linux systems.

---

## What I Learned

### What is the ip Command?
- The ip command is a modern Linux networking tool used to:
    - Configure network interfaces
    - Manage IP addresses
    - Control routing tables
- It replaces older tools like:
    - ifconfig
    - route
- It supports:
    - IPv4 and IPv6
    - Real-time monitoring
    - Advanced network configurations

### Command Structure
ip [OPTIONS] OBJECT {COMMAND}

- OBJECT → network component (e.g., address, link, route)
- COMMAND → action (e.g., show, add, del) 

#### Key Components of ip Command
1. Address Management
- Displays and manages IP addresses
ip addr show
Shows:
    - Interface names
    - IPv4 and IPv6 addresses
    - MAC address
    - Subnet details

2. Link Management
- Manages network interfaces
ip link
ip -s link
Shows:
    - Interface status (UP/DOWN)
    - MTU
    - Packet statistics

3. Routing Table
Displays how traffic flows in the network
ip route

4. Neighbor (ARP Table)
Maps IP addresses to MAC addresses
ip neighbour

5. Monitoring Network Changes
ip monitor
Displays real-time changes in:
Interfaces
IP addresses
Routes

### Key Operations
#### Assign IP Address (Requires sudo)
ip addr add 192.168.1.100/24 dev eth0

#### Delete IP Address (Requires sudo)
ip addr del 192.168.1.100/24 dev eth0

#### Enable Interface (Requires sudo)
ip link set eth0 up

#### Disable Interface (Requires sudo)
ip link set eth0 down

#### Add Default Gateway (Requires sudo)
ip route add default via 192.168.1.254 dev eth0

### Interface Statistics
#### Monitor Traffic
ip -s link show eth0

#### Check Errors and Dropped Packets
ip -s link show eth0 | grep -E 'errors|dropped'
---

## What I Practiced

- Viewed Network Interfaces
`ip addr show`

- Checked Interface Status using 
`ip link`

- Viewed Routing Table
`ip route`
---

## Challenges Faced

- Due to lack of sudo, i can not 
    - sign IP addresses
    - Modify routing tables
   
---

## Key Takeaways

- The ip command is the modern standard for Linux networking
- Provides more flexibility and detail than ifconfig
Core components to understand:
    - address → IP configuration
    - link → interface control
    - route → traffic direction
    - neighbour → device mapping
Without admin access, strong understanding can be built through:
Observation
Output analysis
Command exploration
- 

---

## Resources

- https://www.geeksforgeeks.org/linux-unix/ip-command-in-linux-with-examples/