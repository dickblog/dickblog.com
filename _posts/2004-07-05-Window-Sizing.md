---
layout: default
title: "Window Sizing"
permalink: /2004/07/05/Window-Sizing/
---

<P>Having great prob finding the size of the current window. What I'm looking for is a way to dynamically resize the window to enclose the whole of a table that can change size. I'll found the following sites, but I'm still not&nbsp; clear...</P>
<P><A class="" href="http://www.quirksmode.org/viewport/compatibility.html" target=_blank>http://www.quirksmode.org/viewport/compatibility.html</A></P>
<P><A class="" href="http://www.howtocreate.co.uk/tutorials/index.php?tut=0&amp;part=16" target=_blank>http://www.howtocreate.co.uk/tutorials/index.php?tut=0&amp;part=16</A></P>
<P><STRONG>STOP PRESS</STRONG></P>
<P>I've just worked this out, which seems to work with IE 6. The reference to the spacer image is related to <A class="" href="http://www.dickblog.com/index.cfm/blog/1334859/">an earlier blog</A>. The trick seems to be to call this script from with the body tag and after the spacer image.</P><PRE>&lt;script language="JavaScript" type="text/javascript"&gt;<BR>//&nbsp;reduce the window width to ensure that the spacer image grows the table<BR>&nbsp;window.resizeTo(0,document.body.offsetHeight + 27);</PRE><PRE>//&nbsp;get the size of the spacer image which will be the width of the table<BR>&nbsp;var intTableWidth = document.images['spacer'].width;</PRE><PRE>//&nbsp;now resize the window to enclose the width of the table plus an allowance<BR>&nbsp;window.resizeTo(intTableWidth + 60,document.body.offsetHeight + 27);<BR>&lt;/script&gt;<BR></PRE>