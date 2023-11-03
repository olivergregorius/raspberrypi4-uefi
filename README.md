# Raspberry Pi 4 UEFI

This repository provides Tiano UEFI firmware builds for the Raspberry Pi 4.
The firmware is built from the official [EDK II Project](https://github.com/tianocore/edk2).

## How To Run It

1. Create a FAT partition on an SD-card.
2. Download the latest UEFI release archive from the [Releases](https://github.com/olivergregorius/raspberrypi4-uefi/releases).
3. Extract the archive onto the SD-card.
4. Insert the SD-card into the Raspberry Pi 4 and boot it up.

## Changed UEFI Defaults

- Option for using >3 GB of RAM is enabled by default
- ACPI + Devicetree option is selected by default
- Changed boot media enumeration to boot from removable and fixed boot media last (enables booting from PXE first by default)

## Adjust UEFI Settings

To enter the configuration menu, press <kbd>ESC</kbd> right after booting the device up.

## License

- The UEFI firmware (`RPI_EFI.fd`) is licensed under the [EDK II Project license (BSD-2-Clause-Patent)](https://github.com/tianocore/edk2/blob/master/License.txt).
- The files `start4.elf` and `fixup4.dat` are the GPU firmwares. Their licence is described in [LICENCE.broadcom](https://github.com/raspberrypi/firmware/blob/master/boot/LICENCE.broadcom).
- The files `bcm2711-rpi-4-b.dtb`, `gpio-shutdown.dtbo` and `disable-bt.dtbo` are built from Linux kernel sources, released under the [GPL](https://github.com/raspberrypi/firmware/blob/master/boot/COPYING.linux).
