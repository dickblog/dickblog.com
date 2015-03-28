---
layout: default
title: "Duplicating a Function"
permalink: /2005/04/12/Duplicating-a-Function/
---

To stop you accidently defining a function more that once, try bracketing your code like this...<br/><br/>&lt;cfif StructKeyExists(variables,&quot;Foo&quot;) AND NOT IsCustomFunction(Foo)&gt;<br/>&nbsp;&nbsp;&nbsp; &lt;cfscript&gt;<br/>&nbsp;&nbsp;&nbsp; function StripHTMLscope() {<br/>&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; ...<br/>&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; return true;<br/>&nbsp;&nbsp;&nbsp; }<br/>&nbsp;&nbsp;&nbsp; &lt;/cfscript&gt;<br/>&lt;/cfif&gt;<br/>