# Network-scanning

Network Scanning - Network scanning is the process of probing server or host for open ports to identify services running and potential vulnerabilities.

Here we are using a tool named Nmap for network scanning it is a open source tool ans has multiple options which helps us to map a organizations network structure.

In Nmap there are multiple scan options but here we are going to perform a SYN scan which is also known as half open scan or stealth scan.

command - nmap -sS 192.168.0.0/24 -oN basicscan.txt
-sS represents for stealth scan and -oN for storing the otput result in a text file.

Basically what happens in the stealth scan is that instead of going for a full three-way-handshake it performs only half handshake that is after the initial SYN packet if the system got the SYN-ACK it sonfirms that the port is open and stop the process before sending the ACK packet.


In my network there are only few devices which are 192.168.0.1(router) 192.168.0.114(my machine) 192.168.0.118, 192.168.0.137.
The common ports which are opened in my network are  SSH, DNS, HTTP, NetBios.The result will be uploaded in the repo.

Wireshark - wireshark is a free opensource network protocol analyzer that captures and inspects the network traffic through a network interface card.

Once you opend the wireshark you can see the interface with all the adapter of your machine and the one with network traffic.

<img width="1919" height="1044" alt="image" src="https://github.com/user-attachments/assets/d3ac428d-42bd-4812-94c3-f5bba62b96ab" />

Once you opened the right interface you can see the traffic flow from your NIC .
Here we will see the network traffic generated from our Nmap scan<img width="1920" height="1080" alt="Screenshot From 2025-09-22 18-20-32" src="https://github.com/user-attachments/assets/6a2a76fd-9d70-4f50-8bb8-1a3d863ffd09" />

We can see the traffic generated from our system to the remaining systems in our network.
<img width="1920" height="1080" alt="Screenshot From 2025-09-22 18-21-08" src="https://github.com/user-attachments/assets/35916de1-5001-4b27-aa6e-9ccb90daa30d" />

We can also inspect the individual packet to see aditional information from each layer , once we tap on the packet we can see the extra info from the bottom left tab.<img width="1920" height="1080" alt="Screenshot From 2025-09-22 18-29-52" src="https://github.com/user-attachments/assets/82f3b860-fe9c-4906-8433-a533b7771385" />
