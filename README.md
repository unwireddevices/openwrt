# openwrt
OpenWRT patches for Black Swift board

Patches are intended to use with OpenWRT 14.07 r45620. To download it, use *svn co -r 45620 svn://svn.openwrt.org/openwrt/branches/barrier_breaker openwrt*

*patch -p0 &lt; bsb.patch* — adds Black Swift board to the list of targets

*patch -p0 &lt; gpio-irq-728.patch* — GPIO IRQ support by GBert, https://github.com/GBert

*patch -p0 &lt; new_modules.patch* — kernel modules developed by Black Swift team

*patch -p0 &lt; new_files.patch* — avahi-daemon and uboot-envtools configuration files

*patch -p0 &lt; mjpg.patch* — enable mjpg_streamer service by default

*patch -p0 &lt; console.patch* — patch to allow to completely disable UART console using bootloader's environment variable. Must be re-applied after *make clean* and must be preceeded with *make kernel_menuconfig*

*.config* — ready to use OpenWRT Buildroot configuration file

For more details, please visit http://www.black-swift.com/wiki
