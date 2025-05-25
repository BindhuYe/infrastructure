Logical Structure of Active Directory:
1: Configuring Additional Domain Controller
2: Configuring Child Domain
3: Configuring New Domain Tree in Existing Forest

Additional Domain Controllers:
• If you already have one domain controller in a domain,
you can add additional domain controllers to the
domain to improve the availability and reliability of
network services.

• Adding additional domain controllers can help provide
fault tolerance, balance the load of existing domain
controllers, and provide additional infrastructure
support to sites.

• The replication type between two read/write dc’s is
multi master replication.

Domain Tree:
• Tree is a set of one or more domains with contiguous names.

• If more than one domain exists, you can combine the multiple domains into hierarchical tree structures.

• The first domain created is the root domain of the first tree.

• Other domains in the same domain tree are child domains.

• A domain immediately above another domain in the same domain tree is its parent.

Domain Forest:
• Multiple domain trees within a single forest do not form a contiguous namespace.

• Although trees in a forest do not share a namespace, a forest will have a single root domain, called the forest root domain.

• The forest root domain is the first domain created in the forest.

• These two forest-wide predefined groups reside in forest root domain.
  – Enterprise Admins
  – Schema Admins
