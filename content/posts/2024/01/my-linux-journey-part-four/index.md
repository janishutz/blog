+++
title = 'My Linux Journey (Part 4) - New WM Setup'
date = 2024-01-07T14:17:56+01:00
lastmod = 2024-01-07T14:17:56+01:00
draft = false
author = 'Janis Hutz'
tags = [ 'Linux' ]
categories = [ 'Stories' ]
series = [ 'my-linux-journey' ]
series_weight = 4
featuredImage = "/images/linux-journey.jpg"
+++

**Attribution for featured image:**

Thanks to ["malkowitch"](https://www.deviantart.com/malkowitch/gallery) for the feature graphic of this post. No modifications were made. This image is licensed under the [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) licence


# Happy new year 2024!
Welcome back in 2024! And with the change to the new year, here is the fourth part of my Linux journey. I have been hard at work over the past few days completely redesigning my user interface. As we have now hit the "today" in this series, this will be the last part for now, but I'll keep you updated on what I', going to be doing on my system. 

# New WM Setup
With my old system suffering from massive bloat which was caused by me being fairly careless when removing packages, it was time to wipe and start afresh. Especially, since my GPU drivers were completely shot and my ROCm install completely messed up. I could have probably salvaged it, but I thought, why not start clean. This time I also decided to go for a separate partition for my home directory, which will be easier to manage when I reinstall in the future, as it is separated. 

## New Waybar config
For Waybar, in terms of contents and organization thereof, it hasn't changed much, as I was quite happy with my config as it was. What changed though was looks, going from a purple-ish to a deep blue, which gives it a fresh new look. I was also considering going down the route of Eww, which I decided against, as I didn't have much time to work on the reinstallation. Trying to migrate to that is on my to-do list for the future. 

## New Hyprland config
The Hyprland config hasn't changed much, except a few colour changes, as I wasn't going to change my keybinds which have since become muscle memory. I solely added a few and changed the background image for my desktop.

## New Rofi config
This is the part which has changed the most. Not only does it have a new set of icons, but also a complete redesign and a lot more features. Additionally, I now have a Rofi-Based power menu.

## New wlogout config
For wlogout, except design, nothing has changed. It, too, went from a purple-ish colour to a dark blue with some green accents.

## New cursors, themes & icons
This change was long overdue. I was still using the Breeze-Dark cursors, which are clearly not the fanciest cursors out there. I switched to the Oreo-Spark-Blue cursors. Whilst I was happy with the Papirus Icon Theme, I switched to the Candy icon theme to have a much fancier file manager look. 

For the themes, I installed Kvantum for the Qt apps and I am using the KvAdaptaDark theme and for GTK apps I am using the Material-Black-Blueberry theme. Whilst they don't look identical, as apps would if they were to use a theme that is ported to GTK and Qt, this is good enough for me. 


# ML setup
I have also started working on the ML setup, as I have bought a new GPU, namely a RX 7800XT to allow me to do ML. Whilst the setup isn't completed just yet, it's so much cleaner, with everything ML-related being inside a docker container.