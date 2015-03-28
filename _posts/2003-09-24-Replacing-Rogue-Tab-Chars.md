---
layout: default
title: "Replacing Rogue Tab Chars"
permalink: /2003/09/24/Replacing-Rogue-Tab-Chars/
---

<P>Do you get fed up with Dreamweaver poking tab chars into the text of your page?</P>
<P>Yeah, I know I it doesn't make any difference to the final display, but it just looks untidy.</P>
<P>Well, I think I've got a search and replace regular expression which will strip those blighters out.</P>
<P>Try putting this into the search box: <CODE>(\w|[.,%&amp;'])\t(\w|[.,%&amp;'])</CODE></P>
<P>...and this into the replace box: <CODE>$1 $2</CODE></P>
<P>...remembering to check the "Use Regular Expressions" checkbox!</P>
<P>It may not be perfect, but I'll refine it over time with experience.</P>