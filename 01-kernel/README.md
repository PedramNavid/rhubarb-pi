# Kernel Building

While there are pre-built kernel images, and even full Linux distributions
available that make it easy to get started, I found it more helpful to build
the components from scratch. A lot of projects have been largely abandoned and
so features such as a 64-bit kernel may not be easily achievable.

The goal here it to give you the pieces needed to build a distirbution
from scratch, learning something about kernel building along the way.

## The Raspberry Pi Bootloader

Standard Raspberry Pi OS's have two filesystems, a boot partition formatted as
FAT, and a Linux partition formated as ext4. The boot partition contains the
minimum set of files required to bootstrap a Linux operating system.

Further Reading: [The Boot Folder](https://www.raspberrypi.org/documentation/configuration/boot_folder.md) and [Boot Options](https://www.raspberrypi.org/documentation/configuration/config-txt/boot.md), [config.txt](https://www.raspberrypi.org/documentation/configuration/config-txt/README.md)

* `bootcode.bin`: a bootloader which then loads one of the `start*.elf` files. No
longer used on RPI4s
* `start*.elf`: firmware loaded that takes over the boot process including camera
drives and codecs. the `start_cd.elf` file is a cut-down version without support
for hardware blocks like codecs and 3D.
* `fixup*.dat`: linker files, matched with `start*.elf`
* `cmdline.txt`: passes kernel commands to the kernel on boot.
* `config.txt`: configuration paramters for setting up the Pi.
* `ssh.txt`: this file enables ssh on boot
* `kernel8.img`: this is the 64-bit kernel, we'll be building this


## Firmware Files

