+++
title = 'My Linux Journey (Part 6) - New Design'
date = 2025-06-22T14:33:53+02:00
lastmod = 2025-06-22T14:33:53+02:00
draft = false
author = 'Janis Hutz'
tags = [ 'Linux', 'Development' ]
categories = [ 'Stories' ]
series = [ 'my-linux-journey' ]
series_weight = 6
featuredImage = "/images/linux-journey.jpg"
+++

**Attribution for featured image:**

Thanks to ["malkowitch"](https://www.deviantart.com/malkowitch/gallery) for the feature graphic of this post. No modifications were made. This image is licensed under the [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/) licence


It's not been all that long since my last post in this series. I have since completely revamped the design of my desktop, using a much more flat design. Writing the new elements has taken absolutely *forever*, since I used [Astal](https://aylur.github.io/astal) to write the status bar and notifications. 

# Astal Components
Using Astal, I have spent a bunch of time fighting TypeScript React (and I strongly dislike React) to write a new user interface using GTK. It looks really quite good and the accent colours used throughout the desktop are all extracted from the current wallpaper.

# Theme
I have also spent countless hours modifying a GTK theme I liked to make it my own and replaced the colours in it with colours from the wallpaper and some presets. My apps now all look neat and very similar, giving the whole desktop a much nicer feel. 

# Build Script
You can't just write a Theme and be having to update it regularly by hand. That would be incredibly annoying. No, I have templated all config files that have colours in them and used mustache and JavaScript to generate the config files with the colours from the wallpaper, which I extracted using Color-Thief, a library whose TypeScript variant I maintain. 

If you are interested to see my desktop, you may find my dotfiles [here](https://git.janishutz.com/janishutz/dotfiles), which I have also published now.


# NeoVim changes
My NeoVim config has also seen some major changes, as I added a bunch of new plugins to make my life easier. And I won't be switching to a different editor any time soon, that's for sure! You may find my nvim config [here](https://git.janishutz.com/janishutz/nvim)
