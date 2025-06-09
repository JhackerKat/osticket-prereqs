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
<img width="499" alt="osTicket - Step 1" src="https://github.com/user-attachments/assets/9cba801d-b9a8-4977-b3fe-512c9a9f5424" />
</p>
<p>
- Step 1: Create an Azure Virtual Machine Windows 10, 4 vCPUs
Name: osticket-vm
Username: labuser
Password: Password1!
</p>
<br />

<p>
<img width="396" alt="osTicket - Step 2" src="https://github.com/user-attachments/assets/51e2f8ee-b529-406e-b281-038c01bc2942" />
</p>
<p>
- Step 2: Log into the VM with Remote Desktop
</p>
<br />

<p>
<img width="498" alt="osTicket - Step 3" src="https://github.com/user-attachments/assets/759da765-a34c-4001-b563-7cee7ba7899a" />
</p>
<p>
- Step 3: Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files” 
We will use the files in this folder to install osTicket and some of the dependencies.
</p>
<br />

<p>
<img width="498" alt="osTicket - Step 4 (a" src="https://github.com/user-attachments/assets/0a383820-9def-4ab7-9ecc-cbe071657518" />
<img width="498" alt="osTicket - Step 4 (b" src="https://github.com/user-attachments/assets/c6f05638-9d1b-4884-8ee2-a5960a214e07" />
</p>
<p>
- Step 4: Install / Enable IIS in Windows WITH CGI
Go to Control Panel > Programs > Click on "Turn Windows Features On or Off"
Enable IIS in Windows WITH CGI
World Wide Web Services - Application Development Features →> [X] CGI
</p>
<br />

<p>
<img width="497" alt="osTicket - Step 5" src="https://github.com/user-attachments/assets/763de8b8-4cfe-4afb-b782-b03bd9404203" />
</p>
<p>
- Step 5: From the "osTicket-Installation-Files" folder, install PHP Manager for lIS
(PHPManagerForlIS_V1.5.0.msi)
</p>
<br />

<p>
<img width="499" alt="osTicket - Step 6" src="https://github.com/user-attachments/assets/5302d85a-6aee-473d-ba31-ae4d989f309f" />
</p>
<p>
- Step 6: From the "osTicket-Installation-Files" folder install the Rewrite Module
(rewrite_amd64_en-US.msi)
</p>
<br />

<p>
<img width="499" alt="osTicket - Step 7" src="https://github.com/user-attachments/assets/97bbb7a6-854e-418b-b3a0-dd1691fe9cde" />
</p>
<p>
- Step 7: Create the directory C:\PHP
</p>
<br />

<p>
<img width="499" alt="osTicket - Step 8" src="https://github.com/user-attachments/assets/2254a8f0-6f91-4c9e-aa80-b4de417fde52" />
</p>
<p>
- Step 8: From the "osTicket-Installation-Files" folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip)
into the "C:IPHP" folder
</p>
<br />

<p>
<img width="499" alt="osTicket - Step 9" src="https://github.com/user-attachments/assets/62bf0c55-82bd-43b2-9151-b3a6c6628709" />
</p>
<p>
- Step 9: From the "osTicket-Installation-Files" folder, install VC redist.x86.exe.
</p>
<br />

<p>
<img width="498" alt="osTicket - Step 10" src="https://github.com/user-attachments/assets/016c96a4-04d1-4ed7-b17a-d2013c846a9d" />
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
<img width="499" alt="osTicket - Step 11" src="https://github.com/user-attachments/assets/6f7f3dda-300b-4950-aebb-c49cc2c38d13" />
</p>
<p>
- Step 11: Open IIS as an Admin
</p>
<br />

<p>
<img width="499" alt="osTicket - Step 12" src="https://github.com/user-attachments/assets/64ce7bbb-e7f9-48ce-8a5d-cf0746c42445" />
</p>
<p>
- Step 12: Register PHP from within IIS (PHP Manager -> C:|PHP\php-cgi.exe)
</p>
<br />

<p>
<img width="499" alt="osTicket - Step 13 (a" src="https://github.com/user-attachments/assets/8bf49025-0f0b-4fcd-8c2a-130ad72d5b70" />
<img width="500" alt="osTicket - Step 13 (b" src="https://github.com/user-attachments/assets/acb63924-d4b3-4521-9f56-16a0d4459581" />
</p>
<p>
- Step 13: Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
<img width="499" alt="osTicket - Step 14 (a" src="https://github.com/user-attachments/assets/213d5fa9-26b5-4c3f-9cb2-c14211e1aac8" />
<img width="499" alt="osTicket - Step 14 (b" src="https://github.com/user-attachments/assets/47b39e24-703e-4a8a-9c02-e80811e16dc1" />
<img width="498" alt="osTicket - Step 14 (c" src="https://github.com/user-attachments/assets/4f781032-56c5-4c28-913d-43004e3f8926" />
</p>
<p>
- Step 14: Install os Ticket v1.15.8
From the "osTicket-Installation-Files" folder, unzip "os Ticket-v1.15.8.zip" and copy the
"upload" folder into "Cilinetpub|wwwroot"
Within "C:\inetpub|wwwroot", Rename "upload" to "os Ticket"
</p>
<br />

<p>
<img width="499" alt="osTicket - Step 15 (a" src="https://github.com/user-attachments/assets/6654133a-0a63-49ec-bc00-420f74891926" />
<img width="499" alt="osTicket - Step 15 (b" src="https://github.com/user-attachments/assets/ba8d2096-ad1e-435b-ae88-dbcf0b5391e4" />
</p>
<p>
- Step 15: Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
<img width="499" alt="osTicket - Step 16 (a" src="https://github.com/user-attachments/assets/3c57140a-7983-4f22-887c-31343fce960c" />
<img width="502" alt="osTicket - Step 16 (b " src="https://github.com/user-attachments/assets/a099ee95-1aa7-4131-bcfe-a9f691ab663f" />
</p>
<p>
- Step 16: Go to sites - Default - os Ticket
On the right, click "Browse *:80"
</p>
<br />

<p>
<img width="500" alt="osTicket - Step 17 (a" src="https://github.com/user-attachments/assets/0be8a1b6-7577-45dc-bdb3-47e7558e435b" />
<img width="500" alt="osTicket - Step 17 (b" src="https://github.com/user-attachments/assets/75b3afe8-04f9-487a-a753-28c5154ad13b" />
<img width="500" alt="osTicket - Step 17 (c" src="https://github.com/user-attachments/assets/a35a5533-7243-4939-9f34-a65cf765edfd" />
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
<img width="499" alt="osTicket - Step 18 (a" src="https://github.com/user-attachments/assets/650cd20b-ab11-493e-8502-07a6cd850051" />
<img width="500" alt="osTicket - Step 18 (b" src="https://github.com/user-attachments/assets/61c39ce0-4731-4ccb-a9f4-c26d45e0607e" />
</p>
<p>
- Step 18: Rename: ost-config.php
From: C:\inetpublwwwrootlosTicket\includelost-sampleconfig.php
To: C:\inetpub|wwwrootlosTicket\includelost-config.php
</p>
<br />

<p>
<img width="500" alt="osTicket - Step 19 (a" src="https://github.com/user-attachments/assets/b78a02b9-9b29-44c0-a62d-ccf20d491895" />
<img width="500" alt="osTicket - Step 19 (b" src="https://github.com/user-attachments/assets/aa061d25-43c5-429d-886e-9159535663bb" />
</p>
<p>
- Step 19: Assign Permissions: ost-config.php
  Disable inheritance -> Remove All
  New Permissions -> Everyone →> All
</p>
<br />

<p>
<img width="499" alt="osTicket - Step 20" src="https://github.com/user-attachments/assets/cedc5fd4-ff63-4df6-a2c2-e5014f23f6ff" />
</p>
<p>
- Step 20: Continue Setting up os Ticket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)
</p>
<br />

<p>
<img width="499" alt="osTicket - Step 21 (a" src="https://github.com/user-attachments/assets/ed31e531-ce2b-46b5-bb64-5568c77f9770" />
<img width="501" alt="osTicket - Step 21 (b" src="https://github.com/user-attachments/assets/ba8c3cac-b533-46b6-9bf5-753cb285c68e" />
<img width="500" alt="osTicket - Step 21 (c" src="https://github.com/user-attachments/assets/bc02f355-4bc4-4c66-96f3-6836b7c54d17" />
<img width="501" alt="osTicket - Step 21 (d" src="https://github.com/user-attachments/assets/99063a45-3b00-4094-ae66-afd438e4accc" />
<img width="500" alt="osTicket - Step 21 (e" src="https://github.com/user-attachments/assets/de7ecdf0-9868-4c71-822b-1083f1c16db6" />
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
<img width="499" alt="osTicket - Step 22 (a" src="https://github.com/user-attachments/assets/fda18e98-339f-4d22-b320-ed7689a52683" />
<img width="501" alt="osTicket - Step 22 (b" src="https://github.com/user-attachments/assets/b898fac3-7249-4de9-b9b6-5c4477cc5dd6" />
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
<img width="499" alt="osTicket - Step 23 (a" src="https://github.com/user-attachments/assets/43951487-56f6-4c8b-a79e-719e6bc88690" />
<img width="500" alt="osTicket - Step 23 (b" src="https://github.com/user-attachments/assets/6ce67bac-a9ed-4216-91da-f981ad246dde" />
<img width="501" alt="osTicket - Step 23 (c" src="https://github.com/user-attachments/assets/8fec7a1c-5906-4cce-a9dd-a27e68275e24" />
</p>
<p>
- Step 23: Browse to your help desk login page: http://localhost/os Ticket/scp/login.php
End Users os Ticket URL: http://localhost/osTicket/
</p>
<br />

