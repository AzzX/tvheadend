Tvheadend TV streaming server
		    =============================

		 (c) 2006 - 2012 Andreas Öman, et al.

Tested on Ubuntu 12.04 LTS


On latest Ubuntu Distros
========================

If you are using any Smartcard reader like the easymouse2 you could have problems
with the Auto On/Off switch. You can't disable it in the Ubuntu package.

Use an older Package.
Manual Downgrade with sudo dpkg -i <package>

libpcsclite1_1.5.3-1ubuntu4_arch.deb
libpcsclite1_1.5.3-1ubuntu4_arch-dev.deb
pcscd_1.5.3-1ubuntu4.2_arch.deb

Now the card should be alway online

Compiling Requirements
======================
Ubuntu users can use the following one-liner in order the install the
software required to compile tvheadend:

$ sudo apt-get install build-essential pkg-config libssl-dev 

If you want avahi support (optional):

$ sudo apt-get install libavahi-client-dev

If you plan on doing transcoding (also optional):

$ sudo apt-get install libavcodec-dev libavfilter-dev libavformat-dev libavutil-dev libswscale-dev

You might also like to install the extra codecs pack (incl. H264 encoder):

$ sudo apt-get install libavcodec-extra-53

How to build for Linux
======================

First you need to configure:

$ ./configure

If any dependencies are missing the configure script will complain or attempt
to disable optional features.

$ make

Build the binary, after build the binary resides in 'build.linux/'.
Thus, to start it, just type:

$ ./build.linux/tvheadend

Settings are stored in $HOME/.hts/tvheadend

Further information
===================

For more information about building, including generating packages please
visit https://www.lonelycoder.com/redmine/projects/tvheadend/wiki/Building
