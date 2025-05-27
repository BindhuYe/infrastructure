Trust Relationships:
• Secure communication paths that allow objects in one
domain to be authenticated and accepted in other domains

• Some trusts are automatically created.

 – Parent-child domains trust each other
 – Tree root domains trust forest root domain

• Other trusts are manually created

• Forest-to-Forest transitive trust relationships can be created
in Windows Server 2003, 2008,2012 and Windows server 2022
forests only.

Trust Relationships:
rust categories     : Transitive trusts
                  : Nontransitive trusts 

Trust directions     : One-way incoming trust
                   : One-way outgoing trust
                   : Two-way trust

Trust types       : Five types of trusts: Default, 
         Shortcut, External, Forest and Realm


Types of Trusts:

DEFAULT : Two-way- transitive Kerberos trusts (Intraforest)

SHORTCUT: One or two-way transitive Kerberos trusts
    (Intraforest) Reduce authentication requests

EXTERNAL: One way non-transitive NTLM trusts. Used to connect to/from Windows NT or external
   2000 domains Manually created

FOREST : One or two-way transitive Kerberos trusts. Only between 2003,2008 or 2012 Forest Roots, Creates                    
transitive domain relationship

REALM : One or two-way – non-transitive Kerberos trusts Connect to/from UNIX Kerberos realms


Domain & Forest Functional Levels:
• Domain functional levels can be raised independently of
  other Domains

• Raising forest functional level is performed by Enterprise Admin
 – Requires all Domain Functional levels to be at Windows Server
   2000 or Windows Server 2012 functional levels


Active Directory Recycle Bin:
• Active Directory Recycle Bin provides a way to restore
deleted objects without AD DS downtime

• Uses Windows PowerShell with Active Directory Module or
the Active Directory Administrative Center to restore
objects