# Ethernet Communication Investigation and Traffic Analysis Using Linux

## Project Overview

This project focuses on investigating Ethernet communication and analyzing network traffic using Ubuntu Linux. It explores the working of different networking protocols and demonstrates how network packets can be captured and analyzed using Wireshark.

The project includes practical experiments using Linux networking commands, Wireshark, and Netcat.

## Objectives

- To understand Ethernet communication and network architecture.
- To study MAC addresses and IP addresses.
- To understand the working of ARP and ICMP protocols.
- To analyze TCP and UDP communication.
- To capture and examine network packets using Wireshark.
- To learn basic Linux networking commands.
- To compare TCP and UDP protocols.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Ubuntu Linux | Operating system |
| Wireshark | Network packet analysis |
| Tcpdump | Network packet capturing |
| Netcat (nc) | TCP and UDP communication |
| Git | Version control |
| GitHub | Project hosting |

## Linux Networking Commands

The following commands were used during the investigation:

| Command | Description |
|---|---|
| `ip addr` | Displays network interfaces and IP addresses |
| `ip route` | Displays routing information |
| `arp -a` | Displays the ARP table |
| `ping -c 4 8.8.8.8` | Tests network connectivity |
| `ss -tuln` | Displays listening TCP and UDP ports |
| `netstat -tuln` | Displays network connections and listening ports |
| `hostname -I` | Displays the system IP address |

## Practical Experiments

### 1. ARP (Address Resolution Protocol)

ARP is used to identify the MAC address associated with an IPv4 address on a local network.

**Procedure:**
- Opened Wireshark and selected the wireless network interface.
- Applied the display filter `arp`.
- Cleared the neighbor cache.
- Pinged the default gateway.
- Observed ARP request and reply packets.

**Observation:** ARP packets were successfully captured and analyzed using Wireshark.

### 2. ICMP (Internet Control Message Protocol)

ICMP is used for network diagnostics and error reporting.

**Procedure:**
- Used the `ping` command to test connectivity.
- Captured ICMP packets using Wireshark.
- Applied the display filter `icmp`.
- Examined Echo Request and Echo Reply packets.

**Observation:** The local gateway responded successfully to the connectivity test.

### 3. TCP (Transmission Control Protocol)

TCP is a connection-oriented protocol that provides reliable data transmission.

**Procedure:**
- Created a TCP server using Netcat on port 5000.
- Connected a client using the loopback address `127.0.0.1`.
- Sent a test message from the client to the server.
- Captured packets using Wireshark.
- Applied the filter `tcp.port == 5000`.

**Observation:** TCP communication was successfully tested using Netcat.

### 4. UDP (User Datagram Protocol)

UDP is a connectionless protocol that allows data transmission without establishing a connection.

**Procedure:**
- Created a UDP listener on port 5001.
- Connected a UDP client using Netcat.
- Sent a test message.
- Captured packets using Wireshark.
- Applied the filter `udp.port == 5001`.

**Observation:** UDP communication was successfully tested using Netcat.

**Note:** TCP and UDP experiments were performed through the loopback interface (`127.0.0.1`). These experiments demonstrate local communication, not transmission over the physical wireless network.

## TCP vs UDP Comparison

| Feature | TCP | UDP |
|---|---|---|
| Connection | Connection-oriented | Connectionless |
| Reliability | Reliable | No delivery guarantee |
| Speed | Generally slower | Generally faster |
| Acknowledgment | Supported | Not provided by UDP itself |
| Data Delivery | Ordered delivery | No ordering guarantee |
| Applications | Web browsing, file transfer | Streaming, online gaming |

## Project Structure

```text
Ethernet_Project/
│
├── README.md
│
├── docs/
│   ├── Study_Report.pdf
│   └── Analysis_Report.pdf
│
├── screenshots/
│   ├── ip_addr.png
│   ├── ip_route.png
│   ├── arp_table.png
│   ├── ping_test.png
│   ├── ss_output.png
│   ├── netstat_output.png
│   ├── hostname_ip.png
│   ├── arp_analysis.png
│   ├── icmp_analysis.png
│   ├── tcp_analysis.png
│   └── udp_analysis.png
│
└── wireshark/
    ├── arp_capture.pcapng
    ├── icmp_capture.pcapng
    ├── tcp_capture.pcapng
    └── udp_capture.pcapng
```

*The folder structure above represents the intended project organization. Only files actually included in the repository should be expected.*

## Results

- Identified network interfaces and IP addresses using Linux commands.
- Examined routing information and ARP table entries.
- Captured and analyzed ARP packets.
- Captured and analyzed ICMP packets.
- Tested TCP communication using Netcat.
- Tested UDP communication using Netcat.
- Used Wireshark to inspect network traffic.
- Studied the differences between TCP and UDP.

## Conclusion

This project provided practical knowledge of Ethernet communication and network traffic analysis using Ubuntu Linux. It helped in understanding networking protocols such as ARP, ICMP, TCP, and UDP.

By using Linux networking commands, Wireshark, and Netcat, different network communication processes were investigated and analyzed. The project improved practical understanding of computer networks, packet capturing, and network troubleshooting.

## Author

**Project Title:** Ethernet Communication Investigation and Traffic Analysis Using Linux

**Operating System:** Ubuntu Linux

**Tools Used:** Wireshark, Netcat, Tcpdump, Git, and GitHub
