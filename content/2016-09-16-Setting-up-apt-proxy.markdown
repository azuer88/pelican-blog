Title: "Setting up apt-cacher-ng"
Date: 2016-09-16 14:51:29 +0800
Tags: apt-cacher-ng, config, howto 
Category: howto
Slug: Setting-up-apt-proxy
Authors: Blue Cuenca
Summary: How to setup apt-cache-ng to handle https traffic


apt-cacher-ng needs to be told how to handle traffic using HTTPS.

For most repository sources, this isn't a problem.  For some, like nodesource.com, it can cause the cacher/proxy to choke.

I added this line to `acng.conf`:

```
PassThroughPattern: deb\.nodesource\.com
```

to enable the nodesource source.



