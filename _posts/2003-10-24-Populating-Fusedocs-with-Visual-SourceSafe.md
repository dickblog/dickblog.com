---
layout: default
title: "Populating Fusedocs with Visual SourceSafe"
permalink: /2003/10/24/Populating-Fusedocs-with-Visual-SourceSafe/
---

<P>Here's a neat trick I've found out about VSS. By enabling keyword expansion of *.cfm files in the VSS Administrator you can get VSS to expand a number of keywords codes in your script.</P>
<P>By putting these keywords in your Fusedocs you can get some self-documenting. It's not perfect. The keywords codes are left in the output and checking in via Dreamweaver MX doesn't run the update code in VSS so the keywords are not updated.</P>
<P class=label><B>To expand keywords:</B></P>
<P>
<TABLE cols=2 cellPadding=5 rules=rows width=480 border=1 frame=below>

<TR vAlign=top>
<TD class=label width="35%"><B>Type this keyword</B></TD>
<TD class=label width="65%"><B>To add the following</B></TD></TR>
<TR vAlign=top>
<TD width="35%">$Archive: $</TD>
<TD width="65%">VSS archive file location</TD></TR>
<TR vAlign=top>
<TD width="35%">$Author: $ </TD>
<TD width="65%">User who last changed the file</TD></TR>
<TR vAlign=top>
<TD width="35%">$Date: $ </TD>
<TD width="65%">Date and time of last checkin</TD></TR>
<TR vAlign=top>
<TD width="35%">$Header: $ </TD>
<TD width="65%">Logfile, Revision, Date, Author</TD></TR>
<TR vAlign=top>
<TD width="35%">$History: $ </TD>
<TD width="65%">File history, VSS format</TD></TR>
<TR vAlign=top>
<TD width="35%">$JustDate: $</TD>
<TD width="65%">Date, without the time addendum.</TD></TR>
<TR vAlign=top>
<TD width="35%">$Log: $&nbsp; </TD>
<TD width="65%">File history, RCS format</TD></TR>
<TR vAlign=top>
<TD width="35%">$Logfile: $ </TD>
<TD width="65%">Same as Archive</TD></TR>
<TR vAlign=top>
<TD width="35%">$Modtime: $ </TD>
<TD width="65%">Date and time of last modification</TD></TR>
<TR vAlign=top>
<TD width="35%">$Revision: $ </TD>
<TD width="65%">VSS version number</TD></TR>
<TR vAlign=top>
<TD width="35%">$Workfile: $ </TD>
<TD width="65%">File name</TD></TR>
<TR vAlign=top>
<TD width="35%">$NoKeywords: $</TD>
<TD width="65%">No keyword expansion for all keywords that follow </TD></TR></TABLE><BR></P>