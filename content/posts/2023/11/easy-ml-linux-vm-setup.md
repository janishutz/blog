+++
title = 'Easy ML Linux VM Setup'
date = 2023-11-26T10:47:31+01:00
draft = true
author = 'Janis Hutz'
tags = [ 'Linux', 'Windows', 'Development' ]
categories = [ 'Tutorials' ]
+++

Developing Software on Windows is a massive pain. This is why I have created a guide for beginners that are looking to start learning machine learning and don't have a proper Operating System to do serious ML work. You may, depending on your level of commitment also install this OS as it is as Dual-Boot, I will run you through doing that down below. 

# Installation of a VM-Hypervisor
*If you want to install this as a Dual-Boot setup, you may skip ahead*

On Windows, if you have the pro-edition, a Hypervisor comes already with the OS, but I don't recommend using Hyper-V and opt for VMWare Workstation or QEMU instead. For this guide we will be using VMWare Workstation Player as it is much easier to use. Before we get started though, please enable VT-x or AMD-V depending on if you have an Intel or AMD CPU. You can do that by heading into your device's BIOS and enabling it there. You might need to look up how this works on your device, as every BIOS is different. If you are unaware of how to get into the BIOS, the easiest way to do this on Windows is by holding down shift whilst clicking onto "Restart" and then, once it comes up, clicking onto Troubleshoot and then UEFI-Firmware settings and then restart. This will take you straight to the BIOS without having to spam the BIOS access key on boot. 

With that setting enabled, it is now time to download and install VMWare Workstation Player from the official website and then following the installation prompts.
