![image](https://github.com/user-attachments/assets/eab3ae6c-be5c-40c7-a68b-2292233b26d5)

Migrating VMware Virtual Machine to Azure

Step-by-Step Guide and Troubleshooting
Migrating virtual machines from on-premises VMware environments to Microsoft Azure can be a game-changer for organizations seeking greater scalability, flexibility, and cost-efficiency. In this comprehensive guide, we’ll walk you through the entire process of VMware VM to Azure migration, including setting up Azure Migrate, deploying the Azure Migration Appliance, and addressing common migration challenges.

Table of Content
- Creating a Landing Zone in Azure Portal
- Installing and Configuring Azure Migration Appliance
- Installing VMware Virtual Disk Development Kit
- Discovering Servers
- Replicating the VM
- Migrating the VM
- Post-Migration Best Practices

Create Landing Zone in Azure Portal
Set Up Your Azure Migrate Project
Log in to Azure Portal: Access the Azure Portal and search for the Azure Migrate service. Select “Assess and migrate servers.”

Create Landing Zone in Azure Portal Create a Resource Group and a Vnet in the RG.

![image](https://github.com/user-attachments/assets/db66cf4d-7fe0-4743-a3d3-e91d9114b30a)

Installing and Configuring Azure Migration Appliance
Install and Configure the Azure Migration Appliance and Start Discovery How to Setup an Azure Migrate Project First, we need to set up an Azure Migrate project. Once logged into the Azure Portal search for the Azure Migrate service and select Assess and migrate servers:

![image](https://github.com/user-attachments/assets/a2718b5b-4f51-4be8-b7ea-c9ab7bde9910)

Now start Discovery, click on Discovery and Select Yes, with VMware and vSphere Hypervisor.

![image](https://github.com/user-attachments/assets/df1fdb27-9e6e-4774-83ca-cb8124ecdcba)

Start Discovery: Click on “Discovery” and choose “Yes, with VMware and vSphere Hypervisor.” Download the Azure Migration Appliance OVA file (approximately 12 GB) from the provided link.

![image](https://github.com/user-attachments/assets/b6c2a187-4862-4f1a-ac88-162d4a0b52ad)

Next go to vCenter On the vCenter select a Cluster and select deploy OVF Template. Here import the OVA file which we downloaded.

![image](https://github.com/user-attachments/assets/3a739bb2-0577-4a1f-90e2-e6ee0720dc4d)

Select name and Appliance in the folder.

![image](https://github.com/user-attachments/assets/020f7c43-f846-4e77-a32b-237d04c120de)

Here we deployed the AzureMigrateAppliance

![image](https://github.com/user-attachments/assets/00242938-5aac-4a37-8819-0fc2ac784c7c)

Launch the web console of the appliance.

![image](https://github.com/user-attachments/assets/20983f64-2376-4f66-84d2-9ab8db06ca3a)

Generate the Appliance Key

![image](https://github.com/user-attachments/assets/f3fa13d7-2dfb-4ff4-aa62-d7f47da01196)

Paste the key and click verify

![image](https://github.com/user-attachments/assets/c2674d8d-0a1e-41ac-9ac4-82733ad3ad4f)

Once the key is verified, it will start the appliance update

![image](https://github.com/user-attachments/assets/72af2dbe-b549-4acc-bb7e-26f2312222fe)

After connecting to appliance, create a password and finish. Login with password now, Appliance will be directly redirected to the browser. It checks the prerequisites, then copy and paste the Migrate Project key generated in the Azure Portal. Verify the key now.

![image](https://github.com/user-attachments/assets/f9e62568-e29f-4a87-b7d9-8db442f8f659)

Ensure to have the required permissions at the Subscription level (Contributor or Owner).

Then click on Login with a code auto-generated. This is to login to Microsoft Azure PowerShell.

Installing VMware Virtual Disk Development Kit
Now, we have to install the VMware virtual disk development kit in the appliance.

![image](https://github.com/user-attachments/assets/697c0a1e-914a-4031-80c0-066f9993e9df)

We will right click on the download, then will copy the link and open the new tab and will paste the copied key here. Click on Download now.

![image](https://github.com/user-attachments/assets/29293bd0-2476-40e4-b8c5-ac7e8e3a1b15)

Provide VMware portal credentials here. Paste the copied content in the path below.

![image](https://github.com/user-attachments/assets/083870de-2c5d-42b0-b378-6b3fe1025502)

Discovering Servers
Then Add credentials to discover Hyper-V

![image](https://github.com/user-attachments/assets/c16f540a-7a56-49a2-b0a4-6a2482e3ae57)

Then we can see the Discovered servers.

![image](https://github.com/user-attachments/assets/735460d9-7f6d-420d-a50d-3cc6326c51d0)

The Discovery process has been completed below.

![image](https://github.com/user-attachments/assets/6b99eefb-1802-4e42-b16f-df734368eb5b)

Replicating the VM
On this page under the migration tools click on replicate and here on the drop down we will select the our appliance name which we had given.

![image](https://github.com/user-attachments/assets/ea52b473-0f99-40d6-a9d6-e37d431e8f00)

Migrating the VM
Go to azure migrate servers and click on Migrate.

Select the VM and click Migrate

Below we can see the Migrated machines.

Migration has been done. Now Associate the Public IP and access the VM.

virtual machine has been successfully migrated and it is ready for use.

Post-migration best practices
⦁ For increased resilience: ⦁ Keep data secure by backing up Azure VMs using the Azure Backup service. ⦁ Keep workloads running and continuously available by replicating Azure VMs to a secondary region with Site Recovery. ⦁ For increased performance: ⦁ By default, data disks are created with host caching set to “None”. Review and adjust data disk caching to your workload needs. ⦁ For increased security: ⦁ Lock down and limit inbound traffic access with, Microsoft Defender for Cloud — Just in time administration. ⦁ Restrict network traffic to management endpoints with, Network Security Groups. ⦁ Deploy, Azure Disk Encryption to help secure disks and keep data safe from theft and unauthorized access. Below are the errors we came across in the migration process.
