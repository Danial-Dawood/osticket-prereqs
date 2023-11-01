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
- Item 6 - This is the PHP that you need to download(PHP 7.3.8-nts-win32-v15-x86.zip) <img width="1440" alt="Screen Shot 2023-11-01 at 12 15 34 AM" src="https://github.com/Danial-Dawood/osticket-prereqs/assets/149525309/e1b6b563-2f16-43c1-b196-f4695395ae18">
- Item 6.5 - Download PHP - https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 Unzip the contents into C:\PHP( when doing this step its easiest to go tot the 
  downloads and right click the PHP and click extract all and it will ask where you want to extract to, click browse and go to c drive and then click the PHP folder you made earlier 
- Item 7 - Download and Install VC_redist (no special steps) - https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view
- Item 8 - Download and Install  MySQL - https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view
- Item 8.5 - Instaltion setting for My SQL (Typical Setup ->Launch Configuration Wizard (after install) ->Standard Configuration )(this is going to be the data base for osTicket)
- Item 9 - Open IIS as an Admin, (click on PHP Manager should have a error message that says PHP is not enabled. Register New PHP version to enable PHP via FastCGI.)Click on Register 
  new Version PHP.
- Item 9.5 - A window will pop up you will have the option to browse, go to the c drive, go to the PHP folder that was made, click it and we are going to select PHP-CGI. (It even gives 
  you the pathway you suppose to take as the example and the item youre supposed to click) <img width="1440" alt="Screen Shot 2023-11-01 at 1 20 21 AM" src="https://github.com/Danial-Dawood/osticket-prereqs/assets/149525309/b2b4d3f7-92ba-4400-85f1-d0f64d88ed3d">
- Item 9.75 - Its good practice to restart your server everytime you change soemthing so click the name of your server(on the top right under connections) and then click the restart 
  button(all the way on your right under the action tab.) 
- Item 10 - Install osTicket v1.15.8 - https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
- Item 10.5 - Extract and copy “upload” folder to c:\inetpub\wwwroot , Within c:\inetpub\wwwroot,<img width="1440" alt="Screen Shot 2023-11-01 at 1 29 30 AM" src="https://github.com/Danial-Dawood/osticket-prereqs/assets/149525309/1c6015b0-1ae1-4ea6-b19d-d85c899e2caf"> (the pathway you need to go is shown at the top takes a couple minutes to copy the folder over) After rename “upload” to “osTicket” ,Reload IIS same way as before( click the server and click restart) 
  (Open IIS, Stop and Start the server)
- Item 11 - Go back to IIS, sites -> Default web site-> osTicket, then browse*:80(http)<- all the way on the right should come up after only after click osTciket once and a page should 
  pop up (osTicket Installer) <img width="1440" alt="Screen Shot 2023-11-01 at 1 39 10 AM" src="https://github.com/Danial-Dawood/osticket-prereqs/assets/149525309/ecb5b22e-8cd9-45e4-bb3b-4804aac1a84d">
  (if does not pop up one of the prerequisites was not done correctly. Restart or find out where you messed up)
- Item 11.5 - Double-click PHP Manager(Use drop down menus on the right until you find osTicket and PHP manger should be displayed in the middle section of the screen(with full screen 
  it is in the middle row all the way to your right. <img width="1440" alt="Screen Shot 2023-11-01 at 1 44 58 AM" src="https://github.com/Danial-Dawood/osticket-prereqs/assets/149525309/70b6608c-a953-4c48-9759-cf89c414edf3">
  Once in PHP Manger click “Enable or disable an extension”(all the way at the bottomunder PHP Extentions)
  Enable: php_imap.dll
  Enable: php_intl.dll
  Enable: php_opcache.dll
-  Item 11.75 - Once you have enabled all of those extensions you will go back and refresh your server in IIS manager and then go to the web browser where you have the osTciket 
   installer and refresh that and you will notice some of the (x)'s have gone away and have been replacced with checks. this is what is should look like <img width="1440" alt="Screen Shot 2023-11-01 at 1 50 08 AM" src="https://github.com/Danial-Dawood/osticket-prereqs/assets/149525309/27352d83-02e8-469e-ab12-329c07150612">
- Item 12 - Rename: ost-config.php From: ost-sampleconfig.php remove the 'sample' To make is ost-config.php (The pathway you need to follow is going to your "C Drive" then to "inetpup" 
   to "wwwroot" to "osTicket" then finally into "include" you can searcher for it in the include folder or just scroll down. The pathway will also be at the top of the ScreenCap <img width="1440" alt="Screen Shot 2023-11-01 at 1 58 29 AM" src="https://github.com/Danial-Dawood/osticket-prereqs/assets/149525309/52574581-295f-4596-b109-6564046d6d86">
- Item 13 - Dont close out of the file manger yet after changed the name of the osTicket right click it and go to properties then Security and then Advanced. At the bottom left their 
  will be a button that says disable inheritance( this means it will start getting all of its persmissions from its parent.) Then we will click on Disable inheritance(the bottom 
  option) then click "select a principal" a pop up will appear and at the bottom of the three spaces where you can enter information(The one with nothing in it, it also says "Enter a 
  object name to Select right above it " You will enter "everyone" then click check names. if it does this correctly it will underline it and caps the first letter. then click Okay and 
  Check the Box that states full control.Then Apply and Okay(x3)
- Item 13.5 - Go to the browser with the osTicket installer and click continue at the bottom of the page. Then start setting it up, under "Helpdesk Name" put your name and then "help 
  desk." Under Default Email put "your name @helper.com" (Write all this information down) <img width="1440" alt="Screen Shot 2023-11-01 at 2 28 13 AM" src="https://github.com/Danial-Dawood/osticket-prereqs/assets/149525309/50499327-6099-43d4-ac5c-6c0de71db825"> Before we can finish bottom section we need to install HeidiSQL.
- Item 14 - Download and Install HeidiSQL - https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe (normal installed just make sure that at the last page of the install the 
  box that says "Lanuch HeidiSQL" is checked. So that it will open upon completion of instaltion.
- Item 14.25 - Click new at the bottom left, then at the right side under Username and Password, the user should be "root" and which ever password you have made. This is what it looks 
  like when you have established a connection with MySQL Server. Fill out the username(root) and the password you have made iside the osTicket Installer in your browser.   
- Item 14.5 - Create a database called “osTicket” Inside HeidiSQL (Right clicked the Unnamed folder at the top left under the words data based filter, Create a database and Makesure to 
  spell the name "osTicket" if no error messages have come after you click okay then your good to go.) All thats left is for you is to input the name of the data base you just created 
  into the osTicket installer under My SQL Databs.
- Item  14.75 - All thats left is to clean up and setting permissions to read only, First we will delete the setup folder. Which is under your C Drive then inetpub/wwwroot/osTciket and the folder is called setup(the Pathway is also listed at the top) <img width="1440" alt="Screen Shot 2023-11-01 at 1 53 59 PM" src="https://github.com/Danial-Dawood/osticket-prereqs/assets/149525309/66abe9b6-47cb-4937-8b1f-a993e3649b91"> 
   
- Item 15 -  Login site - http://localhost/osTicket/scp/login.php (Help Desk Workers)
- Item 15.5 - Client site - http://localhost/osTicket/ (Customer)

