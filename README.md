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

- From osTicket-Installation-Files folder:

- Install PHP Manager for IIS: PHPManagerForIIS_V1.5.0.msi

- Install IIS Rewrite Module: rewrite_amd64_en-US.msi


![14](https://github.com/user-attachments/assets/e3b27d38-88d6-4256-9eda-e5dba48e1bc3)

![image](https://github.com/user-attachments/assets/23a6b6d2-27ba-4118-9eb2-f6a77ca028f9)

![image](https://github.com/user-attachments/assets/9ba28a46-c4a5-4b3b-b006-ba23896e595b)

![image](https://github.com/user-attachments/assets/372403a9-dd8d-4729-a30a-08a35d0ad4fa)

![image](https://github.com/user-attachments/assets/81d46187-a7df-456e-aff1-227210d1a24c)

![image](https://github.com/user-attachments/assets/8e92092f-b96c-4b06-a54a-38ed1fe6b37e)

![image](https://github.com/user-attachments/assets/3623c91b-3dad-404c-9d4b-8185f1129499)

![image](https://github.com/user-attachments/assets/9c091722-9c31-4168-9118-72a819f7c1bd)

![image](https://github.com/user-attachments/assets/68c13ba7-c2dd-4b2d-862a-37accfa01ef2)

![image](https://github.com/user-attachments/assets/f643020f-096d-4eb6-bd81-97bcb0a3d5b3)

![image](https://github.com/user-attachments/assets/4551617b-f3a5-4be0-8f03-bd218b66d61c)

![image](https://github.com/user-attachments/assets/3df50747-dcbb-4648-93ba-4a8e64b4780a)


Step 8: Set Up PHP Runtime

- Create folder: C:\PHP

- Unzip php-7.3.8-nts-Win32-VC15-x86.zip into C:\PHP

- Install VC_redist.x86.exe (Visual C++ Runtime)

![image](https://github.com/user-attachments/assets/7e64f96b-6465-4a76-a73f-d41805106f5a)

Step 9: Install MySQL Server

- Run mysql-5.5.62-win32.msi

- Choose: Typical Setup

- After install, launch MySQL Configuration Wizard

- Choose Standard Configuration

Set username: root, password: root

![image](https://github.com/user-attachments/assets/6ebbafe9-3ab4-4d87-80fd-1f716df90b94)

![image](https://github.com/user-attachments/assets/27c6ee78-de9f-4141-a0b1-89eafb36a00b)

![image](https://github.com/user-attachments/assets/d5dbd62c-9ed7-44fa-9106-0d03905209ae)

![image](https://github.com/user-attachments/assets/2d2c14ac-e354-4ca4-9f36-4efecebe021b)

![34](https://github.com/user-attachments/assets/6238ba50-829d-469b-ad5e-15cb54e32dcf)

![image](https://github.com/user-attachments/assets/ececa8e6-9500-4481-8d01-21c2ac9b99eb)

![36](https://github.com/user-attachments/assets/c63b9b9a-6016-4d89-9b79-e116e3660771)


Step 10: Register PHP with IIS

Open IIS as Administrator

Click your computer name  → PHP Manager

Register new PHP → Path: C:\PHP\php-cgi.exe

Restart IIS (Stop/Start from within IIS Manager)

![image](https://github.com/user-attachments/assets/51e677ed-1375-44d5-889b-8a176ec5ec33)

![image](https://github.com/user-attachments/assets/6c231706-eb78-405b-8d8a-d169de4f83c7)

![image](https://github.com/user-attachments/assets/3e9947f9-075a-47c4-8f5a-98d47b6264a4)

![image](https://github.com/user-attachments/assets/033924e6-7a4f-437b-aacb-61a69e6ae3da)

![image](https://github.com/user-attachments/assets/84beebcc-da65-44a9-bc04-7438ffcd8640)

![Screenshot 2025-07-09 171808](https://github.com/user-attachments/assets/47aeacc0-1791-494e-a18a-ab158f90c011)

![image](https://github.com/user-attachments/assets/737aa44b-6673-4ad0-80ff-3b7f648b693d)


Step 11: Unzip & Move osTicket Files

From osTicket-Installation-Files folder:

Unzip osTicket-v1.15.8.zip

Copy the upload folder into C:\inetpub\wwwroot

Rename upload to osTicket

![image](https://github.com/user-attachments/assets/d40b0a96-119c-44a5-90ee-c8d4b3147ab5)

![image](https://github.com/user-attachments/assets/4c0ce0fa-dd1f-457c-aaff-8334467a25b7)

![45](https://github.com/user-attachments/assets/83470ebc-bf9e-4a64-9924-0def1f9b1142)


</p>
<br />

