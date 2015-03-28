---
layout: default
title: "CFSCRIPT Samples"
permalink: /2003/10/04/CFSCRIPT-Samples/
---

<P>From: <A href="http://tutorial84.easycfm.com/" target=_blank>http://tutorial84.easycfm.com/</A></P>
<P><FONT size=2><STRONG><FONT color=#800000>Looping in CFSCRIPT</FONT></STRONG> <BR></P></FONT>
<P>
<TABLE cellSpacing=0 border=0>

<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>1.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana color=#800000 size=2>&lt;cfscript&gt;</FONT></TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>2.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana size=2>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;myList = 'George,Paul,John,Ringo'; // creates the variable myList, which holds 4 names</FONT> </TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>3.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana size=2>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;for (i = 1; i LTE listLen(myList); i = i+1) {</FONT> </TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>4.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana size=2>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;writeOutput(listGetAt(myList, i) &amp; "<FONT color=#000080>&lt;br&gt;</FONT>");</FONT> </TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>5.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana size=2>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</FONT></TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>6.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana color=#800000 size=2>&lt;/cfscript&gt;</FONT></TD></TR></TABLE></P>
<P>
<TABLE cellSpacing=0 border=0>

<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>1.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana color=#800000 size=2>&lt;cfscript&gt;</FONT></TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>2.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana size=2>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;myRandomNumber = randRange(1,100);</FONT></TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>3.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana size=2>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;if (myRandomNumber GTE 1 AND myRandomNumber LTE 25) {</FONT></TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>4.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana size=2>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;writeOutput(myRandomNumber &amp; ' is in the first quarter');</FONT></TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>5.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana size=2>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} else if (myRandomNumber GTE 26 AND myRandomNumber LTE 50) {</FONT></TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>6.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana size=2>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;writeOutput(myRandomNumber &amp; ' is in the second quarter');</FONT></TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>7.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana size=2>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} else if (myRandomNumber GTE 51 AND myRandomNumber LTE 76) {</FONT></TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>8.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana size=2>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;writeOutput(myRandomNumber &amp; ' is in the third quarter');</FONT></TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>9.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana size=2>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} else {</FONT></TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>10.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana size=2>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;writeOutput(myRandomNumber &amp; ' is in the fourth quarter');</FONT></TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>11.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana size=2>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</FONT></TD></TR>
<TR>
<TD vAlign=top><FONT face=Verdana color=#808080 size=2>12.&nbsp;&nbsp;</FONT></TD>
<TD vAlign=top><FONT face=Verdana color=#800000 size=2>&lt;/cfscript&gt;</FONT></TD></TR></TABLE></P>