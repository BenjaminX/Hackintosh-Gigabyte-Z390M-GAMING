# Hackintosh-Gigabyte-Z390M-GAMING
Only for [OpenCore](https://github.com/acidanthera/OpenCorePkg) bootloader by 0.5.8 version


## Gigabyte Z390M GAMING hackintosh by OpenCore

Verified working with 10.15.4 (19E287) Catalina

macOS version
![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)


## Overview
Installation is simple and requires no prior knowledge or experience with Hackintoshes.


## Hardware List
Components | Brand | Comments
------------ | ------------- | -------------
CPU | Intel i7 9700K | 8th/9th-gen
MotherBoard | Gigabyte Z390M Gaming mATX | Support only
Memory | Corsair Vengeance LPX 64GB (2x32GB) DDR4 | Recommend 3200MHz / Better 3600HMz
GraphicCard | Dataland RX580 2304SP 8G | Don't buy 2048SP
HardDisk (SSD) | Samsung 960 PRO M.2 NVMe 512G | MZ-V6P512BW
WiFiCard | BCM943602CDP | Bluetooth 4.2 (Including mini PCI-E Adapter)
Power | Seasonic Focus Plus 650FX | Full-Modular / 80+ Gold
Case | Jonsbo RM2 ATX | Silver
CPU Cooler | Jonsbo TW2-240 | 601 version
Fan | Noctua NF-F12 PWM | 12cm
Keyboard & Mouse | Magic Keyboard 2 & Mouse 2
Monitors | LED Cinema Display 24 & AOC U2790PQU IPS 4K

Z390M Gaming please upgrade [BIOS](https://www.gigabyte.com/Motherboard/Z390-M-GAMING-rev-10/support#support-dl-bios) last version to 'f9g'.

If you wanted smoothly using AirDrop / AirPlay / Sidecar / etc, important these WiFi Card. Recommended to buy BCM94360CD/BCM943602CDP/BCM943602CS first.

## BIOS Settings
Comes from [tonymacx86](https://www.tonymacx86.com/threads/success-jbarnettes-build-gigabyte-z390-m-gaming-i9-9900k-sapphire-rx-vega-64-8gb-32gb-ram-macos-10-14-3-w-usb3-working.273381/).

- Save & Exit
    - Load Optimized Defaults then make (or confirm) the following settings -- important settings in **bold**:
- M.I.T.
    - Extreme Memory Profile (X.M.P.) → **Profile 1**
- BIOS
    - Windows 8/10 Features → **Other OS**
    - CSM Support → **Disable**
        - Secure Boot will be disabled by default, but good to check
- Peripherals
    - Initial Display Output → PCIe Slot 1. If your discrete graphics card is in Slot 2, change this appropriately.
    - Intel Platform Trust Technology (PTT) → Disabled
    - Thunderbolt(TM) Configuration
        - TBT Vt-d Base Security → **Disabled**
        - Thunderbolt Boot Support → **Disabled**
        - Security Level → **No Security**
    - USB Configuration
        - Legacy USB Support → Enabled
        - XHCI Hand-off → **Enabled**
    - Network Stack Configuration
        - Network Stack → **Disabled**
- Chipset
    - Vt-d → **Disabled**
    - Internal Graphics → **Enabled**
    - DVMT Pre-Alloc → 64M
    - DVMT Total Gfx Mem → 256M
    - Audio Controller → **Enabled**
    - Above 4G Decoding → **Enabled**
- Power
    - ErP → Disabled
    - RC6 (Render Standby) → Enabled


## Tips
* How to unlock CFG?
* How to change BIOS loading logo image?
* How to reconfig USB ports?
* How to enable & config TB3?


## Not Working/Issues
Please [report and track](https://github.com/BenjaminX/Hackintosh-Gigabyte-Z390M-GAMING/issues).


## Ref
* [https://github.com/iGuan7u/OpenCore-Gigabyte-Z390M-Gaming](https://github.com/iGuan7u/OpenCore-Gigabyte-Z390M-Gaming)
* [https://github.com/wellsgz/Opencore-Gigabyte-Z390M-Gaming-Hackintosh](https://github.com/wellsgz/Opencore-Gigabyte-Z390M-Gaming-Hackintosh)


## Kexts
* [Lilu](https://github.com/acidanthera/Lilu)
* [AppleALC](https://github.com/acidanthera/AppleALC)
* [VirtualSMC](https://github.com/acidanthera/VirtualSMC)
* [WhateverGreen](https://github.com/acidanthera/WhateverGreen)
* [IntelMausi](https://github.com/acidanthera/IntelMausi)
* [USBInjectAll](https://bitbucket.org/RehabMan/os-x-usb-inject-all)
* [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/)





