Network Scanning with Nmap on Kali Linux

Overview

This project demonstrates a basic network scanning task performed using **Nmap** on **Kali Linux**. The objective was to identify active hosts within a specific target network and then perform a full TCP port scan on those hosts. The process included host discovery and a comprehensive scan of all TCP ports using appropriate Nmap flags.

Tools Used

Kali Linux (Operating System)
Nmap (Network Mapper)

Target Network
192.168.233.0/24


Steps Performed

1. Host Discovery

To identify live hosts within the target network, the following Nmap command was used:

nmap -sn 192.168.233.0/24
-sn flag performs a "ping scan" to detect which hosts are up.

Once the active hosts were identified, a full TCP scan was performed on all ports using the following command:

nmap -p- -sS 192.168.233.X

Replace 192.168.233.X with the IP address of the discovered live host(s).

-p- flag scans all 65535 TCP ports.

-sS performs a SYN scan (stealth scan).

Conclusion

The scanning exercise provided insights into discovering live hosts in a network and identifying open ports using different Nmap scanning techniques. This is a foundational step in network reconnaissance and penetration testing.
