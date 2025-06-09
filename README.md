<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Step 1: Create an Azure Virtual Machine Windows 10, 4 vCPUs
Name: osticket-vm
Username: labuser
Password: Password1!

- Step 2: Log into the VM with Remote Desktop

- Step 3: Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files” 
We will use the files in this folder to install osTicket and some of the dependencies.

- Step 4: Install / Enable IIS in Windows WITH CGI
Go to Control Panel > Programs > Click on "Turn Windows Features On or Off"
Enable IIS in Windows WITH CGI
World Wide Web Services - Application Development Features →> [X] CGI

- Step 5: From the "osTicket-Installation-Files" folder, install PHP Manager for lIS
(PHPManagerForlIS_V1.5.0.msi)

- Step 6: From the "osTicket-Installation-Files" folder install the Rewrite Module
(rewrite_amd64_en-US.msi)

- Step 7: Create the directory C:\PHP

- Step 8: From the "osTicket-Installation-Files" folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip)
into the "C:IPHP" folder

- Step 9: From the "osTicket-Installation-Files" folder, install VC redist.x86.exe.

- Step 10: From the "os Ticket-Installation-Files" folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
  Typical Setup →>
Launch Configuration Wizard (after install) ->
  Standard Configuration ->
  Username: root
  Password: root

- Step 11: Open IIS as an Admin

- Step 12: Register PHP from within IIS (PHP Manager -> C:|PHP\php-cgi.exe)

- Step 13: Reload IIS (Open IIS, Stop and Start the server)

- Step 14: Install os Ticket v1.15.8
From the "osTicket-Installation-Files" folder, unzip "os Ticket-v1.15.8.zip" and copy the
"upload" folder into "Cilinetpub|wwwroot"
Within "C:\inetpub|wwwroot", Rename "upload" to "os Ticket"

- Step 15: Reload IIS (Open IIS, Stop and Start the server)

- Step 16: Go to sites - Default - os Ticket
On the right, click "Browse *:80"

- Step 17: Note that some extensions are not enabled
  Go back to IIS, sites -> Default -> os Ticket
  Double-click PHP Manager
  Click "Enable or disable an extension"
  Enable: php_imap.dll
  Enable: php_intl.dll
  Enable: php_opcache.dll
  Refresh the os Ticket site in your browser, observe the changes

- Step 18: Rename: ost-config.php
From: C:\inetpublwwwrootlosTicket\includelost-sampleconfig.php
To: C:\inetpub|wwwrootlosTicket\includelost-config.php

- Step 19: Assign Permissions: ost-config.php
  Disable inheritance -> Remove All
  New Permissions -> Everyone →> All

- Step 20: Continue Setting up os Ticket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)

- Step 21: From the "os Ticket-Installation-Files" folder, install HeidiSQL.
  Open Heidi SQL
  Create a new session, root/root
  Connect to the session
  Create a database called "os Ticket"

- Step 22: Continue Setting up os Ticket in the browser
  MySQL Database: osTicket
  MySQL Username: root
  MySQL Password: root
  Click "Install Now!" 

- Step 23: Browse to your help desk login page: http://localhost/os Ticket/scp/login.php
End Users os Ticket URL: http://localhost/osTicket/

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 1: Create an Azure Virtual Machine Windows 10, 4 vCPUs
Name: osticket-vm
Username: labuser
Password: Password1!
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 2: Log into the VM with Remote Desktop
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 3: Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files” 
We will use the files in this folder to install osTicket and some of the dependencies.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 4: Install / Enable IIS in Windows WITH CGI
Go to Control Panel > Programs > Click on "Turn Windows Features On or Off"
Enable IIS in Windows WITH CGI
World Wide Web Services - Application Development Features →> [X] CGI
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 5: From the "osTicket-Installation-Files" folder, install PHP Manager for lIS
(PHPManagerForlIS_V1.5.0.msi)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 6: From the "osTicket-Installation-Files" folder install the Rewrite Module
(rewrite_amd64_en-US.msi)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 7: Create the directory C:\PHP
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 8: From the "osTicket-Installation-Files" folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip)
into the "C:IPHP" folder
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 9: From the "osTicket-Installation-Files" folder, install VC redist.x86.exe.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 10: From the "os Ticket-Installation-Files" folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
  Typical Setup →>
Launch Configuration Wizard (after install) ->
  Standard Configuration ->
  Username: root
  Password: root
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 11: Open IIS as an Admin
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 12: Register PHP from within IIS (PHP Manager -> C:|PHP\php-cgi.exe)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 13: Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 14: Install os Ticket v1.15.8
From the "osTicket-Installation-Files" folder, unzip "os Ticket-v1.15.8.zip" and copy the
"upload" folder into "Cilinetpub|wwwroot"
Within "C:\inetpub|wwwroot", Rename "upload" to "os Ticket"
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 15: Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 16: Go to sites - Default - os Ticket
On the right, click "Browse *:80"
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 17: Note that some extensions are not enabled
  Go back to IIS, sites -> Default -> os Ticket
  Double-click PHP Manager
  Click "Enable or disable an extension"
  Enable: php_imap.dll
  Enable: php_intl.dll
  Enable: php_opcache.dll
  Refresh the os Ticket site in your browser, observe the changes
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 18: Rename: ost-config.php
From: C:\inetpublwwwrootlosTicket\includelost-sampleconfig.php
To: C:\inetpub|wwwrootlosTicket\includelost-config.php
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 19: Assign Permissions: ost-config.php
  Disable inheritance -> Remove All
  New Permissions -> Everyone →> All
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 20: Continue Setting up os Ticket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 21: From the "os Ticket-Installation-Files" folder, install HeidiSQL.
  Open Heidi SQL
  Create a new session, root/root
  Connect to the session
  Create a database called "os Ticket"
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 22: Continue Setting up os Ticket in the browser
  MySQL Database: osTicket
  MySQL Username: root
  MySQL Password: root
  Click "Install Now!" 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
- Step 23: Browse to your help desk login page: http://localhost/os Ticket/scp/login.php
End Users os Ticket URL: http://localhost/osTicket/
</p>
<br />

