---
layout: default
title: "Faster Form Entry Test"
permalink: /2003/10/08/Faster-Form-Entry-Test/
---

<P>Rather than use...</P><PRE>&lt;cfif isDefined("form.fieldName")&gt;</PRE>
<P>... to check to see if a form field has been entered use...</P><PRE>&lt;cfif NOT structKeyExists(form,"fieldName")&gt; </PRE>
<P>...as it's faster because ColdFusion has to parse the IsDefined into a string before it can evaluate it rather than just check to see if a variable exists.</P>