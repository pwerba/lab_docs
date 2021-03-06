# Walter Lab Server "UNICORN.UCSF.EDU"

The Walter lab has a server called "unicorn" this server is located in one of the server rooms here at Mission bay and provides reliable network storage for lab research data.

The server capacity is about 50TB and currently contains the data the lab has collected over the last few years. We just upgraded the server to this amount of storage to fit the needs of the lab.

Currently the server is setup running open source software connected to a very large array of disks running the ZFS file system.

The server is setup so that each lab member gets a home folder that is fully accessible to that lab member and is "read-only" to others in the lab this means that each user can create their own folders and files in that folder, while others in the lab can read all the files in each other members folders they can not make changes. This setup allows for others to use data from other members folders and at the same time makes sure that others can not alter the original files.

There is also a folder called "Lab_Shared" this is a folder that has shared files and folders for anyone to access. It is important to not that that folder is "read-writable" to all members of the lab so take care when making changes to that folder.

We also created a folder called "data_temp" this is a folder that will be used by the instruments to collect data to a "temp" folder that will be deleted every 30 days. This folder will allow you to collect data from instruments in the lab and then move those files or folders to either your personal folder or the lab shared folder.

Please contact (me) Peter Werba if you need any custom folders or permissions I am happy to work with you to make sure that the server is helping you with your research.

NOTE: If you have data that is stored on the old server all that data has been transferred to the new server.


# Connecting to the server (MAC_OS)
Requirements:

You must be on the Campus network either by connected to ethernet (preferred for large files) or wireless
or from home you must be using UCSF VPN link <https://it.ucsf.edu/services/vpn>

supported MAC OS (10.7 - current release)

## Step One
In the Finder select Connect to Server from the Go menu (command-k).

![step one](img/server_step1.png)

## Step Two

Type in the address of the server:  smb://server.ucsf.edu/folder
NOTE: It is important to use SMB:// before the server address

![step two](img/server_step2.png)

## Step Three

When prompted enter in your UCSF email username and password.
NOTE: this would be the same credentials you use when logging into UCSF webmail.

![step three](img/server_step3.png)

Click the "connect" button

## Step Four

You are now presented with a list of available shares. Choose the share you wish to be connected to and click "OK"

NOTE: You may not have full access to each share that is shown if a share-point shows up ad grey it most likely means that you are already connected to the share.

![step four](img/server_step4.png)

#Connecting to the server (Windows_OS7)

###If your computer is bound to the campus Active Directory

![step one](img/ad_win_step1.png)

![step two](img/ad_win_step2.png)

![step three](img/ad_win_step3.png)

###If your computer is NOT bound to the campus Active Directory

![step one](img/wo_ad_win_step1.png)

![step one](img/wo_ad_win_step2.png)

![step one](img/wo_ad_win_step3.png)

![step one](img/wo_ad_win_step4.png)

![step one](img/wo_ad_win_step5.png)

# Connecting to the server (Windows_OS)
### How to connect to cmp file server from Windows OS (Windows XP)

1. Right-click on "My Computer" (note this can vary on the version of windows you are on.. if not on the desktop please look in the "Start" menu.
2. Select the option "map network drive"
3. A window will appear the default drive map will be Z: (*NOTE: you can change this if you wish, it's best to leave the default*)
4. In the field labeled "Folder:" please type the path to the network share that you are trying to connect to eg: `\\servername.ucsf.edu\share_point`
5. Depending on your options either select or deselect the "Reconnect at logon" box (*NOTE: if this is a share you use every day this is a good option.*)
6. If you are not bound to the server or the password differs from your login please choose the option "Connect using a different user name" "different user name" is a hyperlink if selected you get a box to type your username and pass into.
7. Type your username and password and then choose "Finish" this will give you access to the share.. you should now see the Z: drive mounted under your computer.



### How to connect to the CMP File Server from Windows OS (VISTA OR WIN7)

NOTE: If you are running Windows Vista or Windows 7 you will have to make the following changes to the Windows Security Policy. The default setup allows you to connect to a bound windows server … Please make the following changes

<code>
Open Control Panel - Administrative Tools - Local Security Policy

Local Policies - Security Options

Network security: LAN Manager authentication level
Send LM &amp; NTLM responses

Minimum session security for NTLM SSP
Disable Require 128-bit encryption
</code>

After you make the following changes you should be able to follow steps 1-7 above and connect to the server.
