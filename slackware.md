# Slackware Linux Installation/Configuration Guide, 2022   
![](Pictures/slacksample/initialslack.png)

Hello, this is a guide to installing the **BEST** Linux distribution for learning, Slackware-Current  
This guide will cover installing Slackware-Current. I recommend Slackware-Current, the "rolling release" version, at least until 15.0 is released.  

Slackware, created by Patrick "The Man" Volkerding in 1993, is the *oldest* actively maintained Linux distribution.  
It aims to be the simplest, most Unix-like Linux distribution, and in my opinion succeeds greatly in this aim.  

Some say that "Slackware is Dead!", because the last official release, 14.2, is around 5 years old.  
This is not the case, for example, Slackware-Current has a more recent version of GCC than the highly-touted Arch Linux.  

Installation is quite simple.  
Simple does not inherently mean "easy" in this context; don't let that worry you however.  
Certainly it will serve to make you more comfortable administrating a Linux system from the command-line interface. We will be testing it using VirtualBox until you learn more about drive partitioning, as we don't want you to "nuke" your Windows installation due to inexperience. 

A basic overview of the process is:  
 
* Download Alienbob's Slackware-Current iso, and configure your virtual machine to use it as the virtual optical drive
* Boot the installer, and partition your hard drive with GDisk or whatever command-line partition tool you're most comfortable with  
* Run "setup", and install your system!  
* Boot your fresh system!  

And that's it!  *MUCH* simpler in my opinion than getting an Arch or Gentoo installation running "properly", with development tools, desktop environments, web browsers, and the like, as Slackware has a full, comprehensive development environment already installed!  


Whether you're using Windows or Mac OS, I recommend for you to install Virtualbox and test it out in a virtualized environment. 
This requires less of an "investment" as opposed to a "bare metal" installation.  
If you do this, make sure virtualization is enabled in the BIOS settings.  

* Download Alienbob's Slackware-Current iso from [https://slackware.uk/people/alien-current-iso/slackware64-current-iso/slackware64-current-install-dvd.iso]  
* Create a new virtual hard disk, with a minimum dynamically allocated size of 25 GB.
* Click on "virtual optical drive" and select the slackware64-current iso, and proceed to hit "Start" to boot the operating system.
 ![](Pictures/slacksample/slack1.png)

Hit enter when the "boot" prompt comes up, and the Slackware installer will boot. Now it's time to partition your drive.  

There are excellent guides on how to partition a hard disk such as (insert relevant codecademy link), this is a simple overview that will serve it's purpose however.   

* Type 'fdisk -l' to list the hard drives connected to the system. There will only be one proper hard drive, as we are using Virtualbox, but this is still worth making a habit of. 
* Next, type 'gdisk /dev/sdx' where "sdx" is the "name" of the hard drive you intend to install to.  
* Enter '?' into gdisk, and familiarize yourself with the commands.  
* You will only need to make one partition of default type, this is accomplished by typing 'n' to create  a new partition, hitting Enter a few times to accept the defaults, and running 'w' to write the partition table before quitting with 'q'  
* I am omitting a swap partition and EFI compatibility for simplicity and brevity.  
* Type 'setup' to enter the installer.  
![](Pictures/slacksample/slack3.png)

The "hard" part is thankfully over; manually partitioning a disk is an important thing to learn, and this is a good way to do so.  


* In setup, select "add target", and hit enter a few times to accept the defaults.
* When it asks where your installation media is, select the CD/DVD option. Leave all the package series selected until you know what you're doing, then select "full" or "terse" for installation display method. Feel free to take a break while Slackware is installed.
![](Pictures/slacksample/slack4.png) 
* Skip making a USB boot stick.
* Install LILO using the "simple" method, to the MBR
* Finish the installation as you wish; my recommendation is to not configure your network now, use XFCE as your window manager, and leave the rest default.

Congratulations, Slackware is installed, and ready to boot!
![](Pictures/slacksample/slack6.png)

I recommend installing the following tools if you wish to experiment with Slackware further:

Slackpkg+: [https://slakfinder.org/slackpkg+.html]  

sbotools: [https://pink-mist.github.io/sbotools/]




