# Hackintosh-Gigabyte-Z390M-GAMING
Only for [OpenCore](https://github.com/acidanthera/OpenCorePkg) bootloader, not support Clover.

## Gigabyte Z390M GAMING hackintosh by OpenCore

Verified working with macOS version 10.15.4 (19E287) Catalina

![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)

## Updates log

Date 2020-05-14 / Version 0.0.2

Upload mod BIOS based on 'F9g'.

Date 2020-05-11 / Version 0.0.1

First inital commits.


Items | Last Version | Comments
------------ | ------------- | -------------
[BIOS](https://www.gigabyte.com/Motherboard/Z390-M-GAMING-rev-10/support#support-dl-bios) | F9g | [original BIOS](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/raw/master/BIOS/mb_bios_z390-m-gaming_f9g.zip) / [mod BIOS](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/raw/master/BIOS/modBIOS_Z390M_Gaming.rom.zip)
[OpenCore](https://github.com/acidanthera/OpenCorePkg/releases) | 0.5.8 | 0.5.9 beta
[Lilu](https://github.com/acidanthera/Lilu/releases) | 1.4.4 | 
[AppleALC](https://github.com/acidanthera/AppleALC/releases) | 1.4.9 |
[VirtualSMC](https://github.com/acidanthera/VirtualSMC/releases) | 1.1.3 |
[WhateverGreen](https://github.com/acidanthera/whatevergreen/releases) | 1.3.9 |
[NVMeFix](https://github.com/acidanthera/NVMeFix/releases) | 1.0.2 |
[IntelMausi](https://github.com/acidanthera/IntelMausi/releases) | 1.0.2 | 1.0.3 beta

GA Z390M Gaming motherboard, please upgrade [BIOS](https://www.gigabyte.com/Motherboard/Z390-M-GAMING-rev-10/support#support-dl-bios) last version 'F9g'.

**A better way, mod BIOS based on 'F9g' version. Download [mod BIOS](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/tree/master/BIOS) and flash it, Easy to go (unlocked CFG, disabled SERIAL PORT and modified startup logo).**

## Overview
Installation is simple, but requires prior knowledge or experience with Hackintoshes. 
It's both simple and complicated, in the easiest way, refer directly to the here.


## Hardware
Components | Brand | Comments
------------ | ------------- | -------------
CPU | Intel i7 9700K/9900K | 8th/9th-gen both fine (9900/9700/8700/etc)
Motherboard | Gigabyte Z390M Gaming mATX | Only support
WiFi Card | BCM943602CDP (4 antennas) | Bluetooth 4.2 (Including mini PCI-E Adapter)
Graphic Card | Dataland RX 580 8G X-Serial God of War **2304SP** | **Don't buy 2048SP** / Recommend Sapphire 5700XT
Thunderbolt Card | Gigabyte GC-TITAN RIDGE | Thunderbolt 3 Certified
SSD | Samsung 960 PRO M.2 NVMe 512G | MZ-V6P512BW
Memory | Corsair Vengeance LPX 64GB (2x32GB) DDR4 | Recommend 3200MHz / Better 3600HMz
Power Case | Seasonic Focus Plus 650FX | Recommend upgrade GX850 / GX1000
Box Case | Jonsbo RM2 ATX | Silver
CPU Cooler | Jonsbo TW2-240 | 601 version
Cooling Fan | Noctua NF-F12 PWM | 12cm
Monitors | Cinema Display 24 & AOC U2790PQU IPS 4K | ACD 24 including Camera / Mic / USB hub / Speaker
Keyboard & Mouse | Magic Keyboard 2 & Magic Mouse 2 | Wireless first
Hard Disk | Seagate BarraCuda 2TB 2.5 Inch | Backup / Time Machine

**The three most important components: MotherBoard / GraphicCard / WiFiCard, it must be respected follow above list.**

If you wanted smoothly using AirDrop / AirPlay / Sidecar / Handoff / iMessage / Facetime / etc, very important which wifi card you choose. **Strongly recommend buying one of three BCM94360CD/BCM943602CDP/BCM943602CS**


## BIOS Settings
Ref from [tonymacx86](https://www.tonymacx86.com/threads/success-jbarnettes-build-gigabyte-z390-m-gaming-i9-9900k-sapphire-rx-vega-64-8gb-32gb-ram-macos-10-14-3-w-usb3-working.273381/) post thread.

* Save & Exit
    - Load Optimized Defaults then make (or confirm) the following settings -- important settings in **bold**:
* M.I.T.
    - Extreme Memory Profile (X.M.P.) → **Profile 1**
* BIOS
    - Windows 8/10 Features → **Other OS**
    - CSM Support → **Disable**
    - Secure Boot → **Disable** (Secure Boot will be disabled by default, but good to check)
* Peripherals
    - Initial Display Output → PCIe Slot 1. If your discrete graphics card is in Slot 2, change this appropriately.
    - Intel Platform Trust Technology (PTT) → **Disabled**
    - Thunderbolt(TM) Configuration
        - TBT Vt-d Base Security → **Disabled**
        - Thunderbolt Boot Support → **Disabled**
        - Security Level → **No Security**
        - Discrete Thunderbolt Configuration
        	- Thunderbolt USB Support → **Enabled**
        	- GPIO3 Force Pwr → **Enabled**
    - USB Configuration
        - Legacy USB Support → **Enabled**
        - XHCI Hand-off → **Enabled**
    - Network Stack Configuration
        - Network Stack → **Disabled**
* Chipset
    - Vt-d → **Disabled**
    - Internal Graphics → **Enabled**
    - DVMT Pre-Alloc → 64M
    - DVMT Total Gfx Mem → 256M
    - Audio Controller → **Enabled**
    - Above 4G Decoding → **Enabled**
* Power
    - ErP → **Disabled**
    - RC6 (Render Standby) → **Enabled**


## Tips
* How to reconfig USB ports? (TBD)
* How to modify SN/UUID/MLB? (TBD)
* How to enable High-Speed USB port charging? (TBD)
* How to config GC-TITAN RIDGE Thunderbolt 3? (TBD)


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
* [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator)
* [Hackintool](https://github.com/headkaze/Hackintool)
* [PLIST Editor](https://apps.apple.com/us/app/plist-editor/id1157491961?mt=12)


## Reference
* [https://github.com/iGuan7u/OpenCore-Gigabyte-Z390M-Gaming](https://github.com/iGuan7u/OpenCore-Gigabyte-Z390M-Gaming)
* [https://github.com/wellsgz/Opencore-Gigabyte-Z390M-Gaming-Hackintosh](https://github.com/wellsgz/Opencore-Gigabyte-Z390M-Gaming-Hackintosh)



