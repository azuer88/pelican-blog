---
layout: post
title: "Solved: Firefox hangs when clicking on 'Open containing folder'"
date: 2016-09-27 13:33:34 PHT+0800
excerpt_separator: <!--more-->
categories: fixes firefox hangs
---

I have added and removed several file managers on my Linux Mint.  After a while I noticed that when I click on Firefox's "Open containing folder" in downloads, Firefox hangs.

<!--more-->
Actually, Firefox doesn't really hangs, as it will eventually receive the timeout from its request to open the (presumably) dead filemanager binary.

I finally found how to solve it.  I ran `xdg-mime default pcmanfm.desktop inode/directory`.

After that, Firefox no longer "hangs".
