---
layout: default
title: "Convert String to Number and Back Again"
permalink: /2004/02/06/Convert-String-to-Number-and-Back-Again/
---

<P>If you need to convert a string to a number...</P>
<BLOCKQUOTE dir=ltr style="MARGIN-RIGHT: 0px"><PRE>var mystring = '123';<BR>var myinteger = mystring - 0;</PRE></BLOCKQUOTE>
<P dir=ltr>...and back again...</P>
<BLOCKQUOTE dir=ltr style="MARGIN-RIGHT: 0px"><PRE>var myinteger = 123;<BR>var mystring = myinterger + '';</PRE></BLOCKQUOTE>