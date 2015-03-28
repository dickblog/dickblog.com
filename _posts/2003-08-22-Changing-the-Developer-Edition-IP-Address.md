---
layout: default
title: "Changing the Developer Edition IP Address"
permalink: /2003/08/22/Changing-the-Developer-Edition-IP-Address/
---

<P>The developer edition of both ColdFusion MX and 5 allows you to access the the server from the local server/machine via localhost or the IP equivalent 127.0.0.1 and a single other IP address.</P>
<P>The method used to keep store this information is that the first non-local IP address that accesses the server will be written into the <SPAN class=code>license.properties</SPAN> file in the <SPAN class=code>{CFMX}/lib</SPAN>.</P>
<P>With the ColdFusion 5 Developer Edition, you could only access the server from one IP as with MX, however the server 'forgot' the IP address that was stored each time the server was restarted.</P>
<P>With ColdFusion MX the server will remember the second IP address (localhost &amp; non-local) permanently. The way to change the second IP is to edit the <SPAN class=code>license.properties</SPAN> and then restart the server.</P>