
## Rule 1 — ICMP Ping Detection
Detects any ICMP ping packet hitting the network.

## Rule 2 — ICMP Ping Sweep
Detects when same source sends 3+ ICMP packets in 3 seconds.
Used to catch Nmap ping sweeps with --send-ip flag.

## Rule 3 — TCP SYN Port Scan
Detects when same source sends 20+ SYN packets in 3 seconds.
Catches Nmap SYN stealth scans (-sS).

## Rule 4 — FTP Login Attempt
Detects any FTP login by looking for USER keyword in payload.
FTP sends credentials in plaintext — visible in Wireshark.

## Rule 5 — FTP Anonymous Login
Specifically detects anonymous FTP login attempts.
Anonymous FTP is a security risk if misconfigured.

## Rule 6 — SSH Brute Force
Detects 5+ SYN packets to port 22 within 60 seconds.
Catches Hydra brute force attacks against SSH.

## Rule 7 — Telnet Connection
Alerts on any Telnet connection attempt.
Telnet is unencrypted — no legitimate use in secure networks.

## Rule 8 — DoS SYN Flood
Detects 100+ SYN packets in 1 second from same source.
Catches hping3 SYN flood attacks.

## Rule 9 — Nmap OS Fingerprint
Detects SYN+FIN flag combination used by Nmap OS detection.
Normal traffic never uses SYN+FIN together.

## Rule 10 — HTTP Directory Traversal
Detects ../ in HTTP requests going to port 80.
Used to catch attempts to navigate outside web root.
