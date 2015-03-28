---
layout: default
title: "UK Database Date Entry"
permalink: /2003/09/15/UK-Database-Date-Entry/
---

<P>This is the only way I can find to ensure that a UK date is formated correctly for any kind of database interaction.</P>
<P>Use:</P>
<BLOCKQUOTE dir=ltr style="MARGIN-RIGHT: 0px">
<P>SetLocale("English (UK)")<BR>LSParseDateTime(<EM>date</EM>)<BR>CreateODBCDate(<EM>date</EM>)</P></BLOCKQUOTE><PRE><P>&lt;cfset form.dteDate="3/10/71"&gt;</P><P>&nbsp;</P><P>&lt;cfset SetLocale("English (UK)")&gt;<BR></P><P>&lt;cfset dteDate=CreateODBCDate(LSParseDateTime(form.dteDate))&gt;</P><P>&nbsp;</P>&lt;cfquery name="test" datasource="dsn"&gt;<BR>	select dteDOB<BR>	from tbluser<BR>	where dteDOB = #dteDate#<BR>&lt;/cfquery&gt;</PRE>