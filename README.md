# Alpine Linux iso-boot support
Directly boot & install Alpine Linux from Official Alpine Linux Installation Media using grub2 without burning to usb-drive.

# Features
- Filesystems: ext4, fat 
- Provide boot menu
- Supported ISOs: Alpine-Linux-x86_64 standard & extended of 2025/26 (3.23.x & 3.24.x tested).

# Usage
Load provided 'alpine323.img' file along with the main 'initrd' of the installation media via grub loopback module.
If you are using 'https://github.com/Mexit/MultiOS-USB', it is just a few steps:

0. Use MultiOS-USB partition on 'ext4' or 'fat' filesystem.
1. Copy your Alpine-iso files to 'ISOs' directory.
2. Create a directory for 'grub.cfg' files: '/MultiOS-USB/config_priv/Alpine-Linux-sc'
3. Copy 'alpine323.img', 'Alpine-Linux-extented.cfg' & 'Alpine-Linux-standard.cfg' over there.
4. Reboot into 'MultiOS-USB' and start e.g. 'alpine-extended-3.24.2-x86_64.iso [scandev]' entry.
5. Installer will start same way as from usb-stick.
