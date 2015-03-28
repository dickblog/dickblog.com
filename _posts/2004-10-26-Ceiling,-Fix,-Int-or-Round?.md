---
layout: default
title: "Ceiling, Fix, Int or Round?"
permalink: /2004/10/26/Ceiling,-Fix,-Int-or-Round?/
---

<P>Reproduced from <A class="" href="http://www.corfield.org/blog/index.cfm?mode=entry&amp;entry=D240856B-9CC8-A132-9A655C53B727FBF0" target=_blank>Sean Corfield's bog</A>...</P>
<P>"ColdFusion has four functions that take a floating point number and return an integer. Although the documentation is pretty clear about what each function does, you might not realize just how subtle the differences are between the functions. Here's sample output from a small test program that demonstrates how the four functions behave for a variety of positive and negative numbers:</P>
<P>ceiling(-4.9) is -4, fix(-4.9) is -4, int(-4.9) is -5, round(-4.9) is -5<BR>ceiling(-4.4) is -4, fix(-4.4) is -4, int(-4.4) is -5, round(-4.4) is -4<BR>ceiling(4.9) is 5, fix(4.9) is 4, int(4.9) is 4, round(4.9) is 5<BR>ceiling(4.4) is 5, fix(4.4) is 4, int(4.4) is 4, round(4.4) is 4</P>
<P>Some of you will recognize the behavior of <TT>int()</TT> as being what some languages provide as <TT>floor()</TT>."</P>