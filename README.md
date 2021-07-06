# Hackintosh-Gigabyte-Z390M-GAMING
[OpenCore](https://github.com/acidanthera/OpenCorePkg) bootloader ONLY, Clover not supported (Let it go).

## Gigabyte Z390M GAMING hackintosh w/ OpenCore

Verified working with macOS version 11.4 (20F71) Big Sur and OpenCore 0.7.1.

![System](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/About-System.png?raw=true)

## Important! Important! Important!

**F9m BIOS from GIGABYTE resolves the Apple Watch unlock(SERIAL PORT disabled) issue and provides the CFG Unlock in the BIOS. CFG Unlock is required for this EFI to work properly. Be sure to upgrade F9m.**

**YOU MUST modify SN/UUID/MLB/ROM values in config.plist file. ROM value is the MAC address of your motherboard built-in network card, check it on BIOS settings.**
![SN/UUID/MLB](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/MLBUUIDSN.png?raw=true)

## Updates
2021-07-06 / Version 1.8.5
Verified working with 11.4 (20F71) and Upgrade to OpenCore 0.7.1 / AppleALC 1.6.2 / VirtualSMC 1.2.5 / NVMeFix 1.0.9 / WhateverGreen 1.5.1 / Lilu 1.5.4 / IntelMausi 1.0.7.

2021-06-08 / Version 1.8.4
Verified working with 11.4 (20F71) and Upgrade to OpenCore 0.7.0 / AppleALC 1.6.1 / VirtualSMC 1.2.4 / NVMeFix 1.0.8 / WhateverGreen 1.5.0.

2021-05-04 / Version 1.8.3
Verified working with 11.3.1 (20E241) and Upgrade to OpenCore 0.6.9 / AppleALC 1.6.0 / VirtualSMC 1.2.3 / NVMeFix 1.0.7 / IntelMausi 1.0.6 / Lilu 1.5.3.


> [Changelog History](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/tree/master/Changelog.txt)

Included items table

Items | Last Version | Comments
------------ | ------------- | -------------
[BIOS](https://www.gigabyte.com/Motherboard/Z390-M-GAMING-rev-10/support#support-dl-bios) | F9m | Be sure to upgrade F9m
[OpenCore](https://github.com/acidanthera/OpenCorePkg/releases) | 0.7.1 |
[Lilu](https://github.com/acidanthera/Lilu/releases) | 1.5.4 | 
[AppleALC](https://github.com/acidanthera/AppleALC/releases) | 1.6.2 |
[VirtualSMC](https://github.com/acidanthera/VirtualSMC/releases) | 1.2.5 |
[WhateverGreen](https://github.com/acidanthera/whatevergreen/releases) | 1.5.1 |
[NVMeFix](https://github.com/acidanthera/NVMeFix/releases) | 1.0.9 |
[IntelMausi](https://github.com/acidanthera/IntelMausi/releases) | 1.0.7 |
[RadeonBoost](https://forums.macrumors.com/threads/tired-of-low-geekbench-scores-use-radeonboost.2231366/) | 1.6 |
[AGPMInjector](https://github.com/Pavo-IM/AGPMInjector/releases) | 3.3.4 |


**Important! Important! Important!**

**Highly recommended to make sure to use the latest BIOS 'F9m' version. Download [BIOS](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/tree/master/BIOS/mb_bios_z390-m-gaming_f9m.zip) and flash it for CFG unlocked, SERIAL PORT disabled from BIOS settings.**

## Overview
Installation procedure is quite straightforward, but requires prior knowledge or experience with Hackintoshes. 
It can be simple and complicated at the same time, refer directly to this manual for a better experience.

## Hardware
Components | SKU | Comments
------------ | ------------- | -------------
**CPU** | Intel i7-9700K | 8th/9th-gen both fine (9900K/9700/8700/etc)
**Motherboard** | Gigabyte Z390M Gaming mATX | Not interchangeable with other SKUs
**WiFi Adapter** | BCM943602CDP (4 antennas) | Bluetooth 4.2 (Including NGFF to M.2 Adapter)
**Graphics Card** | Dataland RX 580 8G X-Serial God of War **2304SP** | **DO NOT USE 2048SP VERSION** and **Flash VBIOS ASRock.RX580.8192.180329.rom**
Thunderbolt Card | Gigabyte GC-TITAN RIDGE V1 | Thunderbolt 3 Certified (Need hard-flash, See below for details)
SSD | WD Black SN750 NVMe SSD 1TB | Recommend upgrade to Samsung 970 Pro 1TB
RAM | Corsair Vengeance LPX 128GB (4x32GB) DDR4 X.M.P | Recommend 3200MHz / Better 3600MHz
PSU | Seasonic Focus Plus 650FX | Recommend upgrade to GX850 / GX1000
PC Case | Jonsbo RM2 ATX | Silver
CPU Cooler | Jonsbo TW2-240 | Version 601
SSD Cooler | CRYORIG Frostbit (M.2) | 
Cooling Fan | Noctua NF-F12 PWM | 12cm
Monitors | LED Cinema Display 24 & AOC U2790PQU IPS 4K | ACD 24 including Camera / Mic / Speaker / USB hub
Keyboard & Mouse | Magic Keyboard & Magic Mouse 2 & Magic Trackpad 2 | Prefer to wireless devices
Hard Disk | WD20SPZX 2TB SATA | Backup / Time Machine

**KEY TIPS: Core components (Motherboard / Graphics Card / WiFi Adapter) are CRUCIAL and you HAVE TO follow the instructions above.**

If you want a smooth experience using wireless functionalities such as AirDrop / AirPlay / Sidecar / Handoff / iMessage / Facetime / Contiuenity / etc, only a specific range of wifi card are recommended: **BCM94360CD/BCM943602CDP/BCM943602CS**

## BIOS Settings

Based on F9m version.

#### First setup,

* Save & Exit
	- Load Optimized Defaults, Save & Exit Setup reboot it.

#### Second setup,

* Tweaker
	- Enhanced Multi-Core Performance → **Enabled**
	- Advanced CPU Settings
		- VT-d → **Disabled**
		- No. of CPU Cores Enabled → 8
		- CPU EIST Functions → **Enabled**
		- Race To Halt (RTH) → **Enabled**
		- Voltage Optimization → **Enabled**
		- Intel(R) Speed Shift Technology → **Enabled**
		- Energy Efficient Turbo  → **Enabled**
		- Intel(R) Turbo Boost Technology → **Enabled**
		- C-States Control
			- CPU Enhanced Halt(C1E) → **Enabled**
			- C3 State Support → **Enabled**
			- C6/C7 State Support → **Enabled**
			- C8 State Support → **Enabled**
			- C10 State Support → **Enabled**
			- Package C State limit → **Auto**
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
		- DVMT Total-Gfx Mem → **MAX** (Need reboot)
		- Aperture Size → **256M**
		- Audio Controller → **Enabled**
    	- Above 4G Decoding → **Enabled**
    	- Resize BAR Support → **Disabled**
    	- Super IO Configuration
    		- Serial Port → **Disabled**
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
* Boot
	- CFG Lock → **Disabled**
	- Full Screen LOGO Show → **Disabled**
	- Fast Boot → **Enabled**
		- PS2 Devices Support → **Disabled**
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
* How to hard-flash GC-TITAN RIDGE BIOS with SSDT patched? Ref here [Post 1](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1640#post-2087524) [Post 2](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1624#post-2086862) [Post 3](https://github.com/ameyrupji/thunderbolt-macpro-5-1/blob/master/GC-TitanRidge.md) [Post 4](https://github.com/ameyrupji/thunderbolt-macpro-5-1/blob/master/GC-TitanRidge-CustomFirmware.md) [Post 5](https://elitemacx86.com/threads/how-to-flash-custom-firmware-on-thunderbolt-card-for-macos.685/)
* How to force RGB mode for displays? Ref [here](https://forums.macrumors.com/threads/big-sur-force-rgb-mode-for-displays.2268099/)
* Fixing iMessage and other services with OpenCore Ref [here](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#generate-a-new-serial)


## Not Working / Issues
Please [report and track](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/issues)

## Known Issues
* Big Sur seems to break the support for Apple TV+ DRM. [Ref](https://github.com/acidanthera/bugtracker/issues/1034) [WEG](https://github.com/acidanthera/WhateverGreen/blob/master/Manual/FAQ.Chart.md) [WEG Ref](https://github.com/acidanthera/WhateverGreen/commit/5f6c19243f343719fdbc3e94ec22a9e2b1d16ce9)
* Multiple key press to wake from sleep with bluetooth (known issue with Gigabyte Gaming X or M boards)
* TB3 card removed, 11.3 caused 'Kernel Panic' issue. [Ref](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/issues/63)

## Kexts & Tools
* [AGPMInjector](https://github.com/Pavo-IM/AGPMInjector)
* [USBInjectAll](https://bitbucket.org/RehabMan/os-x-usb-inject-all)
* [OpenCore Configurator](https://mackie100projects.altervista.org/category/opencore-configurator-changelog/)
* [QtOpenCoreConfig](https://github.com/ic005k/QtOpenCoreConfig)
* [OcBinaryData](https://github.com/acidanthera/OcBinaryData)
* [Hackintool](https://github.com/headkaze/Hackintool)
* [PLIST Editor](https://apps.apple.com/us/app/plist-editor/id1157491961?mt=12)
* [HackinDROM](https://hackindrom.zapto.org)


## References
* [https://github.com/iGuan7u/OpenCore-Gigabyte-Z390M-Gaming](https://github.com/iGuan7u/OpenCore-Gigabyte-Z390M-Gaming)
* [https://github.com/wellsgz/Opencore-Gigabyte-Z390M-Gaming-Hackintosh](https://github.com/wellsgz/Opencore-Gigabyte-Z390M-Gaming-Hackintosh)
* [https://github.com/sarkrui/Hackintosh-Z390-Aorus-Pro-9700K-RX580](https://github.com/sarkrui/Hackintosh-Z390-Aorus-Pro-9700K-RX580)
* [https://github.com/blacklizard/gigabyte-z390-aorus-pro-wifi-hackintosh-opencore](https://github.com/blacklizard/gigabyte-z390-aorus-pro-wifi-hackintosh-opencore)
* [https://www.tonymacx86.com/threads/gigabyte-z390-m-gaming-build-with-working-nvram.291193/](https://www.tonymacx86.com/threads/gigabyte-z390-m-gaming-build-with-working-nvram.291193/)
* [https://dortania.github.io/OpenCore-Install-Guide/](https://dortania.github.io/OpenCore-Install-Guide/)
* [https://dortania.github.io/Getting-Started-With-ACPI/](https://dortania.github.io/Getting-Started-With-ACPI/)


## Geekbench 5 Scores
![CPU](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/CPUbench.png?raw=true)
![OpenCL](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/OpenCLbanche.png?raw=true)
![CPU](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/Metalebench.png?raw=true)


## System ScreenShots
![Display](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/Display.png?raw=true)
![RAM](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/RAM.png?raw=true)
![H264H265](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/H264H265.png?raw=true)
![Watch](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/watchunlock.png?raw=true)
![SSDSpeed](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/SSDSpeed.png?raw=true)
![RAWSpeed](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/RAWSpeed.png?raw=true)
![IntelPower](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/intelpower.png?raw=true)
![TB3](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/tb3.png?raw=true)
![TB3PCI](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/tb3pci.png?raw=true)
![SSD](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/SSD.png?raw=true)
![USB](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/USB.png?raw=true)
![RAMSlots](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/RAMSlots.png?raw=true)
![VideoCard](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/VideoCard.png?raw=true)
![Power](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/power.png?raw=true)
![Audio](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/audio.png?raw=true)
![Bluetooth](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/bluetooth.png?raw=true)