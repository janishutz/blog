+++
title = 'Webkit Rant'
date = 2023-12-07T16:19:38+01:00
lastmod = 2023-12-07T16:19:38+01:00
draft = true
author = 'Janis Hutz'
tags = [ 'Linux', 'macOS', 'Development' ]
categories = [ 'Rants' ]
series = [ 'web-dev' ]
series_weight = 1
featuredImage = ""
+++

WebKit, WebKit, WebKit, why are you so bad?

WebKit, the rendering Engine of Safari is most definitely the worst modern rendering engine. Riddled with bugs, partially or improperly implemented standards, lagging behind Gecko and Chromium by sometimes years, doing their own thing with CSS attributes occasionally, the list goes on.

# What's so bad?
Well for once, if you expect a site to look a certain way on all browsers, you can almost bet that something will be off in WebKit. But good luck finding out, because on iOS or iPadOS there are *no developer tools*. Or there is an API that isn't supported or not supported properly. Or there is a function that, because of an error in the JS engine just doesn't execute as it should... well good luck seeing the stack trace in the non-existent developer console. Safari for Mac isn't much better, as the developer tools it has are terrible and have literally less than half the feature set of Gecko's or even Chromium's developer tools (which arguably have got much better recently).

The worst part is, if you have to truly support those browsers in complex web-apps like [libreevent](https://libreevent.janishutz.com). 