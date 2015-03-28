---
layout: default
title: "FB3: XFA Names"
permalink: /2003/08/15/FB3-XFA-Names/
---

<P>Each Exit FuseAction (XFA) should be named to suit it's purpose on the display. </P>
<P>For example:</P>
<P>
<TABLE cellSpacing=0 cellPadding=5 align=center border=0>

<TR vAlign=top>
<TD>xfa.formAction</TD>
<TD>
<P>The action attribute of a form tag.</P><PRE>&lt;form name="forExample" <BR>	action="#xfa.formAction#" <BR>	method="post"&gt;</PRE></TD></TR>
<TR vAlign=top>
<TD>xfa.next</TD>
<TD>
<P>The action with a "Next" button is pressed.</P><PRE>&lt;a href="#"&gt;<BR> &lt;img name="btnNext" src="next.gif" <BR>  onClick="window.location.href='#xfa.next#'"&gt;<BR>&lt;/a&gt;</PRE></TD></TR>
<TR vAlign=top>
<TD>xfa.back</TD>
<TD>
<P>The action of a url link.</P><PRE>&lt;a href="#xfa.back#"&gt;Back&lt;/a&gt;</PRE></TD></TR></TABLE></P>