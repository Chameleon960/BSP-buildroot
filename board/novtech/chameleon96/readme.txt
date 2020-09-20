Chameleon96 

Intro
=====


More information about this board can be found here:
https://www.96boards.org/product/chameleon96/


Build
=====

First, load socrates config for buildroot

    make chameleon96_defconfig

Build everything

    make

Following files will be generated in output/images

.
├── boot.vfat
├── rootfs.ext2
├── rootfs.ext4 -> rootfs.ext2
├── rootfs.tar
├── sdcard.img
├── socfpga_chameleon96.dtb
├── u-boot-spl.bin
├── u-boot-spl.bin.crc
├── u-boot.bin
├── u-boot.img
├── uboot-env.bin
├── uboot.img
└── zImage


Creating bootable SD card
=========================

Simply invoke

dd if=output/images/sdcard.img of=/dev/sdX

Where X is your SD card device (not partition)


