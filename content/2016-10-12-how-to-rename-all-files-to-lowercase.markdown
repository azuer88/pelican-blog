---
layout: post
title: "How to rename all files to lowercase"
date: 2016-10-12 09:14:24 PHT+0800
excerpt_separator: <!--more-->
categories: terminal howto rename
---


How do you rename all files in the current directory to all lowercase?


```ls | while read upName; do loName=`echo "${upName}" | tr '[:upper:]' '[:lower:]'`; mv "$upName" "$loName"; done```

<!--more-->

I had to rename all the font files to lowercase.  I found this solution [here][ubuntuforums.org]

[ubuntuforums.org]: https://ubuntuforums.org/showthread.php?t=1336909

