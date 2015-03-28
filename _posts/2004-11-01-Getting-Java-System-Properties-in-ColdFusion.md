---
layout: default
title: "Getting Java System Properties in ColdFusion"
permalink: /2004/11/01/Getting-Java-System-Properties-in-ColdFusion/
---

<P>Try this...</P>
<P>&lt;cfdump var="#CreateObject("java", "java.lang.System").getProperties()#"&gt;</P>