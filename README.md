# CodeAlpha-Cyber-Security-Task 1
Perform tasks of CodeAlpha Cyber Security Internship 
# Network Sniffer

## Overview

This project is a network sniffer tool implemented in Python. It captures and analyzes network traffic, providing detailed information about each packet. The tool utilizes the Npcap library for packet capture on Windows systems.

## Features

- Captures network packets in real time.
- Provides detailed information about each packet, including source and destination IP addresses, protocol, packet length, time of capture, TTL, flags, and more.
- Supports analysis of protocols such as TCP, UDP, and ICMP.
- Displays source and destination MAC addresses for Ethernet packets.
- Supports capturing and analyzing fragmented IP packets.
- Provides TCP-specific information such as sequence numbers, acknowledgment numbers, and TCP flags.

## Installation

1. **Install the required dependencies:**
   ```bash
   pip install scapy
   vi sniffer.py ##upload code in this file##
python sniffer.py

### Explanation

TCP Packet:
Time: Timestamp of the packet capture.
Source IP: 192.168.1.2
Destination IP: 192.168.1.1
Protocol: 6 (TCP)
Length: 74 bytes
TTL: 64
Flags: TCP flags (e.g., SYN, ACK, etc.)
Fragment Offset: 0
Source MAC: 00:14:22:01:23:45
Destination MAC: 00:14:22:67:89
TCP Source Port: 54321
Destination Port: 80 (HTTP)
Sequence Number: 123456789
Acknowledgment Number: 987654321
Flags: S (SYN)
Payload: TCP payload (truncated in the sample)

ICMP Packet:
Time: Timestamp of the packet capture.
Source IP: 192.168.1.1
Destination IP: 192.168.1.2
Protocol: 1 (ICMP)
Length: 98 bytes
TTL: 64
Flags: None
Fragment Offset: 0
Source MAC: 00:14:22:67:89
Destination MAC: 00:14:22:01:23:45
ICMP Type: 0 (Echo Reply)
Code: 0
Payload: ICMP payload (truncated in the sample)

UDP Packet:
Time: Timestamp of the packet capture.
Source IP: 192.168.1.2
Destination IP: 192.168.1.3
Protocol: 17 (UDP)
Length: 60 bytes
TTL: 64
Flags: None
Fragment Offset: 0
Source MAC: 00:14:22:01:23:45
Destination MAC: 00:14:22:67:89
UDP Source Port: 12345
Destination Port: 53 (DNS)
Payload: DNS query response (truncated in the sample)

******Example Output**********

Time: 1627834207.123456, Source IP: 192.168.1.2, Destination IP: 192.168.1.1, Protocol: 6, Length: 74
    TTL: 64, Flags: , Fragment Offset: 0
    Source MAC: 00:14:22:01:23:45, Destination MAC: 00:14:22:67:89:ab
    TCP Source Port: 54321, Destination Port: 80
    Sequence Number: 123456789, Acknowledgment Number: 987654321, Flags: S
    Payload: <Raw  load='\x16\x03\x01\x00\x95\x01\x00\x00\x91\x03\x03[...]\n'>
Time: 1627834207.234567, Source IP: 192.168.1.1, Destination IP: 192.168.1.2, Protocol: 1, Length: 98
    TTL: 64, Flags: , Fragment Offset: 0
    Source MAC: 00:14:22:67:89:ab, Destination MAC: 00:14:22:01:23:45
    ICMP Type: 0, Code: 0
    Payload: <Raw  load='\x08\x00\x7d\x4b\x00\x01\x00\x01[...]\n'>
Time: 1627834207.345678, Source IP: 192.168.1.2, Destination IP: 192.168.1.3, Protocol: 17, Length: 60
    TTL: 64, Flags: , Fragment Offset: 0
    Source MAC: 00:14:22:01:23:45, Destination MAC: 00:14:22:67:89:ac
    UDP Source Port: 12345, Destination Port: 53
    Payload: <DNS  id=0x1c85 qr=1 opcode=QUERY aa=0 tc=0 rd=1 ra=1 z=0 rcode=0 qdcount=1 ancount=1 nscount=0 arcount=0 qd=<DNSQR  qname='www.example.com.' qtype=A qclass=IN |> an=<DNSRR  rrname='www.example.com.' type=A rclass=IN ttl=86400 rdlen=4 rdata=93.184.216.34 |> ns=None ar=None |>
