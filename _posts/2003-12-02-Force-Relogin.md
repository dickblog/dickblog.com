---
layout: default
title: "Force Relogin"
permalink: /2003/12/02/Force-Relogin/
---

<P>If you wish for a user to be redirected to the login page after they have been inactive for x number of minutes instead of waiting for them to jump to another page, add the following line inside the &lt;head&gt;...&lt;/head&gt; block of your html: </P>

<div class="code"><FONT COLOR=NAVY>&lt;META http-equiv=<FONT COLOR=BLUE>"refresh"</FONT> content=<FONT COLOR=BLUE>"901;URL='login.cfm'"</FONT>&gt;</FONT></div>
<P>This assumes that your session timeout is set for 15 minutes (900 seconds).</P>