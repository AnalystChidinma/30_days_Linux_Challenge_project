# Day 14 - managing network connection

## Objective

To understand how to manage and inspect network connections in Linux using the nmcli command, with a focus on practical commands that can be executed without elevated (sudo) privileges.

---

## What I Learned

#### What is nmcli?
nmcli (NetworkManager Command Line Interface) is a tool used to:
- Manage network connections
- View network device status
- Configure networking settings
It works with NetworkManager, which handles:
- Network interfaces
- Wi-Fi and Ethernet connections
- IP configuration and connectivity
It is especially useful for:
- Server environments without GUI
- Automation and scripting

#### Key Capabilities of nmcli

1. View Network Devices
nmcli device status
Displays:
Device name (e.g., eth0, wlan0)
Device type (Ethernet, Wi-Fi)
Current state (connected/disconnected)

2. View Active Connections
nmcli connection show
Lists:
All configured connections
Active and inactive profiles

3. Display Detailed Network Information
nmcli device show
Provides:
IP addresses
DNS configuration
Gateway details

4. Check General Network Status
nmcli general status
Shows:
Overall connectivity state
NetworkManager status

5. Monitor Network Changes
nmcli monitor
Tracks:
Connection changes
Device state updates in real time

#### Commands That Require Elevated Privileges

The following operations typically require sudo access:

Connecting to a network
Modifying connection profiles
Restarting NetworkManager

Examples:

nmcli connection up <connection_name>
nmcli connection down <connection_name>
nmcli device wifi connect <SSID>

---

## Key Takeaways

- nmcli is a powerful CLI tool for managing network connections in Linux systems
- It complements lower-level tools like:
    - ip (interface and routing control)
    - ifconfig (legacy networking tool)
- Core understanding includes:
    - Devices → physical or virtual interfaces
    - Connections → configuration profiles
    - States → connected, disconnected, unavailable
- Even without administrative privileges, meaningful learning can be achieved by:
    - Inspecting configurations
    - Monitoring system behavior
    - Understanding network architecture
- In production environments, nmcli is critical for:
    - Remote server management
    - Network troubleshooting
    - Automated deployments

---

## Resources

- https://www.geeksforgeeks.org/linux-unix/nmcli-command-in-linux-with-examples/

---