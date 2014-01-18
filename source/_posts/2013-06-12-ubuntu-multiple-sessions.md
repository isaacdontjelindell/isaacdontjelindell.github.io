---
layout: post
title:  "Multiple Ubuntu Unity Sessions"
date:   2013-06-8 16:20:41
comments: true
categories: linux
---

I often find myself working on several programming projects at once. This generally involves one or more Chrome windows, multiple Vi terminal windows, and miscellaneous text editors, Gimp windows, Evernote pages, etc, all arranged over multiple workspaces (usually the same ones so I can find stuff quickly!). 

I've often wished I could have multiple X sessions running at the same time, completely independent of each other. Then I could have one project open and spread out, while being able to quickly switch to a different project, with its unique set of windows and layout options.

I just discovered that if multiple users are logged in to an Ubuntu machine, it'll put each user's X session in a separate TTY (virtual terminal). The first 6, TTY1 - TTY6, are console sessions. The first user to log into a graphical session in Ubuntu is on TTY7. If you switch users (Gear menu -> Switch Users) and log in to a different user account on the computer, it will start that session on TTY8. 

Note: TTY's can be accessed by typing `<ctrl><alt><tty_num %F%>`. So to access TTY8, for example, I would type `<ctrl><alt><F8>`.

I had originally hoped that I could start a separate X session but still log in as my main user account. Unfortuantely, this doesn't seem to be possible with Unity - I can start another X session and log in, and even manually start Unity, but every time I open programs, they appear in the first Unity session, on TTY7. 

<!-- more -->

As a workaround, I created another user account so that I can start another session. It's kind of a hack, because the second user obviously doesn't have access to all the customizations, files, etc. Since a large portion of my work is at the terminal anyway, I can just run `sudo su <main_user_account>` and impersonate my main user account from the second one. 


As far as other customizations, it'll probably take a little to get them all there (wobbly windows, anyone?) but I think it's worth it. I'm already pretty attached to being able to `<ctrl><alt><f8>` and instantly switch to a completely different project.


