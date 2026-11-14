Ethernet Communication Investigation and Traffic Analysis Using Linux
Project Overview

This project investigates Ethernet communication and analyzes network traffic using Ubuntu Linux. It demonstrates important networking protocols such as ARP, ICMP, TCP and UDP using Linux commands, Wireshark and Netcat.
Objectives

    Understand Ethernet communication.

    Identify network interfaces and IP addresses.

    Examine routing tables and ARP information.

    Capture and analyze ARP packets.

    Test network connectivity using ICMP.

    Demonstrate TCP client-server communication.

    Demonstrate UDP client-server communication.

    Compare TCP and UDP protocols.

Tools and Technologies

    Ubuntu Linux

    Wireshark

    Netcat

    TCPdump

    iproute2

    net-tools

    Git and GitHub

Experiments Performed
1. Linux Network Configuration

Commands used:

ip addr
ip route
arp -a
hostname -I

2. Network Connectivity Testing

ping -c 4 8.8.8.8
ping -c 4 10.79.119.232

3. Network Port Analysis

ss -tuln
netstat -tuln

4. ARP Traffic Analysis

Wireshark filter:

arp

ARP Request and Reply packets were captured and analyzed.
5. ICMP Traffic Analysis

Wireshark filter:

icmp

Ping was used to generate ICMP Echo Request and Echo Reply packets.
6. TCP Communication

Server command:

nc -l 5000

Client command:

nc 127.0.0.1 5000

Message sent:

Hello from TCP Client

7. UDP Communication

Server command:

nc -u -l 5001

Client command:

nc -u 127.0.0.1 5001

Message sent:

Hello from UDP Client

TCP vs UDP
TCP	UDP
Connection-oriented	Connectionless
Reliable delivery	No delivery guarantee
Maintains packet order	No ordering guarantee
Three-way handshake	No handshake
Project Structure

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

Results

The investigation demonstrated network configuration using Linux commands and practical traffic analysis using Wireshark.

ARP, ICMP, TCP and UDP experiments were performed. TCP and UDP communication were tested locally using the loopback interface.
Conclusion

This project provided practical knowledge of Ethernet communication, network protocols, Linux networking commands and packet analysis. Wireshark helped inspect network traffic, while Netcat demonstrated client-server communication.

The project improved understanding of network communication and basic network troubleshooting.
