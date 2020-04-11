# platformio-realtek-rtl8710b

PlatformIO development system platform for realtek microcontrollers.

## Requirements

PlatformIO core. Instructions can be found at: https://docs.platformio.org/en/latest/installation.html

## Usage

PlatformIO is well documented in their website at: https://docs.platformio.org/en/latest/index.html. The platform in this repository is custom, not yet confirmed by the PlatformIO developers, so it won't be found in official PlatformIO repositories. Example of 'platformio.ini' configuration when using this platform:

    [env:environment]
    platform = git@github.com:8devices/platformio-realtek-rtl8710b.git
    board = realtek_amebaz_dev01_1v0
    framework = sdk-ameba-amb1

All necessary frameworks and tools will be automatically downloaded once you start developing your applications.

## Framework

The platform uses 'Ameba One SDK' maintained by the developer, Realtek, on GitHub, at: https://github.com/ambiot/amb1_sdk.

## DAP firmware

DAP firmware for the CMSIS-DAP interface located on realtek boards can be downloaded from the [MBED DAPLink project](https://github.com/ARMmbed/DAPLink/releases). Choose any of the archived binaries that after the version number contain the string 'lpc11u35'. One of such binaries is located in the 'dap_firmware' folder. Instructions on installing DAP firmware can be found at the [official realtek website](https://www.amebaiot.com/en/change-dap-firmware/.) or at the realtek documentation in their framework.

For linux users - if 'drag and drop' seems to fail to ugprade firmware, try:

    umount /media/[USER]/CRP\ DISABLD
    sudo dd if=[BINARY] of=/dev/[DEVICE DRIVE] seek=4

## License

* Project code is provided under The MIT License (MIT)
