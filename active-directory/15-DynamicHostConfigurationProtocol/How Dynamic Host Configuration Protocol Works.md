Types of IP addresses:
IP addresses can be

• Static IP address
  – Addresses that are manually assigned and do not change over time

• Dynamic IP address
  – Addresses that are automatically assigned for a specific period of time and might change

What is DHCP?:
• It gives IP Addresses automatically to the clients who is requesting for 
an IP Address

• Centralized IP Address management

• DHCP prevents IP address conflicts and helps conserve the use of 
client IP Address on the network

• DHCP reduces the complexity and amount of administrative work by 
assigning TCP/IP configuration automatically to the Clients.

AUTHORIZATION:
• In Domain model the DHCP server should be authorized to assign
the IP Addresses to clients.

• It is a security precaution that ensures that only authorized DHCP
servers can run in the network. To avoid computers running illegal
DHCP servers in the network.

SCOPE:
• A scope is a range of IP addresses that are available to be leased to clients.

DHCP Lease Generation Process:
1. DHCP client broadcasts a DHCP-DISCOVER packet


2. DHCP servers broadcast a DHCP-OFFER packet
3. DHCP client broadcasts a DHCP-REQUEST packet
4. DHCP Server1 broadcasts a DHCP-ACK packet

DHCP Lease Renewal Process:
1. DHCP Client sends a DHCP-REQUEST packet
2. DHCP Server1 sends a DHCP-ACK packet
