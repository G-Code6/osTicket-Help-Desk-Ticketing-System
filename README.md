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
- Download PHP zip file and unzip the contents into C:\PHP folder
- Download and install VC_redist.x86.exe.
- Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)

![Screenshot 2024-04-16 at 6 31 18 PM](https://github.com/G-Code6/osTicket-Help-Desk-Ticketing-System/assets/163748328/13849fae-657a-4614-9e10-944028f0f620)

- Typical Setup 
- Launch Configuration Wizard (after installation)
- Standard Configuration
- Password1

![Image 4-16-24 at 6 48 PM](https://github.com/G-Code6/osTicket-Help-Desk-Ticketing-System/assets/163748328/d66b481d-9c14-488b-b2a7-2955b307600d)

- Open IIS as an Admin
- Register PHP from within IIS
- Reload IIS (Open IIS, Stop and Start the server)

<h4>3. Install osTicket v1.15.8</h4>

- Download osTicket & install
- Extract and copy “upload” folder to c:\inetpub\wwwroot
- Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

Reload IIS (Open IIS, Stop and Start the server)

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

![Screenshot 2024-04-16 at 7 28 18 PM](https://github.com/G-Code6/osTicket-Help-Desk-Ticketing-System/assets/163748328/1986ad9c-3556-4874-a2d3-b622bbf0f72d)

- Note that some extensions are not enabled
- Go back to IIS, sites -> Default -> osTicket
- Double-click PHP Manager
- Click “Enable or disable an extension”
- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache.dll
- Refresh the osTicket site in your browse, observe the changes

<h4>4. Rename: ost-config.php</h4>

- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

<h4>Assign Permissions: ost-config.php</h4>

- Right-click on ost-config.php
- then click on properties > security > SYSTEM > Advanced > Disable inheritance > Remove All
- New Permissions > Everyone > All

![Screenshot 2024-04-23 at 12 32 47 PM](https://github.com/G-Code6/osTicket-Help-Desk-Ticketing-System/assets/163748328/cb4c4c4c-4684-439b-abe8-92818a8b5f65)

<h4>Continue Setting up osTicket in the browser (click Continue)</h4>

- Fill out all the necessary information 
- Name Helpdesk
- Default email (receives email from customers) etc.

![Screenshot 2024-04-23 at 1 12 59 PM](https://github.com/G-Code6/osTicket-Help-Desk-Ticketing-System/assets/163748328/bf2f6e6c-ab12-40d7-a86a-76df008b8be7)

<h4>5. Download and install HeidiSQL.</h4>

- Open Heidi SQL
- Create a new session, root/Password1
- Connect to the session
- Create a database called “osTicket”

![Screenshot 2024-04-23 at 1 33 01 PM](https://github.com/G-Code6/osTicket-Help-Desk-Ticketing-System/assets/163748328/31e8878a-f294-4247-b57c-1fbc43d19e6d)

<h4>6. Continue Setting up osticket in the browser.</h4>

- MySQL Database: osTicket
- MySQL Username: root
- MySQL Password: Password1
- Click “Install Now!

<h4>Congratulations we have installed osTicket.</h4>

![Screenshot 2024-04-23 at 1 41 07 PM](https://github.com/G-Code6/osTicket-Help-Desk-Ticketing-System/assets/163748328/ba299a75-a468-48ef-952e-572fb26a4ace)

















