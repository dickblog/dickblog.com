---
layout: default
title: "Accessing the Admin API"
permalink: /2005/09/08/Accessing-the-Admin-API/
---

Dan Switzer offered a idea to <a target="_blank" href="http://blog.pengoworks.com/blogger/index.cfm?action=blog:471">find the CF Mail &quot;Spool Interval&quot;</a> but Andy Allan came back with a neat way to hook into the CF Admin API.<br/><br/>&nbsp;&nbsp;&nbsp; adminObj = createObject(&quot;component&quot;,&quot;cfide.adminapi.administrator&quot;)<br/>&nbsp;&nbsp;&nbsp; adminObj.login(&quot;password&quot;)<br/>&nbsp;&nbsp;&nbsp; myObj = createObject(&quot;component&quot;,&quot;cfide.adminapi.mail&quot;)<br/>&nbsp;&nbsp;&nbsp; spoolInterval = myObj.getMailProperty(&quot;spoolInterval&quot;)<br/>