# Scan-Your-Local-Network-for-Open-Ports
# Discover open ports in local network to understand network exposure.

*****************************************************************************************************************************************************

# Nmap Zenmap (GUI) Installation

Official website : https://nmap.org/download.html

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/666d273a-43f3-4389-a7da-60d0618fa1bf" />
                
Click on Windows OR https://nmap.org/download.html#windows

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/b766c06f-b939-429e-8839-a0603bccb5aa" />
                
                

Selected Latest stable release self-installer: nmap-7.97-setup.exe


<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/d526f8c9-b8b2-4384-a60d-4af87479c817" />


After installation open Command Prompt or Zenmap GUI.


<img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/fd613431-7b24-4976-a480-dd0483c35cd6" />


Identified the Nmap version using Zenmap

nmap --version

<img width="700" height="500" alt="image" src="https://github.com/user-attachments/assets/e8f164f3-956e-46ab-a4ce-287c6faadd3c" />



Scanned the nmap
nmap -v scanme.nmap.org

<img width="500" height="700" alt="image" src="https://github.com/user-attachments/assets/743b5a5f-5c76-4b3f-813f-c181fe5ffadf" />



From nmap scanning identified the ports, Services and state of each ports

<img width="500" height="200" alt="image" src="https://github.com/user-attachments/assets/25ca2a7c-d281-4215-8f33-c7f0e87d4a3f" />

<img width="500" height="200" alt="image" src="https://github.com/user-attachments/assets/bf100454-8447-4419-b7be-da5eb9678232" />

#------------------------------------------------------------------------------


# Identification of IP Range 

How to find the IP range using the IP address and subnet mask.

First need to open the command prompt using

    Press Win + R
    
<img width="300" height="150" alt="image" src="https://github.com/user-attachments/assets/22e24c5f-e4b7-46d2-bcb1-bd96aea922ff" />


Type cmd, press Enter.


<img width="300" height="150" alt="image" src="https://github.com/user-attachments/assets/c49f7cbe-09ed-47d9-b0fc-100b14a9089f" />

Command prompt opened

<img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/1fd11598-6c94-486b-801e-2e196c6d03ce" />

Type this command: 

    ipconfig

<img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/40bbcb0b-c4cd-4191-a828-9946f8c36838" />
 
        IPv4 Address = 192.168.31.39
        Subnet Mask = 255.255.255.0
        Network IP range =  192.168.31.0 to 192.168.31.255
        Total usable IPs: 254


Run below command to perform TCP SYN Scan

      nmap -sS 192.168.31.0/24

<img width="500" height="400" alt="image" src="https://github.com/user-attachments/assets/093bf114-aa1e-40ce-979a-31b8cd2889cf" />



<img width="500" height="400" alt="image" src="https://github.com/user-attachments/assets/2a6f040a-2bb6-4436-99ed-015affab64f5" />


    Identified the tcp ports, services and open state in command prompt
    IP address is 192.168.31.39
    Open ports are 135, 139 and 445
    Services are msrpc, netbios-ssn and microsoft-ds  



After receving the Network IP Range need to take the nmap report using Zenmap, 

Entered target as 192.168.31.0/24 in the command promt and command with nmap -sS 192.168.31.0/24.

<img width="300" height="700" alt="image" src="https://github.com/user-attachments/assets/61b7caef-d8fe-431b-9ceb-42e6000cc6ed" />


 
    Identified the tcp ports, services and open state in Zenmap
    IP address is 192.168.31.39
    Open ports are 135, 139 and 445
    Services are msrpc, netbios-ssn and microsoft-ds  



*****************************************************************************************************************************************************

# Wireshark Installation

To install Wireshark on a Windows system, follow these steps:

    Go to the official website: https://www.wireshark.org
    
    Click “Download” for Windows.

<img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/da7c8c26-e769-4024-a8bd-5a1df357b884" />

Choose the appropriate installer (usually the 64-bit Windows Installer).


<img width="383" height="115" alt="image" src="https://github.com/user-attachments/assets/61d2c5c5-808e-4449-95c6-da3fbd0b326a" />


<img width="581" height="481" alt="image" src="https://github.com/user-attachments/assets/0834a388-46e8-4121-96b3-f720e96853f2" />

   
    Click Install to begin. Wait for the process to complete.

<img width="576" height="476" alt="image" src="https://github.com/user-attachments/assets/7118ce1d-fbd6-4677-ad7e-58e347a9efdb" />
    

After Installation
   
    Launch Wireshark from the desktop or Start Menu.
    
    Select a network interface to start capturing packets.




Analyzed the packet capture which newly created .pcap with Wireshark
Found the three section and identified the service in the protocol section 
Identified the common service

Identified the risk from open port like 

    Unauthorized Access – Hackers may brute-force login ports like SSH (22), RDP (3389).
    Service Exploits – Attackers can target vulnerable services running on open ports.
    Information Leakage – Ports like SNMP or Telnet may leak system info.
    Malware Channels – Malware can use open ports to communicate with C2 servers.
    DDoS Attacks – Ports like DNS (53) and NTP (123) can be used in amplification attacks.
    Insecure Protocols – Ports running FTP (21), Telnet (23), or HTTP (80) transmit data without encryption.
    Unnecessary Exposure – Every open port increases the attack surface.

# OUTCOME RECEIVED
    Practiced the Nmap Scanning to identify the open ports
    Identification of IP address, subnet Mak and IP Range Identified
    Identified the risks of the open port
    
