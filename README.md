# Scan-Your-Local-Network-for-Open-Ports
# Discover open ports in local network to understand network exposure.

# Installed Nmap Zenmap (GUI) https://nmap.org/download.html#windows 
# Selected Latest stable release self-installer: nmap-7.97-setup.exe
# First identified the Nmap version using Zenmap
nmap --version
<img width="945" height="440" alt="image" src="https://github.com/user-attachments/assets/e8f164f3-956e-46ab-a4ce-287c6faadd3c" />

# Then scanned the nmap
nmap -v scanme.nmap.org
# From nmap scanning identified the ports, Services and state of each ports
# Identified open ports are 22, 80, 9929 and 31337
# Services are ssh, http, nping-echo and Elite

# Then identified the IP address and Subnet mask to get the IP range
# IPv4 Address = 192.168.31.138
# Subnet Mask = 255.255.255.0
# Network IP range =  192.168.31.0 to 192.168.31.255
# Total usable IPs: 254

# Then found the Nmap report in command promt using same 192.168.31.0/24 in Target and command with nmap -sS 192.168.31.0/24
# Found the tcp ports, services and open state in command prompt
# IP address is 192.168.31.138
# Open ports are 135, 445 and 5432
# Services are msrpc, microsoft-ds and postgresql

# After that installed wireshark
# Then analyzed the packet capture which newly created .pcap with Wireshark
# Found the three section and identified the service in the protocol section 
# Identified the common service

# Then identified the risk from open port like 
# Unauthorized Access – Hackers may brute-force login ports like SSH (22), RDP (3389).
# Service Exploits – Attackers can target vulnerable services running on open ports.
# Information Leakage – Ports like SNMP or Telnet may leak system info.
# Malware Channels – Malware can use open ports to communicate with C2 servers.
# DDoS Attacks – Ports like DNS (53) and NTP (123) can be used in amplification attacks.
# Insecure Protocols – Ports running FTP (21), Telnet (23), or HTTP (80) transmit data without encryption.
# Unnecessary Exposure – Every open port increases the attack surface.

# OUTCOME RECEIVED
# IP address, subnet Mak and IP Range Identified
# scanned the open ports
# Identified the risk of the open port
# Undertood the limit 
