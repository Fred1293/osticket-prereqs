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

- PHP Manager for IIS
- Rewrite Module
- Php 7.3.8
- VC_redist.x86.exe
- MySQL 5.5.62
- HeidiSQL

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/H5i3tWE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install and enable IIS in windows with CGI and common Http features
</p>
<br />

<p>
<img src="https://i.imgur.com/v842QRm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install PHP manager
<br />

<p>
<img src="https://i.imgur.com/3gTr8GL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install rewrite module, then create the directory C:\PHP.
</p>
<br />

<img src="https://i.imgur.com/Tcj5xLz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP

</p>
<br />

<img src="https://i.imgur.com/b3e5afE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
download and install VC_redist.x86.exe.
</p>
<br />

<img src="https://i.imgur.com/Pv7Sq2o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
  Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Set Password

</p>
<br />

<img src="https://i.imgur.com/qU9IEEO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS as an Admin-->
Register PHP from within IIS-->
Reload IIS (Open IIS, Stop and Start the server)

</p>
<br />

<img src="https://i.imgur.com/yqgVYaM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install osTicket.v1.15.8-->
Extract and copy “upload” folder to c:\inetpub\wwwroot-->
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
Reload IIS (Open IIS, Stop and Start the server)-->
Go to sites -> Default -> osTicket-->
On the right, click “Browse *:80”


</p>
<br />

<img src="https://i.imgur.com/Pj0uxw3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back to IIS, sites -> Default -> osTicket-->
Double-click PHP Manager-->
Click “Enable or disable an extension”-->
Enable: php_imap.dll,
Enable: php_intl.dll,
Enable: php_opcache.dll

</p>
<br />

<img src="https://i.imgur.com/BAjGgrn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Rename: ost-config.php-->
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php-->
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Assign Permissions: ost-config.php-->
Disable inheritance -> Remove All-->
New Permissions -> Everyone -> All

</p>
<br />

<img src="https://i.imgur.com/MQiqwsm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continue Setting up osTicket in the browser (click Continue)-->
Name Helpdesk-->
Default email (receives email from customers)

</p>
<br />

<img src="https://i.imgur.com/qW5DVKe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install HeidiSQL.-->
Open Heidi SQL-->
Create a new session, root/Password1-->
Connect to the session-->
Create a database called “osTicket”
  
Continue Setting up osticket in the browser-->
MySQL Database: osTicket,
MySQL Username: root,
MySQL Password: Password1,
Click “Install Now!”


</p>
<br />

<img src="https://i.imgur.com/4TdzwYd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Set up is Complete!
</p>
<br />
