+++
title = 'Arch Linux Development Virtual Machine'
date = 2023-11-28T10:47:31+01:00
lastmod = 2023-11-29T20:42:40+01:00
draft = false
author = 'Janis Hutz'
tags = [ 'Linux', 'Windows', 'Development' ]
categories = [ 'Tutorials' ]
series = [ 'arch-dev-vm' ]
series_weight = 1
lightgallery = true
featuredImage = 'featured-image.png'
+++

**Attribution for featured image:**

Thanks to ["wavering-radiant"](https://www.deviantart.com/wavering-radiant/gallery) for the feature graphic of this post. No modifications were made. This image is licensed under the [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) licence

# Arch Linux Development Virtual Machine

Developing Software on Windows is a massive pain. This is why I have created a guide for beginners that are looking to start learning machine learning and don't have a proper Operating System to do serious ML work. You may, depending on your level of commitment also install as Dual-Boot, but not with this script, as this partitions automatically for a full system wipe. You can also use this script as a starting point for a full install, as it installs all important packages automatically for you. 

The GitHub repository you are going to clone when following this guide is the following: [https://github.com/simplePCBuilding/arch-dev-vm](https://github.com/simplePCBuilding/arch-dev-vm).
It contains all scripts that are executed as part of the installation

# Installation of a VM-Hypervisor
On Windows, if you have the pro-edition, a Hypervisor comes already with the OS, but I don't recommend using Hyper-V and opt for VMWare Workstation or QEMU instead. For this guide we will be using VMWare Workstation Player as it is much easier to use. 

{{< admonition type=failure title="Be careful: Enable VT-x or AMD-V in your BIOS" open=true >}}
Please enable VT-x or AMD-V depending on if you have an Intel or AMD CPU. Failing to do so will not allow you to launch your VM. You can do that by heading into your device's BIOS and enabling it there. You might need to look up how this works on your device, as every BIOS is different.  
{{< /admonition >}}

{{< admonition type=tip title="Tip: Entering the BIOS on your PC / Laptop" open=false >}}
The easiest way to enter the BIOS on Windows is to hold down shift whilst clicking onto "Restart" and then, once it comes up, clicking onto Troubleshoot and then UEFI-Firmware settings and then restart. This will take you straight to the BIOS without having to spam the BIOS access key on boot.
{{< /admonition >}}


With VT-x or AMD-V enabled, it is now time to download and install VMWare Workstation Player from the official website.


# Setting up a VM
To create a new VM, you want to first download the Arch Linux ISO from the [link](https://pkg.adfinis.com/archlinux/iso/latest/). Download the file that says 
`archlinux-x86_64.iso`. 

Now, set up a Virtual Machine, selecting the Arch Linux ISO you have just downloaded

{{< admonition type=tip title="Tip: Setting up a VM in VMWare Workstation Player" open=false >}}
Then, launch VMware workstation, click "New Virtual Machine". Click next on the now opening dialogue. Now select the ISO you have just downloaded and click next. 

Now enter a virtual machine name (like "arch-dev-vm") and select a location for the virtual machine. This should be on your local disk and preferably outside your user folder. Please create a new folder to not clutter up the folder it resides in. For the size, give the VM at least 20 GB, but preferably more, if you can spare it

Now, click next and in the next part, give the virtual machine half the System Memory your PC has. 

To check how much memory your PC has, press Ctrl + Shift + Esc to open up Task Manager and expand it to see more detailed infos and head to the resources tab. There it will tell you under memory how much memory you have left. Head back to the Virtual Machine Setup dialogue and give it at most half of the system memory or, if your OS uses more than half of your memory, subtract the amount currently used by your OS form the total and subtract another 2GB to be on the safe side. 

Next off, you need to select how many CPU cores you want to give it. If you don't expect to do anything outside of the VM on your host OS whilst the VM is running, then you can go ahead and give the VM all the cores available to have maximum performance (recommended). Also ensure that 3D graphics is turned ON!

Now click finish and you're done!
{{< /admonition >}}

{{< admonition type=warning title="Warning: Configuration" open=true >}}
Please ensure that the VM has adequate storage (at least 20 GB) and system memory (at least 2 GB, preferably half your system memory). But do make sure that your host OS can still run fine without the amount of RAM you allocate to the VM.

Additionally, give the VM all the CPU horsepower you can spare, it'll make it much more snappy. I recommend adding as many CPU cores as you have in your system.
{{< /admonition >}}


# Installing
Once the VM is booted, enter these commands to start the installation. Press enter between each of the commands:

{{< admonition type=tip title="Tip: Setting a keyboard layout" open=false >}}
If your keyboard layout isn't US, then you might want to change it.
Run the following command in the terminal of the booted VM:
```bash
ls /usr/share/kbd/keymaps/**/*.map.gz > kb.txt
nano kb.txt
```

This will spit out a list of keymaps. Then to select an appropriate keymap, press Ctrl + x and type only the last part (after the last slash and without the .map.gz) after `loadkeys `, so for example for the default Swiss keyboard layout:
```bash
loadkeys de_CH-latin1
```

{{< /admonition >}}


```bash
pacman -Sy git
git clone https://github.com/simplePCBuilding/arch-dev-vm
cd arch-dev-vm
./install.sh
```

Then follow the on-screen prompts to complete the installation. 



# After the install
After the script has finished running, you may type reboot, and you should end up in the fully set up Arch Linux VM. Press enter to select the user and type the password you entered during installation. You are now greeted by the GNOME desktop environment. This is one of the easiest to use and most polished user interfaces that exists. The next post in this series will go over using the user interface.

A thing you might now want to do is install a so-called AUR-Helper.

{{< admonition type=tip title="Tip: Installing recommended extensions if failed during install" open=false >}}
To use all my recommended extensions in VSCodium, run the `setup-vscodium.sh` script by opening a terminal and typing the following commands:
```bash
cd arch-dev-vm
./setup-vscodium.sh
```
{{< /admonition >}}

{{< admonition type=tip title="Tip: Installing an AUR-Helper" open=false >}}
I personally use YAY (yet another yogurt). You install it by running the following commands in Terminator (press the Windows key and type Terminator):

```bash
cd /tmp
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```
{{< /admonition >}}

# Using the OS
Have a look at the next post in this series
