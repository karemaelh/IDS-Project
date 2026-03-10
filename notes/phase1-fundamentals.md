# Phase 1 — Fundamentals Notes

## TCP/IP Model
- 4 layers: Application, Transport, Internet, Network Access
- Data gets encapsulated at each layer going down
- Data gets unwrapped at each layer going up

## TCP vs UDP
- TCP = reliable, uses 3-way handshake (SYN, SYN-ACK, ACK)
- UDP = fast, no handshake, no guaranteed delivery
- TCP used for: SSH, HTTP, FTP
- UDP used for: DNS, VoIP, Gaming

## TCP Flags
- SYN = start connection
- ACK = acknowledge
- FIN = close connection
- RST = force reset
- A port scan = many SYN packets with no ACK back

## Packets
- Every packet has a Header + Payload
- Header contains: source IP, destination IP, ports, flags
- Payload contains: the actual data

## CIDR
- /32 = single IP
- /24 = 256 IPs (used for lab: 192.168.56.0/24)
- /16 = 65,536 IPs

## IDS vs IPS
- IDS = detects and alerts only
- IPS = detects and blocks
- We are building an IDS using Snort

## Detection Types
- Signature-based = matches known patterns (what Snort uses)
- Anomaly-based = detects deviation from normal behavior

## False Positives vs False Negatives
- False positive = alerts on safe traffic (annoying)
- False negative = misses real attack (dangerous)

## Common Attacks to Detect
- Port scan = many SYN packets to different ports
- Ping sweep = ICMP pings to find live hosts
- Brute force = repeated login attempts
- DoS = flood of packets to overwhelm target
- Telnet = unencrypted protocol, always suspicious
- Banner grabbing = reading service version info via netcat
