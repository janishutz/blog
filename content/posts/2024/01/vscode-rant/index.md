+++
title = 'VSCode Rant'
date = 2024-01-21T07:23:13+01:00
lastmod = 2024-01-21T07:23:13+01:00
draft = false
author = 'Janis Hutz'
tags = [ 'Linux', 'Windows', 'macOS', 'Development' ]
categories = [ 'Rants' ]
series = []
series_weight = 1
featuredImage = "cover.jpg"
+++

# VSCode and its requirements to have an official build by Microsoft to use certain extensions

Recently, whilst starting to learn to do ML stuff, I noticed that I didn't get any code suggestions for Python in VSCodium, which is a tracker-less build of VSCode. As Visual Studio Code is open source, it should therefore be possible to build your own version of the software and being able to use it however you like to. At least this is what the MIT license would imply, under which VSCode is licensed. But as Micro$oft is Micro$oft, they had to have their strings attached and make all FOSS builds of VSCode basically worthless as they are excluded from the extensions store by default. Yes, there are workarounds which do work, but some Extensions made my Micro$oft have checks in them that prevent it from running in unofficial builds.

This has forced me to download a second IDE, just for Python, as it just wouldn't work. Thanks Micro$oft!