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

<h2>Prerequisites</h2>


<a href="https://drive.google.com/drive/folders/1c6dPX9EbGpAyBfZ37vl7MnD8sA8P5nht?usp=sharing">Installation Files</a>

 ![image](https://user-images.githubusercontent.com/42724831/235358687-73b3f7c5-b09b-42bc-9261-d9baf31bb71c.png)

<h2>Installation Steps</h2>

<p>
Part 1 (Create Virtual Machine in Azure)

- Create a Resource Group

- Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs

- When creating the VM, allow it to create a new Virtual Network (Vnet)

</p>

![image](https://user-images.githubusercontent.com/42724831/235459426-25e481a2-c28e-4a58-b14a-a3cb2b7e611d.png)

<p>
<br />
<br />
Part 2 (osTicket Installation)
</p>
<br />
1. Remote Connect to Windows 10 Virtual Machine
<p>
 
![image](https://user-images.githubusercontent.com/42724831/235456411-54af1242-1d4f-41ef-b1ab-8691d4458c84.png)


</p>
<p>

</p> 1.1 Open Installation Files in browser window.
</p>
<br />
2. Install / Enable IIS in Windows WITH CGI
<p> - World Wide Web Services -> Application Development Features -> [X] CGI

<p>

 ![image](https://user-images.githubusercontent.com/42724831/235457816-c0e73476-307a-4032-9309-5e3654a28dd3.png)

</p>
<p>
<br />

![image](https://user-images.githubusercontent.com/42724831/235458304-f3e470ec-1ff9-46be-8fc7-2170fe31dfc7.png)

</p>
<br />
<br />
<br />
3. From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
<p>
<br />

![image](https://user-images.githubusercontent.com/42724831/235460363-116f09aa-8a99-49b7-aead-2c16dc958da5.png)

</p>
<p>

![image](https://user-images.githubusercontent.com/42724831/235460657-eee4e685-7d3b-4472-84b7-4b164f95f86a.png)

</p>
<br />
<br />
<br />
3.1 From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi)
<br />
<br />
<p>

![image](https://user-images.githubusercontent.com/42724831/235461557-cd2d0999-9de3-4736-b2a9-a4ebd23747f7.png)

</p>
<p>

![image](https://user-images.githubusercontent.com/42724831/235461931-e3326cab-dc53-4f03-b1f6-33cc1141c21d.png)
</p>
<br />
<p>
</p>
<br />
<p>
3.2 Create the directory C:\PHP
</p>3.3 From the Installation Files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP

<br />
<br />
<p>

![image](https://user-images.githubusercontent.com/42724831/235465647-bc8f655f-455f-4bb1-8b1a-5174d6069c15.png)

</p>
<p>

![image](https://user-images.githubusercontent.com/42724831/235465854-7d8b00c7-001e-4e10-85a5-11d054b68fb4.png)

</p>
<br />
<br />
<br />
4. From the Installation Files, download and install VC_redist.x86.exe
<p>
<br />

![image](https://user-images.githubusercontent.com/42724831/235466971-e43a5f00-b488-45fb-91d3-723a9416c611.png)
>
</p>
<p>
<br />

![image](https://user-images.githubusercontent.com/42724831/235467398-4c425a67-ac5a-4563-aedc-e8ed12b21371.png)

</p>
<br />
<br />
<br />
<p>
5. From the Installation Files, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
<p>

- Typical Setup ->

- Launch Configuration Wizard (after install) ->

- Standard Configuration ->

- Create Password
<p>

![image](https://user-images.githubusercontent.com/42724831/235468877-489217b4-34cf-4333-9841-268194815998.png)
<br />
</p>
<p>

![image](https://user-images.githubusercontent.com/42724831/235469177-6018695a-8200-4df4-b49e-d7b61777ae32.png)

</p>
<br />
</p>

![image](https://user-images.githubusercontent.com/42724831/235469343-db78a595-66cc-4e67-afb8-f22067a16fb1.png)
</p>
<br />
</p>
<br />
<p>
<br />
<p>
6. Open IIS as an Administrator

</p>
<p>
<br />

![image](https://user-images.githubusercontent.com/42724831/235474403-7eb0a991-4919-443c-8a44-8330d1233b9f.png)

</p>
<br />
<br />
<br />
</p>
6.1 Register PHP from within IIS

6.2 Reload IIS (Open IIS, Stop and Start the server)
<br />
<br />
<p>

![image](https://user-images.githubusercontent.com/42724831/235475506-3cb187d3-24e1-4584-9a75-06f25217d50c.png)

</p>
<br />
<br />
<p>
7. Install osTicket v1.15.8
<p>

- Download osTicket from the Installation Files Folder

- Extract and copy “upload” folder to C:\inetpub\wwwroot

- Within C:\inetpub\wwwroot, Rename “upload” to “osTicket”

- Reload IIS (Open IIS, Stop and Start the server)

</p>
<br />
<p>

![image](https://user-images.githubusercontent.com/42724831/235478176-bf8c25f5-1181-4320-ae9e-e8073b8fef61.png)

</p>
<p>

![image](https://user-images.githubusercontent.com/42724831/235478788-8c2e50bf-fd2e-4ade-9dc8-aceab4c88b5c.png)

</p>
<br />
8. On the left, go to Sites -> Default -> osTicket
<p>

- On the right, click “Browse *:80”

</p>
<br />
<p>

![image](https://user-images.githubusercontent.com/42724831/235480907-bf6c9f53-ff2a-4955-a741-f4c51107c3e5.png)

</p>
<p>
**Note that some extensions are not enabled**
</p>
<br />
<p>
8.1 Go back to IIS, sites -> Default -> osTicket
<p>

- Double-click PHP Manager

- Click “Enable or disable an extension”

- Enable: php_imap.dll

- Enable: php_intl.dll

- Enable: php_opcache.dll

- Refresh the osTicket site in your browse, observe the changes

</p>
<br />
<p>

![image](https://user-images.githubusercontent.com/42724831/235488216-37103522-3d12-4deb-8c4b-84128f6670f9.png)

</p>
<br />
<p>
<p>
</p>
<p>
9. Rename: ost-config.php
<p>

- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

</p>
<br />
<p>

![image](https://user-images.githubusercontent.com/42724831/235500091-70b1c82a-8910-4bf4-bcba-324a078280ab.png)

</p>
<br />
<p>
</p>
<p>
9.1 Assign Permissions: ost-config.php
<p>

- Disable inheritance -> Remove All

- New Permissions -> Everyone -> All

</p>
<br />
<p>

![image](https://user-images.githubusercontent.com/42724831/235504768-a26bc784-6f5c-451d-9195-91a995c49eb8.png)

</p>
<br />
<br />
<p>
10. Continue Setting up osTicket in the browser (click Continue)
<p>

- Name

- Default email (receives email from customers)

</p>
</p>
<br />
<p>

![image](https://user-images.githubusercontent.com/42724831/235506150-e3ccaa1c-bc9f-4c8c-9dcb-b4fca51a2be5.png)

</p>
<br />
<br />
<p>
11. From the Installation Files, download and install HeidiSQL.
<p>

- Open Heidi SQL

- Create a new session, root/Password1

- Connect to the session

- Create a database called “osTicket”

</p>
<br />
</p>
<br />
<p>

![image](https://user-images.githubusercontent.com/42724831/235507010-15836773-c458-40f7-a72a-df69e4475211.png)

</p>
<p>

</p>
<br />
</p>
<br />
<p>


</p>
<p>

![image](https://user-images.githubusercontent.com/42724831/235507224-5e0822f7-ccb0-4db4-ae4a-76aecf0888d2.png)

</p>
<br />

![image](https://user-images.githubusercontent.com/42724831/235508423-fd07d573-1404-47f8-a61f-4a2adf2cf676.png)

</p>
<br />
<p>

![image](https://user-images.githubusercontent.com/42724831/235508814-199b240c-8175-49df-92b2-555fa3cb9355.png)

</p>
<br />
</p>
<br />
<p>
12. Continue Setting up osTicket in the browser.
<p>

- MySQL Database: osTicket

- MySQL Username: root

- MySQL Password: Password1

- Click “Install Now”

</p>
<br />
<p>

![image](https://user-images.githubusercontent.com/42724831/235509158-1852b5d3-6011-4c56-9116-548ea2ef212f.png)

</p>
<p>
</p>
<br />
</p>
<br />
</p>
<br />
<p>

![image](https://user-images.githubusercontent.com/42724831/235509619-3b5b17fb-554e-48e3-855c-e278c90260bc.png)

</p>
<p>
osTicket is now successfully installed!
<p>

- Follow the Config File Permmission instructions.

</p>
<br />
</p>

![image](https://user-images.githubusercontent.com/42724831/235510782-c2b551a8-1077-4c75-9254-b1103c80624b.png)

<br />
</p>
<br />
<p>
Notes:
<p>

- Browse to your help desk login page: http://localhost/osTicket/scp/login.php

- End Users osTicket URL: http://localhost/osTicket/ 

</p>
<br />
</p>
<br />
</p>
<br />
<p>

![image](https://user-images.githubusercontent.com/42724831/235511385-29b1a530-f977-49cb-a008-53b261e3d153.png)

</p>
<br />
</p>
<br />
</p>
<br />
<p>
