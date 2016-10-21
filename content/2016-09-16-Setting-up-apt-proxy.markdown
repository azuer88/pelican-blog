---
layout: post
title: "Setting up apt-cacher-ng"
date: 2016-09-16 14:51:29 +0800
excerpt_separator: <!--more-->
categories: apt-cacher-ng config howto 
---

apt-cacher-ng needs to be told how to handle traffic using HTTPS.

<!--more-->
For most repository sources, this isn't a problem.  For some, like nodesource.com, it can cause the cacher/proxy to choke.

I added this line to `acng.conf`:

```
PassThroughPattern: deb\.nodesource\.com
```

to enable the nodesource source.



