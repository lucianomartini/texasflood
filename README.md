# texasflood for sysvinit - the first parallel boot in the World. 

SysVinit TexasFlood, was probably the first init system with parallel boot and much more like services auto-maintenance, priority balancing, but was only available for the brazilian distro "Resulinux", now free for everybody on github.

Capabilities:
=============

-Fix the priorities (auto renice) for the programs that are important for you.
-Parallel Services Loading based on the script name number, put the same number to load in parallel.
   S25-apache S25-postgresql - It will load at same time. 
   S26-mysql - It will wait for apache and postgresql to become loaded 
-Auto restart of service  or just auto send e-mail.  (not included in this version for now (are included on olders resulinux), but it is ready to go in the next),  
-Much more

Is really the fastest way to boot a linux machine without going out from sysvinit, and it is even faster than systemd, without the crap. 

Installation:
=============

To use texasflood you must have SysVinit installed.  (for debian this means apt install sysvinit-core) 

1- After the clone, copy all this files to / in the right paths. 
2- Then move your /etc/init.d/rc to /etc/init.d/rc-backup (this can depends on your distro). 
3- After that just create a link ln -sf /sbin/texasflood-core to /etc/init.d/rc
4- Edit the file /etc/texasflood.conf carefully following the comments. 
5- reboot your machine and hope the best. 

Test first on a VM because that can break your system if you make a mistake, or if your distro are not fully compatible.

