---
layout: default
title: "Logout User"
permalink: /2008/02/16/Logout-User/
---

<p>Logging out a user can normally be a simple matter of &lt;cfset StructClear(session) /&gt; but sometime you might want to do more. So what not invoke the onSessionEnd() method in the Application.cfc and clear the session plus whatever else you want to do.</p>
<p><a href="http://daveshuck.instantspot.com/blog/2008/01/16/Calling-OnSessionEnd-from-outside-the-Applicationcfc-to-log-out-users" target="_blank">Dave Shuck sums it up neatly</a>.</p>
<p>&nbsp;</p>