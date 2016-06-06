###lock your printer
HP printers ship out of the box with a ton of open ports so that they just work
after setting up your HP you should consider doing the following items

1. Disable all protocols that you do not need IPX/SPX, mDNS/Appletalk, MLC/DLC, FTP.
2. set acl for local networks most printers can be a single network if you have more than one subnet you can just add them.
3. SNMP settings change "SET" to something other than private or just leave blank
4. setup a admin password in Jet Direct.