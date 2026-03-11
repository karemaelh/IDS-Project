 Phase 2 — Lab Setup Notes

 Network Architecture
- Network: 192.168.56.0/24 (VirtualBox Host-Only)
- Kali Linux (Attacker): 192.168.56.10
- Ubuntu Server (IDS/Snort): 192.168.56.20
- Metasploitable 2 (Victim): 192.168.56.30

 Configuration Notes
- All VMs set to Host-Only adapter in VirtualBox
- Static IPs assigned manually on each VM
- Kali: configured via /etc/network/interfaces
- Ubuntu: configured via /etc/netplan/00-installer-config.yaml
- Metasploitable: configured via /etc/network/interfaces

 Connectivity Test
- Kali → Ubuntu: ✅ ping successful
- Kali → Metasploitable: ✅ ping successful
- Metasploitable → Ubuntu: ✅ ping successful
