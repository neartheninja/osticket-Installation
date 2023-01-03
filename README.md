# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installation</h1>
This tutorial outlines the installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation requirements</h2>

- Azure Subscription
- VM (Virtual Machine)
- RDP (Remote Desktop Connection)
- Google Drive file (<a href='https://drive.google.com/drive/folders/1Loma_9mi_q4fS4aQbUmUddWVsEdp_13n?usp=share_link'>Link</a>)
- Internet Information Service (IIS) set up

<h2>Installation Steps</h2>

<p>
<a href="https://imgur.com/3y3BBgV"><img src="https://i.imgur.com/3y3BBgV.jpg" title="source: imgur.com" /></a>
</p>
<p>
<a href="https://imgur.com/HkQgyCB"><img src="https://i.imgur.com/HkQgyCB.jpg" title="source: imgur.com" /></a>
</p>
<p>
We will start by opening the start menu search bar amd type "Windows Features" from there you will click "turn window features on or off"  This will pull up a window with a list of folders and checkboxes. From there we will select the IIS(Information Internet Services) and let the IIS install.
</p>
<br />

<p>
<a href="https://imgur.com/UhQlbBF"><img src="https://i.imgur.com/UhQlbBF.jpg" title="source: imgur.com" /></a>
  <a href="https://imgur.com/Ei6JlCe"><img src="https://i.imgur.com/Ei6JlCe.jpg" title="source: imgur.com" /></a>
  <a href="https://imgur.com/2e4ZSlI"><img src="https://i.imgur.com/2e4ZSlI.jpg" title="source: imgur.com" /></a>
</p>
<p>
After the IIS finishes installing, we will go to the installation folder from the link and download the WebPlatformInstaller file. The file will download this launcher as shown above, go through the installation when complete the following will appear. We will also install the MYSQL 5.5 server from Installation folder. You should recieve a prompt on a new username for MySQL as root and to create the password (Document these 2 pieces of information they will be used later).
</p>
<br />

<p>
<a href="https://imgur.com/DejM79d"><img src="https://i.imgur.com/DejM79d.jpg" title="source: imgur.com" /></a>
</p>
<p>
Once we select finish we will then head over to the windows search and type in  web platform. The Web Platform Installer should appear, open it and type in PHP in the search bar and sort by name. Proceed to install all PHP 32-bit vers (x86) up until 7.4.
</p>
<br />
<p>
  <a href="https://imgur.com/0pKGOQR"><img src="https://i.imgur.com/0pKGOQR.jpg" title="source: imgur.com" /></a>
 <p>
</p>
<p>
Once the install has finished, you may receive an error, this is due to old and broken links from the site. Just use the installation folder to install the missing dependecies. There should be 3 that did not get installed, but you only need to install the PHP manager and vcredist.
</p>
<p>
  <img src="https://i.imgur.com/g209LMw.png" height="80%" width="80%" alt=" Steps"/>
 </p>
<br />
<p>
<img src="https://i.imgur.com/j1MGLmo.png" height="80%" width="80%" alt="Steps"/>
</p>
<br />
<p>
<img src="https://i.imgur.com/4ViV05z.png" height="80%" width="80%" alt=" Steps"/>
</p>
<p>
 After that we head back to the installation folder to download and install the osTicket File. Once downloaded extract the zipped folder from the downloads into the downloads, doing this makes the zip folder create a regular folder with the same contents.Next head into the new and unzip folder from the osTicket download and copy the upload folder. Go to <strong>This PC--> then windows(C:)--> then inetpub--> and finally open wwwroot</strong> and paste the upload folder within. Rename that folder to osTicket.
</p>
<br />
<p>
<img src="https://i.imgur.com/Q3LUJgA.png" height="80%" width="80%" alt=" Steps"/>
</p>
<br />
<p>
<img src="https://i.imgur.com/PlitxOI.png" height="80%" width="80%" alt=" Steps"/>
</p>
<p>
Once you are done with the last step we want to head to are windows search bar and type in IIS. Select IIS and restart IIS with the panel on the right side, after that select the drop down arrow key for VM-osTicket or whatever name you selected earlier in the lab on the <strong>left hand panel--> then select sites--> Defualt Website--> and are osTicket folder</strong> should be there.
</p>

<br />
<p>
<img src="https://i.imgur.com/KIGAyir.png" height="80%" width="80%" alt="Steps"/>
</p>
<p> Afterwards you are going to select the PHP Manager within the osTicket Home located in the center. From there <strong>select Enable or disable an extension, look for php_imap.dll is enable along with php_intl.dll and php_opcache.dll.</strong>
</p>
<br />
<p>
<img src="https://i.imgur.com/dRGPdWI.png" height="80%" width="80%" alt=" Steps"/>
</p>
<p>
Now we head back to are wwwroot folder within file explorer, from there we select <strong>osTicket--> Then include</strong>. When inside the "include" folder scroll down to the ost-sampleconfig.php to ost-config.php as shown above.
</p>
<br />
<p>
<img src="https://i.imgur.com/cHBdPn3.png" height="80%" width="80%" alt="Steps"/>
</p>
<p>
After we changed the ost-sampleconfig.php to ost-config.php we will <strong>open its properties then -> open security -> click on advance -> then disable inheritance -> add permission -> select principle at the top left -> from there within the open box below for objects type everyone -> select Check Names -> and select ok -> on the following page select full control to give all basic permissions besides Special permissions for everyone</strong>. Your security panel should display whats above with everyone and full control under access.
</p>
<br />
<p>
<img src="https://i.imgur.com/vCXWto2.png" height="80%" width="80%" alt="Steps"/>
</p>
<p>
 If you have reached the installation page for osticket, all the previous steps have been completed successfully. Now simple fill out all the information as shown (Document The Admin User portion as well as the Database setting username and password will be needed for the lab).
</p>
<br />
<p>
<img src="https://i.imgur.com/mQPzPDm.png" height="80%" width="80%" alt=" Steps"/>
</p>
<p>
Next we head back into are <a href='https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6'>Link</a> to are google Drive for the lab and download the HeidiSQL. Go through the complete download until the finish button is prompt, after you select finish the application will open as shown above.
</p>
<br />
<p>
<img src="https://i.imgur.com/GhJrKSP.png" height="80%" width="80%" alt=" Steps"/>
</p>
<p>
Select the add button on the button left, Heidi will prompt you to put in the password you create earlier when downloading the php files within WebPlatformInstaller 5.1. Enter the password and you will be sent to the page shown.Next <strong>rightclick unnamed -> then hover over create new -> and select Database</strong>. Name that database osTicket
<br />
<p>
<img src="https://i.imgur.com/wvurZnY.png" height="80%" width="80%" alt=" Steps"/>
</p>
<p>
Now go back to the osTicket web browser as shown above and enter the new database name along with the respected credentials. Install and wait for the page to load.
</p>
<br />
<p>
<img src="https://i.imgur.com/aCKlFCn.png" height="80%" width="80%" alt="Steps"/>
</p>
<p>
Once complete you will have this page appear letting you know that you've successfully created the osTicket system. The links below are for the user end and the staff as well.
</p>
<br />
<p>
<img src="https://i.imgur.com/cWrNy3w.png" height="80%" width="80%" alt="Steps"/>
</p>
<p>
Final step, head back to the folder where we were in the include folder. From there <strong>Rightclick properties--> head to security tab --> then advance --> and double click on everyone --> once you are back in permissions change every user to read and execute</strong> press ok and close out the tabs for the properties.
</p>
<br />
<p>
<img src="https://i.imgur.com/2kYWhCm.png" height="80%" width="80%" alt=" Steps"/>
</p>
<p>
To end off the installation for osTicket. Head into the osTicket folder by <strong>clicking on This PC --> then windows (C:) --> select inetpub --> wwwroot --> and finally select osTicket.</strong> There we must delete the setup folder, in order to do so we must delete the contents with the folder. After deleting the contents within the setup folder we can move onto deleting the setup folder from osTicket. And congradulations you have completed the osTicket Installation.
</p>
<br />
<p>
This will conclude the Installation for the osTicket Lab. The next section we will begin to use osTicket and begin with the configurations. Next section <a href='https://github.com/DevilDog2001/osTicket-configurations'>Configurations</a> .
</p>
