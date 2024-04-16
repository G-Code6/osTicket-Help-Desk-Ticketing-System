![Screenshot 2024-04-09 at 8 35 27 PM](https://github.com/G-Code6/osTicket-Help-Desk-Ticketing-System/assets/163748328/0c84d69c-926c-410f-825e-9e74ad5633e2)

</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial explains how to install the open-source help desk ticketing system osTicket with Azure.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Account: Sign up for Azure if you haven't already.
- Virtual Machine: Create a VM on Azure to host osTicket.
- Web Server: Choose Apache or Nginx. We'll install it on the VM.
- PHP: Install PHP on the VM.
- Database: Decide between MySQL or MariaDB. We'll set it up on the VM too.
- SMTP Server (Optional): Set up an SMTP server for email communication.

<h3>Installation Steps:<h3>

<h4>1. Create VM:</h4>

- Go to Azure Portal > Virtual machines > Create VM.
- Choose OS, size, and configuration.

![RG vm](https://github.com/G-Code6/osTicket-Help-Desk-Ticketing-System/assets/163748328/58671ac8-579d-471c-9f53-a9b159d55f86)

<h4>2. Connect to VM:</h4>

- Use RDP (Windows) or SSH (Linux) to access the VM.
- Install / Enable IIS in Windows WITH
  CGI and Common HTTP Features

![Image](https://github.com/G-Code6/osTicket-Help-Desk-Ticketing-System/assets/163748328/9527b80a-60c0-45d2-842b-22430aeef0f2)

- Download and install PHP Manager for IIS
- Download and install Rewrite Module
- Create the directory C:\PHP
- From the Installation Files, download PHP zip file and unzip the contents into C:\PHP folder












