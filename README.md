# Setting up Transmission Jail
Create transmission jail by going to `Plugins > Available > Transmission > Install` and leave DHCP checked, do not touch anything else and press save.

# Adding a Mount Point to the Jail
Go to Jail and stop the jail named "transmission" by pressing on the 3 dot menu button > stop.

In the same menu again, press mount points.

Add a mount point (by going to Actions > Add Mount Point) which sets somewhere in your storage dataset as the source and /media in your jail dataset as the destination.

**Move the downloaded script from this repo into the source that you set in your mount point earlier.**

# Enabling TUN for the Jail
Go to Shell (FreeNAS one and NOT the jail one) and type in the command below:

`iocage set allow_tun=1 transmission`

Reboot FreeNAS.

# Running the Script
After reboot, go into the shell OF YOUR JAIL by clicking on the 3 dot menu next to your jail name (should be transmission) in the list.

Type the following commands:

`cd /media`

`sh freenas-transmission-openvpn.sh`
