---
layout: default
title: "How to Code for Popup"
permalink: /2005/09/12/How-to-Code-for-Popup/
---

Rather than code ...<br/><br/>

<code>
<a href="#" onclick="javascript:window.open('path/to/page',pagename)">link title</a>
</code>

...use this...

<code>
<a href="path/to/page.html" onclick="return popupWindow(this.href,'winPopup','height=400,width=200');">link title</a>
</code>

..and this JavaScript function...

<code>
function popupWindow(strURL,strName,strWindowFeature) {
	objWindow = window.open(strURL,strName,strWindowFeature);
	
	if (window.focus) {
		window.objWindow.focus();
	}

	return false;
}
</code>

Got this idea from <a target="_blank" href="http://jehiah.com/archive/how-to-open-popups">here</a> and there are more ideas <a href="http://www.contentwithstyle.co.uk/Articles/6/dom-scripting-or-how-to-keep-the-code-clean/" target="_blank">here</a> and <a href="http://www.quirksmode.org/js/popup.html" target="_blank">here</a>.