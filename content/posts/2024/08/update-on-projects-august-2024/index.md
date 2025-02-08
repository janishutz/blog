+++
title = 'Project Updates August 2024'
date = 2024-09-02T07:41:02+02:00
lastmod = 2024-09-02T07:41:02+02:00
draft = false
author = 'Janis Hutz'
tags = [ 'Development' ]
categories = [ 'News' ]
series = [ 'project-updates' ]
series_weight = 5
featuredImage = "/posts/2024/04/upcoming-projects/new-projects.jpg"
+++

Welcome back to your monthly dose of project updates! Last month I barely made any progress on my Software, so I decided not to make a project updates blog post... no, let's not kid ourselves, I simply forgot.

This time, I have some exciting news, as some of my projects have finally been completed.

# MusicPlayer
MusicPlayer has finally been released! You can now subscribe to it on my [store](https://store.janishutz.com/product/com.janishutz.MusicPlayer). 


# New GitHub username & NPM account
I have finally changed my GitHub username to janishutz. So all my projects are now located at (https://github.com/janishutz)[https://github.com/janishutz], but are still accessible at my old username. 

On NPM, you can find my account [here](https://npmjs.com/~janishutz)


# ConductorCalc
ConductorCalc has seen some development over the last two months, but nowhere near as much as I had hoped for. I have hit a road block in designing the UI and UX of it, but especially the UX is what I am very much struggling with. It should feel intuitive to use, but also look sleek, which is quite hard to achieve. Additionally, it has to work on all platforms, which is another thing I will have to really look into some more. Therefore, I have pushed the release date back to October 31, which might turn into January 1, 2025 if I end up having more difficulties along the way.

# New Website
I have started to completely re-design my website, as my current one is now over one year old. Some design choices for that site don't really fit in with my current design philosophy, so I am in the process of reworking my website. I have hit quite a few speed bumps along the way, namely my lack of creativity when it comes to my own websites...

# libreevent
I have finally worked a bit on libreevent again... I know, hardly believable... libreevent now has an NPM package, making installation and updating so much easier, as you can simply upload a new package.json file if you want to update. In the future I will also add an endpoint in settings, where you can update libreevent automatically. Well mostly. You will still have to run `npm i` in the directory you installed libreevent in, as usually, node processes can't call system libraries. libreevent will then download a new package.json to update to the latest version.

# id issues
I have mostly figured out the issues with the Account services, and they are back to working as intended most of the time again. I will probably still rewrite them down the line and give them a new UI, but for the time being, the current version will remain in production.