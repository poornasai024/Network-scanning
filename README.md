# Network-scanning

Network Scanning - Network scanning is the process of probing server or host for open ports to identify services running and potential vulnerabilities.

Here we are using a tool named Nmap for network scanning it is a open source tool ans has multiple options which helps us to map a organizations network structure.

In Nmap there are multiple scan options but here we are going to perform a SYN scan which is also known as half open scan or stealth scan.

command - nmap -sS 192.168.0.0/24 -oN basicscan.txt
-sS represents for stealth scan and -oN for storing the otput result in a text file.

Basically what happens in the stealth scan is that instead of going for a full three-way-handshake it performs only half handshake that is after the initial SYN packet if the system got the SYN-ACK it sonfirms that the port is open and stop the process before sending the ACK packet.


In my network there are only few devices which are 192.168.0.1(router) 192.168.0.114(my machine) 192.168.0.118, 192.168.0.137.
The common ports which are opened in my network are  SSH, DNS, HTTP, NetBios.The result will be uploaded in the repo.


