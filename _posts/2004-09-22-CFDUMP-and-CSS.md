---
layout: default
title: "CFDUMP and CSS"
permalink: /2004/09/22/CFDUMP-and-CSS/
---

<P><A href="http://www.camdenfamily.com/morpheus/blog/index.cfm?mode=entry&amp;entry=20CBD1F9-D071-1824-EC1783FE31AB9B3B">http://www.camdenfamily.com/morpheus/blog/index.cfm?mode=entry&amp;entry=20CBD1F9-D071-1824-EC1783FE31AB9B3B</A></P>
<P>"Do you ever use cfdump and notice that the layout doesn't come out right? This is due to a fairly simple issue. Whenever you use cfdump, it checks to see if it has been used already in the current request. If it has not, then it outputs CSS. This helps cut down on your download time. However, it means that if the first cfdump is suppressed in some way, your second cfdump will not look right."</P>