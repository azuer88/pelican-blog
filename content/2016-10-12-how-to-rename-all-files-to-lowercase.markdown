Title: "How to rename all files to lowercase"
Date: 2016-10-12 09:14:24 PHT+0800
Tags: terminal, howto, rename,
Category: howto
Slug: how-to-rename-all-files-to-lowercase
Authors: Blue Cuenca
Summary: Tip on renaming files to lowercase


How do you rename all files in the current directory to all lowercase?


```ls | while read upName; do loName=`echo "${upName}" | tr '[:upper:]' '[:lower:]'`; mv "$upName" "$loName"; done```


I had to rename all the font files to lowercase.  I found this solution [here][ubuntuforums.org]

[ubuntuforums.org]: https://ubuntuforums.org/showthread.php?t=1336909

