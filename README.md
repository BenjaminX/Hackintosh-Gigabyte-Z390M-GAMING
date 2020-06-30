# Hackintosh-Gigabyte-Z390M-GAMING
Only for [OpenCore](https://github.com/acidanthera/OpenCorePkg) bootloader, not support Clover.

## Gigabyte Z390M GAMING hackintosh by OpenCore

Verified working with macOS version 10.15.5 (19F2200) Catalina

![System](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/About-System.png?raw=true)

## Important! Important! Important!

**YOU MUST be modify SN/UUID/MLB/ROM in config.plist file.**
![SN/UUID/MLB](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/MLBUUIDSN.png?raw=true)


## Updates log


Date 2020-06-30 / Version 1.3.0

10.15.5 (19F2200) Verified, updates ACPI aml files. Finally fix sleep issues update BIOS file, then flash new BIOS.

Date 2020-06-10 / Version 1.2.0

Gigabyte GC-TITAN RIDGE supported, pls ref how to hard-flash BIOS.

Date 2020-06-03 / Version 1.1.0

Fixed wakeup issues some applications was freeze.

Date 2020-06-03 / Version 1.0.1

Fixed H.264/H.265 supported.

Date 2020-06-02 / Version 1.0.0

Final Release 1.0.0, 10.15.5 (19F101) well done, OC 0.5.9 and Kexts updates.

Date 2020-05-26 / Version 0.0.9

Prepare to release 1.0.0, waiting 10.15.5 version to publish to App Store.

Date 2020-05-24 / Version 0.0.3

Upload some kexts files.

Date 2020-05-14 / Version 0.0.2

Upload mod BIOS based on 'F9g'.

Date 2020-05-11 / Version 0.0.1

First inital commits.


Items | Last Version | Comments
------------ | ------------- | -------------
[BIOS](https://www.gigabyte.com/Motherboard/Z390-M-GAMING-rev-10/support#support-dl-bios) | F9g | [original BIOS](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/raw/master/BIOS/mb_bios_z390-m-gaming_f9g.zip) / [mod BIOS](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/raw/master/BIOS/mod_Z390MG.F9g.zip)
[OpenCore](https://github.com/acidanthera/OpenCorePkg/releases) | 0.5.9 |
[Lilu](https://github.com/acidanthera/Lilu/releases) | 1.4.5 | 
[AppleALC](https://github.com/acidanthera/AppleALC/releases) | 1.5.0 |
[VirtualSMC](https://github.com/acidanthera/VirtualSMC/releases) | 1.1.4 |
[WhateverGreen](https://github.com/acidanthera/whatevergreen/releases) | 1.4.0 |
[NVMeFix](https://github.com/acidanthera/NVMeFix/releases) | 1.0.2 |
[IntelMausi](https://github.com/acidanthera/IntelMausi/releases) | 1.0.3 |


GA Z390M Gaming motherboard, please upgrade [BIOS](https://www.gigabyte.com/Motherboard/Z390-M-GAMING-rev-10/support#support-dl-bios) last version 'F9g'.

**A better way, mod BIOS based on 'F9g' version. Download [mod BIOS](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/tree/master/BIOS) and flash it, Easy to go (unlocked CFG, disabled SERIAL PORT).**

## Overview
Installation is simple, but requires prior knowledge or experience with Hackintoshes. 
It's both simple and complicated, in the easiest way, refer directly to the here.


## Hardware
Components | Brand | Comments
------------ | ------------- | -------------
CPU | Intel i7 9700K | 8th/9th-gen both fine (9900K/9700/8700/etc)
Motherboard | Gigabyte Z390M Gaming mATX | Only support
WiFi Card | BCM943602CDP (4 antennas) | Bluetooth 4.2 (Including NGFF to M.2 Adapter)
Graphic Card | Dataland RX 580 8G X-Serial God of War **2304SP** | **Don't buy 2048SP** / Recommend Sapphire 5700XT
Thunderbolt Card | Gigabyte GC-TITAN RIDGE | Thunderbolt 3 Certified (Need hard-flash)
SSD | Samsung 960 PRO M.2 NVMe 512G | MZ-V6P512BW, Recommend upgrade 1TB
RAM | Corsair Vengeance LPX 64GB (2x32GB) DDR4 | Recommend 3200MHz / Better 3600HMz
Power Case | Seasonic Focus Plus 650FX | Recommend upgrade GX850 / GX1000
Box Case | Jonsbo RM2 ATX | Silver
CPU Cooler | Jonsbo TW2-240 | 601 version
SSD Cooler | CRYORIG Frostbit (M.2) | 
Cooling Fan | Noctua NF-F12 PWM | 12cm
Monitors | Cinema Display 24 & AOC U2790PQU IPS 4K | ACD 24 including Camera / Mic / USB hub / Speaker
Keyboard & Mouse | Magic Keyboard & Magic Mouse 2 & Magic Trackpad 2 | Wireless first
Hard Disk | Seagate BarraCuda 2TB 2.5 Inch | Backup / Time Machine

**The three most important components: MotherBoard / GraphicCard / WiFiCard, it must be respected follow above list.**

If you wanted smoothly using AirDrop / AirPlay / Sidecar / Handoff / iMessage / Facetime / Contiuenity / etc, very important which wifi card you choose. **Strongly recommend buying one of three BCM94360CD/BCM943602CDP/BCM943602CS**


## BIOS Setting

Based on F9g version.

#### First setup,

* Save & Exit
	- Load Optimized Defaults, Save & Exit Setup reboot it.

#### Second setup,

* Tweaker
	- Advanced CPU Settings
		- VT-d → **Disabled**
	- Extreme Memory Profile(X.M.P.) → **Profile 1**
	- Advanced Memory Settings
		- Memory Boot Mode → **Enable Fast Boot**
		- Memory Enhancement Settings → **Enhanced Performance**
* Settings
	- Platform Power
		- Platform Power Management → **Enabled**
			- PEG ASPM → **Enabled**
			- PCH ASPM → **Enabled**
			- DMI ASPM → **Disabled**
		- AC Back → **Always On**
		- ErP → **Disabled**
		- Soft-Off by PWR-BTTN → **Delay 4 Sec.**
		- Power Loading → **Auto**
		- RC6(Render Standby) → **Enabled**
	- IO Ports
		- Initial Display Output → **PCIe 1 Slot**
		- Internal Graphics → **Enabled**
		- DVMT Pre-Allocated → **64M**
		- DVMT Total-Gfx Mem → **MAX**
		- Aperture Size → **256M**
		- Audio Controller → **Enabled**
    	- Above 4G Decoding → **Enabled**
    	- USB Configuration
    		- XHCI Hand-off → **Enabled**
    		- Legacy USB Support → **Enabled**
    		- USB Mass Storage Driver Support → **Enabled**
    		- Port 60/64 Emulation → **Disabled**
    	- Network Stack Configuration
    		- Network Stack → **Disabled**
	- Miscellaneous
		- Intel Platform Trust Technology(PTT) → **Disabled**
		- Software Guard Extensions(SGX) → **Disabled**
* System Info.
	- System Language → **English**
* Boot
	- Full Screen LOGO Show → **Enabled**
	- Fast Boot → **Disabled**
	- Windows 8/10 Features → **Other OS**
	- CSM Support → **Disable**
	- Secure Boot → **Disable** (Secure Boot will be disabled by default, but good to check)

#### For Thunderbolt Card GC-TITAN RIDGE

* Thunderbolt(TM) Configuration
	- Discrete Thunderbolt(TM) Support → **Enabled**
	- TBT Vt-d base security → **Disabled**
   - Thunderbolt Boot Support → **Boot once**
   - Wake From Thunderbolt(TM) Devices → **Enabled**
   - Security Level → **No Security**
   - Discrete Thunderbolt(TM) Configuration
       - Thunderbolt Usb Support → **Enabled**
       - GPIO3 Force Pwr → **Enabled**


## Tips
* How to modify SN/UUID/MLB? (TBD)
* How to enable High-Speed USB port charging? (TBD)
* How to refresh Unsigned BIOS file? (TBD)
* How to hard-flash GC-TITAN RIDGE BIOS and SSDT patched it？Ref here [Post 1](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1640#post-2087524) [Post 2](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1624#post-2086862) [Post 3](https://github.com/ameyrupji/thunderbolt-macpro-5-1/blob/master/GC-TitanRidge.md) [Post 4](https://github.com/ameyrupji/thunderbolt-macpro-5-1/blob/master/GC-TitanRidge-CustomFirmware.md)


## Not Working / Issues
Please [report and track](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/issues)


## Kexts & Tools
* [Lilu](https://github.com/acidanthera/Lilu)
* [AppleALC](https://github.com/acidanthera/AppleALC)
* [VirtualSMC](https://github.com/acidanthera/VirtualSMC)
* [WhateverGreen](https://github.com/acidanthera/WhateverGreen)
* [IntelMausi](https://github.com/acidanthera/IntelMausi)
* [NVMeFix](https://github.com/acidanthera/NVMeFix)
* [USBInjectAll](https://bitbucket.org/RehabMan/os-x-usb-inject-all)
* [OpenCore Configurator](https://mackie100projects.altervista.org/category/opencore-configurator-changelog/)
* [Hackintool](https://github.com/headkaze/Hackintool)
* [PLIST Editor](https://apps.apple.com/us/app/plist-editor/id1157491961?mt=12)
* [Sanity Checker for config.plist](https://opencore.slowgeek.com)
* [FreeDOS](http://www.freedos.org/download/)


## Reference
* [https://github.com/iGuan7u/OpenCore-Gigabyte-Z390M-Gaming](https://github.com/iGuan7u/OpenCore-Gigabyte-Z390M-Gaming)
* [https://github.com/wellsgz/Opencore-Gigabyte-Z390M-Gaming-Hackintosh](https://github.com/wellsgz/Opencore-Gigabyte-Z390M-Gaming-Hackintosh)
* [https://www.tonymacx86.com/threads/gigabyte-z390-m-gaming-build-with-working-nvram.291193/](https://www.tonymacx86.com/threads/gigabyte-z390-m-gaming-build-with-working-nvram.291193/)
* [https://dortania.github.io/OpenCore-Desktop-Guide/](https://dortania.github.io/OpenCore-Desktop-Guide/)
* [https://dortania.github.io/Getting-Started-With-ACPI/](https://dortania.github.io/Getting-Started-With-ACPI/)


## System ScreenShot
![Display](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/Display.png?raw=true)
![H264H265](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/H264H265.png?raw=true)
![SSDSpeed](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/SSDSpeed.png?raw=true)
![IntelPower](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/intelpower.png?raw=true)
![TB3](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/tb3.png?raw=true)
![TB3PCI](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/tb3pci.png?raw=true)



