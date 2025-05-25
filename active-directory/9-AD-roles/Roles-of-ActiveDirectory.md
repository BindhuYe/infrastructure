Roles of Active Directory(OPERATION MASTERS):

Flexible Single Master Operation Roles(FSMO Roles):
• Naming Master
• Schema Master
• RID Master
• PDC Emulator
• Infrastructure Master

Multi Master Operations Role
• Global Catalog


Naming Master:
• Checks and Maintains the Uniqueness of the Domain Names in the Whole Forest.

• It is Responsible for Adding, Removing and Renaming the domain names in the whole Forest.

Schema Master:
• Schema is a Set of Rules which is used to define the Structure of AD

• Schema contains Definitions of all the Objects which are stored in AD.

• Schema is further classified into:

 – Classes
 • Class is a Template which is used to Create an Object

 – Attributes
 • Attributes are Properties of an Object

Schema Master:
• The Schema Master role owner is the DC responsible for
performing updates to the directory schema.

• This DC is the only one that can process updates to the
directory schema. Once the schema update is complete, it is
replicated from the Schema Master FSMO role owner to all
other DCs in the directory.

• There is only one Schema Master per forest.

RID Master:
• It assigns unique IDs (RIDs) to the objects which are created in the domain

• Allocates pool of Relative IDs (RIDs) to all Domain controllers within a Domain.

SID means Security Identification

SID = Domain ID + RID

PDC Emulator:
• Processes all password updates for clients

• Receives immediate updates from other domain controllers when a user’s password is changed

• It Synchronizes time between the Domain controllers.

Infrastructure Master:
• Infrastructure Master Maintains and Updates the Universal Group Membership information

• It is Used for Inter-Domain Operations

Roles of Active Directory
Forest Wide Roles:
• Naming Master
• Schema Master

Domain Wide Roles:
• RID Master
• PDC Emulator
• Infrastructure Master
