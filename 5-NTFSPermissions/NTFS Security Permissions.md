What are Permissions?
Permissions define the type of access granted to a user,group, or computer to access resources.
Permissions can be applied to resources such as files,folders, and printers.
 -Like: Privilege to read a file, delete a file , or create a new file in folder

Types of Permissions:
Security Level Permissions
Share Level Permissions

1: Security Level Permissions:
• Can be Implemented Only on NTFS partitions.
• Security or NTFS Permissions can be set on Drives,Folders and Files.
• By default, Security permissions will be inherited from its parent drive or folder.
• File permissions override folder permissions.
• Creators of files and folders are their owners.
• Different Security Permissions are
  – Full Control, Modify, Read & Execute, Write, List Folder Contents

2: Share Level Permissions: 
• It can be implemented on NTFS and FAT partitions.

• It can be set on Drives and Shared Folders but not files.

• What are shared folders?
 – Shared folders can be accessed from network.
 – When you copy or move a shared folder, the folder will no longer be shared.
 – To hide a shared folder, include a $ after the name of the shared folder & users access hidden shared folders    by typing the UNC path.

• Different Share Permissions are
  – Read, Read/Write.

Effects on NTFS Permissions when Copying or moving files and folders:

When you copy files and folders within the same partition or
different partition they inherit the permissions of the
destination folder.

• When you move files and folders to a different partition, they
inherit the permissions of the destination folder

• When you move files and folders within the same partition,
they retain their previous permissions.

3: Adding Mapped Drives
Mapping a drive simply means to connect a local drive with a specially allocated shared directory or folder on another computer. After a drive has been mapped, you can access the shared resource and treat it as if it’s located locally on your own computer.

4: Access Based Enumeration:
• Access Based Enumeration displays only the files and
folders that a user has permissions to access.

• If a user does not have read permissions for a folder,
windows hides the folder from the users view


