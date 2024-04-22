+++
title = 'Webkit Rant'
date = 2023-12-13T16:19:38+01:00
lastmod = 2023-12-13T16:19:38+01:00
draft = false
author = 'Janis Hutz'
tags = [ 'Linux', 'macOS', 'Development' ]
categories = [ 'Rants' ]
series = [ 'web-dev' ]
series_weight = 1
featuredImage = "cover.jpg"
+++

WebKit, WebKit, WebKit, why are you so bad?

WebKit, the rendering Engine of Safari is most definitely the worst modern rendering engine. Riddled with bugs, partially or improperly implemented standards, lagging behind Gecko and Chromium by sometimes years, doing their own thing with CSS attributes occasionally, the list goes on.

# What's so bad?
Well for once, if you expect a site to look a certain way on all browsers, you can almost bet that something will be off in WebKit. But good luck finding out, because on iOS or iPadOS there are *no developer tools*. Or there is an API that isn't supported or not supported properly. Or there is a function that, because of an error in the JS engine just doesn't execute as it should... well good luck seeing the stack trace in the non-existent developer console. Safari for Mac isn't much better, as the developer tools it has are terrible and have literally less than half the feature set of Gecko's or even Chromium's developer tools (which arguably have got much better recently).

The worst part is, if you have to truly support those browsers in complex web-apps like [libreevent](https://libreevent.janishutz.com), things get very nasty very quickly. In that project, I had to rewrite basically the whole engine of the seat plan editor because a feature the original version relied on was completely broken in some recent versions of WebKit resulting in the seat plan editor not working at all. 

But that's not all... Many things look slightly differently on WebKit compared to Gecko and Chromium, which makes developing for iOS, where WebKit is forced upon every user harder, as you can't even troubleshoot issues as there are no developer tools. 


# WebKit requirement on iOS
Even though I dislike WebKit a lot, it's still good to have competition, albeit competition which is stirred by anticompetitive behaviour from Apple's side. Apple's been hard at work preventing a Chromium monopoly, but not by actually making a competent rendering engine, but by arbitrarily forcing it onto every iOS user. Yes, there are other browsers than Safari on iOS, but all of them have to use the WebKit rendering engine and a cheapo version of Safari's that doesn't even support extensions... I mean in what year are we? 

But there's a light at the end of the tunnel, with the EU's Digital Markets Act (DMA from now) disallowing such behaviour. Personally, I am torn whether this is good or not. From an egoistic point of view of being able to finally enjoy a proper Web-Engine on iOS with Gecko coming to iOS fairly soon, it's amazing because I can finally just use one web-browser with all my extensions I use on desktop. On the other hand allowing the 65% of iOS users who use the Chrome skin for Safari to now also use Chromium and with that massively decreasing Safari's market share at the cost of increasing Chromium's seems like to big of a risk to the free internet as we know it today for me to say that it is good.

# Where should this go?
Personally, I hope that Apple tries to make WebKit a competent and competitive rendering engine. Competition is important, especially in the lights of the huge market share that Chromium has. Additionally, with that engine being developed by a company that does not have a big ad-business is a plus. As sad as it is to say, Mozilla can't do much about Chromium's dominance currently, even though Firefox is the better browsers in many regards, but Google's $H!T is just too easy to use. Also people don't like change, which further decreases the amount of people switching browsers. 


# What can we do?
The best thing we can do is to never use Chromium browser, except maybe for checking that a website we just developed looks as intended on Chromium based browsers and instead use Gecko based browsers like Firefox, LibreWolf, Mullvad Browser, Waterfox and many more. Additionally, if you are fortunate to be on Linux use GNOME Web (aka Epiphany), Konqueror or similar browsers that are based on WebKit2GTK, which is using a more upstream version of WebKit than Safari is at times.


**Attribution of cover image**
By Apple - https://webkit.org, LGPL, https://commons.wikimedia.org/w/index.php?curid=129303403