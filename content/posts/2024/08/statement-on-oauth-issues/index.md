+++
title = 'Statement on id.janishutz.com Issues'
date = 2024-08-07T17:16:17+02:00
lastmod = 2024-08-07T17:16:17+02:00
draft = false
author = 'Janis Hutz'
tags = [ 'General', 'Hardware' ]
categories = [ 'News' ]
series = []
series_weight = 1
featuredImage = "cover.jpg"
+++

There might be some people experiencing login issues on [id.janishutz.com](https://id.janishutz.com). These issues predominantly occur in browsers with strict cookie policies configured. I am currently working on addressing these issues for these browsers. My development browser is also affected by this issue, so I have a way to reproduce it. 

# When can you expect this issue to be resolved?
I expect this to happen until August 20th, five days before the launch of the new MusicPlayer, whose launch I had to postpone as a result of that.

# What happened that this is even an issue?
That is something I am still investigating to a point. It appears to be a configuration issue for the cookie that the login services use. I am pretty sure I have a quick solution to this issue, which I will try to push asap.

I am taking this opportunity to completely rewrite the UI of the login services as a true web-app, but I will still retain the current login screen as an option, so SSO (Single-Sign-On) functionality uses less resources. This login screen will be used whenever the login sdk is used. All APIs will remain the same. I will also use a database to store login sessions as part of the update, which will allow you to stay logged in for significantly longer periods of time. Login might be slightly slower as a result of that, but I think it is worth the trade of.


# What steps am I taking that similar issues won't occur again in the future?
As part of this investigative work into the issues I am experiencing, I am trying to figure out what part of the software stack is causing these issues to occur. I will use that knowledge to avoid future mistakes of similar kind. I will also further increase the amount of testing I do on this kind of software before pushing it to prod. 