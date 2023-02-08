<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
Hey, I'm Kenneth, an IT Professional. This is the first of a three-part setup of a ticketing software. This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system OSTicket.<br />


<h2>What is osTicket?</h2>
osTicket is a popular open-source support ticketing system. It efficiently merges email, phone, and web-based inquiries, then molds them into a simple, easy-to-use multi-user web interface. Manage, organize, and store all support queries and replies in one location, while offering clients with the accountability and timeliness they need.


<h2>Video Demonstration</h2>

### [YouTube: How To Install osTicket](https://www.youtube.com/watch?v=K7T_JjvEamg&t=13s)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Cloud/VMs)
- Remote Desktop
- Internet Information Services (IIS)
- MySQL Database

<h2>Time it takes </h2>

15-20 mins.

<h2>Operating Systems Used </h2>

Windows 10</b> (21H2)


<h2>List of Prerequisites</h2>

- Setup Virtual Environment-> Virtual Machine Creation in CSP (not required step for installation)
- Enable/Install IIS or IIS web extension
- Download/Install PHP (Most current version for windows)
- Download/Install MySQL (version 5 or above)
- Download/Install PHP Manager for IIS, Rewrite Module, VC Redist (Microsoft Visual C++), & Heidi SQL 
Note: These are add-ons that help other programs run smooth and might already be included in installation packs.  
- Install osTicket (Current version)


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/URI1Iaj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. We must first use CGI to activate and install Windows Internet Information Services (IIS). To achieve this, type "Turn Windows features on or off" into the Windows search box, and the Windows Features control panel will be shown. Scroll down and choose Internet Information Services, making sure to tick the box to enable IIS. Extend the IIS folder (do not deselect any folders), then extend the World Wide Web Services folder and Application Development Features, and last select CGI. Press ok (and apply if applicable). Next Step...
</p>
<br />


<p>
2. To proceed, this part does not require an example because it will explain how to download and install numerous apps into the virtual environment. First, navigate to your system's c: drive and create a folder called "PHP" (this will be needed later). For the time being, download and install the following applications/software (which may be found on the web): PHP Manager for IIS, Rewrite Module, and VC Redist (Microsoft Visual C++). These files are simple and do not require any configuration before installation, just simple click-through. Next Step...
</p>
<br />


<p>
<img src="https://i.imgur.com/Xo2kRFo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3. Moving on, download the zip file of PHP for windows (version 7 or higher). Once downloaded, right click the zip file and select extract then make the location for the extract to the "PHP" folder made in the previous step located on the c: drive. Next step...
</p>
<br />

<p>
<img src="https://i.imgur.com/4OqTKoD.png" height="50%" width="50%" alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/sgkRESx.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
4. Next, download the most recent MySQL (version 5 or higher) for your database. The download and installation are straightforward click-throughs (usual installs), and once installed, "Launch Configuration Wizard" will be indicated (DO NOT UNMARK IT). When the configuration Wizard appears, just click through the steps, first selecting standard configuration (unless you have special customizations you wish to make in detail), then identify a username and password for your database (make sure not to forget these credentials in order to access your database later). Next step...
</p>
<br />

<p>
<img src="https://i.imgur.com/CgDHfmq.png" height="50%" width="50%" alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/xF4TA39.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<p align="center"><img src="https://i.imgur.com/O2NMAzU.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
5. To continue, now open the IIS Manager application as Admin.(right click and select run as administrator). Once opened double click PHP Manager and then select to register a PHP. Navigate to the c: drive PHP folder and then select the "php-cgi". Next step...
</p>
<br />

<p>
<img src="https://i.imgur.com/eJhrQA8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
6. Now download the latest osTicket zip file (located on web or local network). Once downloaded open the zip file and you should see two folders. The one named "upload" copy that folder and navigate to your c:drive into "inetpub" folder and then "wwwroot" folder and place the copy there and rename the copy folder "osTicket" exactly like that no spaces. Next step...
</p>
<br />

<p>
<img src="https://i.imgur.com/NGpOZFz.png" height="50%" width="50%" alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/KJMxd4u.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<p align="center"><img src="https://i.imgur.com/rPJZNUi.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
7. To continue, reopen your IIS Manager (as Admin) then restart the server. Once restarted "osticket" should be located under "sites" and "Default Web Site". Click osticket and then click "Browse *:80 (http), this will take you to the osticket installer page. On this page you can see the required installs we already in order to run osTicket. Note: under the "Recommended" a list of features thate are activated or not. If you wish to enable or disable any features simply go to your IIS Manager (as Admin), navigate back to osTicket folder and double-click PHP Manager. Scroll down and you will see PHP extensions once clicked from there you can enable and disable php features. Next Step...
</p>
<br />

<p>
<img src="https://i.imgur.com/iK6ArM3.png" height="50%" width="50%" alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/yUotIfU.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/9Fgg4mI.png" height="50%" width="50%" alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/vryn8Hw.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
8. Before we go back to browser, go to your file explorer and navigate back to the osTicket folder we copied in your c:\inetpub\wwwroot, open the folder then open the folder named "include" then scroll down untill you see "ost-sampleconfig.php", rename this file "ost-config.php" (exactly like that). Now right click this file and select properities (we are going to change it's security permissions for now). Go to security tab then click advanced. From here click "Disable inheritance" and select remove all. After that click Add and add an object name "Everybody" and then set Everybody's basic permissions to full controll. Note: at the end of installation make sure to come back and change these security persmissions to "read only and/or read & execute". Next step...
</p>
<br />

<p>

<img src="https://i.imgur.com/X5KEcyh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
9. Back to the browser osTicket installer. Click next once you are satisfied with what is installed. This will take you to the Basic Installation where you will registar your helpdesk email, Admin User account with osTicket, and your MySQL database once filled out on to the next step (don't install yet).
</p>
<br />

<p>
<img src="https://i.imgur.com/kEB4lfO.png" height="50%" width="50%" alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/yAZO68j.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
10. Now download and install an application called HeidiSQL, this will allow us to interact with MySQL and create our database. Once downloaded and click finish to launch. Once launched use your User name and Password for MySQL to open a session and then click open. Once Opened create a database called osTicket. After that go back to the browser and click install.
</p>
<br />

<p>
<img src="https://i.imgur.com/Ib85ptO.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p align="center"><b>CONGRATULATIONS!</b> If you are at this page you were successful installing and registering for osTicket. Well done!
</p>
<br />


