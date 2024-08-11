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
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
