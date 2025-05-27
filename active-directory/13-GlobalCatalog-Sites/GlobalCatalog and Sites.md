Global Catalog:
• The global catalog contains Complete information of Host
Domain & partial information of other domains in a forest.

• By searching against the GC, individual domains do not
have to be queried in most cases- GC can resolve

• Servers that hold a copy of the global catalog are called
global catalog servers.


Directory Partitions:
Schema
Configuration
Domain
Application

Physical Structure of Active Directory:
• Physical Structure
Domain Controllers
Sites

Sites
• A set of well-connected IP subnets.
• Site can be generally used for locating services (E.g.Logon), replication, group policy application.
• Sites are connected with site links.
• A site can span multiple domains.
• A domain can span multiple sites.