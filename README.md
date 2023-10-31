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

- Item 1 - Setting Up a Vitural Machine in Microsoft Azure
- Item 2 - Control panel -> Programs -> Turn Windows features on and off -> Install / Enable IIS in Windows With CGI and Common HTTP Features ([X] CGI,
  [X] Common HTTP Features,[X] IIS Management Console)
- Item 3 - Download and install PHP Manager for IIS - https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view
- Item 4 - Download and install Rewrite Module - https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view
- Item 5 - Create the directory C:\PHP
- Item 6 - Download PHP - https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 Unzip the contents into C:\PHP
- Item 7 - Download and Install VC_redist - https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view
- Item 8 - Download and Install  MySQL - https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view
- Item 8.5 - Instaltion setting for My SQL (Typical Setup ->Launch Configuration Wizard (after install) ->Standard Configuration ->)
- Item 9 - Open IIS as an Admin, Register PHP from within IIS, Reload IIS (Open IIS, Stop and Start the server)
- Item 10 - Install osTicket v1.15.8 - https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
- Item 10.5 - Extract and copy “upload” folder to c:\inetpub\wwwroot , Within c:\inetpub\wwwroot, Rename “upload” to “osTicket” ,Reload IIS 
  (Open IIS, Stop and Start the server)
- Item 11 - Go back to IIS, sites -> Default -> osTicket, Double-click PHP Manager,Click “Enable or disable an extension”
  Enable: php_imap.dll
  Enable: php_intl.dll
  Enable: php_opcache.dll
- Item 12 - Rename: ost-config.php From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php remove the 'sample' To:         
  C:\inetpub\wwwroot\osTicket\include\ost-config.php
- Item 13 - Assign Permissions: ost-config.php, Disable inheritance -> Remove All ,New Permissions -> Everyone -> All
- Item 14 - Download and Install HeidiSQL - https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe









<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
