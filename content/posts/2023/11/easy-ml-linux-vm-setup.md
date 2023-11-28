+++
title = 'Easy ML Linux VM Setup'
date = 2023-11-28T10:47:31+01:00
draft = false
author = 'Janis Hutz'
tags = [ 'Linux', 'Windows', 'Development' ]
categories = [ 'Tutorials' ]
+++

Developing Software on Windows is a massive pain. This is why I have created a guide for beginners that are looking to start learning machine learning and don't have a proper Operating System to do serious ML work. You may, depending on your level of commitment also install as Dual-Boot, but not with this script, as this partitions automatically for a full system wipe. You can also use this script as a starting point for a full install, as it installs all important packages automatically for you. 

# Installation of a VM-Hypervisor
On Windows, if you have the pro-edition, a Hypervisor comes already with the OS, but I don't recommend using Hyper-V and opt for VMWare Workstation or QEMU instead. For this guide we will be using VMWare Workstation Player as it is much easier to use. Before we get started though, please enable VT-x or AMD-V depending on if you have an Intel or AMD CPU. You can do that by heading into your device's BIOS and enabling it there. You might need to look up how this works on your device, as every BIOS is different. If you are unaware of how to get into the BIOS, the easiest way to do this on Windows is by holding down shift whilst clicking onto "Restart" and then, once it comes up, clicking onto Troubleshoot and then UEFI-Firmware settings and then restart. This will take you straight to the BIOS without having to spam the BIOS access key on boot. 

With that setting enabled, it is now time to download and install VMWare Workstation Player from the official website and then following the installation prompts.


# Setting up a VM
To create a new VM, you want to first download the Arch Linux ISO from the [link](https://pkg.adfinis.com/archlinux/iso/latest/). Download the file that says 
`archlinux-x86_64.iso`. Then, launch VMware workstation, click "New Virtual Machine". Click next on the now opening dialogue. Now select the ISO you have just downloaded and click next. 

Now enter a virtual machine name (like "arch-dev-vm") and select a location for the virtual machine. This should be on your local disk and preferably outside your user folder. Please create a new folder to not clutter up the folder it resides in. Now, click next and in the next part, give the virtual machine half the System Memory your PC has. 

To check how much memory your PC has, press Ctrl + Shift + Esc to open up Task Manager and expand it to see more detailed infos and head to the resources tab. There it will tell you under memory how much memory you have left. Head back to the Virtual Machine Setup dialogue and give it at most half of the system memory or, if your OS uses more than half of your memory, subtract the amount currently used by your OS form the total and subtract another 2GB to be on the safe side. 

Next off, you need to select how many CPU cores you want to give it. If you don't expect to do anything outside of the VM on your host OS, then you can go ahead and give the VM all the cores available to have maximum performance (recommended). Also ensure that 3D graphics is turned ON!

Now click finish and you're done!


# Installing
Once the VM is booted, enter these commands to start the installation. Before you do that though, read on below:

```
loadkeys [IDENTIFIER HERE (find it in the output above), usually of form de_CH-latin1, refer to below for more instructions]
pacman-key --init
pacman -Sy git
git clone https://github.com/simplePCBuilding/arch-dev-vm
cd arch-dev-vm
./install.sh
```

Then follow the on-screen prompts to complete the installation. 

## Selecting a Keyboard layout
Run the following command in the terminal of the booted VM:
```
ls /usr/share/kbd/keymaps/**/*.map.gz > kb.txt
nano kb.txt
```

This will spit out a list of keymaps. Then to select an appropriate keymap, type only the last part (after the last slash and without the .map.gz) after `loadkeys `, so for example for the default Swiss keyboard layout:
```
loadkeys de_CH-latin1
```

# After the install
After the script has finished running, you may type reboot, and you should end up in the fully set up Arch Linux VM. You may now log in with the password you selected during installation. You are now greeted by the GNOME desktop environment. This is one of the easiest to use and most polished user interfaces that exists.

A thing you might now want to do is install a so-called AUR-Helper. I personally use YAY (yet another yogurt). You install it by running the following commands in Terminator (press the Windows key and type Terminator):

```
cd /tmp
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```

# Using the OS
Look out for another post soon (tm)