# Hackintosh-Gigabyte-Z390M-GAMING
[OpenCore](https://github.com/acidanthera/OpenCorePkg) bootloader ONLY, Clover not supported (Let it go).

## Gigabyte Z390M GAMING hackintosh w/ OpenCore

Verified working with macOS version 12.6 RC (21G115) Monterey and OpenCore 0.8.4.

![System](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/About-System.png)

## Important! Important! Important!

**F9 BIOS from GIGABYTE resolves the Apple Watch unlock(SERIAL PORT disabled) issue and provides the CFG Unlock in the BIOS. CFG Unlock is required for this EFI to work properly. Be sure to upgrade F9.**

**YOU MUST modify SN/UUID/MLB/ROM values in config.plist file. ROM value is the MAC address of your motherboard built-in network card, check it on BIOS settings.**
![SN/UUID/MLB](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/MLBUUIDSN.png)

## Updates

2022-09-09 / Version 2.2.9
Verified working with 12.6 RC (21G115) and fix ResizeAppleGpuBars value to -1 disabled.

2022-09-08 / Version 2.2.8
Verified working with 12.5.1 (21G83) and upgrade to OpenCore 0.8.4 / AppleALC 1.7.5

2022-08-10 / Version 2.2.7
Verified working with 12.5 (21G72) and upgrade to OpenCore 0.8.3 / AppleALC 1.7.4 / WhateverGreen 1.6.1 / Lilu 1.6.2


> [Changelog History](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/tree/master/Changelog.txt)

Included items table

Items | Last Version | Comments
------------ | ------------- | -------------
[BIOS](https://www.gigabyte.com/Motherboard/Z390-M-GAMING-rev-10/support#support-dl-bios) | F9 | Be sure to upgrade F9
[OpenCore](https://github.com/acidanthera/OpenCorePkg/releases) | 0.8.4 |
[Lilu](https://github.com/acidanthera/Lilu/releases) | 1.6.2 |
[AppleALC](https://github.com/acidanthera/AppleALC/releases) | 1.7.5 |
[VirtualSMC](https://github.com/acidanthera/VirtualSMC/releases) | 1.3.0 |
[WhateverGreen](https://github.com/acidanthera/whatevergreen/releases) | 1.6.1 |
[NVMeFix](https://github.com/acidanthera/NVMeFix/releases) | 1.1.0 |
[IntelMausi](https://github.com/acidanthera/IntelMausi/releases) | 1.0.7 |

**Important! Important! Important!**

**Highly recommended to make sure to use the latest BIOS 'F9' version. Download [BIOS](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/tree/master/BIOS/mb_bios_z390-m-gaming_f9_new.zip) and flash it for CFG unlocked, SERIAL PORT disabled from BIOS settings.**

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
Thunderbolt Card | ~~Gigabyte GC-TITAN RIDGE V1~~ | ~~Thunderbolt 3 Certified (Need hard-flash, See below for details, V2 better.)~~ 
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

Based on F9 version.

#### First setup,

* Save & Exit
	- Load Optimized Defaults, Save & Exit Setup reboot it.

#### Second setup,

* Tweaker
	- Enhanced Multi-Core Performance → **Enabled**
	- Advanced CPU Settings
		- VT-d → **Disabled** or **Enabled**
		- No. of CPU Cores Enabled → 8
		- CPU EIST Functions → **Auto**
		- Race To Halt (RTH) → **Auto**
		- Voltage Optimization → **Auto**
		- Intel(R) Speed Shift Technology → **Enabled**
		- Energy Efficient Turbo  → **Auto**
		- Intel(R) Turbo Boost Technology → **Enabled**
		- C-States Control → **Auto**
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
		- Aperture Size → **256M**
		- Audio Controller → **Enabled**
    	- Above 4G Decoding → **Enabled**
    	- Resize BAR Support → **Disabled**  **New Feature, very Important**
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
	- Fast Boot → ** Disabled**
	- Windows 8/10 Features → **Other OS**
	- CSM Support → **Disable**
	- Secure Boot → **Disable** (Secure Boot will be disabled by default, but good to check)

	Save & Exit reboot it.
	
#### Third setup,

* Tweaker
	- Extreme Memory Profile(X.M.P.) → **Profile 1**
	- Advanced Memory Settings
		- Memory Boot Mode → **Enable Fast Boot**
		- Memory Enhancement Settings → **Enhanced Performance**
* Settings
	- IO Ports
		- DVMT Total-Gfx Mem → **MAX**



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
* How to Enable Apple VT-D on macOS [here ](https://elitemacx86.com/threads/how-to-enable-apple-vtd-on-macos.868/)


## Not Working / Issues
Please [report and track](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/issues)

## Known Issues
* Big Sur seems to break the support for Apple TV+ DRM. [Ref](https://github.com/acidanthera/bugtracker/issues/1034) [WEG](https://github.com/acidanthera/WhateverGreen/blob/master/Manual/FAQ.Chart.md) [WEG Ref](https://github.com/acidanthera/WhateverGreen/commit/5f6c19243f343719fdbc3e94ec22a9e2b1d16ce9)
* Multiple key press to wake from sleep with bluetooth (known issue with Gigabyte Gaming X or M boards)
* TB3 card removed, 11.3 caused 'Kernel Panic' issue. [Ref](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/issues/63)

## Kexts & Tools
* [USBInjectAll](https://bitbucket.org/RehabMan/os-x-usb-inject-all)
* [USBToolBox](https://github.com/USBToolBox/tool)
* [OpenCore Configurator](https://mackie100projects.altervista.org/category/opencore-configurator-changelog/)
* [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools)
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
![CPU](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/CPUbench.png)
![OpenCL](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/OpenCLbanche.png)
![CPU](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/Metalebench.png)


## System ScreenShots
![Display](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/Display.png)
![RAM](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/RAM.png)
![H264H265](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/H264H265.png)
![Watch](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/watchunlock.png)
![SSDSpeed](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/SSDSpeed.png)
![RAWSpeed](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/RAWSpeed.png)
![IntelPower](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/intelpower.png)
![TB3PCI](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/tb3pci.png)
![SSD](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/SSD.png)
![USB](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/USB.png)
![RAMSlots](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/RAMSlots.png)
![VideoCard](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/VideoCard.png)
![Power](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/power.png)
![Audio](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/audio.png)
![Bluetooth](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/blob/master/Tips/bluetooth.png)
