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

- Name it: osticket

- Choose your region

![image](https://github.com/user-attachments/assets/a5e7a9ad-4326-4019-8e6f-d9673f335a4a)

![image](https://github.com/user-attachments/assets/94b9e6ff-290a-4041-bdeb-e0dea8f7ff0c)

<p>
</p>

  
Step 2: Create Virtual Machine


Purpose: Deploy Windows 10 VM to run osTicket and its stack

Action:

- Go to Virtual Machines → "Create"

- Name: osticket-vm

- OS: Windows 10 Pro

- Size: 2 vCPUs

- Username: labuser, Password: osTicketPassword1!

- Network:  default VNet and created (automatically)
  
![image](https://github.com/user-attachments/assets/501d4b0a-a741-4b18-9078-8d84530cb569)

![image](https://github.com/user-attachments/assets/dc1cf193-f93f-47b3-9203-07610240ffcd)

![image](https://github.com/user-attachments/assets/c666ba3c-ba6a-44e6-91b1-be10e43b389a)

![image](https://github.com/user-attachments/assets/4c386da7-3a71-4f2f-951a-3ee675fcd7bb)

![7](https://github.com/user-attachments/assets/ff539305-4c0f-42df-8c4e-8c204ce9bbb0)
<p>
<p>


<p>
<p>
  
Step 3: Connect to the Virtual Machine
  
Purpose: Log in via RDP to do the installations

Action:

- After the VM is running → Click “Connect” → RDP

- Download RDP file and open it

- Login with: labuser / osTicketPassword1!
- 
![image](https://github.com/user-attachments/assets/c3603ff1-c8a5-42e1-a5f2-d5ac66fa9f03)

![image](https://github.com/user-attachments/assets/7039000f-70e8-486e-b3ea-08d3ded6e068)

![image](https://github.com/user-attachments/assets/03e91c56-0c9f-480c-8783-2c581763b8a0)

![image](https://github.com/user-attachments/assets/f37ba0ff-fafa-4a3c-a3c0-fff209b88094)
</p>
</p>


Step 4: Prepare the VM Desktop
  
Purpose: Clean up & set up environment before installation

Action:

- Open Edge or Chrome and download [osTicket-Installation-Files.zip](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)

- Extract to Desktop → Folder name: osTicket-Installation-Files
- 
![image](https://github.com/user-attachments/assets/68634608-f48a-4d37-9747-99c4c4afcf6e)

![image](https://github.com/user-attachments/assets/7d75c221-89b0-4c83-8592-7eb49784f34b)

![14](https://github.com/user-attachments/assets/e3b27d38-88d6-4256-9eda-e5dba48e1bc3)


Step 5: Install IIS with CGI Enabled

Go to Start menu → Control Panel → Programs → Turn Windows features on or off

Enable:

- Internet Information Services

- World Wide Web Services → Application Development Features → [✓] CGI

- Wait for the installation to complete.

![15](https://github.com/user-attachments/assets/979cc81c-0c31-40c0-8787-3919437d14fe)

![image](https://github.com/user-attachments/assets/7c33e757-0b7f-4a30-a746-463ea3e6b835)

![image](https://github.com/user-attachments/assets/09e1987e-e506-4a4b-b4d2-4dfc40eff358)

![image](https://github.com/user-attachments/assets/2988ec9e-f910-489d-a21e-9bd8f5bcfa76)

![image](https://github.com/user-attachments/assets/a8abb10e-dfce-4908-9738-83162ba9daee)

![image](https://github.com/user-attachments/assets/5eb41581-27e0-436e-b776-a67db3380aba)

![image](https://github.com/user-attachments/assets/4d951e6b-ff44-4f8c-8a11-25989771e385)


Step 6 : Install IIS Extensions

From osTicket-Installation-Files folder:

Install PHP Manager for IIS: PHPManagerForIIS_V1.5.0.msi

Install IIS Rewrite Module: rewrite_amd64_en-US.msi


![14](https://github.com/user-attachments/assets/e3b27d38-88d6-4256-9eda-e5dba48e1bc3)

![image](https://github.com/user-attachments/assets/23a6b6d2-27ba-4118-9eb2-f6a77ca028f9)

![image](https://github.com/user-attachments/assets/9ba28a46-c4a5-4b3b-b006-ba23896e595b)

![image](https://github.com/user-attachments/assets/372403a9-dd8d-4729-a30a-08a35d0ad4fa)

![image](https://github.com/user-attachments/assets/81d46187-a7df-456e-aff1-227210d1a24c)

</p>
<br />

