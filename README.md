# TP_LINK-WN725-driver-for-Raspberry-PI-2-
The RTL 8188eu that works for ARCH LINUX. 
It is configured for USB but this can be changed in the Makefile if you want to use this as a generic driver for RTL 8188's.

This is based on the TP_LINK driver but it is modified to work with ARCH Linux kernels >4.00. 
Remember to install the linux-headers package e.g "Pacman -S linux-headers" and select the Raspbery PI version.
CD to the LinuxDriver directory and type "make"
If all compiles well, then
You may want to save th existing /lib/modules/\`uname -r\`/kernel/drivers/net/wireless/8188eu.ko to somewhere safe. e.g ~

sudo cp 8188eu.ko /lib/modules/\`uname -r\`/kernel/drivers/net/wireless/

sudo depmod -a

sudo modprobe 8188eu
