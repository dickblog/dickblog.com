---
layout: default
title: "SvnAnt on Mac with Eclipse"
permalink: /2008/01/11/SvnAnt-on-Mac-with-Eclipse/
---

<p>I struggled to get SvnAnt to work on a Windows box some time ago and wasn't looking forward to trying to get it working on my Mac but I shouldn't have been.</p>
<p>It was easy!</p>
<p>Just install <a target="_blank" href="http://downloads.open.collab.net/binaries.html">Subversion for Mac</a> then get <a target="_blank" href="http://subclipse.tigris.org/svnant.html">SvnAnt</a> and put the *.jar in some central place which you then reference in the classpath of the build.xml script. Done!</p>
<p>That said, I heard recently that it's best to use the 1.1 version of SvnAnt as it includes&nbsp; SvnKit and doesn't need the JavaHL installed which can be&nbsp; problematic.</p>
<p>Next is to work out how to sync to a remote server via ftp.</p>
<p>I got ftp working by reading <a href="http://www.phillnacelli.net/blog/index.cfm/2006/6/15/ANT-Builds-and-FTP" target="_blank">ANT Builds and FTP</a> by Phill Nacelli. Which says you need to install commons-net.jar and jakarta-oro-2.0.8.jar and point Eclipse to those files.</p>
<p>More good Ant resources here...</p>
<p><a href="http://www.thecrumb.com/wiki/Ant" target="_blank">http://www.thecrumb.com/wiki/Ant</a></p>
<p>&nbsp;</p>