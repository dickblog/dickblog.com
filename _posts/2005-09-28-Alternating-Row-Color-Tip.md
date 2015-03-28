---
layout: default
title: "Alternating Row Color Tip"
permalink: /2005/09/28/Alternating-Row-Color-Tip/
---

Mark Kruger  has blogged <a href="http://mkruger.cfwebtools.com/index.cfm?mode=alias&alias=alternating.row.color" target="_blank">a tip on colouring alternative rows</a> in HTML using CSS. I've done something similar before, but the use of #currentrow mod 2# is neat. 

<p>I now have a better tip. Use BitAnd() like &lt;tr class="rowBackground#BitAnd(query.currentRow,1)#"&gt;.</p>