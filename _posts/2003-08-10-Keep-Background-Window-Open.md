---
layout: default
title: "Keep Background Window Open"
permalink: /2003/08/10/Keep-Background-Window-Open/
---

<PRE>&lt;body leftmargin="0" topmargin="0" marginwidth="0" marginheight="0" <BR>	onLoad="closing=true"<BR>	onUnload="if (closing) window.myWindow.focus();"&gt;</PRE><PRE>&lt;script language="JavaScript" type="text/javascript"&gt;<BR>	if (opener.closed) {<BR>		window.myWindow = window.open('summary/', 'MyPayBens');<BR>		self.focus();<BR>	} else {<BR>		window.myWindow = opener;<BR>		window.myWindow.location.href='summary/';<BR>		self.focus();<BR>	}<BR>&lt;/script&gt;</PRE><PRE>...</PRE><PRE>&lt;a href="#" onClick="self.close();window.myWindow.focus();"&gt;Close Window&lt;/a&gt;</PRE><PRE>&lt;/body&gt;<BR></PRE>