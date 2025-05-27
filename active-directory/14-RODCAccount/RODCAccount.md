Read-Only Domain Controllers(RODCs):

• RODC addresses some of the problems that are commonly found in branch offices.

• These locations might not have a DC, Or they might have a writable DC but no physical security to that DC, 
  low network bandwidth, or inadequate expertise to support that DC.

Functionality of RODCs:
• Read-only AD DS database
• Uni-directional replication
• Credential caching
• Administrator role separation

Read-only AD DS Database
•  Except for account passwords, an RODC holds all the
Active Directory objects and attributes that a writable
domain controller holds.

• However, changes cannot be made to the database that is
stored on the RODC. Changes must be made on a writable
domain controller and then replicated back to the RODC.

Uni-directional Replication:
• Because no changes are written directly to the RODC, no
changes originate at the RODC. Accordingly, writable DCs
do not have to pull changes from the RODC. This means
that any changes or corruption that a malicious user might
make at branch locations cannot replicate from the RODC
to the rest of the forest.

Credential Caching:
• By default, an RODC does not store any user credentials.

• You must explicitly allow any credential to be cached on an RODC.


Administrator Role Separation:
• You can delegate local administrative permissions for an
RODC to any domain user without granting that user any
user rights for the domain or other domain controllers.

• In this way, the branch user can be delegated the ability to
effectively manage and perform maintenance work on the
server, such as upgrading a driver in the branch office
RODC only, without compromising the security of the rest
of the domain


Install From Media:
• If you have a network that is slow, unreliable, or costly, you
might find it necessary to add another domain controller at
a remote location or branch office.

• IFM process must take place over a potentially unreliable
WAN connection. As an alternative, and to significantly
reduce the amount of traffic copied over the WAN link

• Most of the copying is then done locally (perhaps from a
USB drive), and the WAN link is used only for security
traffic and to ensure that the new domain controller
receives any changes that are made after you create the
IFM backup

Because of this IFM, helps us download all of the AD database and registry settings from our Primary Domain Controller (PDC) to flat files that we can then copy onto a flash drive or a DVD and bring to the branch office
