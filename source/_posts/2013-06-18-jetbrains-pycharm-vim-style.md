---
layout: post
title: "IdeaVim: Pycharm, Vim-Style"
date: 2013-06-18 11:34
comments: true
categories: productivity
---

I've been using Vi (actually Vim) now for about a year as my primary code-editor. I really don't like using a mouse when I can help 
it, so the Vi keyboard-centric philosophy has been a pretty nice change to my workflow. I'm by no means a Vi expert, but for most 
things I'm quicker doing it in Vi than a more GUI based text editor. (I will still sometimes use GEdit or Sublime if I'm going to
be doing a lot of copy-paste work).

However, I've kind of missed having an actual IDE. Code completion[^1] is nice, as is symbol-based code navigation. I doubt I even need 
to mention how nice an integrated debugger is! I used [Jetbrains][jetbrains] [IntelliJ IDEA][intellij] as a Java/JavaScript IDE at an internship a year ago, and really fell in love with it. The attention to detail and the level of polish really can't be matched by any of the open source offerings. Since then, I've also used [Jetbrains PyCharm][pycharm] for various school projects. PyCharm has the same core and mostly the same interface as IDEA, but with superb Python support baked right in. (PyCharm also has the same JavaScript, HTML, and CSS support that IDEA does, so it's perfect for web development.)

I just discovered that there is an excellent plugin for PyCharm[^2] that adds really, really comprehensive Vi-style editing. [IdeaVim][ideavim] supports a pretty large subset of Vi commands. In fact, in my (admittedly pretty novice) usage of Vi commands, I have yet to run in to anything I can do in Vi that I can't in PyCharm with IdeaVim. 

Here's a list of supported features (copied from the docs):

<!-- more -->

    Supported:
        - Motion keys
        - Deletion/Changing
        - Insert mode commands
        - Marks
        - Registers
        - Undo/redo
        - Visual mode commands
        - Some Ex commands
        - Some :set options
        - Full Vim regexps for search and search/replace
        - Macros
        - Digraphs
        - Command line and search history
        - Vim web help

    Not supported (yet):
        - Key mappings
        - Various less used commands
        - Jump lists
        - Window commands


Not only does it provide comprehensive Vi editing, it's even under active development by a paid Jetbrains developer. That means that bugs and missing stuff gets fixed in a nice and timely manner (you can see the activity level on the [GitHub page](https://github.com/JetBrains/ideavim)).

Installation
------------
Installation is dead easy.

1. Open the PyCharm settings (`<ctrl><alt><S>`)

1. Under `IDE Settings`, choose `Plugins`.

1. Click the button that says `Install Jetbrains Plugin...`

1. Type `IdeaVim` into the search box.

1. Double click on the IdeaVim plugin when it shows up.

1. You'll be prompted to install it and restart PyCharm.

1. That's it!

You can easily toggle the Vi-style editing using `<ctrl><alt><V>` or choosing `Vim Emulator` from the `Tools` menu.


I know that Vi isn't for everyone. However, if you love Vi but can't live without an IDE, definitely take a look at IdeaVim! 



[^1]: I know there are some Vi plugins that allow various levels of code completion, but all of them have some issues and most are kind of a pain to get working.

[^2]: It actually supports all of the Jetbrains IDE  based on the IntelliJ platform, including IDEA, PhpStorm and RubyMine.

[jetbrains]: http://www.jetbrains.com/
[intellij]: http://www.jetbrains.com/idea/
[pycharm]: http://www.jetbrains.com/pycharm/
[ideavim]: http://plugins.jetbrains.com/plugin/164


