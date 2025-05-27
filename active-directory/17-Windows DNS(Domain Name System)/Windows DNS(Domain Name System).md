What is DNS:
• Domain Name Service/Domain Name System
• Provides resolution of names to IP addresses and resolution of IP addresses to names
• Defines a hierarchical namespace where each level of the namespace is separated by a “.”

Authoritative & Non-authoritative DNS server:
• An authoritative DNS server will either:
 – Return the requested IP address
 – Return an authoritative “No”

• An Non-authoritative DNS server will either:
 – Check its cache
 – Use forwarders
 – Use root hints

Fully Qualified Domain Name (FQDN):
• Identifies a host’s name within the DNS namespace hierarchy

• Host name + DNS domain name = FQDN
• Example:
 – Host name: Sys1 & Domain name: MS.com
 – Then FQDN = Sys1.Microsoft.com

ZONE:
Zone is a storage database which contains all zone Records

• Forward Lookup Zone
 – Used for Resolving Host Names to IP-Address
 – It maintains Host to IP Address Mapping Information

• Reverse Lookup Zone
 – Used for Resolving IP-Address to Host Names
 – It maintains IP Address to Host Mapping Information

Types of Records:
• SOA Record
 – The first record in any zone file

A start of authority record is a type of resource record in the Domain Name System containing administrative information about the zone,especially regarding zone transfers.

• NS Record
 – Identifies the DNS server for each zone

NS stands for 'nameserver,' and the nameserver record indicates which DNS server is authoritative for that domain (i.e. which server contains the actual DNS records). Basically, NS records tell the Internet where to go to find out a domain's IP address.

• Host Record
 – Resolves a host name to an IP address

• Alias Record
 – Resolves an alias name to a host name

A Canonical Name or CNAME record is a type of DNS record that maps an alias name to a true or canonical domain name. CNAME records are typically used to map a subdomain such as www or mail to the domain hosting that subdomain's content.

• Pointer Record
 – Resolves an IP address to a host name

• MX Record
 – Used by the mail server

Mail exchange (MX) record directs email to a mail server. The MX record indicates how email messages should be routed in accordance with the Simple Mail Transfer Protocol (SMTP, the standard protocol for all email). Like CNAME records, an MX record must always point to another domain.

• SRV Records (Service Records)
 – Resolves names of servers providing services

SRV record specifies a host and port for specific services such as voice over IP (VoIP), instant messaging, and so on. Most other DNS records only specify a server or an IP address, but SRV records include a port at that IP address as well.

What is the purpose of a stub zone?
A stub zone is used to resolve names between separate DNS namespaces. This type of resolution may be necessary when a corporate merger requires that the DNS servers for two separate DNS namespaces resolve names for clients in both namespaces.

What is Active Directory-integrated zone?
AD-integrated DNS zones are stored in directory partitions within Active Directory. These directory partitions replicate along with the rest of AD; therefore, no extra configuration (i.e., zone transfer setup) is required for DNS replication. Further, AD-integrated zones allow the use of secure dynamic updates.

Why is Active Directory-integrated zone important?
AD-Integrated zone is replicated using Active Directory replication. Because Active Directory can compress replication data between sites and replicates data securely, hence DNS replication also becomes fast, secure and efficient.

Zone Types:
• Standard Primary
 – It is the Master Copy of all Zone Information. It is Read/Write copy

• Standard Secondary
 – It is Backup to Primary zone. It is Read Only

• Stub Zone
 – It contains only NS ,SOA & possibly Glue (A) Records which are used to locate name servers

• Active Directory Integrated
 – It stores the information of Zone in ACTIVE DIRECTORY DATABASE

What are Service Records:
• SRV records allow DNS clients to locate TCP/IP-based Services. 

• SRV records are used when: 
 – A domain controller needs to replicate
 – A client searches Active Directory
 – A user attempts to change password
 – An administrator modifies Active Directory