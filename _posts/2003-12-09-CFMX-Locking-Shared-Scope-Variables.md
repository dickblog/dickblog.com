---
layout: default
title: "CFMX: Locking Shared Scope Variables"
permalink: /2003/12/09/CFMX-Locking-Shared-Scope-Variables/
---

<P>Now that CFMX uses Java data structures to store shared scope variables it is no long necessary to lock these variables.</P>
<P>That said, you should be locking variables and processes that maybe subject to Race Conditions.</P>
<P>A&nbsp;Race Condition occurs anytime two threads (in this case, page requests) try to read/write to the same variable at the same time.</P>
<P>To know more, checkout this <A class="" href="http://www.macromedia.com/support/coldfusion/ts/documents/tn18235.htm" target=_blank>Macromedia TechNote</A>.</P>
<P><STRONG>[DickBlog Update: 27-Apr-04]</STRONG></P>
<P><A class="" href="http://www.forta.com/blog/index.cfm?mode=e&amp;entry=1139" target=_blank>Ben Forta's blog</A> has confirmed this understanding. The need for CFLOCK to counteract the prob's with memory corruption in CF v5 and prior is no longer required. It is still required for single-thread events like using CFFILE to write out to a file and race conditions where a users experience may be effected by other sessions changing the value of a variable.</P>