# Day 15 - Networking Basics with ping Command

## Objective

To understand and use the ping command for basic network diagnostics, including testing connectivity, measuring response time, and identifying potential network issues.
---

## What I Learned

- The ping command is a network utility used to:
Test reachability of a host
Measure round-trip time (RTT)
- Diagnose network issues such as latency, packet loss, and DNS problems
- It works by sending ICMP Echo Request packets and receiving responses.

`ping [options] host_or_IP_address` 

---

## What I Built / Practiced

- #### Check internet connectivity
ping google.com

#### Ping a specific IP address
ping 8.8.8.8

#### Limit number of requests
ping -c 4 google.com

#### Show only summary
ping -q -c 5 google.com

#### Set timeout
ping -w 5 google.com

#### Add timestamps
ping -D google.com

---

## Key Takeaways

- ping helps determine if a system or website is reachable
- RTT (Round Trip Time) indicates network speed and latency
- Packet loss indicates network instability

If ping 8.8.8.8 works but ping google.com fails, 

This indicates a DNS resolution issue, not a connectivity issue

---

## Resources

- https://www.geeksforgeeks.org/linux-unix/ping-command-in-linux-with-examples/

---

## Output

to Test internet connection and Observe latency and packet loss I ran this command below 

ping -c 4 google.com

![alt text](image.png)
