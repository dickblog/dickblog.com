---
layout: default
title: "Cross Site Scripting (XSS)"
permalink: /2006/04/26/Cross-Site-Scripting-XSS/
---

After a little investigation I think you shouldn't try to strip out any HTML from a users input, within reason, but to bracket the output of all their input with HTMLEditFormat(). That way any sillyness will be displayed in all it's glory!

This of course is in addition to adding <cfset this.scriptProtect="true"> to your Application.cfc or the scriptprotect attribute of the cfapplication tag in CFMX 7. This is preferred over blindly checking the "Enable Global Script Protection" checkbox in the Administrator as it gives more flexibility.

See <a href="http://www.petefreitag.com/item/362.cfm" target="_blank">Pete Freitag's blog</a> for more info.

Also there's a good article on <a href="http://cfdj.sys-con.com/read/41943.htm" target="_blank">SysCon</a>.

Plus a good faq at <a href="http://www.cgisecurity.com/articles/xss-faq.shtml" target="_blank">http://www.cgisecurity.com/articles/xss-faq.shtml</a>