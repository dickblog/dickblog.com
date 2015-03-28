---
layout: default
title: "Regular Expressions for UK Post Codes"
permalink: /2003/12/09/Regular-Expressions-for-UK-Post-Codes/
---

<P>I got this from <A class="" href="http://www.forta.com/blog/index.cfm?mode=e&amp;entry=996" target=_blank>Ben Forta's website</A>.</P>
<BLOCKQUOTE dir=ltr style="MARGIN-RIGHT: 0px"><PRE>[A-Z]{1,2}\d[A-Z\d]? \d[ABD-HJLNP-UW-Z]{2}</PRE></BLOCKQUOTE>
<P>An alternative posted as a comment was...</P>
<BLOCKQUOTE dir=ltr style="MARGIN-RIGHT: 0px"><PRE>^[A-Za-z]{1,2}[\d]{1,2}([A-Za-z])?\s?[\d][A-Za-z]{2}$ </PRE></BLOCKQUOTE>
<P>When I've had a chance to play with these I'll post some comments of my own.</P>