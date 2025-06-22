+++
title = 'Project Updates June 2025'
date = 2025-06-30T12:23:34+02:00
lastmod = 2025-06-30T12:23:34+02:00
draft = true
author = 'Janis Hutz'
tags = [ 'Development' ]
categories = [ 'News' ]
series = [ 'project-updates' ]
series_weight = 8
featuredImage = "/posts/2024/04/upcoming-projects/new-projects.jpg"
+++

It's been a while since my last Project Updates blog post, as I have not been able to work on projects all too much lately and I didn't really have the motivation to sit down for hours on end figuring out how to best do things whilst also having to juggle university-related tasks. 

Since I have a bit more time now that we have to prepare for the exams, I have spent much more time working on projects again. This ranges from concrete plans for ConductorCalc (finally) to complete rewrites of older software.

# Website
This project's been ongoing for quite some time, but this is the first time that I acknowledge it publicly. I am working on a complete redesign of my website. It is in the late stages of development, only some minor design tweaks are required and I still need to take quite a few screenshots. Expect the website to go live by mid-July, if not earlier. For the meantime, you may check out the [beta site](https://beta.janishutz.com) and report any errors / abnormalities / suggestions to me via my [support page](https://support.janishutz.com)


# Account Services
My Account services have caused some issues in the past. Now, many things don't work as I want them to do and I also needed to redesign them, so I decided to also completely scrap the backend and start afresh. This is currently ongoing and isn't finished yet and likely won't be for quite some time still.


# ConductorCalc
Again, I have underestimated the amount of work still required, so I will have to push back the release date by yet another couple of months to likely the end of 2025. This was partly caused by the need to rewrite the account services to accommodate long login sessions, but also by some delays that happened in the development pipeline.

What I can report that I have made progress on is the design. I have started to re-organize the UI, which will also involve some major rewrite of the UI to make it more flexible and adaptive. This wouldn't have strictly been necessary, but the new design language looks better and is easier to maintain, as I now have lots of reusable, easily configurable components that make building the UI much easier. I was also considering going with Flutter, which has not been ruled out completely as it does seem to be a really good option - albeit with two major downsides: The accounts SDK has to be translated to dart and I have never before written anything using Dart and Flutter.


# BiogasControllerApp
I dug up my oldest public project and have completely reworked it, giving it both a completely new, fully documented backend as well as a fresh look using KivyMD instead of Kivy, which gives me access to Material Design and theming. This projects will likely *not* be useful to you, except you attend the school I used to attend and have picked the subject "Enatech" there. Anyway, here's a [link](https://github.com/janishutz/BiogasControllerApp)
