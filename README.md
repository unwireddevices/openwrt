# openwrt
OpenWRT patches for Unwired One board

Patches were tested with OpenWRT 14.07 r47068. To download it, use *svn co -r 47068 svn://svn.openwrt.org/openwrt/branches/barrier_breaker openwrt*

*patch -p0 &lt; unwired.patch* — adds Unwired One board to the list of targets. Run *touch target/linux/***/Makefile* after applying it.

*patch -p0 &lt; gpio-irq-728.patch* — GPIO IRQ support by GBert, https://github.com/GBert

*patch -p0 &lt; new_modules.patch* — kernel modules developed by Unwired Devices team

*patch -p0 &lt; new_files.patch* — avahi-daemon and uboot-envtools configuration files

*patch -p0 &lt; compile-fixes.patch* — fix some compilation errors by updating package versions

*patch -p0 &lt; mjpg-enable.patch* — enable mjpg_streamer service by default

*patch -p0 &lt; mjpg-nohotplug.patch* — disable mjpg_streamer in /etc/hotplug.d/usb/ (not included in stock firmware)

*patch -p0 &lt; console.patch* — patch to allow to completely disable UART console using bootloader's environment variable (''fw_setenv silent 1'' shell command to set it)

*patch -p0 &lt; opkg.patch* — add Unwired's OpenWRT repository (http://files.black-swift.com/files/openwrt/bbreaker/1.0/packages/) to /etc/opkg.conf

*patch -p0 &lt; vermagic.patch* — set vermagic number with menuconfig instead of automatically generated md5 hash of the kernel config file

*.config* — ready to use OpenWRT Buildroot configuration file

For more details, please visit http://www.unwireddevices.com/wiki
