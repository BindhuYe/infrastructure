1.What Is Active Directory Domain Services?

• The ADDS database stores information on user identity,computers, groups, services and resources.

• ADDS domain controllers also host the service that authenticates user and computer accounts when they log on to the domain

2.Purpose of Active Directory?

Provides User Logon and Authentication Services using Kerberos protocol.

• To Centralize and Decentralize the resource management.

• To centrally organize and manage:

  − User Accounts, Computers, Groups, Network Resources.
 
• Enables authorized Users to easily locate Network Resources.

3. What is Domain?

• Domain is a logical grouping of user, computer, and group
objects for the purpose of management and security.

• Creating the initial domain controller in a network also
creates the domain—you cannot have a domain without at
least one domain controller.

• Each domain is identified by a DNS domain name

4. What is a Domain Controller ?

• A domain controller is a server that is configured to store a
copy of the AD DS directory database (NTDS.DIT) and a copy of the SYSVOL folder.

• All domain controllers except RODCs store a read/write
copy of both NTDS.DIT and the SYSVOL folder.

• NTDS.DIT is the database itself, and the SYSVOL folder
contains all the template settings for GPOs.

• Domain controllers host several other Active Directory–
related services, including the Kerberos authentication
service and the Key Distribution Center (KDC).

• Kerberos authentication service is used by User and
Computer accounts for logon authentication

• KDC is the service that issues the ticket-granting ticket
(TGT) to an account that logs on to the AD DS domain.

5. What is AD DS Logon Process?
 5.1. User Account is authenticated to Domain Controller
 5.2. Domain Controller returns TGT back to Client
 5.3. Client uses TGT to apply for access to Workstation
 5.4. Domain Controller grants access to Workstation
 5.5. Client uses TGT to apply for access to Server
 5.6. Domain Controller returns access to Server