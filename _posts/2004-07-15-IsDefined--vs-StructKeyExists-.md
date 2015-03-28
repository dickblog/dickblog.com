---
layout: default
title: "IsDefined() vs StructKeyExists()"
permalink: /2004/07/15/IsDefined--vs-StructKeyExists-/
---

<P>Sean Corfield&nbsp;suggests that it's better to use StructKeyExists() rather than IsDefined() for reliability and performance.</P>
<P><A class="" href="http://www.corfield.org/blog/past/2004_07.html#000510" target=_blank>isDefined() vs structKeyExists()</A></P>
<P>It seems that, as a general rule, functions() work faster than operators (NEQ, GT, CONTAINS etc.).</P>
<P>So...</P><PRE>&lt;cfif NOT CompareNoCase(string1, string2)&gt;<BR>	...<BR>&lt;/cfif&gt;</PRE>
<P>...is fasters than [string1 EQ string2] and...</P><PRE>&lt;cfif NOT FindNoCase(string1, string2)&gt;<BR>	...<BR>&lt;/cfif&gt;</PRE>
<P>...is fasters than [string2&nbsp;CONTAINS string1] and my favourite...</P><PRE>&lt;cfif Len(Trim(string))&gt;<BR>	...<BR>&lt;/cfif&gt;</PRE>
<P>...is fasters than [string&nbsp;NEQ ""].</P>