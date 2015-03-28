---
layout: default
title: "Force to index.cfm"
permalink: /2003/09/15/Force-to-indexcfm/
---

<STRONG>Securing Access Through index.cfm</STRONG><BR>In early versions of Fusebox, Application.cfm was shunned. In Fusebox 3, it is not recommended to use Application.cfm for much functionality because it is run once per request, regardless of subsequent <cfmodule> calls, which might produce unexpected results. So what should you put in 
Application.cfm and why? You should put code to secure access only to index.cfm (or your default webserver document like default.cfm). That way, you can be guaranteed that all requests by users go through index.cfm. You can still <cfmodule> individual fuses, though. Place this code in Application.cfm: 


<div class="code"><FONT COLOR=MAROON>&lt;cfif listLast(cgi.script_name,'/') neq <FONT COLOR=BLUE>"index.cfm"</FONT>&gt;</FONT>     <FONT COLOR=MAROON>&lt;cflocation url=<FONT COLOR=BLUE>"/index.cfm"</FONT>&gt;</FONT>  <FONT COLOR=MAROON>&lt;/cfif&gt;</FONT></div>