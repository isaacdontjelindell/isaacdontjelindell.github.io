---
layout: post
title: "Using GVM (Go version manager) To Install Golang"
date: 2014-01-19 10:17:59 -0800
comments: true
categories: programming
---

I'm starting a project in Go. The first step was obviously to install Go, but after a half hour wrestling with an old and broken installation and a out-of-date PPA, I got fed up.

Then I found [gvm](https://github.com/moovweb/gvm). If you're familiar with rvm for Ruby, I think you're going to like gvm.

Setup on Ubuntu is pretty simple:

```
bash < <(curl -s https://raw.github.com/moovweb/gvm/master/binscripts/gvm-installer)
```

Then you'll need to restart your terminal.

In may case, I wanted the latest version of Go (1.2 as of this writing), so I ran:

```
gvm install go1.2
gvm use go1.2 --default
```

The `--default` flag sets that particular version of go as the default when you open a new terminal session.

It was fun to see that gvm was written by the devs at [MoovWeb](http://www.moovweb.com/). When I visited them a few days ago I was interested that they were using Go for their backend - clearly they're pretty invested!
