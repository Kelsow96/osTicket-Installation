<h1> osTicket Installation </h1>

<img src="https://github.com/Kelsow96/osTicket-Installation/assets/169297569/c7d566b8-e178-4434-96ba-94fdcbbde1cc" width="500" />

<h2> What is osTicket? </h2>

osTicket is an open-source help desk and ticketing system that efficiently manages customer support. It features ticket management, customizable forms, agent collaboration, automated workflows, a knowledge base, and reporting tools. osTicket supports email integration, multiple languages, and role-based access control, with free and professional support options.

<h2> Overview </h2>

In this lab, we will create an Azure Virtual Machine running Windows 10 (4 vCPUs) named "Vm-osticket" with the username "labuser" and password "osTicketPassword1!". To ensure consistency, we will install osTicket and its dependencies using the provided installation files. The steps include enabling IIS with specific features, installing PHP Manager and the Rewrite Module, setting up PHP 7.3.8, MySQL 5.5.62, and configuring osTicket. We will then finalize the setup by configuring the necessary PHP extensions and setting up the database. Finally, we will clean up by securing configuration files and setting appropriate permissions.

<h2> Environments and Technologies Used: </h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Virtual Machine (VM-osticket)
- Internet Information Services (IIS)
- PHP
- MySQL
- VC Redist
- osTicket
- HeidiSQL
- Web Browser

<h2> Operating Systems Used: </h2>

- Windows 10

<h2> List of Prerequisites: </h2>

- Azure Account/Subscription
- [Installation Files](https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)

<h2> High-Level Steps: </h2>

**1. Create Azure VM:**
- Set up a Windows 10 virtual machine in Azure with 4 vCPUs.
- Name the VM Vm-osticket.
- Use the username labuser and password osTicketPassword1!.

**2. Install IIS:**
- Enable Internet Information Services (IIS) with CGI, Common HTTP Features, Application Development Features (CGI), and the IIS Management Console.

**3. Install PHP and Dependencies:**
- Install PHP Manager for IIS.
- Install the Rewrite Module.
- Create a directory C:\PHP.
- Download and unzip PHP 7.3.8 into C:\PHP.
- Install Visual C++ Redistributable (VC_redist.x86.exe).

**4. Install MySQL:**
- Download and install MySQL 5.5.62.
- Complete the typical setup and configure it with the password Password1.

**5. Configure IIS for PHP:**
- Open IIS as an administrator.
- Register PHP in IIS.
- Reload IIS (stop and start the server).

**6. Install osTicket:**
- Download osTicket v1.15.8.
- Extract and copy the "upload" folder to C:\inetpub\wwwroot, renaming it to osTicket.
- Reload IIS and browse to osTicket site.

**7. Enable PHP Extensions:**
- Enable php_imap.dll, php_intl.dll, and php_opcache.dll in IIS PHP Manager.
- Refresh the osTicket site.

**8. Configure osTicket:**
- Rename ost-sampleconfig.php to ost-config.php.
- Assign necessary permissions to ost-config.php.

**9. Set Up Database:**
- Install HeidiSQL.
- Create a new MySQL session and database named osTicket.

**10. Complete osTicket Setup:**
- Finish the osTicket setup in the browser by entering the database details.
- Install osTicket and verify the installation.

**11. Post-Installation:**
- Clean up by deleting the setup directory.
- Set permissions to read-only for the ost-config.php file.

<h2> Steps: </h2>

**1. Create Azure VM:**
- Set up a Windows 10 virtual machine in Azure with 4 vCPUs.


- Name the VM Vm-osticket.


- Use the username labuser and password osTicketPassword1!.
