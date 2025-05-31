+++
title = 'Kernel Level Anti Cheat - The epitome of evil practices of gaming companies'
date = 2025-05-31T11:13:37+02:00
lastmod = 2025-05-31T11:13:37+02:00
draft = false
author = 'Janis Hutz'
tags = [ 'Linux', 'Windows' ]
categories = [ 'Rants' ]
series = []
series_weight = 1
featuredImage = "cover.png"
+++

It's again been a while since my last blog post, so sorry for that


{{< admonition type=tip title="What is Kernel-Level anti-cheat?" open=false >}}
**What is the Kernel**
The Kernel is the core of the operating system, essentially managing devices, memory access and much more. You may read this [wikipedia article](https://en.wikipedia.org/wiki/Kernel_%28operating_system%29) to learn more

**Kernel-Level Anti-Cheat**
Now that you understand what a Kernel is, Kernel-Level Anti-Cheat is Anti-Cheat software with access to the Kernel itself, and it is allowed to tamper with core, low-level functionality of the operating system to, as they say, prevent cheating much more effectively, while in fact, it makes little to no difference.
{{< /admonition >}}

# The rant
Today, we got a bit of a rant going. Apparently, EA decided to include Kernel-Level Anti-Cheat in F1 24 and newer, as well as EA Sports WRC. 
Now, you might ask, what is the problem with that? They are simply trying to stop cheaters and trolls. If it worked, then granted, sure enough. 
The problem though: It doesn't. And will never, especially since EA's moderation tools have never really worked ever and multiplayer lobbies in F1 games have been a disaster ever since their inception. 
Kernel-Level Anti-Cheat doesn't fix that. Certainly not. All it does, is prevent people on Linux from enjoying the game, because an evil company decided it wanted to block it by using invasive malware they call "Anti-Cheat" software that has access to the KERNEL(!!) of your operating system. 
***THE KERNEL!!!***, the piece of software only drivers and core system components should have direct access to.
No wonder are there many Anti-Cheat related CVEs out there.

Luckily however, Crowdstrike came to the rescue, crashing millions of PCs with their Kernel-Level AV software with a buggy update.
This truly served as a wake-up call to Micro$oft to finally address the issues of granting... well, basically everything that wants to have it, Kernel access. Yes, that software needs to be signed, blah, blah, blah, but it still doesn't fix the underlying issue of Kernel access: Security and the substantial risk of crashing the whole system with a bug. 

For a long time I did not have any EA games and wanted to keep it that way, but then I got back into F1 and wanted to drive F1 cars too much, so I got some of the F1 games, which are made by EA. 
I also got into driving WRC a bit with WRC 9 and saw that the new one was actually pretty good, albeit developed by EA, and got it as well. 
At the time I got it, it didn't yet have Kernel-Level anti-cheat, but only mere weeks later it got, as I just found out.
I had been a bit lazy with setup for my Thrustmaster SF1000 Addon Wheel, so I never moved these games to Linux, even though they would have worked perfectly, so I only just figured it out when I tried to do it on the day I am writing this.

I have never really understood the point of having *Kernel-Level* Anti-Cheat. Anti-Cheat for sure, but you can do without Kernel-Access, for sure. The Kernel-Access is just simply for extra data-mining and to prevent Linux users from using it. 
And it's mostly just the latter. Which is a true shame, as these evil practices prevent people who otherwise would have switched to Linux from doing that. 
Only because a few evil companies decide to ***intentionally*** prevent their apps from working on Linux. 
Like I get it, you don't want to support Linux, that is fine. 
I am also fine if you tell the user that you likely won't be able to support them, but don't *spend time and thus MONEY that your CUSTOMERS PAY YOU TO USE YOUR DAMN SOFTWARE* to prevent people from using it if they are using an operating system you *chose not to support*. 
Again, I am fine if you don't support it officially, but *blocking it is the problem I have with it*. 
I don't blame them if their software doesn't work well. I don't blame them if their software doesn't work at all if they haven't intentionally done so.

# Conclusion
I really do hope you see my point and why it is important to give these shady companies a financial incentive to stop these kinds of practices. Because if they keep getting away with it and nobody complains or they aren't hurt financially, they will keep doing this BS
