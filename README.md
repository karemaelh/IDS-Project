# Intrusion Detection System — Home Lab

> A full IDS lab built from scratch to detect real network attacks using Snort, Kali Linux, and Splunk.

##  Status — COMPLETED

## Project Summary
Built a virtualized network security lab simulating real-world attack scenarios and detecting them using a custom-configured Snort IDS. All attacks were captured, analyzed in Wireshark, detected by Snort, and visualized in Splunk.

## Lab Architecture

Kali Linux (Attacker)     → 192.168.56.10
Ubuntu Server (IDS/Snort) → 192.168.56.20
Metasploitable 2 (Victim) → 192.168.56.30
Network: 192.168.56.0/24 — Isolated Internal Network

##  Attacks Simulated & Detected

| # | Attack | Tool | Rule Triggered |
|---|--------|------|----------------|
| 1 | ICMP Ping | ping | ICMP PING DETECTED |
| 2 | Ping Sweep | Nmap | ICMP PING SWEEP DETECTED |
| 3 | TCP SYN Port Scan | Nmap -sS | TCP SYN PORT SCAN |
| 4 | FTP Login Attempt | ftp/Hydra | FTP LOGIN ATTEMPT |
| 5 | FTP Anonymous Login | ftp | FTP ANONYMOUS LOGIN |
| 6 | SSH Brute Force | Hydra | SSH BRUTE FORCE |
| 7 | Telnet Connection | telnet | TELNET CONNECTION ATTEMPT |
| 8 | DoS SYN Flood | hping3 | POSSIBLE DOS SYN FLOOD |
| 9 | Nmap OS Fingerprint | Nmap -O | NMAP OS FINGERPRINT |
| 10 | HTTP Directory Traversal | curl | HTTP DIRECTORY TRAVERSAL |

## Tools Used

| Tool | Purpose |
|------|---------|
| Snort 2.9.x | Intrusion Detection System |
| Kali Linux | Attack simulation |
| Metasploitable 2 | Vulnerable target |
| Wireshark | Packet analysis |
| Splunk | Alert visualization |
| Nmap | Port scanning & OS detection |
| Hydra | Brute force attacks |
| hping3 | DoS simulation |
