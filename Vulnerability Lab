# Cyber-Projects
Aspiring Cyber Security Professional. This will contain Folders that expand through different skills and will be reporting on all of projects in detail

Project 1#  Kali Linux & Metasploitable 2 Vulnerabilty Scanning 

Project Overview:The Objective of this project was to simulate basic vulnerabiliry assesments against an already vulnerable host (Metasploitable 2) to practice finding and identifying vulnerabilities and the risk associated with them.

Tools:
Attacker Vm: Kali Linux /IP address:10.02.15
Target Vm :Metasploitble 2 /IP address:192.168.56.102
Hypervisor:Oracle Virtual Box
The VM's are isolated from the rest of the network and they are only connected to Each other.



Step 1:
Discover Metasploitable 2 VM and Performed Pinging to confirm its activeness.:
<img width="549" height="181" alt="image" src="https://github.com/user-attachments/assets/b341826f-9281-47f1-a768-d255e1f5cb04" />

This image shows that 3 packets were sent and were received, Confirming that the Metasploitable Vm is active on same network. 

Step 2: Perform Vulnerability Scans on network Using Nmap.
-Used nmap to scan the Ip addr:192.16.56.102 in stealth mode
-Used the command -sS ( a SYn scan is the best fast and stealthy Scan due to the fact that it does not complete the TCP Handshake keeping you anonymous.)

-Scan Allowed me to identify open ports on the Vm that could be potentially be exploitated.


Starting Nmap 7.95 at 2025-09-16 23:17 EDT 

Nmap Scan report for IP addr: 192.168.56.102

Showed the Following Report:

<img width="524" height="365" alt="image" src="https://github.com/user-attachments/assets/060ff6f4-0df4-43c6-a63b-5d2fa89bc06b" />

The following important ports are reported as open:

-21/tcp open (FTP):High -Authentication is weak allowing unathorized files uploads and downloads.

-23/tcp open (Telnet):Critical- Is very vulnerable to brute force attacks, due to credentials not being encrypted.

-445/tcp (SMB) : High- Various amounts of critical vulnerabiliteis(Eternal Blue)

This showed multiple ports that could be exploitaped by an attacker to gain aunthorized access and can lead to data breaches and system compromise.

The next scan that was used to further investigate was:

nmap --script vuln 192.162.56.102
 This scan searches for known vulnerabilities on the network

 When the initial Nmap vuln scan was ran it failed with the following error
 
 Warning :192.168.56.102 giving up on port because retransmission cap hit (10)
    -This error shows that the host is either not active or the scan is getting blocked by a protection system. As the we know the host is online proven by the ping, We can assume that the usage of TCP traffic being blocked is a classic sign of a host-based firewall preventing these TCP requests.

Continued Investigation:

In order to confirm this I had to log onto Meta Sploitable VM to confirm this.
By logging on to the Vm using the admin account I was able to run the folowing command

 -sudo iptables -L (This output of this code would show active rules, confirming that a firewall was blocking the requests
 
 <img width="531" height="425" alt="image" src="https://github.com/user-attachments/assets/d90130ad-3cb5-4f34-89ea-4b9c95a623da" />

These findings were the completely opposite though. The image shows that all of the rules of the Firewall are completely all on accept, which shows that the firwall is not the issue as it is fully open.

This finding led to me the discovery that the reason the full vuln scan wasn't working was due to the massive and general scope the system was given. In order to fix this I ran the same scan in a more specific command which narrowed the scope and allowed the command to work.
 

Conclusion:
This project allowed me to gain hands-on practice with gaining vulnerability assesment abilities against a known vulnerable environment. This project helped me to use my practical knowledge and use in in a technical setting. Even thought the project had it's setbacks it allowed me to focus on trouble shooting and further investigating to find the root of errors and the workarounds to them in order to reach my goals.



