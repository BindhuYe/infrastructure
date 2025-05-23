OSI Model:
Application Layer (Layer-7): This is where the user application sits that needs to transfer data between or among hosts. For example − HTTP, file transfer application (FTP) and electronic mail etc.

Presentation Layer (Layer-6): This layer helps to understand data representation in one form on a host to other host in their native representation. Data from the sender is converted to on-the-wire data (general standard format) and at the receiver’s end it is converted to the native representation of the receiver.

Session Layer (Layer-5): This layer provides session management capabilities between hosts. For example, if some host needs a password verification for access and if credentials are provided then for that session password verification does not happen again. This layer can assist in synchronization, dialog control and critical operation management (e.g., an online bank transaction).

Transport Layer (Layer-4): This layer provides end to end data delivery among hosts. This layer takes data from the above layer and breaks it into smaller units called Segments and then gives it to the Network layer for transmission.

Network Layer (Layer-3): This layer helps to uniquely identify hosts beyond the subnets and defines the path which the packets will follow or be routed to reach the destination.

Data Link Layer (Layer-2): This layer takes the raw transmission data (signal, pulses etc.) from the Physical Layer and makes Data Frames, and sends that to the upper layer and vice versa. This layer also checks any transmission errors and sorts it out accordingly.

Physical Layer (Layer-1): This layer deals with hardware technology and actual communication mechanism such as signaling, voltage, cable type and length, etc.

• What is NIC ?
A network interface controller (NIC, also known as a network interface card, network adapter, LAN adapter or physical network interface, and by similar terms) is a computer hardware component that connects a computer to a computer

• What is Mac or Physical Address?
The physical address which is also called a media access control or MAC address, identifies a device to other devices on the same local network. it's 48 bit address

Two Versions of Addressing Scheme
– IP version 4 – 32 bit addressing (IPv4)
– IP version 6 – 128 bit addressing (IPv6)

IP Address Classes
• Total IP Addressing Scheme is divided into 5 Classes
 – CLASS A  LAN & MAN & WAN
 – CLASS B  LAN & WAN
 – CLASS C  LAN & WAN 
 – CLASS D Multicasting
 – CLASS E Research & Development

IP Address Classes Range
•CLASS A Range
 – 0.0.0.0 - 126.255.255.255

Loop Back Address : 127.0.0.1

• CLASS B Range
 – 128.0.0.0 - 191.255.255.255

• CLASS C Range
 – 192.0.0.0 - 223.255.255.255

• CLASS D Range
 – 224.0.0.0 - 239.255.255.255

• CLASS E Range
 – 240.0.0.0 - 255.255.255.255

Octet Format:
• IP address is divided into Network & Host Portion
 – CLASS A is written as N.H.H.H
 – CLASS B is written as N.N.H.H
 – CLASS C is written as N.N.N.H

Private and Public IP Address:
• Private IP Address
  – CLASS A 10.0.0.0    - 10.255.255.255 
  – CLASS B 172.16.0.0  - 172.31.255.255
  – CLASS C 192.168.0.0 - 192.168.255.255

• Public IP Address
  – Apart from the above specified IP addresses all other IP addresses are Public IP’s
