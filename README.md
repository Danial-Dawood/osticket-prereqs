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

- Item 1 - Setting Up a Vitural Machine in Microsoft Azure (Windows 10.)
- Item 2 - Control panel -> Programs -> Turn Windows features on and off -> Install / Enable IIS in Windows With CGI and Common HTTP Features ([X] CGI,
  [X] Common HTTP Features,[X] IIS Management Console)  These are all the options that need to be Checked off. After doing this click okay and it will install IIS(Internet 
  Information Servies.) <img width="1440" alt="Screen Shot 2023-10-31 at 11 52 19 PM" src="https://github.com/Danial-Dawood/osticket-prereqs/assets/149525309/94c0442a-fc49-414a-9b41-050ac04d877f">

- Item 2.5 - To test if you did download it go to the web browser and go to 127.0.0.1( this is the local host / loopback, this is telling the computer to try and run a website off its 
  self) if this doesnt work go through and uninstal and reinstall IIS and all of the other checks.
- Item 3 - Download and install PHP Manager for IIS (nothing special with this instaltion just go through it.)  - https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view
- Item 4 - Download and install Rewrite Module(Same for this go through and install) - https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view
- Item 5 - Create the directory C:\PHP
- Item 6 - This is the PHP that you need to download(PHP 7.3.8-nts-win32-v15-x86.zip <img width="1440" alt="Screen Shot 2023-11-01 at 12 15 34 AM" src="https://github.com/Danial-Dawood/osticket-prereqs/assets/149525309/e1b6b563-2f16-43c1-b196-f4695395ae18">
- Item 6.5 - Download PHP - https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 Unzip the contents into C:\PHP( when doing this step its easiest to go tot the 
  downloads and right click the PHP and click extract all and it will ask where you want to extract to, click browse and go to c drive and then click the PHP folder you made earlier 
- Item 7 - Download and Install VC_redist (no special steps) - https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view
- Item 8 - Download and Install  MySQL - https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view
- Item 8.5 - Instaltion setting for My SQL (Typical Setup ->Launch Configuration Wizard (after install) ->Standard Configuration )(this is going to be the data base for osTicket)
- Item 9 - Open IIS as an Admin, (click on PHP Manager should have a error message that says PHP is not enabled. Register New PHP version to enable PHP via FastCGI.)Click on Register 
  new Version PHP.
- Item 9.5 - A window will pop up you will have the option to browse, go to the c drive, go to the PHP folder that was made, click it and we are going to select PHP-CGI. (It even gives 
  you the pathway you suppose to take as the example and the item youre supposed to click) <img width="1440" alt="Screen Shot 2023-11-01 at 1 20 21 AM" src="https://github.com/Danial-Dawood/osticket-prereqs/assets/149525309/b2b4d3f7-92ba-4400-85f1-d0f64d88ed3d">


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
- Item 14.5 - Create a database called “osTicket”
- Item 15 -  Login site - http://localhost/osTicket/scp/login.php (Help Desk Workers)
- Item 15.5 - Client site - http://localhost/osTicket/ (Customer)

