# texasflood

TexasFlood with SysVinit, was probably the first init system with parallel boot and more like services auto-maintenance, but was only available for the brazilian distro "Resulinux", now free for everybody on github.

Is really the fastest way to boot a linux machine without going out from sysvinit, and it is even faster than systemd, without the crap. 

To use texasflood you must have SysVinit installed, copy all this files to /, then move your /etc/init.d/rc to /etc/init.d/rc-backup (this can depends on your distro), after that just create a link ln -sf /sbin/texasflood-core to /etc/init.d/rc, edit the file /etc/texasflood.conf carefully, then reboot your machine and you will have texas flood.

Test first on a VM, if you are not very sure, because that can break your system if you make a mistake, or if your distro are not fully compatible.

