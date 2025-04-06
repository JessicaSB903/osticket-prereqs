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
Another component of osTicket is the vc_redist file and mysql. Locate, click, and install both. During the mysql install- select 'typical setup', finish, and launch.
<p>
<img src="https://i.imgur.com/9B7qj4h.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Choose the 'standard configuration' upon launch of 'mysql. Take note of your password. This is very important! Click next, then execute.
<p>
<img src="https://i.imgur.com/2UzMWtP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click Start and search for IIS. Right-click and run as an admin. The PHP manager that you previously installed will be here. Double click it. 
<p>
<img src="https://i.imgur.com/BqLfQQ8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, you will register a new PHP version and navigate to the PHP folder on the (C:). Once inside, double-click PHP-cgi
<p>
<img src="https://i.imgur.com/V6PL2aP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, back into IIS to stop and restart the server. You will find this on the far right side of the IIS window.
<p>
<img src="https://i.imgur.com/0RIEbOE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
osTicket is ready to install! Head back to the osTicket Installation File Folder and extract. In another file explorer window, navigate to (C:)>inetpub>wwwroot and copy the folder named 'upload' (inside of osTicket) into wwwroot. 
<p>
<img src="https://i.imgur.com/VF8kS3j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The copied folder will be renamed to 'osTicket' with NO spaces.
<p>
<img src="https://i.imgur.com/arVgZKy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Running IIS as an admin, stop and start the server once again. Within the left panel, expand the 'sites' and 'Default Web Site', and click osTicket. In the right panel, click 'Browse'.
<p>
<img src="https://i.imgur.com/IxSd02o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The browser will open a page resembling the picture below. Some of the extensions are not enabled, but we will fix this!
<p>
<img src="https://i.imgur.com/2fml2R3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside IIS, navigate to the site>default websites>osTicket and double click PHP manager. Within the PHP manager are 'PHP Extensions' configurations. Click enable or disable an extension
<p>
<img src="https://i.imgur.com/T5jdlPa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
There is a list of grayed-out extensions. You want to find these three: php_imap.dll, php_intl.dll, and php_opcache.dll. Enable all three.
<p>
<img src="https://i.imgur.com/QPatsdn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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

