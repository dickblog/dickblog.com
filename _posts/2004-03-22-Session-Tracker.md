---
layout: default
title: "Session Tracker"
permalink: /2004/03/22/Session-Tracker/
---

<P>I've recently discovered this handy Java call that you can use in CFMX to reveal some session info.</P>
<P>Create an object...</P>
<P>&lt;cfset objSession=createObject("java","coldfusion.runtime.SessionTracker")&gt;</P>
<P>Then if you cfdump the object you can see all the methods available. These include getSessionCollection and getSessionCount which can be really useful!</P>