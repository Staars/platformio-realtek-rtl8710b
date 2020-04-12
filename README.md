# platformio-realtek-ameba

This repository provides a PlatformIO platform definition for these Realtek 'Ameba' microcontrollers:
- RTL8710AF
- RTL8195AM
- RTL8710BN

See the [official Ameba IoT website](https://www.amebaiot.com), promoting these microcontrollers for IoT applications.

## Requirements

- PlatformIO core ([Installation instructions](https://docs.platformio.org/en/latest/installation.html))

## Usage

PlatformIO is well documented [on their website](https://docs.platformio.org/en/latest/index.html). The platform in this repository is not yet accepted by the PlatformIO developers, so it won't yet be found in official PlatformIO repositories. Example of 'platformio.ini' configuration when using this platform:

    [env:ameba]
    platform = https://github.com/chris-hatton/platformio-realtek-ameba.git#amb1-sdk
    board = realtek-amebaz_dev01_1v0
    framework = sdk-ameba-amb1

All necessary frameworks and tools will be automatically downloaded once you start developing your applications.

## Framework

The platform uses 'Ameba One' SDK maintained by the developer, Realtek, in their [GitHub repository](https://github.com/ambiot/amb1_sdk).

## DAP firmware

DAP firmware for the CMSIS-DAP interface located on Realtek boards can be downloaded from the [MBED DAPLink project](https://github.com/ARMmbed/DAPLink/releases). Choose any of the archived binaries that after the version number contain the string 'lpc11u35'. One of such binaries is located in the 'dap_firmware' folder. Instructions on installing DAP firmware can be found at the [official realtek website](https://www.amebaiot.com/en/change-dap-firmware/.) or at the realtek documentation in their framework.

For Linux users - if 'Drag and Drop' fails to ugprade the firmware, try:

    umount /media/[USER]/CRP\ DISABLD
    sudo dd if=[BINARY] of=/dev/[DEVICE DRIVE] seek=4

## License

* Project code is provided under The MIT License (MIT)
