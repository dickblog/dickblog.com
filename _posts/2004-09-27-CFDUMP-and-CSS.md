---
layout: default
title: "CFDUMP and CSS"
permalink: /2004/09/27/CFDUMP-and-CSS/
---

<P>From Raymond Camden's Blog</P>
<P>"Do you ever use cfdump and notice that the layout doesn't come out right? This is due to a fairly simple issue. Whenever you use cfdump, it checks to see if it has been used already in the current request. If it has not, then it outputs CSS. This helps cut down on your download time. However, it means that if the first cfdump is suppressed in some way, your second cfdump will not look right. This can happen if you cfmail your cfdump. Here is a simple example showing this behaviour: </P>
<P>
<P class=code><FONT color=maroon>&lt;cfsavecontent variable=<FONT color=blue>"foo"</FONT>&gt;</FONT><BR>&nbsp;&nbsp;&nbsp;<FONT color=maroon>&lt;cfdump var=<FONT color=blue>"#server#"</FONT>&gt;</FONT><BR><FONT color=maroon>&lt;/cfsavecontent&gt;</FONT><BR><BR><FONT color=maroon>&lt;cfdump var=<FONT color=blue>"#request#"</FONT>&gt;</FONT></P>
<P>Luckily there is a simple way around it - turn off the request variable cfdump checks for: 
<P>
<P class=code><FONT color=maroon>&lt;cfsavecontent variable=<FONT color=blue>"foo"</FONT>&gt;</FONT><BR>&nbsp;&nbsp;&nbsp;<FONT color=maroon>&lt;cfdump var=<FONT color=blue>"#server#"</FONT>&gt;</FONT><BR><FONT color=maroon>&lt;/cfsavecontent&gt;</FONT><BR><BR><FONT color=maroon>&lt;cfset request.cfdumpinited=false&gt;</FONT><BR><FONT color=maroon>&lt;cfdump var=<FONT color=blue>"#request#"</FONT>&gt;</FONT></P>
<P class=code><FONT face="Courier New"></FONT>&nbsp;</P>