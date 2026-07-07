# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This Project outlines the prerequisites and installation of the open-source help desk ticketing system osTicket on a virtual machine hosted on a cloud service environment run by Microsoft Azure.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket
- Heidi
- mysql
- PHP
- Remote Desktop Connection

<h2>Operating Systems Used </h2>

- Windows 11 (Desktop)
- Windows 11</b> (25H2) (Virtual Machine)

<h2>List of Prerequisites</h2>

- Microsoft Azure subscription
- HeidiSQL_12.3.0.6589_Setup.exe
- mysql-5.5.62-win32.msi
- osTicket-v1.15.8.zip
- php-7.3.8-nts-Win32-VC15-x86.zip
- PHPManagerForIIS_V1.5.0.msi
- rewrite_amd64_en-US.msi
- VC_redist.x86.exe

<h2>Installation Steps</h2>

<p>
<img src="https://github.com/user-attachments/assets/3cf16e95-c676-4b5f-9075-4c6f7ed927f5" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate to the Microsoft Azure homepage. To begin create a virtual machine and create your own name for the virtual machine as well as a username and password for the machine.
</p>
<br />
<h2></h2>

<p>
<img src="https://github.com/user-attachments/assets/59f71a53-bcfd-43b2-b559-ddf1d0caa1cb" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/078dcb4c-79b4-40db-967f-cce75d2d3b60" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/f4f61947-66f7-466b-bd77-ae4c2423ae53" height="400%" width="400%" alt="Disk Sanitization Steps"/>
</p>

<p>
In the process of creating your virtual machine, go to the networking tab and let the virtual machine create a new virtual network, that will create all the necessary resource groups for you to use the virtual machine properly. Ensuring the size of the virtual machine is at least 2vcpus and you have memorized your credentials press create virtual machine. Use Remote Desktop to connect to the virtual machine and connect using the public IP address. Login using the username and password when you created the machine. 
</p>
<br />
<h2></h2>

<p>
<img src="https://github.com/user-attachments/assets/e8ac155c-b94e-4b8a-8dac-d039aaa9c9a7" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD 
</p>
<p>
Once inside the virtual machine open a webpage and Input the link above into the URL and download onto the virtual machine. Download This folder to get all the required folders to install osTicket and its dependencies. Right click on the zip folder and press extract all onto the desktop. Then, access your control panel to begin the stepsto enable IIS services to allow host websites, web applications, and other services.
</p>
<br />
<h2></h2>

<p>
<img src="https://github.com/user-attachments/assets/52b96637-41be-487f-8853-ef4d78699100" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside the control panel menu click on programs -> Programs and Features -> Turn Windows features on or off. Enable Internet Information Services then expand the file and find World Wide Web Services -> Application Development Features -> And then Enable CGI. Now web services are enabled so we can prepare the environment for osTicket.
</p>
<br />
<h2></h2>

<p>
<img src="https://github.com/user-attachments/assets/4e517738-5567-4193-9415-8341bbccb71f" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/70a0d92a-f141-4b08-baff-2310cd94907b" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open the osTicket-Installation-Files downloaded earlier. Open the PHPManagerForIIS_V1.5.0.msi and run it, once downloaded head back to the installation files folder and open and run rewrite_amd64_en-US.msi and once the download is complete press done and head to your Windows C: Drive
</p>
<br />
<h2></h2>

<p>
<img src="https://github.com/user-attachments/assets/94fa9407-71a9-4075-a554-227f0e30af71" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside the Windows C: Drive create a new folder called PHP. Concurrently head over to the osTicket-Installation-Files and inside the folder right click on the php-7.3.8-nts-Win32-VC15-x86.zip and press extract all and direct the path into the new PHP folder just created in the C: drive then In the osTicket-Installation-Files download and run the VC_redist.x86 package to install microsoft C and C++ runtimes so the osTicket application can be allowed to  run.
</p>
<br />
<h2></h2>

<p>
<img src="https://github.com/user-attachments/assets/c679f0f3-107b-4dc9-8fa9-3c3462780a99" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/61aa3486-5903-426a-81a7-00489433b11a" height="40%" width="40%" alt="Disk Sanitization Steps"/>

</p>
<p> 
In the osTicket-Installation-Files open and install the mysql.5.5.62-win32 file This will help with storing, managing, and querying structured data inside osTicket. In the setup window select typical and install it then check the MySQL Instance Configuration Wizard box and launch the wizard. Inside the configuration wizard select standard and keep going until you need to create a root password, create one then continue and finish the install.
</p>
<br />
<h2></h2>

<p>
<img src="https://github.com/user-attachments/assets/0d3c95cc-43dc-4a99-9152-76136a8bc034" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate to the windows search bar and search for "IIS" (Internet Information Services) and right click on it and choose to run as admin
</p>
<br />
<h2></h2>

<p>
<img src="https://github.com/user-attachments/assets/125b76be-ffaf-42b3-af64-b1c3b9b2a18c" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/465eef38-a91d-4340-bebf-4315bf2d2611" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside "IIS" manager open PHP manager and then click Register new PHP version then browse to the PHP folder in the C: drive and path it to php-cgi.exe inside the PHP folder. Circle back to the "IIS" manager window and Press stop and start on the manage server side for your server to refresh and actuate the new PHP version.
</p>
<br />
<h2></h2>

<p>
<img src="https://github.com/user-attachments/assets/89ee7494-edb3-440b-9c8c-fc07dc880640" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/23fbca04-7e5f-4759-b897-1c1b7cb5a827" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket” Stop and restart server again to refresh and actuate the changes. Then in IIS to the left in the connections tab to the left click on Sites and drop down into Default Web Site then drop down the arrow and select osTicket and click on Browse:80(http) in the manage folder settings on the right. If the website opens and shows osTicket then you have done it correctly. 
</p>
<br />
<h2></h2>

