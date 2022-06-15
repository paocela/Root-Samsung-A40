# ROOT SAMSUNG A40 STEPS

## Prerequisites

- windows PC
- install ODIN tool
- install samsung A40 USB drivers (https://www.droidthunder.com/download-and-install-latest-samsung-usb-drivers/)
- download firmware from https://samfw.com/firmware/SM-A405FN/NEE/A405FNXXU4CVD1 (files: AP, BL, CP, CSC, ...)

## Steps

1) enable in settings:
	- developer mode (click multiple times `about_phone/software_informations/build_number`)
	- USB debug (`developer_options/`)
	- OEM bootloacker (`developer_options/`)
2) unlock bootloader
   - turn-off
   - press volume up + volume down, then plug into pc with USB cable
   - long press volume up
   - confirm with volume up

3) follow instruction to start phone
4) enable:
	- developer mode
	- USB debug
	- OEM bootloacker (if hidden, connect to wifi)
5) copy AP file into phone download folder
6) overwrite Android software
	- download magisk
	- install magisk using AP as patch file (from download folder)
7) copy `magisk_patched` file from phone to firmware directory
8) use odin (files from firmware folder)
	- open odin
	- BL = add BL file
	- AP = add `magisk_patched` file
	- CP = add CP file
	- CSC = add CSC file
	- turn-off phone and disconnect
	- press volume up + volume down, then plug into pc
	- short press volume up
	- start odin download

9) odin ends
	- force turn-off phone with volume up + volume down + power button (**phone should't start automatically**)
	- when booting with samsung and red text, long press volume up into boot options (if it doesn't work, repeat)
10) boot options
	- perform `wipe data / factory reset`
	- perform `wipe cache partition`
	- do `reboot system now`
11) follow instruction to start phone
12) enable:
	- developer mode
	- USB debug
	- OEM bootloacker (if hidden, connect to wifi)
13) download magisk
14) set-up magisk:
	- if not installed when open, perform `factory reset` in `settings/general_management/reset/factory_reset`
	- open magisk again if needed
	- allow magisk do its thing (rebooting...)
15) download termux and check `su` (need to grant permission from magisk)
