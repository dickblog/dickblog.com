---
layout: default
title: "Looping over Dates"
permalink: /2004/08/23/Looping-over-Dates/
---

<P>From <A class="" href="http://www.beynon.org.uk/index.cfm?mode=entry&amp;entry=7BA78CEB-EE43-DA13-E796B06B1B36BD46" target=_blank>John Beynon's blog</A>...</P><PRE><FONT color=#800000>&lt;cfset startdate= </FONT><FONT color=blue>"06/01/2004"</FONT><FONT color=#800000>&gt;<BR></FONT><FONT color=maroon>&lt;cfset enddate = <FONT color=blue>"10/06/2004"</FONT>&gt;</FONT><BR><BR><FONT color=maroon>&lt;cfloop from=<FONT color=blue>"#startdate#"</FONT> to=<FONT color=blue>"#enddate#"</FONT> index=<FONT color=blue>"i"</FONT>&gt;</FONT><BR><FONT color=maroon>&lt;cfoutput&gt;</FONT><BR>#dateformat(i, <FONT color=blue>"mm/dd/yyyy"</FONT>)#<FONT color=navy>&lt;br /&gt;</FONT><BR><FONT color=maroon>&lt;/cfoutput&gt;</FONT><BR><FONT color=maroon>&lt;/cfloop&gt;</FONT></PRE>