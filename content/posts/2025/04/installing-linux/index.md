+++
title = 'Installing Linux'
date = 2025-04-17T14:56:34+02:00
lastmod = 2025-04-17T14:56:34+02:00
draft = true
author = 'Janis Hutz'
tags = [ 'Linux', 'Windows' ]
categories = [ 'Guides', 'Tutorials' ]
series = [ 'linux-beginner-guide' ]
series_weight = 2
featuredImage = ""
+++

With End Of Life of Windows looming, you will have at least four options (sorted in order of best experience):
- Switch to Linux (what will be covered here)
- Buy a new device that can run Windows 11 (or update to it if you are eligible)
- Run Windows 11 with hacky workaround on your current hardware
- Continue using Windows 10 after EOL

Security and stability-wise, only two of these options are a true option. You probably have not downgraded to Windows 11 yet because either your device doesn't support it or you don't like it. You might think that you will have to bite the bullet and just buy a new Windows 11-ready device. But there is a better option.

Tux will approve of that way. And you certainly don't want to make a penguin unhappy. 

# Getting prepared
I have previously done a [series](https://blog.janishutz.com/series/arch-dev-vm/) on some Linux concepts, so reading them will be a good idea if you want to learn more about Linux.

Before switching to Linux, you will need to be aware of a few things and make a few choices. Let's start with the things you need to be aware of:
- Linux is *not* Windows and it will ***never*** be.
- Some software *simply doesn't work*. Examples: Micro$oft Office (recent ones), Adobe Suite. There are though always alternatives for these pieces of software, most of which are even free to use and you may always use the online version of Office.
- Some very specialized hardware might not work fully
- You will have a great time updating


{{< admonition type=tip title="Info: Installing Software on Linux" open=false >}}
Installing Software on Linux does work very differently compared to Windows. It *is* possible to download a piece of software from the website of the project, but it is not recommended. Usually, when you download a project from the project's website, you will get what is known as an AppImage, which is similar to an Installer on Windows. The problem with this is that you won't get the advantages of installing with the *package manager*, which will allow you to update your ***entire*** system in one go.

Most beginner friendly distros include a *software store*, which is similar to the App Stores on your phone, just (most) software is free of charge and also does not have any ads or the like and does not collect any personal data.

When installing using the package manager, you get the advantage that the software works better with your system and you get automatic updates and are updated together with the rest of the system.
{{< /admonition >}}

With that out of the way, let's see what kind of choices you will have to make before switching:
- Choose a User Interface you'd like to use. Below you can find a (non-exhaustive) table of user interfaces I recommend. 
- Based on that user interface, choose a distribution from the same table you found all user interfaces in
- Choose a web-browser and software you want to use (you can do that later too, after you installed, as that can easily be changed)


# Choosing Desktop & Distro
Below you can find a table of various user interfaces and distros that are ideal for them

| Desktop | Design philosophy | Advantages | Disadvantages | Beginner Distro | Challenge Distro |
----------|-------------------|------------|---------------|-----------------|------------------|
| GNOME   | Sleek, Easy to use | Easy, Sleek, Stable, Good defaults, a lot of native apps | Not very customizable, heavy | EndeavourOS | Arch Linux / Fedora / Debian |
| KDE Plasma | Customizability | Easy, very customizable, Good defaults, lots of native apps | Not as sleek as gnome, very heavy | EndeavourOS | Arch Linux / Debian |
| Cinnamon | Windows-like | Easy, Stable, Good defaults, customizable | heavy, some people find it ugly | Linux Mint | Arch Linux / Debian |
| Xfce     | Light weight | Light weight, Stable, customizable | can be a bit difficult, looks awful without modifications, harder to use | EndeavourOS / Linux Mint | Arch Linux / Debian |

These are the main desktops I would recommend. Be aware that you will be able to customize them and make sure to look at the latest versions. Xfce especially can look ugly. Look at how it looks in EndeavourOS, that does look quite nice.

For all people who want to say "*Why did you not include distro X or desktop Y*", hear me out: Giving people to much choice can be detrimental. If you still want to discuss, head to the [GitHub repo of the blog](https://github.com/janishutz/blog) and open an issue. For people who want to see more options, check out [this Arch Linux Wiki entry](https://wiki.archlinux.org/title/Desktop_environment).


# Setting up
Once you have chosen your distribution and desktop, go to the download page of the distribution you want and download it. You can find downloads for EndeavourOS [here](https://endeavouros.com) (be aware it is aimed towards *slightly* more tech-savvy people), for Linux Mint [here](https://linuxmint.com/download.php), for Fedora [here](https://fedoraproject.org/workstation/download), for Debian [here](https://debian.org/download), for Arch [here](https://archlinux.org/download).

Now, you will need to find an empty USB drive (or empty a USB drive) and download [Rufus](https://rufus.ie/). Rufus is a tool to write a .iso file to a USB drive. After the download is complete, open up Rufus and select the Device. Rufus should only show one option, but do make sure the drive you want to use is selected and that nothing important is on it. *THIS STEP WILL ERASE ALL DATA ON THAT DRIVE*. Then pick the just downloaded ISO file in the input field just below. Then, once you have done that, simply click "Start" below and wait for the process to finish.

Congratulations, you are now the proud owner of one Linux installer!

# Rebooting & Installing
Now, we want to actually install the operating system. Here are a few notes of caution:
- Installing Linux with a full drive wipe (or following the [installation guide of Arch Linux](https://wiki.archlinux.org/title/Installation_Guide)) will delete all data on your current Windows drive, so make sure you have copied all the data you want to retain to somewhere safe. 
- This guide aims to be as accurate as possible, but it can't cover all aspects, so better check online if you are unsure. AI is your friend here, believe it or not. I will take no responsibility if you loose data here.

With that out of the way, let's get started. In Windows, open the start menu, and hold down shift while you click "Restart". Then in the menu that appears, click "Troubleshoot" > "Advanced Options" > "UEFI Firmware Settings"
