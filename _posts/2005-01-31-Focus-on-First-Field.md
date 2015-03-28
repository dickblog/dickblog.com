---
layout: default
title: "Focus on First Field"
permalink: /2005/01/31/Focus-on-First-Field/
---

Saw this code on&nbsp; <span class="description"><a href="http://www.markme.com/cantrell/archives/006864.cfm" target="_blank">Christian Cantrell's blog</a>. I had something earlier, but it wasn't as compact. <br/><br/></span>function focusCursor()<br/><pre>{<br/>    for (var i = 0; i &lt; document.forms.length; ++i)<br/>    {<br/>        var f = document.forms[i];<br/>        for (var j = 0; j &lt; f.elements.length; ++j)<br/>        {<br/>            if (f.elements[j].type == 'text' ||<br/>                f.elements[j].type == 'textarea')<br/>            {<br/>                f.elements[j].focus();<br/>                return;<br/>            }<br/>        }<br/>    }<br/>}<span class="description"><span style="font-family: arial,verdana,sans-serif;"><br/></span><br/><br/>I usually put this on the onLoad event, but comments in the blog seem to advise against that.<br/></span></pre>