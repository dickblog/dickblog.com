---
layout: default
title: "Dynamic Variable Names"
permalink: /2003/08/08/Dynamic-Variable-Names/
---

<P>Is there any exceptions to these rule 'cause I've learnt that we should avoid using Evaluate if possible..<BR>Correct me if I'm wrong.<BR><BR></P>
<P>If you use CFMX, there's rarely a need for it. You can access all<BR>variable scopes as structures, so you can do this:<BR><BR>myvar = variables["something"&amp;dynamic]<BR><BR>Rather than<BR><BR>myvar = evaluate("variables.something"&amp;dynamic)<BR><BR>That caters for about 95% of the times I have had to use it in prior<BR>versions of CF.<BR>Sometimes in CFCs one still has to use evaluate() because local<BR>variables do not exist in a "scope", so one cannot use structure/array<BR>notation on them.<BR></P>