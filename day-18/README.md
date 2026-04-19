# Day 18 - Traceroute Command in Linux

## Objective

To understand and apply the `traceroute` command for analyzing network paths, identifying latency issues, and troubleshooting connectivity problems across multiple network hops.

---

## What I Learned

### What is traceroute

`traceroute` is a network diagnostic tool used to track the path that data packets take from your system to a destination. 

 It sends packets across the internet and shows you every "hop" (router or server) it passes through along the way, as well as how long each step takes.

It provides visibility into:
- Each **hop (router/server)** along the path
- **Round-trip time (RTT)** for each hop
- Points of **delay or failure** in a network

### Syntax

`traceroute [options] destination`

- To use Traceroute, you need to install the Traceroute package. Here's how you can do it: 

 `sudo apt install traceroute`

 ### Basic Traceroute usage

 To perform a basic traceroute operation to a destination, simply execute the following command:

 `traceroute google.com`

### How Traceroute Works (TTL Mechanism)

Traceroute works using the **Time To Live (TTL)** field in IP packets:

- A packet is sent with TTL = 1 → expires at first router  
- Router sends back an **ICMP Time Exceeded** message  
- TTL increases (2, 3, 4…) until destination is reached  

This process allows traceroute to map each hop along the route.

### Key Concepts

- **Hop** → A router or network device along the path  
- **RTT (Round Trip Time)** → Time taken for packet to go and return  
- `* * *` → No response (timeout, firewall, or dropped packet)  

### Difference Between Ping and Traceroute
ping - Checks if a host is reachable
traceroute - Shows the path taken to reach the host

- If a service is down, use ping
- If latency exists, use traceroute
- If port is closed,  use ss

Used IPv4 explicitly
    `traceroute -4 google.com`

Disabled DNS resolution for faster output
    `traceroute -n google.com`

Limited number of hops
    `traceroute -m 5 google.com`

Reduced number of probes per hop
    `traceroute -q 1 google.com`

Specified destination port
    `traceroute -p 8080 google.com`
---

## Challenges Faced

- unable to install the traceroute

---

## Key Takeaways

- traceroute shows the full path packets take across networks
- Helps identify where latency or failure occurs
- Works using the TTL expiration mechanism
- Essential for diagnosing network issues in distributed systems
- 

---

## Resources

- https://www.geeksforgeeks.org/linux-unix/traceroute-command-in-linux-with-examples/

---
