<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Prerequisites for Deploying Active Directory Infrastructure within Azure (Azure)</h1>
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
<img src="https://github.com/user-attachments/assets/b566d11d-8eb4-4e82-9dc1-bee3610f9ffb" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To begin setting up an on-premises Active Directory environment in Azure, first create a **Resource Group** to organize and manage related resources. Next, set up a **Virtual Network (VNet)** with a subnet to provide isolated and secure communication between virtual machines. Then, deploy a **Windows Server 2022 VM** named **DC-1**, which will serve as the **Domain Controller** for your environment.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/132c4fe4-6a74-4d21-9a57-6f5aef7c41ef" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After creating the DC-1 virtual machine, configure its network interface in the Azure Portal to use a static private IP address, ensuring consistent DNS resolution and connectivity. This prevents the IP address from changing during reboots or updates. Then, log into the VM and temporarily disable the Windows Firewall to make it easier to test connectivity between devices during setup.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/a6c6bd88-8c82-4e1f-9fcd-7e12bc205ce6" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Deploy a Windows 10 VM named Client-1 in the same region and Virtual Network as DC-1 to ensure they can communicate with each other internally. After the VM is created, update Client-1’s DNS settings to use the private IP address of DC-1, allowing it to locate and connect to the Domain Controller. Once the DNS configuration is complete, restart Client-1 from the Azure Portal to apply the changes.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/a6c6bd88-8c82-4e1f-9fcd-7e12bc205ce6" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After restarting Client-1, log into the virtual machine using the credentials you set during creation. Open **Command Prompt** or **PowerShell** and run the `ping` command using **DC-1’s private IP address** to confirm that the machines can communicate over the network. Then, use the command `ipconfig /all` to verify that **Client-1’s DNS settings** correctly reflect DC-1’s private IP, ensuring proper name resolution for domain services.

</p>
<br />
