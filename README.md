**# osticket-prereqs**<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />






<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop (RDP)
- osTicket
- Internet Information Services (IIS)
- Hypertext Preprocessor (PHP)
- Structure Query Language (HeidiSQL)
  
<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create a VM (virtual machine)
- Log in to VM via RDP (remote desktop)
- Download osTicket (https://osticket.com)
- Unzip files
- Install
- Configuration

<h2>Installation Steps</h2>
Create a Virtual Machine within Azure using Windows 10 with a size that includes 2 vCPUs for sufficient processing power. Remember your username and password!
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Retrieve the VM's IP address and log in via RDP. Use the set credentials for a successful connection. (Did you remember your username and password?)
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download osTicket and unzip the files on the desktop. Right-click on the icon and select 'extract all'. Make sure the extraction is to the desktop.
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
osTicket needs a web server! Let's enable IIS by going into our VMs' control panel> programs> program features. In the right panel, you will see "Turn Windows Features On or Off", click this.
</p>
<br />
