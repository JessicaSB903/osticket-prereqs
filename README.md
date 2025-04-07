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
<p align="center">Create a Virtual Machine within Azure using Windows 10 with a size that includes 2 vCPUs for sufficient processing power. Remember your username and password!
<p>
<img src="https://i.imgur.com/zv6EpWi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Retrieve the VM's IP address and log in via RDP. Use the set credentials for a successful connection. (Did you remember your username and password?)
<p>
<img src="https://i.imgur.com/gO2FsDz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Download osTicket and unzip the files on the desktop. Right-click on the icon and select 'extract all'. Make sure the extraction is to the desktop.
<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">osTicket needs a web server! Install IIS via the VMs control panel> programs> program features. In the right panel, you will see "Turn Windows Features On or Off", click this.
<p>
<img src="https://i.imgur.com/qkuS0xV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Locate the Internet Information Servies, check the box, and expand. You also need to install CGI, so expand the World Wide Web Services as well. Under here you will see Application Development Features and through that you will find CGI. Check the CGI box and click 'Okay".
<p>
<img src="https://i.imgur.com/IICWCAU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Go inside your osTicket Installation Files Folder located on the desktop and find the PHP Manager and rewrite AMD folder. Click to install both.
<p>
<img src="https://i.imgur.com/SVsQb3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Right click to create and name a folder 'PHP' on the (C:). This will serve as your directory.
<p>
<img src="https://i.imgur.com/Q874hyi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">From the osTicket Installation Files Folder locate the PHP zip file and extract all contents to your newly created directory. (Browse to (C:) to find PHP folder)
<p>
<img src="https://i.imgur.com/UqpikmV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Another component of osTicket is the VC_redist file and mysql. Locate, click, and install both. During the mysql install- select 'typical setup', finish, and launch.
<p>
<img src="https://i.imgur.com/9B7qj4h.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Choose the 'standard configuration' upon launch of 'mysql. Take note of your password. This is very important! Click next, then execute.
<p>
<img src="https://i.imgur.com/2UzMWtP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Click Start and search for IIS. Right-click and run as an admin. The PHP manager that you previously installed will be here. Double click it. 
<p>
<img src="https://i.imgur.com/BqLfQQ8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Next, you will register a new PHP version and navigate to the PHP folder on the (C:). Once inside, double-click php-cgi
<p>
<img src="https://i.imgur.com/V6PL2aP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Now, back into IIS to stop and restart the server. You will find this on the far right side of the IIS window.
<p>
<img src="https://i.imgur.com/0RIEbOE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">osTicket is ready to install! Head back to the osTicket Installation File Folder and extract. In another file explorer window, navigate to (C:)>inetpub>wwwroot and copy the folder named 'upload' (inside of osTicket) into wwwroot. 
<p>
<img src="https://i.imgur.com/VF8kS3j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">The copied folder will be renamed to 'osTicket' with NO spaces.
<p>
<img src="https://i.imgur.com/arVgZKy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Running IIS as an admin, stop and start the server once again. Within the left panel, expand the 'sites' and 'Default Web Site', and click osTicket. In the right panel, click 'Browse'.
<p>
<img src="https://i.imgur.com/IxSd02o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">The browser will open a page resembling the picture below. Some of the extensions are not enabled, but you will fix this!
<p>
<img src="https://i.imgur.com/2fml2R3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Inside IIS, navigate to the site>default websites>osTicket and double click PHP manager. Within the PHP manager are 'PHP Extensions' configurations. Click enable or disable an extension
<p>
<img src="https://i.imgur.com/T5jdlPa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">There is a list of grayed-out extensions. You want to find these three: php_imap.dll, php_intl.dll, and php_opcache.dll. Enable all three.
<p>
<img src="https://i.imgur.com/QPatsdn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Navigate back to the wwwroot folder ((C:)>inetpub>wwwroot), go into 'osTicket'. Locate the folder named 'include'. Within this folder, scroll to 'ost-sampleconfig.php and right-click to rename. The new name will read 'ost-config.php'. THIS IS VERY IMPORTANT! MAKE SURE THE RENAMING IS THE SAME AS SHOWN BELOW.
<p>
<img src="https://i.imgur.com/XKFOkRF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Next, you'll assign permissions for osTicket to make changes to the 'ost-config.php folder by right-clicking and selecting 'properties'. In the new window, select the 'security' tab, then advanced.
<p>
<img src="https://i.imgur.com/B4sVW0C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Click 'disable inheritance', then 'remove all inherited permissions'.
<p>
<img src="https://i.imgur.com/d2kldj0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">All permissions have been stripped, so now you can add permissions relevant to your needs! Simply click 'add', then 'select principal'. For instructional purposes, 'Everyone'  will be added. (This is highly NOT RECOMMENDED--FOR TUTORIAL PURPOSES ONLY.) Click 'check names' then 'ok'. Give access to your preference, click apply.
<p>
<img src="https://i.imgur.com/1PqpFcA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Go back to the osTicket page inside the browser and click continue for setup. Here you will add your Help Desk name, Admin User info, etc. DO NOT CLICK INSTALL
<p>
<img src="https://i.imgur.com/0Tmmrhs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">On your desktop inside the osTicket Installation File folder, locate 'HeidiSQL and double-click to install. Launch HeidiSQL.
<p>
<img src="https://i.imgur.com/JYD8COc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">In the Heidi Session Manager, click 'New' located in the bottom left corner. Fill in the password for the root user, and click 'Open'. This opens a connection to your database. Right click 'unnamed' in the new window and select 'create new'. 'Database' will be your option.
<p>
<img src="https://i.imgur.com/fmwS1Ge.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Name the database exactly as follows: "osTicket'. Now return to the browser. 
<p>
<img src="https://i.imgur.com/7ozvWCr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Finish filling out the database settings with your newly created database credentials. (Remember your username and password!) Click 'install now'. (ROOT will be lowercase only)
<p>
<img src="https://i.imgur.com/ODyIqNf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>  

<p align="center">osTicket has been successfully installed!
<p>
<img src="https://i.imgur.com/bAh5w2n.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p align="center">Happy Ticketing!

