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

- Enable IIS in windows with CGI and common HTTP features
- PHP Manager
- Rewrite Module
- Create the directory C:\PHP
- PHP 7.3.8
- MySQL 5.5.62
- Open IIS as an Administrator and register PHP

<h2>Installation Steps</h2>

<p>

![image](https://github.com/user-attachments/assets/8851fadd-70c5-4d96-b119-d56f2088d73e)
</p>
<p>

- From our osTicket installation files we extract and copy the 'upload' folder to c:\inetpub\wwwroot

- Within c:\inetpub\wwwroot we rename 'upload' to 'osTicket'

- Then reload IIS
</p>
<br />

<p>

![image](https://github.com/user-attachments/assets/b31ed481-61e9-4b7e-a580-2a1d23c92eab)

</p>
<p>

- In IIS go to Sites -> Default -> osTicket

- On the right, Click 'Browse *:80'

- Notice that some plugins are not enabled by default

- Back in IIS go to Sites -> Default -> osTicket, and open PHP Manager

- Click 'Enable or disable an extension'

    - Enable php_imap.dll

    - Enable php_intl.dll

    - Enable php_opcache.dll

- Refresh the osTicket site in your browser and note that we have enabled these plugins

- Navigate to C:\inetpub\wwwroot\osTicket\include\

    - Change the file name 'ost-sampleconfig.php' to 'ost-config.php'

    - Change the permissions of 'ost-config.php' so that 'Everyone' has 'Full Control' permission
</p>
<br />

<p>

![image](https://github.com/user-attachments/assets/4ff320fa-4836-4d08-b9aa-0fa6531184ce)

</p>
<p>

- Download and install Heidi SQL

    - Open Heidi SQL

    - Create a new session using the same password used in MySQL

    - Connect to the session

    - Create a database called “osTicket”
</p>
<br />

<p>

![image](https://github.com/user-attachments/assets/b5d7e8ca-24a2-4131-8195-d236bc868877)

</p>
<p>

- Continue Setting up osTicket in the browser (click Continue)

    - Fill out the 'System Settings' and 'Admin User' Sections as needed

- In the 'Database Settings' section:

    - MySQL Database: osTicket

    - MySQL Username: root

    - MySQL Password: (The same password as MySQL and Heidi SQL)

- Click 'Install Now'

- If done correctly you can now browse to your help desk login page here: http://localhost/osTicket/scp/login.php

    - And the end-user page here: http://localhost/osTicket/ 

- Clean Up

    - Delete: C:\inetpub\wwwroot\osTicket\setup

    - Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

