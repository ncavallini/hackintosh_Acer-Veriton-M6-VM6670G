# Hackintosh -- OpenCore UEFI Firmware for the Acer Veriton M6 VM6670G
This repo provides an OpenCore 0.6.5-based UEFI firmware for the Acer Veriton M6 VM6670G.
This UEFI was built following the excellent [Dortania OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)

## Hardware Specs
|Piece of Hardware|Type
|--|--|
|CPU| Intel Core i9 10900  
|CPU Code Name| Comet Lake
|CPU Frequecy | 2.80 GHz
|Mainboard| Acer Veriton M660G
|RAM|32 GB (DDR4)
|GPU| NVIDIA Quadro P620
|Ethernet|Intel I219-LM
|Wi-Fi|Intel(R) Wi-Fi 6 AX201
|SSD|1TB
|HDD| 2TB

## Disclaimer
This is for teaching and personal use **only**. Hackintoshes violate the macOS EULA. **DO NOT** rely on Hackintoshes for your work! They may broke at any time (as a result of an update which broke compatibility, etc.). 

## HOW-TO
For a complete tutorial, please refer to the [Dortania OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)

 1. Format a >=4 GB USB-stick in FAT-32 using the GPT partition table (use [Rufus](http://rufus.ie) for that)
 2. Delete the files that Rufus put in there
 3. In the root directory, create a folder named `com.apple.recovery.boot`
 4. [Download the OS X version of your choice](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/winblows-install.html#downloading-macos)
 5. Copy both `BaseSystem.dmg` and `BaseSystem.chunklist` in the `com.apple.recovery.boot` directory
 6. Copy the `EFI` folder you downloaded from this repo in the root of your USB-stick
 7. Your USB-stick's directory structure should now look like this
 

    ``` *USB-Letter*
    ├───EFI
    │   ├───BOOT
    │   └───OC
    │       ├───ACPI
    │       ├───Bootstrap
    │       ├───Drivers
    │       ├───Kexts
    │       │   ├───SMCSuperIO.kext
    │       │   │   └───Contents
    │       │   │       └───MacOS
    │       │   ├───VirtualSMC.kext
    │       │   │   └───Contents
    │       │   │       ├───MacOS
    │       │   │       └───Resources
    │       │   │           └───VirtualSMCSDK
    │       │   ├───SMCProcessor.kext
    │       │   │   └───Contents
    │       │   │       └───MacOS
    │       │   ├───Lilu.kext
    │       │   │   └───Contents
    │       │   │       ├───MacOS
    │       │   │       └───Resources
    │       │   │           ├───Library
    │       │   │           │   └───wrappers
    │       │   │           └───Headers
    │       │   │               └───capstone
    │       │   ├───WhateverGreen.kext
    │       │   │   └───Contents
    │       │   │       └───MacOS
    │       │   ├───AppleALC.kext
    │       │   │   └───Contents
    │       │   │       └───MacOS
    │       │   ├───IntelMausi.kext
    │       │   │   └───Contents
    │       │   │       └───MacOS
    │       │   └───AirportItlwm.kext
    │       │       └───Contents
    │       │           └───MacOS
    │       ├───Resources
    │       │   ├───Audio
    │       │   ├───Font
    │       │   ├───Image
    │       │   └───Label
    │       └───Tools
    └───com.apple.recovery.boot 
    ```

8. Make sure SATA-Mode is set to `AHCI` in your BIOS 
9. Your good to boot from the stick

**Please note that I don't offer technical support for this! Please refer to the guide above or google your problem!**  
