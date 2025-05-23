<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial covers setting up the Virtual Machines within Azure before creating the Active Directory infrastructure. This will outline the essential components and configurations required before beginning the setup process.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: Prerequisites for Deploying on-premises Active Directory Infrastructure within Azure VM](https://www.youtube.com/watch?v=NNdO2ntHIYk&list=PLAnyL2H5UDKJMvD8S6Tw0vygNQYxSWuRe&index=4)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Deployment  Steps</h2>

- Create a Resource Group, Virtual Network, and deploy a Windows Server 2022 VM named DC-1 as the Domain Controller in Azure
- Set DC-1’s private IP address to static and disable the Windows Firewall to allow connectivity testing.
- Deploy a Windows 10 VM named Client-1 in the same region and Virtual Network as DC-1.
- Configure Client-1’s DNS settings to use DC-1’s private IP, then restart the VM from the Azure Portal.
- Log into Client-1, confirm network connectivity by pinging DC-1, and verify DNS settings using ipconfig /all in PowerShell.

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://github.com/user-attachments/assets/a6c6bd88-8c82-4e1f-9fcd-7e12bc205ce6" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To begin setting up an on-premises Active Directory environment in Azure, first create a **Resource Group** to organize and manage related resources. Next, set up a **Virtual Network (VNet)** with a subnet to provide isolated and secure communication between virtual machines. Then, deploy a **Windows Server 2022 VM** named **DC-1**, which will serve as the **Domain Controller** for your environment.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/132c4fe4-6a74-4d21-9a57-6f5aef7c41ef" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
