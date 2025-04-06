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
<img src="https://i.imgur.com/zv6EpWi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Retrieve the VM's IP address and log in via RDP. Use the set credentials for a successful connection. (Did you remember your username and password?)
<p>
<img src="https://i.imgur.com/gO2FsDz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download osTicket and unzip the files on the desktop. Right-click on the icon and select 'extract all'. Make sure the extraction is to the desktop.
<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
osTicket needs a web server! Install IIS via the VMs control panel> programs> program features. In the right panel, you will see "Turn Windows Features On or Off", click this.
<p>
<img src="https://i.imgur.com/qkuS0xV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Locate the Internet Information Servies, check the box, and expand. We also need to install CGI, so expand the World Wide Web Services as well. Under here you will see Application Development Features and through that you will find CGI. Check the CGI box and click 'Okay".
<p>
<img src="https://i.imgur.com/IICWCAU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go inside your osTicket Installation Files Folder located on the desktop and find the PHP Manager and rewrite AMD folder. Click to install both.
<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Right click to create and name a folder 'PHP' on the (C:). This will serve as your directory.
<p>
<img src="https://i.imgur.com/Q874hyi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the osTicket Installation Files Folder locate the PHP zip file and extract all contents to your newly created directory. (Browse to (C:) to find PHP folder)
<p>
<img src="https://i.imgur.com/UqpikmV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

