# T530 hackintosh
I wanted to try hackintoshing, so I did.
My conclusion is that I don't like MacOS and will not use it.

Interestingly, this EFI folder only works with 1vyrain custom BIOS and not coreboot with Tianocore as its payload.
Thanks to [5T33Z0 for their repo](https://github.com/5T33Z0/Lenovo-T530-Hackintosh-OpenCore)!
I had to change some stuff to make it work with my T530 like changing out the Broadcom WiFi kexts for Intel ones.

# Pre install
- (the config.plist is only for your inspection, you don't need to manually copy it as it's already included in the EFI tarball)
- Extract the .tar to a FAT32 formatted USB drive (preferably USB3).
- Use [macrecovery](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/mac-install-recovery.html) to get a apple recovery folder and copy that to the root of the FAT32 drive aswell.
- Plug in ethernet to the ThinkPad T530 and boot the USB, make sure to reset the NVRAM on first boot (show with space on the OpenCore boot menu) and then select the .DMG option and install as "normal".

# Post install
- Make sure to download OCLP to get the Intel HD4000 graphics to work properly: https://github.com/dortania/OpenCore-Legacy-Patcher/releases
- And download HeliPort to manage your Intel WiFi card: https://github.com/OpenIntelWireless/HeliPort/releases/latest
