+++
title = 'Change your Linux Desktop Environment'
date = 2023-12-02T15:30:11+01:00
lastmod = 2023-12-03T14:03:11+01:00
draft = false
author = 'Janis Hutz'
tags = [ 'Linux' ]
categories = [ 'Guides' ]
series = [ 'arch-dev-vm' ]
series_weight = 4
featuredImage = "featured-image.png"
+++

After using Linux for some time, you might start getting bored by your current user interface, and you might want to switch to something new and exciting. This is exactly where this guide comes in

# What is a desktop environment?
On Linux, a Desktop Environment is an assortment of Software that contains everything that is important for a complete user interface.

{{< admonition type=info title="Info: Components of a Desktop Environment" open=true >}}
All major Linux desktop environments consist of the following components:

- A Window Manager or WM, which is the software that allows you to move, resize, minimize, etc. your windows
- A settings manager, which is the software that allows you to adjust settings using a graphical user interface
- A Display Manager or DM, sometimes also known as Login Manager. This software allows you to log into your user interface.
- A screen locker, a software that allows you to lock your screen.
- A notification daemon, used to create desktop notifications
- An application launcher, a software that allows you to graphically launch software
- A logout dialogue or logout manager, allows you to log out, shut down or reboot your system or suspend it
- An Authentication agent, used to authenticate apps, like the UAC interface in Windows.
- Various control software (Bluetooth, audio, screen, media control, power management, ...)
- An assortment of software, like a file manager, camera software, web browser, etc
{{< /admonition >}}

You can however also use only certain parts of a desktop environment, like the WM, which is something many advanced Linux users do. These WMs however are usually not part of a desktop environment but are standalone. 

The most famous Window Managers are `i3wm`, `bspwm` and `awesome`, but there are numerous amazing Window Managers. I personally use `Hyprland` on both my Laptop and PC.

# Changing the desktop environment
On Linux, you can have as many desktop environments on a single system as you like. In your DM, you can choose which desktop to launch. How you choose depends on the specific DM, but on GDM, it's the small gear symbol in the bottom right corner after selecting the user, on SDDM, there is a dropdown somewhere, as there is on LightDM. 

You can install a new desktop environment using your package manager. The desktop environments are usually so-called package groups, so you're going to be prompted to select what packages you want to install. 

So, for example, if you want to install the `Xfce` desktop environment, you can do this by running:
```bash
yay -S xfce4
```

or if you don't have `yay`
```bash
sudo pacman -S xfce4
```

Then, when prompted to select which packages to install, just press enter for now, or you can go ahead and look up what each package does exactly.


# Desktop Environments and WMs to try out
There are numerous very interesting DEs and WMs to try out, here's a list. In square brackets you can find the package / group name to install.

## Desktop Environments
- GNOME: Super polished, very user-friendly [gnome]
- KDE: Very customizable, polished [plasma]
- Xfce: Polished, incredibly stable, highly customizable (through config files), very lightweight [xfce4]
- Cinnamon: Windows-Like, somewhat customizable [cinnamon]
- (Cosmic: Once there is a stable release, it's going to be tiling-wm like, customizable, superfast and lightweight [cosmic-epoch-git]{AUR}. Only install and use if you know what you are doing!)

## Window Managers
- i3wm [i3-wm]
- Sway [sway]
- bspwm [bspwm]
- awesome [awesome]
- Hyprland [hyprland]
