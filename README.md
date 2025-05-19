<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com/watch?v=k_CDukV-bcs)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create VM in Azure 
- Install / Enable IIS in Windows WITH CGI  
- Installing web platform PHP
- Create a Directory 
- install C++
-  install my squal user name and password
- config permission/ install Os ticket


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/TzbZBmK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create an Azure Virtual Machine Windows 10, 4 vCPUs 
create your own username and password
Once username and password has been created, log into the VM with Remote Desktop using your created credential. 
</p>
<br />

<p>
<img src="https://i.imgur.com/fgX3kew.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and extract Osticket file within the VM. The folder should be called "os Ticket-Installation-Files"
</p>
<br />

<p>
<img src="https://i.imgur.com/AH3Qg25.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install / Enable IIS in Windows WITH CGI Installing web platform PHP
</p>
<br />

<p>
<img src="https://i.imgur.com/mRvd97a.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
install PHP Manager for IIS and Create the directory C:\PHP
</p>
<br />

<p>
<img src="https://i.imgur.com/7MQ7no0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the “osTicket-Installation-Files” folder, install C++
</p>
<br />

<p>
<img src="https://i.imgur.com/QElLowk.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/qaGZM2y.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the “osTicket-Installation-Files” folder, install MySQL
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration -> center your username and password
</p>
<br />

<p>
<img src="https://i.imgur.com/BLjfoZI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS as an Admin
</p>
<br />

<p>
<img src="https://i.imgur.com/CBSBsYg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
<img src="https://i.imgur.com/PYodZq0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
  Reload IIS (Open IIS, Stop and Start the server)
Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
</p>
<br />

<p>
<img src="https://i.imgur.com/wEB6g2j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
<img src="https://i.imgur.com/5SYJKgK.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/nVscxlx.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes
</p>
<br />

<p>
<img src="https://i.imgur.com/avPfSra.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All
</p>
<br />

<p>
<img src="https://i.imgur.com/xXTCH0N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)
</p>
<br />

<p>
<img src="https://i.imgur.com/ymRLxq9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the “osTicket-Installation-Files” folder, install HeidiSQL.
Open Heidi SQL
Create a new session, root/root
Connect to the session
Create a database called “osTicket”
</p>
<br />

<p>
<img src="https://i.imgur.com/VFC9cU2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Create a database called “osTicket”
</p>
<br />

<p>
<img src="https://i.imgur.com/WA8R0Qt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”
</p>
<br />

<p>
<img src="https://i.imgur.com/YXEhe7z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Congratulations,Osticket is installed with no errors!
</p>
<br />

