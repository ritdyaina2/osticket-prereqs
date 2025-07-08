<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azurre account with an active subscription.
- Created a resource group.
- Created a virtual network and subnet.
- Created a virtual machine in Azure.
- Connected to the vitual machine using remote desktop (RDP)

<h2>Installation Steps</h2
                        
 Step 1: Create Resource Group.
 

 
Purpose: This is your logical container for Azure resources like VM, networks, etc.



Action:

- Go to Azure Portal → Resource Groups → Click "Create".

- Name it: osticket-resources

- Choose your region



<p>
</p>






Step 2: Create Virtual Network & Subnet

Purpose: Set up a private network so your VM has secure, isolated access

Action:

- Azure Portal → Virtual Networks → Click "Create"

- Name: osticket-vnet

- Add subnet (e.g., name: default, range: 10.0.0.0/24)

                            

<p>
<p>


  
Step 3: Create Virtual Machine


Purpose: Deploy Windows 10 VM to run osTicket and its stack

Action:

- Go to Virtual Machines → "Create"

- Name: osticket-vm

- OS: Windows 10 Pro

- Size: 4 vCPUs

- Username: labuser, Password: osTicketPassword1!

- Network: Select the VNet and subnet you created







Step 4: Connect to the Virtual Machine
  
Purpose: Log in via RDP to do the installations

Action:

- After the VM is running → Click “Connect” → RDP

- Download RDP file and open it

- Login with: labuser / osTicketPassword1!




</p>



Step 5: Prepare the VM Desktop
  
Purpose: Clean up & set up environment before installation

Action:

- Open Edge or Chrome and download osTicket-Installation-Files.zip

- Extract to Desktop → Folder name: osTicket-Installation-Files


</p>
<br />

