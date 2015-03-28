---
layout: default
title: "Clear Cache"
permalink: /2003/11/15/Clear-Cache/
---

<p>Insert this code into your script and it should clear the browser cache then you next visit the page</p>
<p>&lt;cfheader name=&quot;Pragma&quot; value=&quot;no-cache&quot;&gt;<br/>&lt;cfheader name=&quot;Cache-Control&quot; value=&quot;no-cache&quot;&gt;</p>
<p>[12-May-04: DickBllg] <a class="" href="http://www.markme.com/cantrell/archives/004957.cfm" target="_blank">Christian Cantrell</a> has blogged an extension to this which is...</p><pre>&lt;cfheader name=&quot;Cache-Control&quot; value=&quot;no-store&quot; /&gt;<br/>&lt;cfheader name=&quot;Pragma&quot; value=&quot;no-cache&quot; /&gt;<br/>&lt;cfheader name=&quot;Expires&quot; value=&quot;Tue, 16 Oct 1973 00:00:00 GMT&quot; /&gt;</pre>
<p>...and others have added other worthwhile thoughts.<br/></p><p>Here's another one...<br/></p><p><a target="_blank" href="http://www.bpurcell.org/blog/index.cfm?mode=entry&amp;entry=1075">http://www.bpurcell.org/blog/index.cfm?mode=entry&amp;entry=1075</a></p><p>... and from the <a href="http://www.coldfusioncookbook.com/entry/54/How-can-I-prevent-a-browser-from-caching-my-page?" target="_blank">ColdFusion Cookbook</a>.<br type="_moz"/></p>