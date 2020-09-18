# Hackintosh-Gigabyte-Z390M-GAMING
[OpenCore](https://github.com/acidanthera/OpenCorePkg) bootloader ONLY, Clover not supported.

## Gigabyte Z390M GAMING hackintosh w/ OpenCore

Verified working with macOS version 10.15.6 (19G2021) Catalina and OpenCore 0.6.1

![System](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/About-System.png?raw=true)

## Important! Important! Important!

**YOU MUST modify SN/UUID/MLB/ROM values in config.plist file.**
![SN/UUID/MLB](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/MLBUUIDSN.png?raw=true)


## Updates
2020-09-09 / Version 1.6.3 Upgrade to OpenCore 0.6.1 and others Kexts.(Lilu/AppleALC/WhateverGreen/etc)

2020-08-18 / Version 1.6.2
Fixed GFX frequency to 1.2Ghz 

2020-08-14 / Version 1.6.1
Verified working with 10.15.6 (19G2021)

2020-08-04 / Version 1.6.0
Upgrade to OpenCore 0.6.0 and others Kexts.(Lilu/AppleALC/WhateverGreen/etc)

2020-07-05 / Version 1.5.0
Upgrade to 10.15.6 (19G73) and verified, but OpenCore 0.6.0 not release, waiting for 1.6.0.

2020-07-05 / Version 1.4.0
Waiting for OC 0.6.0 release, Optimized some kexts and ACPI aml files.

2020-06-30 / Version 1.3.0
10.15.5 (19F2200) Verified, updates ACPI aml files. Finally, fixed sleep issues, update BIOS file, then flash new BIOS.

2020-06-10 / Version 1.2.0
Gigabyte GC-TITAN RIDGE supported, pls ref how to hard-flash BIOS.

2020-06-03 / Version 1.1.0
Fixed wakeup issues some applications was freeze.

2020-06-03 / Version 1.0.1
Fixed H.264/H.265 supported.

2020-06-02 / Version 1.0.0
Final Release 1.0.0, 10.15.5 (19F101) well done, OC 0.5.9 and Kexts updates.

2020-05-26 / Version 0.0.9
Prepare to release 1.0.0, waiting 10.15.5 version to publish to App Store.

2020-05-24 / Version 0.0.3
Upload some kexts files.

2020-05-14 / Version 0.0.2
Upload mod BIOS based on 'F9g'.

2020-05-11 / Version 0.0.1
First inital commits.


Items | Last Version | Comments
------------ | ------------- | -------------
[BIOS](https://www.gigabyte.com/Motherboard/Z390-M-GAMING-rev-10/support#support-dl-bios) | F9g | [original BIOS](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/raw/master/BIOS/[original]-mb_bios_z390-m-gaming_f9g.zip) / [mod BIOS](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/raw/master/BIOS/mod_Z390MG.F9g.zip)
[OpenCore](https://github.com/acidanthera/OpenCorePkg/releases) | 0.6.1 |
[Lilu](https://github.com/acidanthera/Lilu/releases) | 1.4.7 | 
[AppleALC](https://github.com/acidanthera/AppleALC/releases) | 1.5.2 |
[VirtualSMC](https://github.com/acidanthera/VirtualSMC/releases) | 1.1.6 |
[WhateverGreen](https://github.com/acidanthera/whatevergreen/releases) | 1.4.2 |
[NVMeFix](https://github.com/acidanthera/NVMeFix/releases) | 1.0.3 |
[IntelMausi](https://github.com/acidanthera/IntelMausi/releases) | 1.0.3 |


For GA-Z390M-Gaming motherboard, please upgrade [BIOS](https://www.gigabyte.com/Motherboard/Z390-M-GAMING-rev-10/support#support-dl-bios) to the latest version 'F9g'.

**Highly recommended to try this optimized modded BIOS based on 'F9g' version. Download [mod BIOS](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/tree/master/BIOS) and flash it for extended functionalities (CFG unlocked, SERIAL PORT disabled).**

## Overview
Installation procedure is quite straightforward, but requires prior knowledge or experience with Hackintoshes. 
It can be simple and complicated at the same time, refer directly to this manual for a better experience.


## Hardware
Components | Recommended SKU | Comments
------------ | ------------- | -------------
**CPU** | Intel i7-9700K | 8th/9th-gen both fine (9900K/9700/8700/etc)
**Motherboard** | Gigabyte Z390M Gaming mATX | Not interchangeable with other SKUs
**WiFi Adapter** | BCM943602CDP (4 antennas) | Bluetooth 4.2 (Including NGFF to M.2 Adapter)
**Graphics Card** | Dataland RX 580 8G X-Serial God of War **2304SP** | **DO NOT USE 2048SP VERSION** / Recommend upgrade to Sapphire RX5700XT/RX5500
Thunderbolt Card | Gigabyte GC-TITAN RIDGE | Thunderbolt 3 Certified (Need hard-flash)
SSD | Samsung 960 PRO M.2 NVMe 512G | MZ-V6P512BW, Recommend upgrade to Samsung 970 Pro 1TB
RAM | Corsair Vengeance LPX 64GB (2x32GB) DDR4 X.M.P | Recommend 3200MHz / Better 3600MHz 4x32GB = 128GB
PSU | Seasonic Focus Plus 650FX | Recommend upgrade to GX850 / GX1000
PC Case | Jonsbo RM2 ATX | Silver
CPU Cooler | Jonsbo TW2-240 | Version 601
SSD Cooler | CRYORIG Frostbit (M.2) | 
Cooling Fan | Noctua NF-F12 PWM | 12cm
Monitors | Cinema Display 24 & AOC U2790PQU IPS 4K | ACD 24 including Camera / Mic / USB hub / Speaker
Keyboard & Mouse | Magic Keyboard & Magic Mouse 2 & Magic Trackpad 2 | Prefer wireless
Hard Disk | Seagate BarraCuda 2TB 2.5 Inch | For backup / Time Machine

**IMPORTANT: Core components (Motherboard / Graphics Card / WiFi Adapter) are CRUCIAL and you HAVE TO follow the instructions above.**

If you want a smooth experience using wireless functionalities such as AirDrop / AirPlay / Sidecar / Handoff / iMessage / Facetime / Contiuenity / etc, only a specific range of wifi adapters are recommended: **BCM94360CD/BCM943602CDP/BCM943602CS**


## BIOS Settings

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
		- Platform Power Management → **Disabled**
		- AC Back → **Always On**
		- ErP → **Disabled**
		- Soft-Off by PWR-BTTN → **Delay 4 Sec.**
		- Power Loading → **Enabled**
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
* How to hard-flash GC-TITAN RIDGE BIOS with SSDT patched? Ref here [Post 1](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1640#post-2087524) [Post 2](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1624#post-2086862) [Post 3](https://github.com/ameyrupji/thunderbolt-macpro-5-1/blob/master/GC-TitanRidge.md) [Post 4](https://github.com/ameyrupji/thunderbolt-macpro-5-1/blob/master/GC-TitanRidge-CustomFirmware.md)


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
* [OcBinaryData](https://github.com/acidanthera/OcBinaryData)
* [Hackintool](https://github.com/headkaze/Hackintool)
* [PLIST Editor](https://apps.apple.com/us/app/plist-editor/id1157491961?mt=12)
* [Sanity Checker for config.plist](https://opencore.slowgeek.com)
* [FreeDOS](http://www.freedos.org/download/)


## References
* [https://github.com/iGuan7u/OpenCore-Gigabyte-Z390M-Gaming](https://github.com/iGuan7u/OpenCore-Gigabyte-Z390M-Gaming)
* [https://github.com/wellsgz/Opencore-Gigabyte-Z390M-Gaming-Hackintosh](https://github.com/wellsgz/Opencore-Gigabyte-Z390M-Gaming-Hackintosh)
* [https://github.com/sarkrui/Hackintosh-Z390-Aorus-Pro-9700K-RX580](https://github.com/sarkrui/Hackintosh-Z390-Aorus-Pro-9700K-RX580)
* [https://github.com/blacklizard/gigabyte-z390-aorus-pro-wifi-hackintosh-opencore](https://github.com/blacklizard/gigabyte-z390-aorus-pro-wifi-hackintosh-opencore)
* [https://www.tonymacx86.com/threads/gigabyte-z390-m-gaming-build-with-working-nvram.291193/](https://www.tonymacx86.com/threads/gigabyte-z390-m-gaming-build-with-working-nvram.291193/)
* [https://dortania.github.io/OpenCore-Install-Guide/](https://dortania.github.io/OpenCore-Install-Guide/)
* [https://dortania.github.io/Getting-Started-With-ACPI/](https://dortania.github.io/Getting-Started-With-ACPI/)


## System ScreenShots
![Display](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/Display.png?raw=true)
![RAM](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/RAM.png?raw=true)
![H264H265](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/H264H265.png?raw=true)
![SSDSpeed](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/SSDSpeed.png?raw=true)
![IntelPower](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/intelpower.png?raw=true)
![TB3](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/tb3.png?raw=true)
![TB3PCI](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/tb3pci.png?raw=true)
![SSD](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/SSD.png?raw=true)
![USB](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/USB.png?raw=true)
![RAMSlots](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/RAMSlots.png?raw=true)
![VideoCard](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/VideoCard.png?raw=true)

